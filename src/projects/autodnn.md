---
title: AutoDNN Early-Exit Integration
date: 2024-10-01
topics: ["C++", "Python", "Inference Serving"]
lead: Dynamic early-exit integration for adaptive inference serving.
---

Enhanced AutoDNN, a programmable inference serving system, with dynamic
early-exit capabilities to reduce inference costs while maintaining SLA
compliance under bursty demand.

Introduced adaptive branching policies that decide when to exit early from
neural network computation based on confidence thresholds and current load.
Developed compatibility shims to integrate seamlessly with the existing AutoDNN
runtime.

The system maintains 99.99% SLA compliance while reducing average inference
latency and cost by allowing simpler models to handle easier requests.

Key features:

- Adaptive early-exit branching policies
- Dynamic threshold adjustment based on load
- Compatibility layer for AutoDNN runtime
- Maintains SLA compliance under traffic bursts
- Cost reduction through selective early termination

Technologies: C++, Python, PyTorch
