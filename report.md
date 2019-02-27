[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135619-d90f2f28-7d12-11e8-8823-82b970a54d7e.gif "Trained Agent"

# Report

### Method

Used DQN (Deep Q learning) to navigate an agent to maximize yellow banana collections.
The algorithm does not use pixels but rather velocity, along with ray-based perception of objects around the agent's forward direction

![Trained Agent][image1]

There are three main modules:

1- model.py is the neural network representing the Q function



A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.  Thus, the goal of the agent is to collect as many yellow bananas as possible while avoiding blue bananas.  

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction.  Given this information, the agent has to learn how to best select actions.  Four discrete actions are available, corresponding to:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

The task is episodic, and in order to solve the environment, your agent must get an average score of +13 over 100 consecutive episodes.

### Getting Started

follow the steps in the link below to have an environment ready

https://github.com/udacity/deep-reinforcement-learning#dependencies


### Instructions

`Navigation2.ipynb` has the code to start the unity environment and then train the agent. 
dqn_agent2.py has the agent training methods. The training based on DQN algorithm with experience replay buffer.
the file model.py is the neural network representing the Q function 