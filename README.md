# Real-World Optical Flow Benchmark

This Real-World Optical Flow benchmark consists of three datasets, **Slow Flow**, **TAP Flow**, and **FlowFactor**, totaling 8,373 frame pairs.

## Dataset Download Links

The three datasets can be downloaded [here](https://data.4tu.nl/)

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
@inproceedings{janai2017slow,
  title={Slow flow: Exploiting high-speed cameras for accurate and diverse optical flow reference data},
  author={Janai, Joel and Guney, Fatma and Wulff, Jonas and Black, Michael J and Geiger, Andreas},
  booktitle={Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition},
  pages={3597--3607},
  year={2017}
}
```

### TAP Flow

TAP Flow is derived from the point-track annotations released as part of **TAP-Vid**:

> C. Doersch, A. Gupta, L. Markeeva, A. Recasens, L. Smaira, Y. Aytar, J. Carreira, A. Zisserman, and Y. Yang.
> **TAP-Vid: A Benchmark for Tracking Any Point in a Video.**
> *Google DeepMind, 2022.*

```bibtex
@article{doersch2022tap,
  title={Tap-vid: A benchmark for tracking any point in a video},
  author={Doersch, Carl and Gupta, Ankush and Markeeva, Larisa and Recasens, Adria and Smaira, Lucas and Aytar, Yusuf and Carreira, Joao and Zisserman, Andrew and Yang, Yi},
  journal={Advances in Neural Information Processing Systems},
  volume={35},
  pages={13610--13626},
  year={2022}
}
```

The TAP-Vid **annotations** (point tracks) are released under a **Creative Commons BY** license. We use the DAVIS dataset from TAP-ViD which was introduced in the following paper:

> F. Perazzi, J. Pont-Tuset, B. McWilliams, L. Van Gool, M. Gross, and A. Sorkine-Hornung.
> **A Benchmark Dataset and Evaluation Methodology for Video Object Segmentation.**
> *Computer Vision and Pattern Recognition (CVPR), 2016.*

```bibtex
@inproceedings{perazzi2016benchmark,
  title={A benchmark dataset and evaluation methodology for video object segmentation},
  author={Perazzi, Federico and Pont-Tuset, Jordi and McWilliams, Brian and Van Gool, Luc and Gross, Markus and Sorkine-Hornung, Alexander},
  booktitle={Proceedings of the IEEE conference on computer vision and pattern recognition},
  pages={724--732},
  year={2016}
}
```
