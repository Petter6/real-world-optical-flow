# Real-World Optical Flow Benchmark

This Real-World Optical Flow benchmark consists of three datasets, **Slow Flow**, **TAP Flow**, and **FlowFactor**, totaling 8,373 frame pairs.

## Dataset Download Links

- [Slow Flow](#)
- [TAP Flow](#)
- [FlowFactor](#)

## Usage

All datasets are provided in **KITTI format**. To easily test different models, we recommend using the [PTLFlow](https://github.com/hmorimitsu/ptlflow) framework.

### Steps with PTLFlow

1. In `datasets.yaml`, change the path of `kitti_2015` to point to one of the three datasets (Slow Flow, TAP Flow, or FlowFactor).

2. Run the validation script:

```bash
   python validate.py --model raft --ckpt_path things --data.val_dataset kitti-test
```

   Replace `raft` with your model of choice and `things` with your checkpoint.

