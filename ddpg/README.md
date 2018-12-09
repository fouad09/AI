
# DDPG for reacher

## Geting started 

### 1) Intro
In this environment, a double-jointed arm need to move to target locations.

### 2) Reward
A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of the agent is to maintain its position at the target location for as many time steps as possible.


### 3) State space
The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. 

### 4) Action space
Each action is a vector with four numbers, corresponding to torque applicable to two joints.Every entry in the action vector should be a number between -1 and 1.

### 5) Goal
The task is episodic, and in order to solve the environment, we train 20 agents to get an average score of +30 over 100 consecutive episodes.

### 6) Authors
fouad kouidmir

### 7) Acknowledgments
Udacity deep reinforcement learning nanodegree https://www.udacity.com/course/deep-reinforcement-learning-nanodegree--nd893
