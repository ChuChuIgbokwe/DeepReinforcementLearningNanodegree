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
* Learning Algorithm: I implemented a [DDPG](https://arxiv.org/pdf/1509.02971.pdf) on 20 agents
a deep deterministic policy gradient
* Hyperparameters
* Neural Network Architecture

### Plot of Rewards

**A plot of rewards per episode is included to illustrate that the agent is able to receive an average reward 
(over 100 episodes, and over all 20 agents) of at least +30.**
![](https://github.com/ChuChuIgbokwe/deep_reinforcement_learning_nanodegree/blob/master/p2_continuous-control/p2_plot.png)

**The submission reports the number of episodes needed to solve the environment.**
* The environment was solved in 343 episodes

### Ideas for Future Work
**The submission has concrete future ideas for improving the agent's performance.**

### Notes and Observations

### References
1. https://arxiv.org/pdf/1509.02971.pdf
2. 
