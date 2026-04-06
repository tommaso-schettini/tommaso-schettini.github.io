---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

My research develops **optimization methods for large-scale, structured, and stochastic decision problems**, with a focus on sustainable transportation. The goal is to build algorithms that are innovative, rigorously grounded, and practically useful.

---

## Application Domains

### Public Transit & Metro Systems

<div style="display:flex; gap:2em; align-items:flex-start; flex-wrap:wrap;">
<div style="flex:1; min-width:220px;" markdown="1">

How to schedule trains to match fluctuating passenger demand, when to deploy short-turning strategies to absorb disruptions, how to integrate multiple modes (rail, bus, micromobility) into a coherent network. My work addresses these problems through demand-driven optimization frameworks that adapt schedules dynamically rather than relying on fixed timetables.
Currently I am expanding on this area to focus on **Network Design** and multimodal transportation.

Key themes:
- Demand-driven timetabling and frequency setting
- Short-turning and adaptive metro operations
- Multimodal and express transit planning

</div>
<figure style="flex:1; min-width:200px; margin:0;">
  <img src="/images/research-transit-short-turning.png" alt="Short-turning timetable patterns: regular, periodic, and non-periodic strategies with their efficiency-complexity tradeoffs" style="width:60%;">
</figure>
</div>

### Electric Vehicle Infrastructure

The transition to electric mobility requires coordinated decisions about where to locate charging stations, how to size them, and how to plan their deployment over multi-year horizons.
A related challenge is integrating EV fleets into ride-hailing and shared mobility systems. My research addresses these problems as structured stochastic optimization models with realistic operational constraints.

Key themes:
- Location and capacity planning for charging infrastructure
- Multi-period investment under demand uncertainty
- EV integration in ride-hailing and shared fleets

These two domains serve as primary case studies. The methods are designed to generalize: the underlying algorithms apply to logistics, energy systems, and infrastructure planning more broadly.

<figure style="flex:1; min-width:220px; margin:0;">
  <center>
  <img src="/images/chargers.png" alt="EV charger location pipeline: from demographic data to candidate locations to planned infrastructure" style="width:60%;">
  </center>
</figure>

---

## Methodological Approaches

### Decomposition Algorithms

Many large-scale optimization problems in transportation and infrastructure have a **block-angular** or **stochastic** structure that can be exploited algorithmically. I specialize in **Benders decomposition** and related exact-hybrid methods that break a hard problem into a master problem and subproblems, enabling solutions at scales that monolithic solvers cannot reach. A significant part of my work focuses on strengthening these methods to make them practical on real instances.

### Discrete Simulation-Based Optimization (DSO)

<div style="display:flex; gap:2em; align-items:flex-start; flex-wrap:wrap;">
<div style="flex:2; min-width:220px;" markdown="1">

Some problems are too complex for closed-form models: stochastic dynamics, heterogeneous agents, non-linear interactions. **Discrete simulation-based optimization** couples a high-fidelity discrete-event simulation with an optimization layer that iteratively searches for better decisions based on simulated outcomes. My postdoctoral work at HEC Montréal / GERAD developed DSO frameworks for stochastic combinatorial problems, with applications in ride-hailing fleet management and EV charging operations.

A central challenge in DSO is computational cost: high-fidelity simulations are expensive, and naively running thousands of them to explore the solution space is impractical. My work addresses this by **integrating machine learning directly into the search process**. Learned surrogate models approximate the simulation objective from past evaluations, guiding the optimizer toward promising regions of the solution space without requiring a full simulation at every step.

</div>
<figure style="flex:1; min-width:180px; margin:0;">
  <img src="/images/simulation-2.gif" alt="Animated simulation of an electric ride-hailing fleet operating across a city network" style="width:100%;">
  <figcaption>Discrete-event simulation of an electric ride-hailing fleet.</figcaption>
</figure>
</div>


### Heuristics and Metaheuristics

Exact methods are not always tractable. I have extensive experience designing **problem-specific heuristics and metaheuristics** that find high-quality solutions efficiently on hard combinatorial problems.

---

## Collaboration & Funding

This research program is supported by an **NSERC Discovery Grant** (2025–2030). I am open to collaboration with industry partners in transit agencies, EV operators, and logistics.

