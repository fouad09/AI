## The Algorithm

We used a simple DQN architecture with the following components.

## The Q-Network:
  A neural network with 2 hidden layers with 64 units each.
  
## The Agent:
 #### 1) 2 Q-networks: a local netwok and a target network.
         * the q-network is used to estimate the state / action-value function.
         * the target network is used to stabilize the learning process.
        
 #### 2) A replay buffer to store the tuples (state, action, next state, reward)
        * After each iteration the agent store the following tuple inside a buffer.
        * We will simple from this buffer a batch in order to estimate the state / action-value function.
        * We use this value function to derive the optimal policy.
 
 
## The Parameters
        * Replay buffer size = 10000
        * Batch size = 64
        * Gamma (discount factor for the bellman equation) = 0.99
        * Learning rate = 0.0005
        * Update frequency of the target network = 4
        * Number fo episodes = 2000

## Results
 * The agent was able to reach an average score of 15 after 800 episodes with this simple architecture.

## Improvement
 * One simple improvement is to apply the n-step dqn  to speedup convergence. for more details refere to (Sutton 1988).
 * The idea is simple:
    Since Q[St,at] = rt + gamma * max(Q[St+1, at+1])    &
          Q[St+1,at+1] = rt + gamma * max(Q[St+2, at+2])    than
          Q[St,at] = rt + gamma * rt+1 + gamma^2 * max(Q[St+2, at+2])
          
   So the one step transition simpling will be replaced by longer transition simpling (usually 2 or 3 steps max). 
