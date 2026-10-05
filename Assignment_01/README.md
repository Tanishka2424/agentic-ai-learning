# Comparative Agent Architecture Simulator

## 📌 Overview

This project implements and compares four fundamental **Agentic AI architectures** in a common **Grid-World environment**:

- Simple Reflex Agent
- Model-Based Reflex Agent
- Goal-Based Agent
- Utility-Based Agent

The agents are evaluated across **5 different environment configurations** based on their steps taken and task completion rate.

## 🎯 Objective

To understand how different agent architectures perceive an environment, make decisions, and perform tasks, while comparing their **efficiency, decision-making, and robustness** under changing environmental conditions.

## 🗺️ Environment

A grid-world environment is used where:

- `0` → Free cell
- `1` → Obstacle
- **Start** → Agent's initial position `(0, 0)`
- **Goal** → Target position `(3, 4)`

The environment provides percepts about the agent's surroundings and supports movement in four directions:
```
UP
DOWN
LEFT
RIGHT
```

## 🤖 Agent Architectures

### 1. Simple Reflex Agent

Uses **condition-action rules** based primarily on the current percept.
```
Current Percept → Rule → Action
```

### 2. Model-Based Reflex Agent

Maintains an **internal model** of previously observed environment states.
```
Percept → Internal Model → Decision → Action
```

### 3. Goal-Based Agent

Uses **goal-directed search** to determine an efficient path to the target. **Breadth-First Search (BFS)** is used to find the shortest path.
```
Current State + Goal → BFS → Path → Action
```

### 4. Utility-Based Agent

Evaluates possible actions using a **utility function** considering factors such as distance, battery/resource level, and previously visited cells.
```
Candidate Actions → Utility Evaluation → Best Action
```

## 🧪 Experimental Setup

The four agents are tested across **5 Grid-World configurations** with different obstacle arrangements.

Total experiments:
```
4 Agents × 5 Configurations = 20 Experiments
```

Performance metrics:

- Number of steps
- Task completion
- Completion rate
- Average steps across configurations

## 📊 Results

| Agent                    | Average Steps | Completion Rate |
| ------------------------ | ------------- | --------------- |
| Goal-Based Agent         | 7.0           | 100%            |
| Model-Based Reflex Agent | 7.4           | 100%            |
| Simple Reflex Agent      | 15.6          | 80%             |
| Utility-Based Agent      | 41.4          | 20%             |

The **Goal-Based Agent** achieved the best performance in the tested configurations, while the Model-Based Reflex Agent also demonstrated reliable performance.

## 🛠️ Technologies Used

- Python 3.x
- Google Colab / Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- Python `collections.deque`

## 📚 Assignment Context

This project was developed as **Assignment 01 — Unit I: Introduction to Agentic AI and Autonomous Systems** for the Agentic AI course.

The assignment focuses on understanding the distinction between different autonomous agent architectures and their **perception, reasoning, planning, action, and feedback** behaviour
