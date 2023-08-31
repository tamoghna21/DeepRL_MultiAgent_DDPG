[//]: # (Image References)

[image1]: https://video.udacity-data.com/topher/2018/May/5af7955a_tennis/tennis.png "Trained Agent"

[image2]: score_plot.png "Score Plot"

# Project 3: Collaboration and Competition - Multi Agent RL - Tennis Environment

This project is part of the Udacity [Deep Reinforcement Learning Nanodegree Program](https://www.udacity.com/course/deep-reinforcement-learning-nanodegree--nd893).

The goal is to create and train an Agent to solve the [Tennis](https://github.com/Unity-Technologies/ml-agents/blob/main/docs/Learning-Environment-Examples.md#tennis) environment. This project solves the Tennis environmet in Mac OSX.

![Trained Agent][image1]

### Environment Details

The envoronment is built using [Unity Machine Learning Agents](https://github.com/Unity-Technologies/ml-agents) (**ML-Agents**), which is an open-source Unity plugin that 
enables games and simulations to serve as environments for training intelligent agents.
The project environment, provided by Udacity is similar to, but not identical to the [Tennis](https://github.com/Unity-Technologies/ml-agents/blob/main/docs/Learning-Environment-Examples.md#tennis) 
environment. The Udacity provided environment has been downloaded from [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip) for Mac OSX. 

#### State and Action spaces

In this environment, two agents control rackets to bounce a ball over a net. If an agent hits the ball over the net, it receives a reward of +0.1. If an agent lets a ball 
hit the ground or hits the ball out of bounds, it receives a reward of -0.01. Thus, the goal of each agent is to keep the ball in play.

The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation. Two 
continuous actions are available, corresponding to movement toward (or away from) the net, and jumping.

#### Solving the environment

The task is episodic, and in order to solve the environment, your agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over 
both agents). Specifically,

- After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. We then take the maximum of these 2 scores.
- This yields a single score for each episode.

The environment is considered solved, when the average (over 100 episodes) of those scores is at least +0.5.
