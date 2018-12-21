# DDPG for Tennis

## Geting started
### 1) Intro
In this environment, two agents control rackets to bounce a ball over a net.

<p align="center"><img src="https://user-images.githubusercontent.com/10624937/42135623-e770e354-7d12-11e8-998d-29fc74429ca2.gif" alt="Example" width="50%" style="middle"></p>

### 2) Reward
If an agent hits the ball over the net, it receives a reward of +0.1. If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01. Thus, the goal of each agent is to keep the ball in play.

### 3) State space
The observation space consists of 24 variables variables corresponding to position and velocity of ball and racket.

### 4) Action space
Each action is a vector with 2 numbers, corresponding to movement toward net or away from net, and jumping.Every entry in the action vector should be a number between -1 and 1.

### 5) Goal
The task is episodic, and in order to solve the environment, your agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents). Specifically,

* After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. We then take the maximum of these 2 scores.
* This yields a single score for each episode.

The environment is considered solved, when the average (over 100 episodes) of those scores is at least +0.5.

### 6) Authors
fouad kouidmir

### 7) Acknowledgments
Udacity deep reinforcement learning nanodegree https://www.udacity.com/course/deep-reinforcement-learning-nanodegree--nd893
