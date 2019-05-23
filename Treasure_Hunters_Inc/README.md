# Treasure Hunters Inc.
## By Ronald Moore and Austin Adams
  
### *Purpose*
The purpose of this project is to show how reinforcement learning algorithms can be used to train an agent to solve environments without any prior information. In this particular project, the agent will be traversing a maze in order to find a treasure chest. However, there are various obstacles scattered throughout the maze, including snakes, pits, and quicksand traps.


### *Reinforcement Learning Implementation*
The reinforcement learning algorithm used was the q-learning algorithm. Q-learning is the most popular reinforcement algorithm used due to its simplistic nature. The algorithm is given by the equation

Q_new[s(t), a(t)] = (1-alpha) * Q_old[s(t), a(t)] + alpha * (r + gamma * max_a{Q[s(t+1), a]})

#### State (s)
This represents the state in which the agent is in currently. For this particular problem, the state refers to the agent's position within the environment. There are since there are 25 positions within the environment, there are 25 possible states for the agent.

#### Action (a)
This represents the agent's action regarding making a decision. An action causes the agent to transition from its current state to a different state. Depending on the agent's current state, it may be limited to take certain actions or it may only be able to transition to certain states.

#### Reward (r)
This represents the reward value that an agent obtains from being in a certain state. For this environment, depending on the state, the reward value may be positive, negative, or zero.

#### Learning Rate (alpha)
The learning rate *alpha* controls how much of the new information that an agent obtains overrides its past knowledge. If alpha is set to 0, then the agent will discard any new information that it receives when it comes to decision making. However, if alpha is set to 1, then the agent will only consider the new information about the environment when determning which actions to take.

#### Discount Factor (gamma)
The discount factor *gamma* determines the importance of future rewards. If gamma is set to 0, then future rewards will be of no significance to the agent and it will take actions that are extremely short-sighted. However, if gamma is equal to 1, then the agent will aim to take actions that reflect long-term high reward values.

### *Discussion*
From the notebooks, it can be seen that the agent learns to solve the maze faster after each learning session. Additionally, different values of the alpha and gamma seem to dictate how well a given agent is able to learn the environment.

### *References*
https://towardsdatascience.com/introduction-to-q-learning-88d1c4f2b49c

https://en.wikipedia.org/wiki/Q-learning
