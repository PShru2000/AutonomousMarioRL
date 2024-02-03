# Autonomous Gameplay in Super Mario Bros. Using Reinforcement Learning



## Problem Statement 
The objective of this project is to develop a reinforcement learning algorithm capable of autonomously navigating and completing the first level of the Super Mario Bros. game. This entails developing a system that can understand and interact with the game environment in real-time, making decisions to move Mario through the level efficiently and reach the flag at the end of the level as quickly as possible. Here the  game is expressed as a sequence of states(s), actions(a) and rewards(r).


## Installations

- Python
- Pytorch
- TensorFlow
- Gym
- MATLAB


## Setting up the Environment

Created a virtual environment and installed gym-super-mario-bros with **pip install gym-super-mario-bros** for Super Mario Bros. gameplay with reinforcement learning.



## Algorithms implemented

#### 1) Policy Gradient

This method uses a neural network with convolutional and linear layers to learn the optimal policy for playing Super Mario Bros. The network outputs action probabilities, and training involves episodes where actions are sampled according to the policy and associated with rewards. The model updates focus on encouraging actions leading to higher rewards, using a policy gradient update rule. Training visualization includes plotting the mean reward per batch to monitor learning progress.


#### 2) Double Deep Q-Network (DDQN)

This implementation enhances the standard DQN by using two networks to reduce overestimation of Q-values. It stabilizes learning by separating action selection (online network) from Q-value estimation (target network). The agent learns optimal policies through experience replay, where it updates the online network using sampled past experiences and periodically synchronizes the target network's weights with the online network's weights.


#### 3) Proximal Policy Optimization with Generalized Advantage Estimation (PPO+GAE)

PPO+GAE combines the PPO algorithm with GAE for efficient and effective training. It features an actor-critic model where the actor selects actions and the critic evaluates their potential reward. PPO ensures stable policy updates through policy clipping, while GAE provides a more accurate estimation of action advantages, facilitating a balanced exploration-exploitation trade-off and improving agent performance over time.



# Result Analysis

**A. Policy Gradient Analysis:**

The policy gradient method showed a quick understanding of the game's dynamics, as seen in the rapid increase in average rewards over the first 1000 episodes. This initial success plateaued as the method fine-tuned its strategies to deal with more complex scenarios. The gap between average and peak rewards suggests room for improvement in specific game situations.

**B. Double Deep Q-Network Analysis:**

The DDQN method demonstrated consistent learning progress, with a steady rise in average rewards and occasional peaks indicating the potential for excellent performance. The persistent variance between average and maximum rewards indicates opportunities for optimization to achieve more consistent high performances.

**C. Proximal Policy Optimization with Generalized Advantage Estimation Analysis:**

PPO-GAE showed remarkable efficiency, with a steep increase in average rewards early on and a stable growth thereafter. It achieved significantly high rewards in a relatively short amount of training, highlighting its effectiveness in the Super Mario Bros. environment.


## Conclusion

In our comparative analysis of reinforcement learning strategies for Super Mario Bros., Proximal Policy Optimization with Generalized Advantage Estimation (PPO-GAE) emerged as the leading approach. It significantly outperformed Policy Gradient and Double Deep Q-Network (DDQN) methods in several key aspects:


- **Learning Speed:** PPO-GAE achieved notable average rewards much faster, showing a steep learning curve within the first 1000 episodes.
- **Performance:** It attained the highest average and peak rewards, demonstrating its superior capability in mastering the game's complexities.
- **Time Efficiency:** PPO-GAE reached optimal performance levels quicker than its counterparts, making it the most time-efficient algorithm in our study.
- **Computational Resource Utilization:** The algorithm's effective use of computational resources highlights its suitability for complex gaming scenarios, advocating for rapid strategy development.
