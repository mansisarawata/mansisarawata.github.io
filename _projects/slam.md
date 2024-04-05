---
layout: page
title: Advancing DynaVINS through Visual Bundle Adjustment
description: Visual-inertial SLAM leverages various Bundle Adjustment (BA) methods which optimize camera poses and 3D maps by incorporating both visual and inertial measurements. BA holds significant importance as it refines system estimates, aligns sensor data, and ensures global consistency in real time. Our approach involves incorporating insights from a baseline paper (DynaVINS) and tries to enhance its robustness and accuracy. The framework is robust to dynamic and temporarily static objects, utilizing a tightly coupled sensor fusion approach to integrate visual and inertial measurements. 
img: assets/img/slam1.gif
importance: 3
category: SLAM & Perception
---

The DynaVINS pipeline's BA formulation is expressed as a minimization problem, addressing residuals for marginalization, IMU, and visual reprojection measurements. It utilizes the Huber loss, a balanced approach that mitigates sensitivity to outliers in regression problems. The effectiveness of the Huber loss is discussed in scenarios with varying proportions of outliers, highlighting its robustness but acknowledging limitations in the presence of a high ratio of outliers.

To address challenges associated with outliers, the BA method introduces a two-step process involving a regularization factor leveraging IMU preintegration and a momentum factor considering the previous state of each weight. A novel loss term inspired by B-R duality is introduced to reject outlier features while robustly estimating poses. This regularization factor, along with a weight momentum factor, aims to mitigate the impact of features with high reprojection errors.

The paper emphasizes the need for these adjustments when dealing with dynamic objects and aggressive motion. It introduces a regularization factor inspired by B-R duality to reject outlier features while robustly estimating poses. Additionally, a weight momentum factor is introduced to make previously estimated feature weights unaffected by aggressive motion.

The final Bundle Adjustment formulation incorporates both the regularization and weight momentum factors, presenting a comprehensive strategy to address the challenges associated with outliers in VI-SLAM. The major takeaways include the comparative performance analysis of the conventional BA switched into the DynaVINS framework and the justification for utilizing the Huber loss. The robust BA strategy with weights demonstrates its efficacy in avoiding dynamic obstacles, showcasing the importance of these factors in improving VI-SLAM performance.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/slam1.gif" title="" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    DynaVINS performance with and without Bundle Adjustment. Blue represents DynaVINS with BA whereas Red represents without BA.
</div>



