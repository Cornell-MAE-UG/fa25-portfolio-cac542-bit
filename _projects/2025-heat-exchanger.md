---
layout: project
title: Heat Exchanger
description: analysis of a heat exchanger for ENGRD 2210
image: /assets/images/regular-flow.jpeg
---
#### Introduction
This project involved the analysis of a heat exchanger, which is a device that transfers heat from one fluid to another by running the fluids in parallel. To maximize the amount of heat that is exchanged, a good heat exchanger will typically run the liquids in such a way that the surface area connecting the two is very high. In the heat exchanger used for this investigation, this was achieved by running the fluids back and forth across a rectangular prism in parallel.

---

#### Experimental Setup

For the initial experiment, the input of the heat exchanger was connected via plastic tubing to two tubs of water. One, which had blue food coloring, was kept very cold with a steady stream of ice added to maintain its coldness. The second tub of water, which had red food coloring, was kept warm using an electric water heater which was kept inside the tub. Each of the tubs had an electric pump attached to the mouth of the plastic tube in each tub that would eventually pump water from the tube into the heat exchanger, but both pumps were kept initially powered off. The output of the heat exchanger was connected to two empty tubs of water, one which would collect the output of the blue, initially cold water and one that would collect the output of the red, initially hot water. 

First, the temperature of the water contained in each of the two input tubs was measured using a thermometer. Then, both pumps were turned on at the same time, letting the water flow through the heat exchanger until the water in the initial tubs began to run low, which happened about 30 seconds in. Once this happened, both pumps were stopped at the same time and the temperature of the water contained in each of the two output tubs was measured using a thermometer. 

The experimental setup was then reset, with water in the output tubs dumped out and new water added to the input tubs, with heat and ice added to return to originally low and high temperatures within the input tubs. Then, for a second experiment, the tube leading from the cold water input tub to the heat exchanger and the tub leading from the heat exchanger to the output tub for the blue, initially cold water were switched in positions on the heat exchanger. This meant that now, the cold water would be run in the opposite direction as the hot water through the heat exchanger, in counter flow. 

See below an image of the parallel flow experimental setup:

![2025-heat-exchanger]({{ "/assets/images/regular-flow.jpeg" | relative_url}})

See below an image of the counter flow experimental setup:

![2025-heat-exchanger]({{ "/assets/images/counter-flow.jpeg" | relative_url}})

---

#### Analysis of Parallel Flow Setup

For the parallel flow setup, the initial tempterature measured in the tub of cold water was T_C=8.0 *C and the initial temperature measured in the tub of hot water was T_H=45.0 *C. After the flow had run its course, the temperature measured in the output tub for the hot water was T_C,f=23.6 *C and the temperature measured in the output tub for the cold water was T_H,f=27.3 *C. Converting these into Kelvin gives us:

T_C = 281.15 K

T_H = 318.15 K

T_C,f = 296.75 K

T_H,f = 300.45 K

To analyze this system, a control volume approach was used, with the system boundary defined as enclosing the interior of the side of the heat exchanger through which the blue, initially cold water ran. For this system boundary, there is a positive mass flow m_dot,in of the blue water entering the system at the heat exchanger's input, a negative mass flow m_dot,out of the blue water exiting the system at the heat exchanger's output, and a positive heat transfer from the red, initially hot water Q_in. Since the same water is coming into and out of the heat exchanger, we can refer to a more general flow rate as m_dot=m_dot,in=m_dot,out with the rather more important difference coming from the input and output's enthalpies, h_in and h_out. If we model the heat exchanger as adiabatic, assume the system is in steady-state, and that kinetic and potential energy differences in the system are negligible, our energy balance equation comes out as this:

E_dot = Q_dot - W_dot + m_dot * (h_in - h_out + change in KE + change in PE)

0 = Q_dot - 0 + m_dot * (h_in - h_out)

Q_dot = - m_dot * (h_in - h_out)

If we model this system as having a constant pressure, the change in enthalpy between the input and output of the system will be equal to the change in temperature between the input and output, times the specific heat of water under constant pressure, c_p. For this analysis, we'll use c_p for 300K, which is about room temperature. This means c_p=4.179 kJ/kg*K. Substituting this into our energy balance gives this:

Q_dot = - m_dot * c_p * (T_C - T_C,f)

Q_dot / m_dot = - c_p * (T_C - T_C,f)

Q_dot / m_dot = - 4.179 kJ/kg*K * (281.15 K - 296.75 K)

Q_dot / m_dot = 65.19 kJ/kg

So, using this analysis, the heat transfer per mass flow between hot and cold water is 65.19 kJ/kg*K.

---

#### Analysis of Counter Flow Setup

For the counter flow case, an initial temperature in the cold water tub was recorded as T_C=6.3 *C and in the hot water tub as T_H=40 *C. After the flow had run its course, the temperature in the output tub for the blue, initially cold water was measured as T_C,f = 24.5 *C and in the output tub for the red, initially hot water as T_H,f=20.3 *C. Converting to Kelvin, this gives us the following data:

T_C = 279.45 K

T_H = 313.15 K

T_C,f = 297.65 K

T_H,f = 293.45 K

Using the same analysis and assumptions as the previous setup gives us the following energy balance: 

E_dot = Q_dot - W_dot + m_dot * (h_in - h_out + change in KE + change in PE)

0 = Q_dot - 0 + m_dot * (h_in - h_out)

Q_dot = - m_dot * (h_in - h_out)

Q_dot = - m_dot * c_p * (T_C - T_C,f)

Q_dot / m_dot = - c_p * (T_C - T_C,f)

Q_dot / m_dot = - 4.179 kJ/kg*K * (279.45 K - 297.65 K)

Q_dot / m_dot = 76.06 kJ/kg

This analysis gives us that the heat transfer per mass flow between hot and cold water is 76.06 kJ/kg, which is higher than our values from the first setup.

---

#### Key Findings

The value calculated for the heat transfer per mass flow of the counter flow setup was somewhat higher than that of the parallel flow setup. Since the goal of a heat exchanger is typically to maximize the heat transfer between the two fluids that are run through the heat exchanger, these findings suggest that heat exchanger that run their fluids in the opposite direction are more effective than those running the fluids in the same direction. 

It is important to note some of the limitations of this analysis. While the figures calculated form this analysis are useful, they do rely on many modeling assumptions as outlined above that may not be fully accurate. For example, while it is convenient to model the heat exchanger as adiabatic in both cases, the truth is that the actual heat exchanger was not insulated and had a degree of heat transfer with its outside environment, as one could tell by touching the heat exchanger and noticing it felt warmer and colder at certain points on the heat exchanger once the flow had been underway for a few seconds. Assumptions like these may have affected the exact accuracy of the figure. Additionally, the starting temperatures in the hot and cold tubs were slightly different for the two setups, meaning that heat transfer to the heat exchanger's surroundings may have happened to different amounts in each setup, in a way that is difficult to quantify. For all of these reasons, while it is notable that the counter flow setup seemed to act more efficiently than the parallel flow setup, further investigations are needed to confirm this result.

---



The physical and data collection parts of this project were completed in a group with my classmates Elaine, Jackie, Madeline, and Elise, but the analysis presented was completed independently.
