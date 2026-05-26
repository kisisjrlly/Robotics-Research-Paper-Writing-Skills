# Related Work Writing Guide

## Goal

Position your work against the most relevant lines of research, and make your novelty easy to verify.

For robotics, UAV, and embodied AI papers, Related Work should compare both algorithmic mechanisms and system assumptions: sensing, dynamics, compute, environment, real-world validation, and safety or robustness constraints.

## Workflow

1. List directly competing and recent baseline papers first.
2. Group literature by technical topic (not by publication year alone).
3. For each topic: summarize common paradigm, then key limitation relevant to your challenge.
4. End each topic by clarifying your distinction.

## Topic Design

Use 2-4 focused topics, for example:

1. Task-specific mainstream methods.
2. Methods closest to your core idea.
3. Auxiliary techniques your method builds on.

Robotics/UAV topic options:

1. Classical robotics methods: model-based planning/control, SLAM/state estimation, optimization, MPC, sampling-based planning, or geometric control.
2. Learning-based methods: supervised learning, imitation learning, reinforcement learning, representation learning, foundation-model-based robotics, or sim-to-real learning.
3. System and deployment work: onboard autonomy, real-time perception, UAV platforms, multi-robot coordination, communication-constrained autonomy, or field robotics.
4. Benchmarks and datasets: simulation environments, real-world datasets, evaluation protocols, and diagnostic benchmarks.

## Paragraph Template

1. Topic sentence: define scope of this topic.
2. Representative methods: one compact summary.
3. Limitation tied to your target technical challenge.
4. Transition sentence that leads to your method.

## Do and Don't

1. Do compare mechanisms, assumptions, and failure modes.
2. Do emphasize the exact gap your method fills.
3. Do not make Related Work a citation dump.
4. Do not hide strongest baselines.

## Checklist

1. Are all strongest/recent competitors covered?
2. Is each topic connected to your problem setting?
3. Is your difference explained in technical terms, not marketing terms?
4. Is citation coverage complete for all core claims?
5. Are the assumptions of competing methods compared fairly, especially sensors, compute, platform, and real-world validation?
6. Does the text explain whether the closest baselines are offline, simulated, or deployed on real robots/UAVs?
