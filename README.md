# Project: Continuous Control 

In this project, the DDPG algorithm is implemented to solve the [Reacher](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher) environment (Twenty agents version).

![reacher](reacher.gif "Reacher Environment")

### The Environment

In this environment there are twenty identical agents in which each one is a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

The individual observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

### Solving the Environment

The twenty agents must get an average score of +30 (over 100 consecutive episodes, and over all agents). Specifically, after each episode, the rewards that each agent received (without discounting) are added up, to get a score for each agent. This yields 20 (potentially different) scores. We then take the average of these 20 scores. This yields an average score for each episode (where the average is over all 20 agents).

### Downloading the Environment

1. Set up your Python environment. Install PyTorch, the ML-Agents toolkit, and a few more Python packages required to complete the project.

2. Installing Unity is not necessary and you can download it from one of the links below. You need only select the environment that matches your operating system:

* Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
* Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
* Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)
* Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)

3. Then, place the file in the main folder of this repository, and unzip (or decompress) the file.

4. Open `Continuous_Control.ipynb` and follow the instructions.
