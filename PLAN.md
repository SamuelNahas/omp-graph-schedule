# Plan (draft, to be finalised BEFORE the first benchmark run)

## Questions
1. Which `schedule` (static/dynamic/guided, chunk size) is fastest on heavy-tailed graphs?
2. Does ordering vertices by degree change load imbalance?
3. Where does parallel efficiency drop (threads, graph size)?

## Hypotheses (to review)
- H1: `static` has the worst imbalance (max/mean thread time) on `com-Youtube`.
- H2: `dynamic` with a small chunk balances best but pays scheduling overhead at chunk size 1.
- H3: efficiency drops once threads exceed the number of performance cores.

## Protocol
- 5 repetitions per configuration; report median and spread.
- Threads: 1, 2, 4, 8. Chunk: 1, 16, 256. Schedules: static, dynamic, guided.
- Triangle count must match the sequential baseline and the dataset's published value.
- Record machine, compiler, flags and commit in every result file.
