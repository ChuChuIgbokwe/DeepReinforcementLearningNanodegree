# Report

### Project Details
**The README describes the the project environment details (i.e., the state and action spaces, and when the environment 
is considered solved).**

* Number of agents: 2
* Size of each action: 2
* action_spaces: 24 for each agent. 48 in total
* Solved condition: average score of +0.5 over 100 consecutive episodes

### Getting Started
**The README has instructions for installing dependencies or downloading needed files.**
 * This project requires the [Tennis](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip) 
 linux unity environment to be installed in the p3_collab-compet folder 

### Instructions
**The README describes how to run the code in the repository, to train the agent.**
* Follow the instructions [here](https://github.com/udacity/deep-reinforcement-learning#dependencies) to setup python,
 your dependencies and conda environments
  * open a terminal  
```bash
    cd deep_reinforcement_learning_nanodegree
    source activate drlnd
    jupyter-notebook 
```
* To train the agent , 
    * Go the p3_collab-compet folder and open Tennis.ipynb
    * In the kernel tab change to a drlnd kernel
    * In the kernel tab, click on Restart & Run All


### Learning Algorithm
**The report clearly describes the learning algorithm, along with the chosen hyperparameters.** 
It also describes the model architectures for any neural networks.
* Learning Algorithm: I implemented a [MADDPG](https://papers.nips.cc/paper/7217-multi-agent-actor-critic-for-mixed-cooperative-competitive-environments.pdf)
a multi-agent deep deterministic policy gradient

|Hyperparameter |Value |
| ------ | ------ |
| BUFFER_SIZE | 1e6 |
| BATCH_SIZE | 1024 |
| GAMMA | 0.99 |
| TAU | 1e-3 |
| LR_ACTOR | 5e-4 |
|LR_CRITIC |1e-3 |
| LEARN_INTERVAL | 1 |

* Each Fully connected nueron in both netwks had 128 hidden layers 
* Both the actor and critic were updated after 1 timestep. Attempts at using a higher timesteps failed.

|Actor Neural Network Model Architecture |
| ------ |
| Batch Normalization 1 |
| Fully Connected Layer 1 |
| Batch Normalization 2 |
| Fully Connected Layer 2 |
| Batch Normalization 3 |
| Fully Connected Layer 3 |

|Critic Neural Network Model Architecture |
| ------ |
| Batch Normalization 1 | 
| Fully Connected Layer 1 | 
| Fully Connected Layer 2 | 
| Fully Connected Layer 3 | 




### Plot of Rewards

**A plot of rewards per episode is included to illustrate that the agents get an average score of +0.5 
(over 100 consecutive episodes, after taking the maximum over both agents).**
![](https://github.com/ChuChuIgbokwe/deep_reinforcement_learning_nanodegree/blob/master/p3_collab-compete/p3_plot.png)

**The submission reports the number of episodes needed to solve the environment.**
* The environment was solved in 1874  episodes

### Ideas for Future Work
**The submission has concrete future ideas for improving the agent's performance.**
* A better way to tune hyper-parameters. This was the most time consuming part of this project
* I would like to read up more on multi-agent reinforcement learning and implement 
* Using gradient clipping on the critic agent
* Add prioritized experience replay
* Adding  more noise to my networks for better exploration


### References
1. https://papers.nips.cc/paper/7217-multi-agent-actor-critic-for-mixed-cooperative-competitive-environments.pdf
2. 
