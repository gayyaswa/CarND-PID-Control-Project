# Overview

The objective of this project is to let the vehicle complete the track by tuning the paramteres Proportional(P), Differential(D) and Integral(I) as mentioned in the class lessions. The simulator provides Cross Track Error(CTE) which is used to tune in the proportional, differential and integral errors and update the steer value accordingly. I choose to tune the paramaters manually without using any algorithms such as gradient descent and managed to make the vehicle complete the track successfuly

# Rubic Points

Describe the effect each of the P, I, D components had in your implementation.

## Proportional (P)
This control parameter set in proportion to the existing Cross Track Error(CTE) and this helps steer the vehicle back to the center of lane in either direction, which also means the vehicle can go on a zig zag fashion through the entire track as this paramters keeps correcting based on the CTE. Here is the video from the simulator with just P paramter set.
