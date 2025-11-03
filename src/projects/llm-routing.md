---
title: Heterogeneity-Aware LLM Routing
date: 2025-02-01
topics: ["Python", "PyTorch", "LLM Inference"]
lead: ILP-guided scheduling with telemetry feedback for mixed GPU fleets.
---

A simulator and scheduler for heterogeneous LLM inference clusters that reduces P99 latency by 30% across mixed GPU fleets through intelligent request routing.

The system uses Integer Linear Programming (ILP) to guide initial placement decisions and incorporates real-time telemetry feedback loops to dynamically adjust routing as cluster conditions change.

Designed for production environments where GPU clusters contain multiple hardware generations (A100, V100, T4) with varying performance characteristics.

Key features:
- ILP-based optimization for request placement
- Telemetry feedback loops for adaptive routing
- Support for heterogeneous GPU types
- 30% reduction in P99 latency
- Simulator for offline evaluation

Technologies: Python, PyTorch, CVXPY (ILP solver)
