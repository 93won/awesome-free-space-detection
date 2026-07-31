# Awesome Free Space Detection [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of learning-based and vision-based free space detection / traversability estimation for mobile robots and autonomous driving.

Free space detection answers a simple question for a robot: *"Where can I safely go right now?"*
This list focuses on **learning-based** and **vision-based** approaches — 2D segmentation, depth-guided methods, BEV / 3D occupancy prediction, and self-supervised / foundation-model traversability estimation.

Contributions are welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

## Contents

- [2D Segmentation-based (Camera / RGB-D)](#2d-segmentation-based-camera--rgb-d)
- [Depth-guided Indoor Free Space](#depth-guided-indoor-free-space)
- [BEV / 3D Occupancy Prediction](#bev--3d-occupancy-prediction)
- [Self-supervised / Foundation-model Traversability](#self-supervised--foundation-model-traversability)
- [Surveys & Paper Lists](#surveys--paper-lists)
- [Datasets & Benchmarks](#datasets--benchmarks)

## 2D Segmentation-based (Camera / RGB-D)

Pixel-wise segmentation of drivable / free area from camera (optionally fused with depth).

| Name | Paper | Venue / Year | Code |
|------|-------|--------------|------|
| DeepLabv3+ indoor drivable path | [Drivable path detection for a mobile robot with differential drive using a deep learning based segmentation method for indoor navigation](https://peerj.com/articles/cs-2514/) | PeerJ Computer Science, 2024 | — |
| SNE-RoadSegV2 | [SNE-RoadSegV2: Advancing Heterogeneous Feature Fusion and Fallibility Awareness for Freespace Detection](https://arxiv.org/abs/2402.18918) | IEEE journal ([Xplore](https://ieeexplore.ieee.org/document/10906412/)), 2025 · 1st on KITTI Road | To be released (predecessor [SNE-RoadSeg](https://github.com/hlwang1124/SNE-RoadSeg), ECCV 2020) |
| AGSL | [Effective Free-Driving Region Detection for Mobile Robots by Uncertainty Estimation Using RGB-D Data](https://www.mdpi.com/1424-8220/22/13/4751) | Sensors 22(13), 2022 | — |
| Task-Oriented Pre-Training | [Task-Oriented Pre-Training for Drivable Area Detection](https://arxiv.org/abs/2409.20166) | arXiv, 2024 | — |
| Adversarial-robust free-space segmentation | [Enhancing Robustness of Indoor Robotic Navigation with Free-Space Segmentation Models Against Adversarial Attacks](https://arxiv.org/abs/2402.08763) | IEEE IRC, 2023 | — |

## Depth-guided Indoor Free Space

Depth priors guide the segmentation of navigable floor in cluttered indoor scenes.

| Name | Paper | Venue / Year | Code |
|------|-------|--------------|------|
| Depth-guided Free-space Segmentation | [Depth-guided Free-space Segmentation for a Mobile Robot](https://arxiv.org/abs/2311.01966) | arXiv, 2023 | — |

## BEV / 3D Occupancy Prediction

Camera features are lifted into a BEV / voxel grid; the network directly predicts per-cell free / occupied / semantic states.

| Name | Paper | Venue / Year | Code |
|------|-------|--------------|------|
| Cam4DOcc | [Cam4DOcc: Benchmark for Camera-Only 4D Occupancy Forecasting in Autonomous Driving Applications](https://arxiv.org/abs/2311.17663) | CVPR 2024 | [haomo-ai/Cam4DOcc](https://github.com/haomo-ai/Cam4DOcc) |

See also the curated method collections below for TPVFormer, SurroundOcc, FB-OCC, SparseOcc, GaussianFormer, and more.

## Self-supervised / Foundation-model Traversability

The robot's own driving experience (or a vision foundation model) replaces manual labels.

| Name | Paper | Venue / Year | Code |
|------|-------|--------------|------|
| V-STRONG | [V-STRONG: Visual Self-Supervised Traversability Learning for Off-road Navigation](https://arxiv.org/abs/2312.16016) | ICRA 2024 | — ([project site](https://sites.google.com/view/visual-traversability-learning)) |
| W-RIZZ | [W-RIZZ: A Weakly-Supervised Framework for Relative Traversability Estimation in Mobile Robotics](https://arxiv.org/abs/2406.02822) | RA-L 2024 | [andreschreiber/W-RIZZ](https://github.com/andreschreiber/W-RIZZ) |
| STEPP | [Watch Your STEPP: Semantic Traversability Estimation using Pose Projected Features](https://arxiv.org/abs/2501.17594) | ICRA 2025 | [RPL-CS-UCL/STEPP-Code](https://github.com/RPL-CS-UCL/STEPP-Code) |
| ViTA | [From General Vision to Reliable Traversability Estimation: Adapting Vision Foundation Models for Unstructured Outdoor Environments](https://arxiv.org/abs/2605.29565) | arXiv, 2026 | — |
| Scene-Agnostic Traversability | [Scene-Agnostic Traversability Labeling and Estimation via a Multimodal Self-supervised Framework](https://arxiv.org/abs/2508.18249) | arXiv, 2025 | — |
| COTRATE | [Self-Supervised Online Robot-Agnostic Traversability Estimation for Open-World Environments](https://arxiv.org/abs/2605.28442) | arXiv, 2026 | Announced in paper |

## Surveys & Paper Lists

| Name | Paper | Venue / Year | Code |
|------|-------|--------------|------|
| Occupancy Perception Survey | [A Survey on Occupancy Perception for Autonomous Driving: The Information Fusion Perspective](https://github.com/HuaiyuanXu/3D-Occupancy-Perception) | Information Fusion, 2025 | [HuaiyuanXu/3D-Occupancy-Perception](https://github.com/HuaiyuanXu/3D-Occupancy-Perception) |
| Vision-based 3D Occupancy Review | [Vision-based 3D occupancy prediction in autonomous driving: a review and outlook](https://arxiv.org/abs/2405.02595) | Frontiers of Computer Science ([Springer](https://link.springer.com/article/10.1007/s11704-024-40443-5)) | [zya3d/Awesome-3D-Occupancy-Prediction](https://github.com/zya3d/Awesome-3D-Occupancy-Prediction) |
| Multi-Camera 3D Occupancy Collection | — | — | [lvchuandong/Awesome-Multi-Camera-3D-Occupancy-Prediction](https://github.com/lvchuandong/Awesome-Multi-Camera-3D-Occupancy-Prediction) |

## Datasets & Benchmarks

| Name | Description | Link |
|------|-------------|------|
| KITTI Road | Classic road / free space detection benchmark | [Benchmark](https://www.cvlibs.net/datasets/kitti/eval_road.php) |
| Cam4DOcc | Camera-only 4D occupancy forecasting benchmark (built on nuScenes, nuScenes-Occupancy, Lyft-Level5) | [haomo-ai/Cam4DOcc](https://github.com/haomo-ai/Cam4DOcc) |

## License

[CC0 1.0 Universal](LICENSE) — public domain dedication.
