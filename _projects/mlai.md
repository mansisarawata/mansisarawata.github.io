---
layout: page
title: RNN based Visual Odometry
description: Navigating mobile robots with precision demands accurate vehicle localization, a challenge addressed through vision-based odometry. This study focuses on monocular visual odometry (VO), comparing traditional geometry-based methods with a RNN+CNN model for trajectory estimation. The standard VO pipeline involves feature extraction, camera calibration, and local optimization, requiring prior system knowledge for absolute trajectory recovery. In contrast, the RNN+CNN model infers poses directly, eliminating the need for prior information. The research evaluates both methods using the KITTI Dataset, demonstrating the viability of the end-to-end model over conventional visual odometry systems.
img: assets/img/mlai.png
importance: 4
category: SLAM & Perception
---

Accurate vehicle localization is critical for autonomous navigation in mobile robot applications. Various methods, such as wheel odometry, GPS, INS, and visual odometry, address this challenge, each with its limitations. Visual odometry (VO) emerges as a cost-effective alternative, boasting superior accuracy compared to traditional methods. This research specifically delves into monocular VO, aiming to contribute insights and advancements to the field.

The study utilizes the KITTI Odometry Benchmark dataset, featuring 22 stereo sequences for training and evaluation. This dataset, provided by the Karlsruhe Institute of Technology, Germany, serves as a comprehensive testing ground. The evaluation involves translational and rotational error computation, providing valuable insights into the performance of the proposed methods.

The experimental section presents results from monocular visual odometry and the proposed RNNs for visual odometry on the KITTI dataset. Notably, the research addresses the challenge of aligning localisation results with ground truth due to the lack of absolute scale estimation in most existing monocular VO algorithms.

The dataset is split into training and testing sequences, with the model trained on seven path sequences and tested on five. Training involves leveraging NVIDIA CUDA for 100 epochs, incorporating dropout and early stopping techniques to prevent overfitting. A pre-trained FlowNet model is employed to expedite training.

Stereo Semi-Global Block Matching (SGBM):

The research utilizes OpenCV for stereo depth estimation, employing StereoBM and StereoSGBM methods. Disparity maps and feature matching using SIFT descriptors are visualized, providing insights into tracking vehicle position through sequences.

The performance analysis of trained VO models is conducted based on KITTI VO/SLAM evaluation metrics. The CNN+RNN model demonstrates promising results, with the model mapping the roll, pitch, and yaw of the vehicle, showcasing a reduction in errors as epochs progress.

Thus the study compares geometry-based visual odometry with an innovative CNN+RNN model, highlighting the latter's advantage in eliminating the need for prior system knowledge. By leveraging the KITTI dataset, the research contributes valuable insights and advancements to the field of monocular visual odometry, paving the way for more precise and efficient mobile robot navigation.
