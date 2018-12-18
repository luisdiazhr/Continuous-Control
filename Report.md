# Report: DDPG for Continuous Control

## 1. Model
In this project the DDPG algorithm is implemented to solve the Reacher environment. The Actor is represented by a neural network with

- Fully connected layer 1: with input = 33 (state spaces) and output = 128
- Fully connected layer 2: with input = 128 and output = 128
- Fully connected layer 3: with input = 128 and output = 4 (for each of the 4 actions)

In the other hand, the Critic neural network is composed by 

- Fully connected layer 1: with input = 33 (state spaces) and output = 128
- Fully connected layer 2: with input = 128 (states and actions) and output = 128
- Fully connected layer 3: with input = 128 and output = 1 (maps states and actions to Q-values)

Introducing batch normalization layers for the hidden layers was a determinant factor to get some valuable results in this project. Without it, the algorithm would be oscillating at average score of 4 after 300 episodes, which it clearly was not a good signal of good training. Another factor was the implementation of the gradient cliping method when updating the critic. 

## 3. Hyperparameters

Experimentation showed that learning rates had impact on the training progress.

| Parameter              | Value    | 
| -----------------------|:--------:| 
| Replay buffer size     | 1e5      | 
| Batch size             | 128      |  
| Discount factor        | 0.99     |
| LR_Actor               | 2e-4     |
| LR_Critic              | 2e-4     |
| TAU soft update target | 1e-3     |

## 4. Results

## 5. Future work

