[//]: # (Image References)

[image1]: https://video.udacity-data.com/topher/2018/May/5af7955a_tennis/tennis.png "Trained Agent"

[image2]: score_plot_tennis.png "Score Plot"

# Collaboration and Competition - Multi Agent RL - Tennis Environment

This project is part of the Udacity [Deep Reinforcement Learning Nanodegree Program](https://www.udacity.com/course/deep-reinforcement-learning-nanodegree--nd893).

The goal is to create and train an Agent to solve the [Tennis](https://github.com/Unity-Technologies/ml-agents/blob/main/docs/Learning-Environment-Examples.md#tennis) environment. An agent is trained to play tennis using Mullti Aget Actor Critic Algorithm [MADDPG](https://papers.nips.cc/paper/7217-multi-agent-actor-critic-for-mixed-cooperative-competitive-environments.pdf). This algorithm can be seen as an extension of the [DDPG](https://arxiv.org/abs/1509.02971) algorithm for multi Agent cooperative - competitive environment.

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

### Getting Started

1. Follow the instructions [here](https://github.com/udacity/deep-reinforcement-learning#dependencies) to setup the python environment. These instructions can be found in README.md at the root of the repository.
2. Download this repository (only for Mac OSX), it has the environment included. So for Mac OSX, step 3 can be skipped.
3. Download the Udacity provided environment from one of the links below. Select the environment corresponding to the required operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)
4. Place the file in the repository folder (downloaded in step 2) and unzip (or decompress) the file.


### Instructions

The environment just set up has the files and tools to allow the training of the agent.

Start the Jupyter Notebook server by running the commands below (in Mac OSX). A new browser tab will open with a list of the files in the current folder.

```
$ source activate drlnd
$ jupyter notebook
```

Follow the instructions in `Tennis.ipynb` to get started with training your own agent! 

The task of solving the Tennis environment was completed using Multi Agent DDPG algorithm with modifications.

```
Environment solved in 817 episodes!	Average Score: 0.50
```
![Score Plot][image2]
   
For more details see the [Report](https://github.com/tamoghna21/DeepRL_MultiAgent_DDPG/blob/main/Report.pdf)
