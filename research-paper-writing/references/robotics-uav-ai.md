# Robotics, UAV, and Embodied AI Paper Guide

## Goal

Adapt general research-paper writing rules to robotics, UAV, and embodied AI papers, where reviewers evaluate both algorithmic novelty and deployable system behavior.

Use this file when the paper involves aerial robots, mobile robots, multi-robot systems, robot perception, mapping, planning, control, reinforcement learning, imitation learning, sim-to-real transfer, embodied perception, or robot foundation models.

## Core Reviewer Questions

1. What task is solved, and under what physical assumptions?
2. What is new: task formulation, representation, planner/controller, perception module, learning objective, system integration, dataset, benchmark, or empirical finding?
3. Why is the method suitable for a robot instead of only an offline model?
4. Does the evidence include realistic dynamics, sensors, compute, latency, noise, disturbances, and failure modes?
5. Are safety-relevant claims scoped carefully and supported by tests?

## Paper Story Patterns

### Pattern 1: Real-World Deployment Gap

Use when an AI method works in curated datasets or simulation but fails under robot deployment constraints.

1. Start from the robotics task and operational requirements.
2. Show why standard learning/perception/planning methods are insufficient under latency, uncertainty, partial observability, or dynamics.
3. Introduce the method as a way to close the deployment gap.
4. Prove the claim with real-robot/UAV experiments or high-fidelity simulation plus transfer evidence.

### Pattern 2: System-Aware AI Method

Use when the contribution is an AI model modified for robot constraints.

1. Define the robot-specific bottleneck: onboard compute, limited sensing, changing viewpoints, safety margins, data scarcity, communication limits, or long-horizon compounding error.
2. Explain the AI design around this bottleneck.
3. Report both model metrics and system metrics.

### Pattern 3: Robotics Insight Backed by Learning

Use when the contribution combines model-based robotics and learning.

1. State the classical robotics principle or structure being preserved.
2. Explain what learning component improves: perception, residual dynamics, cost shaping, policy generation, uncertainty estimation, or adaptation.
3. Show that the combination improves robustness, generalization, or data efficiency.

### Pattern 4: New Benchmark, Dataset, or Task

Use when the contribution is mostly a new setting or benchmark.

1. Make the practical gap concrete.
2. Define task inputs, outputs, evaluation protocol, and safety/feasibility constraints.
3. Justify why existing benchmarks do not capture the target failure modes.
4. Provide strong baselines and diagnostic analyses, not only leaderboard results.

## Method Writing Requirements

Always separate these layers when they exist:

1. Problem formulation: state space, observation, action/control interface, objective, constraints, and assumptions.
2. Robot platform: vehicle/body, sensors, compute, controller stack, communication, payload, and sampling rates.
3. Algorithmic modules: perception, state estimation, mapping, planning, control, learning, adaptation, and safety filter.
4. Execution loop: timing, module inputs/outputs, coordinate frames, update rates, and failure handling.
5. Training or data pipeline: simulator, datasets, domain randomization, supervision, reward, curriculum, and transfer path.
6. Deployment details: onboard/offboard compute, real-time budget, calibration, synchronization, and practical parameters.

Good method prose answers three questions for each module:

1. Why is this module needed for the robot task?
2. How does it run in the closed-loop system?
3. What measurable behavior should improve because of it?

## Experiment Evidence Ladder

Use the strongest applicable evidence, and state the boundary of each level.

1. Offline evaluation: validates perception, prediction, representation, or policy components on datasets.
2. Simulation evaluation: validates closed-loop behavior under controlled scenarios and many trials.
3. High-fidelity simulation: adds dynamics, sensor noise, disturbances, and realistic constraints.
4. Real-robot or real-UAV experiments: validates deployment feasibility, latency, robustness, and integration.
5. Stress tests and failure analysis: validates operating envelope and honest limitations.

Do not write a hardware claim if only offline or ideal simulation results exist. Instead, state that the result indicates potential deployment value and identify what remains to be validated.

## Common Metrics

Choose metrics that match the task and claim.

1. Navigation/planning/control: success rate, collision rate, path length, trajectory error, tracking error, smoothness, constraint violation, control effort, recovery rate.
2. UAV-specific systems: flight time, mission completion rate, energy use, payload limit, wind disturbance tolerance, localization drift, communication loss recovery, onboard FPS, end-to-end latency.
3. Perception and mapping: detection/segmentation metrics, depth/pose error, map accuracy, localization error, loop-closure quality, uncertainty calibration.
4. Multi-robot systems: scalability, coordination success, communication bandwidth, task allocation quality, formation error, deadlock rate.
5. Learning systems: sample efficiency, generalization to unseen scenes, robustness to domain shift, adaptation time, sim-to-real gap.

Every table header should show metric direction, for example `Success Rate ↑`, `Collision Rate ↓`, or `Latency (ms) ↓`.

## Baseline Selection

Include baselines from all relevant families, not only learning methods:

1. Classical robotics baseline: model predictive control, sampling-based planning, optimization-based planning, geometric controller, EKF/SLAM pipeline, or rule-based system when relevant.
2. Learning baseline: supervised, RL, imitation, foundation-model-based, or representation-learning method closest to the paper.
3. Strong recent task-specific methods.
4. Ablated versions that remove or replace each core module.
5. Practical baseline used in real systems, even if it is not the newest paper.

When a baseline cannot run on hardware or in real time, state why and keep the comparison fair in simulation/offline settings.

## Claim-Evidence Rules

1. "Real-time" requires runtime, hardware, batch size, and control/update rate.
2. "Robust" requires perturbations, sensor noise, unseen scenes, dynamics changes, or failure recovery tests.
3. "Safe" requires a precise safety definition and evidence on violations or constraints.
4. "Generalizes" requires held-out environments, tasks, platforms, or domain-shift tests.
5. "Deployable" requires platform details, onboard/offboard compute, latency, and real-world or high-fidelity validation.
6. "Outperforms" requires strong baselines under identical protocols.

## Figure and Table Guidance

1. The first figure should usually show the task setting, robot platform, closed-loop pipeline, and result snapshot.
2. Pipeline figures should mark data/control flow and update rates when timing matters.
3. Qualitative figures should show representative successes and failures, not only cherry-picked successes.
4. Tables should separate offline metrics, simulation metrics, and real-world metrics if they validate different claims.
5. Include scenario labels such as wind, clutter, dynamic obstacle, GPS-denied, low light, unseen scene, or payload condition when they matter.

## Final Domain Checklist

Before finalizing a robotics/UAV/embodied AI paper, verify:

1. The paper states robot task, assumptions, and operating envelope.
2. Method details are enough to reproduce the system loop.
3. Experiments include strong baselines, fair protocols, and ablations tied to claims.
4. Real-world or high-fidelity evidence matches the deployment claims.
5. Runtime, compute, sensors, and platform details are reported.
6. Failure cases and limitations are scoped honestly.
7. Safety-relevant claims are precise and not overstated.
