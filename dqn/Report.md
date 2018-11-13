# The Algorithm

We used a simple DQN architecture with the following components.

## The Q-Network:
  A neural network with 2 hidden layers with 64 units each.
  
## The Agent:
 ### 1) 2 Q-networks: a local netwok and a target network.
 ### 2) A replay buffer to store the tuples (state, action, next state, reward)
 
 
# The Parameters
 
Replay buffer size = 10000
Batch size = 64
Gamma (discount factor for the bellman equation) = 0.99
Learning rate = 0.0005
Update frequency of the target network = 4
Number fo episodes = 2000

# Results

The agent was able to reach an average score of 15 after 800 episodes with this simple architecture.
