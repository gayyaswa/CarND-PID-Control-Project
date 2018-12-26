# Overview

The objective of this project is to let the vehicle complete the track by tuning the paramteres Proportional(P), Differential(D) and Integral(I) as mentioned in the class lessions. The simulator provides Cross Track Error(CTE) which is used to tune in the proportional, differential and integral errors and update the steer value accordingly. I choose to tune the paramaters manually without using any algorithms such as gradient descent and managed to make the vehicle complete the track successfuly

# Rubic Points

## Describe the effect each of the P, I, D components had in your implementation.

## Proportional (P)
This control parameter set in proportion to the existing Cross Track Error(CTE) and this helps steer the vehicle back to the center of lane in either direction, which also means the vehicle can go on a zig zag fashion through the entire track as this paramters keeps correcting based on the CTE. Here is the [link to my video result](./capture/P_Video.mp4) from the simulator with just P paramter set.

## Differential (D)
This differential parmaters consideres the rate of change of error and tries bringing it to 0. This helps in correcting the error in a damped manner and helps the vehicle center on the lane gradually which also prevents the zig zag movement of the vehicle. When too much dampening is applied through this paramter then vehicle might overshoot and never recover as shown in the video [link to my video result](./capture/D_Video.mp4).

## Integral (I)
THe integral parameters reacts to the cummulative error over time usually applicable if a vehicle has inherent wheel mis-alighment or drift due to external factors. I managed to drive the vehicle without using this parameter and here is the video [link to my video result](./capture/I_Video.mp4) based on driving with just this parameter set

## Describe how the final hyperparameters were chosen.
The parameters were chosen manually for the first set of trial runs only Proportional parameter were chosen with the right value vehicle managed to go until the second curvature of the track and overshoot. By choosing the differential paraeter which help correcting the overshoot and also dampen the vehicle osciallation into a smoother ride. The integral factor was left unchanged as it made the vechile to overshoot very early in the track. This final parameter values (-0.20, 0.0, -1.0); //P, I, D made the vehicle finish the track successfully.
