---
layout: page
title: Resilient Bicopter Control
description: H ∞ loop shaping, H 2 optimal controller & H ∞ optimal controller.
img: assets/img/controls1.gif
importance: 2
category: Controls
# giscus_comments: true
---


Presenting a solution for the intricate task of designing controllers for multi-input output systems, our project centers on the Quanser Aero system. This system, characterized by dual inputs (motor voltages) and dual outputs (pitch and yaw angles), prompted our exploration into the challenge of substantial coupling between these variables. To address this, we employed four distinct controller design techniques: H ∞ loop shaping, H 2 optimal control, H ∞ optimal control, and µ synthesis.

Utilizing MATLAB for controller development and Simulink for simulation, we meticulously adjusted parameters to ensure optimal performance amidst uncertainties introduced into the plant. The project culminated in the implementation of controllers on the hardware setup, subjecting them to a square wave reference for both Yaw and Pitch axes. Rigorous analysis of the results followed, accompanied by additional parameter fine-tuning for controllers displaying suboptimal performance. Notably, the H ∞ loop shaping controller emerged as the most effective performer in reference tracking.

This comprehensive project not only navigated the intricacies of multi-input output systems but also demonstrated a meticulous approach to design, simulation, and implementation. As a result, it significantly contributes to the field of robust bi-copter control, showcasing our commitment to addressing challenges in this domain.
