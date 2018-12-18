# Report

## 1. Scope
In this project the DDPG algorithm is implemented to solve the Reacher environment. This algorithm is composed by two elements: 

- the Actor, a policy-based algorithm
- and a Critic, a value-based algorithm

It is proven that the performance is best when both algorithms work in conjunction. 

## 2. Architecture
The Actor is represented by a neural network with

- Fully connected layer 1: with input = 33 (state spaces) and output = 400
- Fully connected layer 2: with input = 400 and output = 300
- Fully connected layer 3: with input = 300 and output = 4 (for each of the 4 actions)

In the other hand, the Critic is depicted as a neural network with

- Fully connected layer 1: with input = 33 (state spaces) and output = 400
- Fully connected layer 2: with input = 404 (states and actions) and output = 300
- Fully connected layer 3: with input = 300 and output = 1 (maps states and actions to Q-values)

Introducing a batch normalization layer was a determinant factor to get valuable progress. Without it, the algorithm would be oscillating at average score of 4 after 300 episodes, which it clearly was not a good signal of good training. Another factor was the implementation of the gradient cliping method when updating the critic. 

## 3. Hyperparameters

Parameters are crucial to get a converging algorithm. Experimentation showed that learning rates had impact on the training progress.

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
