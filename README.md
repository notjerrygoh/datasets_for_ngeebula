# Fabricated PS1 solver test datasets

These five input packs match the eight-file schema in the official PS1 `main` branch. Each pack is structurally valid and uses the official dual-line network, buffer rules and 30-week horizon. The demand and selected supply values are synthetic.

| Set | Intended stress | Contracts | Activities | Accesses | Live contracts | Predecessor links | Minimum supply |
| --- | --- | ---: | ---: | ---: | ---: | ---: | ---: |
| set_01_timing_collisions | Many projects become eligible in Weeks 2-3 on overlapping central corridors. Tests conflict resolution, priority ordering, buffers and schedule slip. | 12 | 36 | 108 | 0 | 0 | 1 |
| set_02_capacity_bottleneck | Central interchange and adjacent locations are reduced to one slot while demand concentrates there. Tests Scenario A delay, Scenario B excess supply and Scenario C trade-offs. | 10 | 30 | 120 | 0 | 0 | 1 |
| set_03_predecessor_cascade | Long within-contract and cross-contract finish-to-start chains create knock-on delay. Tests precedence, priority nudges and deadline propagation. | 10 | 40 | 100 | 0 | 35 | 1 |
| set_04_live_mirroring_interchange | Live possessions overlap the shared H01-H02 corridor and flank sectors. Tests opposite-bound mirroring, cross-line Live closures, buffers and weekly caps. | 10 | 30 | 75 | 6 | 0 | 1 |
| set_05_co_sharing_workfronts | PC and C work competes for one-slot central locations while PM work blocks sharing. Tests legal mixes, co-share packing, workfront caps and access-night allocation. | 14 | 42 | 105 | 1 | 0 | 1 |

## How to use

Upload all eight CSV files from one set together. Run Scenarios A, B and C independently and compare feasibility, overrun, excess access nights, ECLO use and hard-rule diagnostics.

These packs are stress tests, not benchmark answers. They intentionally create congestion and competing constraints, so a weak solver may return long delays or no solution within its time limit.

Source schema: official NebulaX Hackathon Problem Statement repository, PS1 `main` branch, commit `966c976`.
