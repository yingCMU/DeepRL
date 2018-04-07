# DeepRL
Highly modularized implementation of popular deep RL algorithms by PyTorch. My principal here is to reuse as much components as possible through different algorithms and switch easily between classical control tasks like CartPole and Atari games with raw pixel inputs.

Implemented algorithms:
* (Double/Dueling) Deep Q-Learning (DQN)
* Categorical DQN (C51, Distributional DQN with KL Distance)
* Quantile Regression DQN (Distributional DQN with Wasserstein Distance)
* Synchronous Advantage Actor Critic (A2C)
* Synchronous N-Step Q-Learning
* Deep Deterministic Policy Gradient (DDPG)
* Synchronous Proximal Policy Optimization (PPO)
* Action Conditional Video Prediction

Following asynchronous algorithms are removed now in this repo but can be found in [previous release ](https://github.com/ShangtongZhang/DeepRL/releases/tag/v0.1)
* Async Advantage Actor Critic (A3C)
* Async One-Step Q-Learning
* Async One-Step Sarsa 
* Async N-Step Q-Learning
* Continuous A3C
* Distributed Deep Deterministic Policy Gradient (Distributed DDPG, aka D3PG)
* Parallelized Proximal Policy Optimization (P3O, similar to DPPO)

# Curves
> Curves for CartPole are trivial so I didn't place it here. And there isn't any fixed random seed. The curves are generated in the same manner as OpenAI baselines (one run and smoothed by recent 100 episodes)
## DQN
![Loading...](https://raw.githubusercontent.com/ShangtongZhang/DeepRL/master/images/DQN-breakout.png)

## A2C 
![Loading...](https://raw.githubusercontent.com/ShangtongZhang/DeepRL/master/images/A3C-Pong.png)

## DDPG 
![Loading...](https://raw.githubusercontent.com/ShangtongZhang/DeepRL/master/images/DDPG.png)

## PPO 
![Loading...](https://raw.githubusercontent.com/ShangtongZhang/DeepRL/master/images/P3O.png)

## Action Conditional Video Prediction

![Loading...](https://raw.githubusercontent.com/ShangtongZhang/DeepRL/master/images/ACVP.png)

**Left**: One-step prediction **Right**: Ground truth

Prediction is sampled after 110K iterations and I only implemented one-step training

## Categorical DQN

![Loading...](https://raw.githubusercontent.com/ShangtongZhang/DeepRL/master/images/CategoricalDQN.png)

## Quantile Regression DQN
![Loading...](https://raw.githubusercontent.com/ShangtongZhang/DeepRL/master/images/QRDQN.png)

## N-Step Q-Learning
![Loading...](https://raw.githubusercontent.com/ShangtongZhang/DeepRL/master/images/A2C-NStepQ.png)

# Dependency
> Tested in macOS 10.12 and CentO/S 6.8
* OpenAI gym
* [Roboschool](https://github.com/openai/roboschool) (Optional)
* PyTorch v0.3.0
* Python 2.7 / 3.6
* [TensorboardX](https://github.com/lanpa/tensorboard-pytorch)


# Usage
```dataset.py```: generate dataset for action conditional video prediction

```main.py```: all other algorithms

# References
* [Human Level Control through Deep Reinforcement Learning](https://www.nature.com/nature/journal/v518/n7540/full/nature14236.html)
* [Asynchronous Methods for Deep Reinforcement Learning](https://arxiv.org/abs/1602.01783)
* [Deep Reinforcement Learning with Double Q-learning](https://arxiv.org/abs/1509.06461)
* [Dueling Network Architectures for Deep Reinforcement Learning](https://arxiv.org/abs/1511.06581)
* [Playing Atari with Deep Reinforcement Learning](https://arxiv.org/abs/1312.5602)
* [HOGWILD!: A Lock-Free Approach to Parallelizing Stochastic Gradient Descent](https://arxiv.org/abs/1106.5730)
* [Deterministic Policy Gradient Algorithms](http://proceedings.mlr.press/v32/silver14.pdf)
* [Continuous control with deep reinforcement learning](https://arxiv.org/abs/1509.02971)
* [High-Dimensional Continuous Control Using Generalized Advantage Estimation](https://arxiv.org/abs/1506.02438)
* [Hybrid Reward Architecture for Reinforcement Learning](https://arxiv.org/abs/1706.04208)
* [Trust Region Policy Optimization](https://arxiv.org/abs/1502.05477)
* [Proximal Policy Optimization Algorithms](https://arxiv.org/abs/1707.06347)
* [Emergence of Locomotion Behaviours in Rich Environments](https://arxiv.org/abs/1707.02286)
* [Action-Conditional Video Prediction using Deep Networks in Atari Games](https://arxiv.org/abs/1507.08750)
* [A Distributional Perspective on Reinforcement Learning](https://arxiv.org/abs/1707.06887)
* [Distributional Reinforcement Learning with Quantile Regression](https://arxiv.org/abs/1710.10044)