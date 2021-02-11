# **Highway Driving**
## Describe in detail the code model for generating paths

The path planning starts in line 101 of main.cpp.

Sensor fusion data is collected. These data are used to track other cars. On the one hand we need this to do a lane change safely
without hitting or disturbing the other cars on that lane. On the other hand it is essential to detect other vehicles in front of the car in the current lane.

This is done by checking if another car is in front of the car within 30 m (the code for this starts in line 140). If there is another car,
I check if it is close enough and the lane where the car is about to change to is free. If there are not any other vehicles on the intended lane within 30 m behind
in front of the car, the car will change the lane. If not, it slows down and continues driving slower behind the car in front of it.
