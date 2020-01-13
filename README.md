# Robot Localization and Landmark Detection Using Graph SLAM

![header](images/readme_slam.gif)

## Objective

In this project, I have implemented Graph SLAM in a 2D grid world where the robot tracks it's movements and detects the surrounding landmarks such as building, trees, rocks etc using its distance measurement sensors and motion poses.

## Project Walkthrough

### 1. Define robot variables and create data

First we define variables with respect to the world and the robot. The variables that I have used are the following:
'''
- 'N': time steps for which we want our robot to have a random walk
- 'num_landmarks': number of landmarks in the world
- 'world_size': the grid size of the world (Here I have taken it as 100 units (10x10))
- 'measurement_range': the range in which the robot measures a landmark
- 'motion_noise': noise or uncertanity present in the robot motion.
- 'measurement_noise': noise or uncertanity present in the robot's distance measurement sensor. These two moise variables are introduced to mimick real-life sceanrios.
- 'distance': distance by which a robot can move during a particular time step.
'''

All of the above variables go into the 'make_data' function and out comes the true landmark locations and the robots final pose co-ordinates.

Let's say data = make_data(*all of the above variables*), then data[time_step][0] = Measurement values given by the robot sensor with respect to each landmark and data[time_step][1] is the motion co-ordinates of the robot.
Please see the helpers.py file for more info

Here I have instantiated the robot at the center of the grid.

### 2. Omega and Xi:



## Results

Please head over to Notebook 3 of the project to see the final results and conclusion.