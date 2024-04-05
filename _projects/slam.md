---
layout: page
title: Advancing DynaVINS through Visual Bundle Adjustment
description: Visual-inertial SLAM leverages various Bundle Adjustment (BA) methods which optimize camera poses and 3D maps by incorporating both visual and inertial measurements. BA holds significant importance as it refines system estimates, aligns sensor data, and ensures global consistency in real time. Our approach involves incorporating insights from a baseline paper (DynaVINS) and tries to enhance its robustness and accuracy. The framework is robust to dynamic and temporarily static objects, utilizing a tightly coupled sensor fusion approach to integrate visual and inertial measurements. 
img: assets/img/slam1.gif
importance: 3
category: SLAM & Perception
---

Visual-inertial SLAM (Simultaneous Localization and Mapping) techniques are crucial for robotics, UAVs, and autonomous vehicles. However, the assumption of static landmarks in most SLAM algorithms poses challenges for accurate localization in dynamic environments. To address this, DynaVINS framework offers a solution specifically designed for dynamic SLAM by integrating bundle adjustment techniques.

The study aims to comprehensively examine the bundle adjustment (BA) module within the DynaVINS pipeline to enhance understanding and proficiency in fine-tuning BA methodologies. The objective is to improve the accuracy and reliability of visual-inertial SLAM systems in dynamic scenarios.

DynaVINS employs bundle adjustment along with IMU preintegration, feature tracking, keyframe grouping, and multi-hypothesis-based constraints grouping to handle dynamic scenes effectively. However, conventional BA formulations face challenges in robustly estimating poses and landmarks in the presence of dynamic objects.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/dynapipe.png" title="" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

The study first establishes a baseline with conventional bundle adjustment. Then, it introduces modifications inspired by DynaVINS and DynamSLAM, including regularization and weight momentum factors. The modified Huber loss function from DynamSLAM is also explored. The VIODE dataset is used for experiments, particularly focusing on the parking lot environment with varying levels of dynamic obstacles.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/dyna_con.gif" title="" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


A comparative analysis between traditional VINS-Fusion and DynaVINS demonstrates the latter's superior performance in trajectory accuracy, especially in scenarios with high dynamic object density. Sensitivity analysis of different loss functions shows DynaVINS' resilience across all functions compared to VINS-Fusion. However, challenges in implementing DynamSLAM hindered its evaluation, emphasizing the complexities in integrating such methods.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/loss_study.png" title="" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


The study showcases the potential of DynaVINS in advancing dynamic SLAM capabilities through bundle adjustment techniques. Despite challenges, the research provides valuable insights into enhancing SLAM performance in dynamic environments.

Code and further details are available at the provided at <a href="https://github.com/mansisarawata/dynaVINS_16833"> GitHub repository </a>.
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/slam1.gif" title="" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    DynaVINS performance with and without Bundle Adjustment. Blue represents DynaVINS with BA whereas Red represents without BA.
</div>



