Reinforcement Learning Algorithms: FVMCC, SARSA, Q-learning, Double-Q, and Lambda-based Methods
Project Overview
This project implements various reinforcement learning algorithms, including:

FVMCC
SARSA
Q-learning
Double-Q learning
SARSA(λ) Replacing
SARSA(λ) Accumulating
Q(λ) Replacing
Q(λ) Accumulating
Dyna-Q
Trajectory Learning
For each algorithm, we analyze the following metrics:

Policy Success Rate (%) vs. Episodes
Estimated Expected Return vs. Episodes
State-value Function Estimation Error vs. Episodes
Table of Contents
Getting Started
Algorithms Implemented
Plots and Observations
Policy Success Rate
Estimated Expected Return
State-value Function Estimation Error
How to Run
Dependencies
License
Getting Started
To run this project, clone the repository and ensure you have the required dependencies installed. Instructions on how to execute the algorithms and generate the plots are provided below.

Algorithms Implemented
1. FVMCC
A first-visit Monte Carlo Control algorithm that estimates optimal policies by averaging the returns of first visits to each state-action pair.

2. SARSA
An on-policy temporal difference learning algorithm that updates the action-value function based on the state, action, reward, next state, and next action.

3. Q-learning
An off-policy temporal difference learning algorithm that updates the action-value function using the maximum estimated future rewards.

4. Double-Q Learning
A variation of Q-learning that reduces overestimation bias by maintaining two separate Q-value estimates and updating them alternately.

5. SARSA(λ) Replacing and Accumulating
SARSA with eligibility traces, which combine TD learning and Monte Carlo methods to propagate rewards to previously visited states.

6. Q(λ) Replacing and Accumulating
Q-learning with eligibility traces to improve learning speed and stability by accumulating or replacing eligibility traces.

7. Dyna-Q
An integrated approach that combines model-based and model-free learning by performing planning updates using simulated experiences.

8. Trajectory Learning
An advanced method that learns from entire trajectories of experiences to improve the policy's success rate and expected return.

Plots and Observations
Policy Success Rate
The Policy Success Rate is defined as the number of times the agent reaches the goal state out of the total number of episodes run using a specific policy. The function getPolicySuccessRate(env, πcurrent, goalState, maxEpisodes=100, maxSteps=200) calculates this metric for each episode.

Observation: As the episodes increase, the Policy Success Rate generally improves for each algorithm, though the rate of improvement and stability may vary.
Estimated Expected Return
The Expected Return is the cumulative reward an agent expects to receive from the start state to the goal state.

Observation: The Estimated Expected Return tends to converge as the agent learns a near-optimal policy. The speed of convergence and final value depend on the algorithm's exploration-exploitation strategy.
State-value Function Estimation Error
The State-value Function Estimation Error measures the difference between the estimated and optimal state-value functions.

Observation: This error typically decreases as the agent learns the optimal policy, with some algorithms showing faster convergence and lower error rates.