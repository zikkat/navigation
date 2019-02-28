[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135619-d90f2f28-7d12-11e8-8823-82b970a54d7e.gif "Trained Agent"

[image2]: images/Training_results.png "results"

[image3]: images/score.png "scores"
# Report

### Method

Used DQN (Deep Q learning) to navigate an agent to maximize yellow banana collections.
The algorithm does not use pixels but rather velocity, along with ray-based perception of objects around the agent's forward direction

![Trained Agent][image1]

There are three main modules:

1- model.py is the neural network representing the Q function
The network is a fully connected network with three layers
  * First layer is input layer: uses state size=37 and outputs: 128. Initially I attempted using 64 nodes, similar to the udacity example, but found that by double the number of neurons, I was able to increase the capacity of the network and therefore better learn the Q function. 
  * Second layer has input: 128 and output: 64
  * Third and Last Layer has input 64 and output: action size=4
  
2- dqn_agent2.py defines how the agent interacts with the environment and sets up the loss function for learning

3- Navigation2.ipynb has the code to start the unity environment and then train the agent, it binds all together. 


Training results were as follows:

![scores][image3]


![results][image2]

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction.  Given this information, the agent has to learn how to best select actions.  Four discrete actions are available, corresponding to:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

The task is episodic, and in order to solve the environment, your agent must get an average score of +13 over 100 consecutive episodes.

### Potential Improvements:

* Use Double DQN. While this is a method that is supposed to improve the learning. My first attempt at this didn't show improvement in learning. 
* Prioritized Replay buffer
* Dueling DQN
