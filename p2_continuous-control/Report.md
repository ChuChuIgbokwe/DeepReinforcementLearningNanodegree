# Report

### Project Details
**The README describes the the project environment details (i.e., the state and action spaces, and when the environment 
is considered solved).**

* number of agents: 20
* state: 2
* action_spaces: 4 for each agent
* state size: 33
* solved condition: average score of +30 over 100 consecutive episodes

### Getting Started
**The README has instructions for installing dependencies or downloading needed files.**
 * This project requires the [Reacher](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip) 
 linux unity environment to be installed in the p2_continuous-control folder 

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
    * Go the p2_continuous-control folder and open Continuous_Control.ipynb
    * In the kernel tab change to a drlnd kernel
    * In the kernel tab, click on Restart & Run All


### Learning Algorithm
**The report clearly describes the learning algorithm, along with the chosen hyperparameters.** 
It also describes the model architectures for any neural networks.
* Learning Algorithm: I implemented a [DDPG](https://arxiv.org/pdf/1509.02971.pdf) on 20 agents
a deep deterministic policy gradient

|Hyperparameter |Value |
| ------ | ------ |
| BUFFER_SIZE | 1e6 |
| BATCH_SIZE | 1024 |
| GAMMA | 0.99 |
| TAU | 1e-3 |
| LR_ACTOR | 5e-4 |
|LR_CRITIC |1e-3 |
| LEARN_INTERVAL | 1 |
| WEIGHT_DECAY |0 |

* Each Fully connected nueron in both netwks had 128 hidden layers 
* Both the actor and critic were updated after 20 timesteps. 

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

**A plot of rewards per episode is included to illustrate that the agent is able to receive an average reward 
(over 100 episodes, and over all 20 agents) of at least +30.**
![](https://github.com/ChuChuIgbokwe/deep_reinforcement_learning_nanodegree/blob/master/p2_continuous-control/p2_plot.png)

**The submission reports the number of episodes needed to solve the environment.**
* The environment was solved in 343 episodes

### Ideas for Future Work
**The submission has concrete future ideas for improving the agent's performance.**
* Implementing other algorithms like PPO
* Using prioritized experience replay to improve the performance of the DDPG algorithm
* Attempting the project using pixel data as opposed to raw inputs

### Notes and Observations

### References
1. https://arxiv.org/pdf/1509.02971.pdf
2. 
