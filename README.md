# python-projects

This repo, created in Fall 2018, hosts some of my projects done in python over the last few years.


-- Icing Project:

A program I wrote as semester project in Dr. Michael Papadakis's "Introduction to Aircraft Icing" course at Wichita State.
The program computes the airflow around a cylinder, and then computes the trajectory of droplets withing the flow.
In theory such a program could be used to predict ice buildup on a surface in an aerodynamic flow in a cloud with temperatures below freezing.

-- Prop Processing:

I was assigned propulsion lead on our five man senior design team at Wichita State. This meant that in our small competitive remote control airplane design, I would be responsible for picking a motor, propellor, and battery pack which would be ideally suited to our mission. The approach which most teams took to this problem was to look at historical data (most of which is for real, full scale airplanes) get a ballpark estimate for propellor size, select a few representative propellors, and analyze each of them at each part of the flight regime, possibly in tandem with a few different motors, taking the one with the best results.
I, instead, wrote this script, which loops through the entire sizable UIUC propellor database, iteratively finding propellor rpm, thrust, and efficiency.
In essence this means that instead of taking a guess and doing a little bit of analytics to narrow it down, I can actually test nearly every single available propellor and give a conclusive result. It worked, and our team won the competition!
One thing that I never got to was that I ideally would have liked to add motor power curves as well as the propellor power to thrust curves. At present the program simply assumes constant power from the motor at all RPMs which is obviously a fairly gross simplification. However, access to good data on small electric motors was not forthcoming at the time and so I simply lived with it.
Note also that because of the large number of propellors processed, along with the relatively lenghty iterative process used to find actual RPMs (I'm sure this could be made much more efficient but for the time it worked) this script takes quite a while to run.

-- Prop Processing-Actual Prop:

Same script as above, but limited to just the one prop which we chose for our plane, this script will show the same functionality but run much more quickly since it just analyzes a single prop.

Note that both of these files will require you to extract the UIUC database zip file to run if downloaded.
