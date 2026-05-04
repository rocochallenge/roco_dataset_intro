# 🦾 RoCo Challenge 2026 Dataset

## 📘 Overview

The **RoCo Challenge 2026** dataset is designed for collaborative gearbox assembly in human-centered manufacturing settings.  
It includes synchronized multimodal observations and robot actions from a bimanual collaborative platform.

## 📂 Dataset Access

The dataset is hosted on Hugging Face:

👉 https://huggingface.co/datasets/rocochallenge2025/rocochallenge2025

## 📊 Data Schema

| Group | Dataset | Shape | Description |
|---|---|---|---|
| `/actions` | `left_arm_action` | `(N, 7)` | Left arm Cartesian + gripper command |
| `/actions` | `right_arm_action` | `(N, 7)` | Right arm Cartesian + gripper command |
| `/observations` | `left_arm_ee_pose` | `(N, 7)` | Left end-effector pose (xyz + quaternion) |
| `/observations` | `right_arm_ee_pose` | `(N, 7)` | Right end-effector pose (xyz + quaternion) |
| `/observations` | `left_arm_joint_position` | `(N, 6)` | Left joint positions (rad) |
| `/observations` | `right_arm_joint_position` | `(N, 6)` | Right joint positions (rad) |
| `/observations` | `left_arm_joint_velocity` | `(N, 6)` | Left joint velocities |
| `/observations` | `right_arm_joint_velocity` | `(N, 6)` | Right joint velocities |
| `/observations` | `left_gripper_position` | `(N, 1)` | Left gripper opening ratio |
| `/observations` | `right_gripper_position` | `(N, 1)` | Right gripper opening ratio |
| `/observations` | `rgb_head` | `(N, 240, 320, 3)` | Head camera RGB frames |
| `/observations` | `rgb_left_hand` | `(N, 240, 320, 3)` | Left wrist camera RGB frames |
| `/observations` | `rgb_right_hand` | `(N, 240, 320, 3)` | Right wrist camera RGB frames |

Each sample corresponds to one synchronized timestep in a demonstration trajectory.
