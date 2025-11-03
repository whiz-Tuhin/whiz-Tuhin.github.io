---
title: Distributed MapReduce Framework
date: 2025-01-01
topics: ["C++", "Distributed Systems", "gRPC"]
lead: Master-worker topology with dynamic partitioning and fault tolerance.
---

A distributed MapReduce framework implementing the classic master-worker pattern with modern systems design principles. Built in C++ using gRPC for high-performance RPC communication.

The framework orchestrates distributed computation across worker nodes with dynamic partitioning, speculative retries for stragglers, and fault-aware checkpointing to handle multi-GB workloads with predictable latency.

Key features:
- Master-worker orchestration with health monitoring
- Dynamic partitioning for load balancing
- Speculative execution to handle slow workers
- Fault-aware checkpointing and recovery
- Handles multi-GB datasets with predictable performance

Technologies: C++17, gRPC, Protocol Buffers
