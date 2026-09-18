# Solver smoke-test results for sets 06-15

These results were produced locally with the team's current backend solver. They are not scores from the organisers' reference validator. Most trials used an 8-second limit per scenario; the two larger search cases used 20 seconds.

| Dataset | Scenario A | Scenario B | Scenario C |
| --- | --- | --- | --- |
| set_06_priority_competition | Feasible | Feasible | Feasible |
| set_07_workfront_saturation | Optimal | Infeasible | Optimal |
| set_08_weekly_access_caps | Optimal | Optimal | Optimal |
| set_09_buffer_separation | Feasible | Optimal | Feasible |
| set_10_opposite_bound_independence | Optimal | Feasible | Feasible |
| set_11_interchange_line_independence | Feasible | Feasible | Feasible |
| set_12_eclo_deadline_pressure | Optimal | Optimal | Optimal |
| set_13_activity_priority_nudges | Feasible | Feasible | Feasible |
| set_14_horizon_edge | Optimal | Infeasible | Optimal |
| set_15_mixed_portfolio | Feasible | Feasible | Feasible |

The intentional Scenario B failures test two different hard limits:

- `set_07_workfront_saturation`: the planned deadline cannot be met without breaching the one-workfront concurrency rule.
- `set_14_horizon_edge`: late predecessor chains cannot satisfy the rigid planned date before the horizon ends.

Every feasible result passed the backend's generated-solution consistency checks for workload completion, planned starts, weekly limits and output-table integrity.
