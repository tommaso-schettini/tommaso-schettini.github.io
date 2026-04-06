---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

My research develops **optimization methods for large-scale, structured, and stochastic decision problems**, with a focus on sustainable transportation. The goal is to build algorithms that are both rigorously grounded and practically useful — methods that can handle the complexity of real transit and energy systems, and that transfer to other infrastructure domains.

---

## Application Domains

### Public Transit & Metro Systems

Urban transit networks face operational decisions of significant scale and complexity: how to schedule trains to match fluctuating passenger demand, when to deploy short-turning strategies to absorb disruptions, how to integrate multiple modes (rail, bus, micromobility) into a coherent network. My work addresses these problems through demand-driven optimization frameworks that adapt schedules dynamically rather than relying on fixed timetables.

Key themes:
- Demand-driven timetabling and frequency setting
- Short-turning and adaptive metro operations
- Multimodal and express transit planning

<figure>
  <img src="/images/research-transit-short-turning.png" alt="Short-turning timetable patterns: regular, periodic, and non-periodic strategies with their efficiency-complexity tradeoffs" style="max-width:620px; width:100%;">
  <figcaption>Three short-turning strategies and their tradeoffs — from simpler regular timetables to non-periodic schedules that minimize waiting times at the cost of greater operational complexity.</figcaption>
</figure>

### Electric Vehicle Infrastructure

The transition to electric mobility requires coordinated decisions about where to locate charging stations, how to size them, and how to plan their deployment over multi-year horizons — all under significant uncertainty in travel patterns and technology costs. A related challenge is integrating EV fleets into ride-hailing and shared mobility systems. My research addresses these problems as structured stochastic optimization models with realistic operational constraints.

Key themes:
- Location and capacity planning for charging infrastructure
- Multi-period investment under demand uncertainty
- EV integration in ride-hailing and shared fleets

These two domains serve as primary case studies. The methods are designed to generalize: the underlying algorithms apply to logistics, energy systems, and infrastructure planning more broadly.

---

## Methodological Approaches

### Decomposition Algorithms

Many large-scale optimization problems in transportation and infrastructure have a **block-angular** or **stochastic** structure that can be exploited algorithmically. I specialize in **Benders decomposition** and related exact-hybrid methods that break a hard problem into a master problem and subproblems, enabling solutions at scales that monolithic solvers cannot reach. A significant part of my work focuses on strengthening these methods — better cuts, tighter bounds, effective warm-starting — to make them practical on real instances.

### Discrete Simulation-Based Optimization (DSO)

Some problems are too complex for closed-form models: stochastic dynamics, heterogeneous agents, non-linear interactions. **Discrete simulation-based optimization** couples a high-fidelity discrete-event simulation with an optimization layer that iteratively searches for better decisions based on simulated outcomes. My postdoctoral work at HEC Montréal / GERAD developed DSO frameworks for stochastic combinatorial problems, with applications in ride-hailing fleet management and EV charging operations.

A central challenge in DSO is computational cost: high-fidelity simulations are expensive, and naively running thousands of them to explore the solution space is impractical. My work addresses this by **integrating machine learning — in particular Bayesian optimization and surrogate modelling — directly into the search process**. Learned surrogate models approximate the simulation objective from past evaluations, guiding the optimizer toward promising regions of the solution space without requiring a full simulation at every step. This hybrid approach — AI-informed search over a combinatorial decision space — substantially reduces the number of simulator calls needed to reach high-quality solutions, making DSO tractable for real-world problem sizes.

<figure>
  <img src="/images/research-dso-flowchart.png" alt="DSO loop: sample feasible space, generate features, cluster points, evaluate, select most promising cluster, repeat" style="max-width:340px; width:100%;">
  <figcaption>The DSO loop: candidate solutions are sampled, clustered, and selectively evaluated by simulation. Machine learning guides which regions to explore, reducing expensive simulator calls.</figcaption>
</figure>

### Heuristics and Metaheuristics

Exact methods are not always tractable. I have extensive experience designing **problem-specific heuristics and metaheuristics** — including large neighborhood search, adaptive procedures, and hybrid exact-heuristic schemes — that find high-quality solutions efficiently on hard combinatorial problems.

---

## Collaboration & Funding

This research program is supported by an **NSERC Discovery Grant** (2025–2030). I am open to collaboration with industry partners in transit agencies, EV operators, and logistics — particularly where real operational data can ground methodological development.

Prospective students and collaborators are welcome to [get in touch](/hiring/).
