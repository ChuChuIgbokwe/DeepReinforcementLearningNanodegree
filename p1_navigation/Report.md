#### Project Environment Details (i.e., the state and action spaces, and when the environment is considered solved).
* state: 37
* action_spaces: 4
* solved condition: Average score of +13 over a 100 episodes

#### The README has instructions for installing dependencies or downloading needed files.
This project requires the [Banana unity environment](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip) to be installed in the p1_navigation folder 

#### How to run the code in the repository, to train the agent.
Assuming you have the conda drlnd environment, 
1. open a terminal  
```bash
    cd deep_reinforcement_learning_nanodegree
    source activate drlnd
    jupyter-notebook 
```
2. To train the agent , 
* Go the p1_navigation folder and open Navigation.ipynb
* In the kernel tab change to a drlnd kernel
* In the kernel tab, click on Restart & Run All

#### The report clearly describes the learning algorithm, along with the chosen hyperparameters. It also describes the model architectures for any neural networks.

|Neural Network Model Architecture |
| ------ |
| Fully Connected Layer 1 |
| ReLU | 64 |
| Fully Connected Layer 2 |
| ReLU |
| Fully Connected Layer 3 |

|Hyperparameter |Value |
| ------ | ------ |
| BUFFER_SIZE | int(1e5) |
| BATCH_SIZE | 64 |
| GAMMA | 0.99 |
| TAU | 1e-3 |
| LR | 5e-4 |
| UPDATE_EVERY | 4 |

#### A plot of rewards per episode is included to illustrate that the agent is able to receive an average reward (over 100 episodes) of at least +13. 
![](https://github.com/ChuChuIgbokwe/deep_reinforcement_learning_nanodegree/blob/master/p1_navigation/p1_plot.png)

#### The submission has concrete future ideas for improving the agent's performance.
The network performance could be improved by using the following extensions
* Double DQN, 
* Prioritized experience replay  
* Dueling DQN
