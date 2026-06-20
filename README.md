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

## Licensing & Citations

### Slow Flow

The Slow Flow dataset and reference optical flow ground truth were introduced in:

> J. Janai, F. Güney, J. Wulff, M. J. Black, and A. Geiger.
> **Slow Flow: Exploiting High-Speed Cameras for Accurate and Diverse Optical Flow Reference Data.**
> *IEEE Conference on Computer Vision and Pattern Recognition (CVPR), 2017.*

```bibtex
@inproceedings{Janai2017CVPR,
  author    = {Joel Janai and Fatma G{\"u}ney and Jonas Wulff and Michael Black and Andreas Geiger},
  title     = {Slow Flow: Exploiting High-Speed Cameras for Accurate and Diverse Optical Flow Reference Data},
  booktitle = {Conference on Computer Vision and Pattern Recognition (CVPR)},
  year      = {2017}
}
```

### TAP Flow

TAP Flow is derived from the point-track annotations released as part of **TAP-Vid**:

> C. Doersch, A. Gupta, L. Markeeva, A. Recasens, L. Smaira, Y. Aytar, J. Carreira, A. Zisserman, and Y. Yang.
> **TAP-Vid: A Benchmark for Tracking Any Point in a Video.**
> *Google DeepMind, 2022.*

```bibtex
@article{doersch2022tapvid,
  title   = {TAP-Vid: A Benchmark for Tracking Any Point in a Video},
  author  = {Doersch, Carl and Gupta, Ankush and Markeeva, Larisa and Recasens, Adri{\`a} and Smaira, Lucas and Aytar, Yusuf and Carreira, Jo{\~a}o and Zisserman, Andrew and Yang, Yi},
  journal = {Google DeepMind},
  year    = {2022}
}
```

The TAP-Vid **annotations** (point tracks) are released under a **Creative Commons BY** license. However, the underlying **source video**  carry their own license. We only use the DAVIS dataset which was introduced by 

> F. Perazzi, J. Pont-Tuset, B. McWilliams, L. Van Gool, M. Gross, and A. Sorkine-Hornung.
> **A Benchmark Dataset and Evaluation Methodology for Video Object Segmentation.**
> *Computer Vision and Pattern Recognition (CVPR), 2016.*

```bibtex
@inproceedings{Perazzi2016CVPR,
  author    = {Federico Perazzi and Jordi Pont-Tuset and Brian McWilliams and Luc Van Gool and Markus Gross and Alexander Sorkine-Hornung},
  title     = {A Benchmark Dataset and Evaluation Methodology for Video Object Segmentation},
  booktitle = {Computer Vision and Pattern Recognition (CVPR)},
  year      = {2016}
}
```
