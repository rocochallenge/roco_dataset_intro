# 🎯 Baseline Training & Fine-tuning

This page summarizes baseline policy training options for RoCo Challenge and provides a minimal ACT workflow for quick reproduction.

## Available Baseline Option

### ACT (Action Chunking Transformer)

1. Clone the ACT repository:

```bash
git clone https://github.com/tonyzhaozh/act.git
```

2. Convert RoCo hdf5 data to ACT-compatible format:

```bash
python ./data_preprocess_act.py
```

3. Start training:

```bash
python3 imitate_episodes.py \
  --task_name <task name in constants.py> \
  --ckpt_dir <checkpoint directory> \
  --policy_class ACT \
  --kl_weight 10 \
  --chunk_size 100 \
  --hidden_dim 512 \
  --batch_size 8 \
  --dim_feedforward 3200 \
  --num_epochs 2000 \
  --lr 1e-5 \
  --seed 0
```

> Note: update the selected task entry in `constants.py` before training.
