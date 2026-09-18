# Solver smoke-test results

These results were produced locally with the team's current backend solver, using an 8-second limit per scenario. They are not scores from the organisers' reference validator.

| Dataset | Scenario A | Scenario B | Scenario C |
| --- | --- | --- | --- |
| set_01_timing_collisions | Feasible | Feasible | Feasible |
| set_02_capacity_bottleneck | Feasible | Feasible | Feasible |
| set_03_predecessor_cascade | Infeasible | Infeasible | Optimal |
| set_04_live_mirroring_interchange | Feasible | Optimal | Optimal |
| set_05_co_sharing_workfronts | Feasible | Feasible | Feasible |

The predecessor-cascade pack deliberately has tight, linked deadlines. Its A/B failures are useful for testing infeasibility explanations and failure handling; Scenario C can solve it by using its permitted trade-offs.

Every feasible solution also passed the backend's generated-solution consistency checks for workload completion, planned starts, weekly limits and output-table integrity.
