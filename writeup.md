# Overview

The objective of this project is to let the vehicle complete the track by tuning the paramteres Proportional(P), Differential(D) and Integral(I) as mentioned in the class lessions. The simulator provides Cross Track Error(CTE) which is used to tune in the proportional, differential and integral errors and update the steer value accordingly. I choose to tune the paramaters manually without using any algorithms such as gradient descent and managed to make the vehicle complete the track successfuly

# Rubic Points

Describe the effect each of the P, I, D components had in your implementation.

## Proportional (P)
This control parameter set in proportion to the existing Cross Track Error(CTE) and this helps steer the vehicle back to the center of lane in either direction, which also means the vehicle can go on a zig zag fashion through the entire track as this paramters keeps correcting based on the CTE. Here is the video from the simulator with just P paramter set.

## Differential (D)
This differential parmaters consideres the rate of change of error and tries bringing it to 0. This helps in correcting the error in a damped manner and helps the vehicle center on the lane gradually which also prevents the zig zag movement of the vehicle. When too much dampening is applied through this paramter then vehicle might overshoot and never recover as shown in the video.

## Integral (I)
THe integral parameters reacts to the cummulative error over time usually applicable if a vehicle has inherent wheel mis-alighment or drift due to external factors. I managed to drive the vehicle without using this parameter and here is the video based on driving with just this parameter set

# Describe how the final hyperparameters were chosen.
