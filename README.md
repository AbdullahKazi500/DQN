# DQN
## source code for Optimized Dynamic Syndrome Measurement Scheduling and Quantum Reinforcement Learning with Cirq and Classical Agents
# Quantum RL Repository

This repository contains experiments for **Quantum Reinforcement Learning (QRL)** using both **DQN** and **LSTD** agents applied to minimal quantum error correction (3-qubit repetition code).

## Repository Structure

- `DQNRL.ipynb`  
  Notebook for **Dynamic Syndrome Measurement Scheduling** using a **DQN agent**.  
  - Trains a Q-learning agent to choose stabilizer measurements efficiently  
  - Uses Cirq for quantum simulation  
  - Visualizes rewards, Q-values, and action distributions  

- `QRLwithLSTD.ipynb`  
  Notebook for **Linear Function Approximation RL** using **LSTD**.  
  - Implements a linear TD agent for syndrome measurement selection  
  - Evaluates logical qubit fidelity  
  - Plots learned weights, logical fidelity, and measurement cost  

## Project Overview

Quantum computers are highly susceptible to errors due to decoherence and noise. This project focuses on a **minimal quantum error correction (QEC) scenario**, specifically a **3-qubit repetition code**, where an RL agent learns to choose stabilizer measurements efficiently.

**Key objectives:**

- Simulate quantum circuits and measurements using **Cirq**  
- Define a reinforcement learning environment representing qubits and syndrome measurements  
- Train classical RL agents to maximize logical qubit fidelity while minimizing measurement costs  
- Visualize learning progress and Q-values  

---

## Features

### Quantum Environment

- Supports noise modeling and measurement of stabilizers  
- Returns features including qubit states and syndrome information  
- Computes rewards based on logical fidelity and measurement costs  

### Agents

- **LSTD Agent:** Uses linear function approximation for Q-value estimation  
- **DQN Agent:** Q-learning agent for discrete state-action mapping  

### Training and Evaluation

- Supports multiple episodes and steps per episode  
- Tracks total rewards, cumulative rewards, and measurement cost  
- Evaluates logical qubit fidelity  

### Visualization

- Episode rewards over time  
- Cumulative and moving-average rewards  
- Q-value heatmaps  
- Action distribution across episodes  

---

## Installation

The project relies on **Python 3** and the following key libraries:

- `numpy`, `scipy` for numerical computation  
- `matplotlib`, `seaborn`, `pandas` for visualization and data analysis  
- `cirq` for quantum circuit simulation  
- `keras-rl` for reinforcement learning utilities  
- `gymnasium` / `stable-baselines3` for environment abstractions  

**Installation steps:**

```bash
# Upgrade pip
pip install --upgrade pip

# Install dependencies
pip install numpy scipy matplotlib seaborn pandas keras-rl gymnasium stable-baselines3

# Install Cirq
pip install cirq
