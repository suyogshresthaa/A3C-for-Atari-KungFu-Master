# Asynchronous Advantage Actor-Critic (A3C) for Atari Kung Fu Master

## Project Overview

This project implements an Asynchronous Advantage Actor-Critic (A3C) reinforcement learning agent trained to play the Atari game Kung Fu Master using deep neural networks and parallelized asynchronous learning.

The model uses multiple worker environments running simultaneously to improve exploration efficiency and training stability. A Convolutional Neural Network (CNN) processes raw visual game frames, while actor-critic learning enables the agent to optimize gameplay decisions over time.

---

# Features

- A3C reinforcement learning implementation
- Parallel asynchronous training
- Convolutional Neural Network (CNN) architecture
- Actor-Critic policy optimization
- Atari Kung Fu Master environment integration
- Frame preprocessing and normalization
- Multi-environment training setup
- PyTorch implementation
- GPU-compatible training pipeline
- Reinforcement learning from raw pixel input

---

# Overview of A3C

Asynchronous Advantage Actor-Critic (A3C) is a reinforcement learning algorithm that trains multiple agents in parallel using separate environment instances.

Unlike Deep Q-Learning, A3C directly learns:

- A policy function (Actor)
- A value function (Critic)

The Actor decides which action to take, while the Critic evaluates how good the current state is. Multiple worker agents asynchronously update a shared global network, improving training efficiency and exploration diversity.

---

# Asynchronous Training

A3C improves training efficiency by using multiple worker environments running in parallel.

Each worker:
1. Interacts with its own environment
2. Collects experiences independently
3. Computes gradients locally
4. Updates the shared global network asynchronously

This approach:
- Reduces sample correlation
- Improves exploration diversity
- Accelerates convergence
- Stabilizes training

---

# Reward Strategy

The reinforcement learning agent learns using rewards provided by the environment.

## Positive Rewards
- Defeating enemies
- Progressing through levels
- Increasing score
- Surviving longer

## Negative Outcomes
- Losing health
- Losing lives
- Inefficient combat behavior

The objective is to maximize long-term cumulative rewards.

---

# Installation

## Clone the Repository

```bash
git clone https://github.com/suyogshresthaa/A3C-for-Atari-KungFu-Master.git
cd A3C-for-Atari-KungFu-Master
```

---

# Install Dependencies

```bash
pip install -r requirements.txt
```

---

# Running the Project

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open the notebook file and run the cells sequentially.

---

# Training Pipeline

The training process includes:

1. Environment initialization
2. Frame preprocessing
3. Parallel worker creation
4. Policy-based action selection
5. Reward collection
6. Asynchronous gradient updates
7. Global network synchronization

Training continues until the agent improves gameplay performance over time.

---

# Future Improvements

Potential future enhancements include:

- PPO implementation
- Distributed GPU training
- Checkpoint saving/loading
- Hyperparameter optimization
- Training visualization dashboard

---

# Project Structure

```text
project-root/
│
├── A3C_for_KungFu.ipynb
├── requirements.txt
└── README.md
```

---

# License

This project is intended for educational purposes.

---

# Author

Suyog Shrestha
Knox College - 2027
````
