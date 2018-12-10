
### The Algorithm to solve the Reacher
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

* The noise is an ou mean reverting process. 

### The agent (step 8)

* batch_size  = 256   # batch size sampled from the replay buffer
* update_every = 20   # frequency of updating the networks
* num_updates = 10    # number of updates per episode
* gamma = 0.99        # discount rate to calculate the q-values
* lr_actor = 1e-3     # learning rate used to optimize the actor network
* lr_critic = 1e-3    # learning rate used to optimize the critic network
* tau = 1e-3          # parameter used to update the actor and critic target networks 
* epsilon = 1.0       # variance rate used to generate the noise added to the action vector
* epsilon_decay=1e-6  # parameter used to decay the variance to and reduce the noise

### results (step 11)
* The agent was able to reach an average score of 30 after 182 episodes.

### Test (step 12)
* After training, the agent has an average score of 36 after 3 test.

### improvements

* Simplify the architecture of the actor network.
* Implement a replay buffer with importance sampling.
* change the number of updates during the learning step.
