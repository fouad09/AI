
### 1) The Algorithm
We used a DDPG architecture with the following components to solve this continous action space problem.

### The actor network (step 5)
* the actor network estimate the action that the agent should take conditional to the actual state.
* The network take the state space as input (33) an the action space as output (4)
* space-input(33) --> batch-normalisation --> fully-connected|relu(128) --> batch-normalisation --> fully-connected|relu(64) --> batch-normalisation --> action-space|tanh (4)

### The critic network (step 5)
* The critic network estimate how good and 
* The network take the state space (33) and the action space (4) as input an the action space as output (4)
* space-input(33) --> batch-normalisation --> fully-connected|relu(128) --> (fully-connected|relu(128) + action-space(4))|relu -->  fully-connected|relu(64)

### The replay buffer (step 6)

* A replay buffer is used like the dqn algorithm to store the tuples (state, action, next state, reward)
* After each iteration the agent store the following tuple inside a buffer.
* We will simple from this buffer a batch in order to estimate the state / action-value function.
* We use this value function to derive the optimal policy.

### The noise process (step 7)

### The agent (step 8)

### The train function (step 9)


### The main function (step 10)

### results (step 11)

### Test (step 12)

### improvements
