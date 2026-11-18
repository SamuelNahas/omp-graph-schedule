# omp-graph-schedule

Scheduling and load-balancing study of OpenMP triangle counting on SNAP graphs.

> **Status:** work in progress. `v0.1` ("Mini-A") is the first milestone: triangle counting on one graph,
> comparing OpenMP `static`, `dynamic` and `guided` schedules.

## Goal

Real-world graphs have heavy-tailed degree distributions, so the cost per loop iteration varies a lot.
This project measures how OpenMP loop scheduling and vertex ordering affect speedup, efficiency and
load imbalance in triangle counting.

## Method (planned)

- Graphs: [SNAP](http://snap.stanford.edu/data) `com-Youtube` first; larger graphs later.
- Algorithm: ordered adjacency-list intersection with vertices ranked by degree.
- Factors: `schedule` (static/dynamic/guided), chunk size, number of threads.
- Metrics: wall time, speedup, efficiency, per-thread time (imbalance = max/mean).
- Hypotheses are written in [`PLAN.md`](PLAN.md) *before* running experiments.

## How to reproduce

_To be filled in as the issues for v0.1 are completed._

## Limits

_To be filled in._

## References

- Leskovec, Krevl. *SNAP Datasets: Stanford Large Network Dataset Collection*. http://snap.stanford.edu/data
- Shun, Tangwongsan. *Multicore triangle computations without tuning*. ICDE 2015. doi:10.1109/ICDE.2015.7113280
