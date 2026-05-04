# 📋 Installation Guide

This guide covers environment setup and sanity checks for the RoCo Challenge simulation stack.

## ✅ Prerequisites

- Python 3.11
- CUDA 12.2
- Git

## 1) Clone the repository

```bash
git clone https://github.com/rocochallenge/gearboxAssembly.git
```

## 2) Install Isaac Lab + Isaac Sim

Install **Isaac Lab 2.3.0** with **Isaac Sim 5.0.0** following the official guide:  
https://isaac-sim.github.io/IsaacLab/main/source/setup/installation/index.html

> We recommend a conda-based setup for easier command-line execution.

## 3) Install RoCo extension in editable mode

Use a Python environment where Isaac Lab is already available:

```bash
python -m pip install -e source/Galaxea_Lab_External
```

## 4) Verify installation

### List available tasks

```bash
python scripts/list_envs.py
```

If task naming changes, update the search pattern in `scripts/list_envs.py`.

### Run dummy agents

- Zero-action agent:

```bash
python scripts/zero_agent.py --task=<TASK_NAME>
```

- Random-action agent:

```bash
python scripts/random_agent.py --task=<TASK_NAME>
```

## 5) Evaluate model performance

Evaluation scripts: **TBA**.
