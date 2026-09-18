# Additional fabricated PS1 solver test datasets

These 10 input packs match the eight-file schema in the official PS1 `main` branch. Each pack is structurally valid and uses the official dual-line network, buffer rules and 30-week horizon. The demand and selected supply values are synthetic.

| Set | Intended stress | Contracts | Activities | Accesses | Live contracts | Predecessor links | Minimum supply |
| --- | --- | ---: | ---: | ---: | ---: | ---: | ---: |
| set_06_priority_competition | Equal-start, equal-deadline work competes at central bottlenecks across contract tiers. Tests whether Priority 1 delay is protected ahead of Priority 2 and 3. | 15 | 30 | 75 | 0 | 0 | 1 |
| set_07_workfront_saturation | A few contracts own many simultaneous activities but only one workfront. Tests per-night concurrent-team limits independently of network capacity. | 6 | 48 | 72 | 0 | 0 | 1 |
| set_08_weekly_access_caps | Location capacity is deliberately generous while each contract has many active jobs. Tests the flat two-night Live and three-night non-Live weekly allocation caps. | 8 | 40 | 160 | 2 | 0 | 4 |
| set_09_buffer_separation | Live, Non-live Consist and buffer-free work starts together on neighbouring sectors. Tests two-sector, one-sector and zero-sector exclusion behaviour. | 12 | 24 | 60 | 4 | 0 | 1 |
| set_10_opposite_bound_independence | Paired EB/WB non-Live jobs should coexist, while late Live jobs must mirror closures. Tests that the solver couples bounds only when required. | 12 | 24 | 60 | 2 | 0 | 1 |
| set_11_interchange_line_independence | Non-Live ALP and BET H01-H02 work should remain independent, while Live work couples both lines. Tests the interchange exception precisely. | 12 | 24 | 60 | 2 | 0 | 1 |
| set_12_eclo_deadline_pressure | High workloads start late against tight planned dates. Tests when B/C use ECLO or extra access and when A accepts schedule slip. | 8 | 24 | 132 | 0 | 0 | 1 |
| set_13_activity_priority_nudges | Each contract contains otherwise similar activities at priorities 1, 2 and 3. Tests the within-contract priority multiplier without crossing contract-tier bands. | 9 | 27 | 81 | 0 | 0 | 1 |
| set_14_horizon_edge | Late starts and predecessor chains approach Week 30. Tests horizon-boundary feasibility, completion accounting and clear no-solution handling. | 8 | 16 | 40 | 0 | 8 | 1 |
| set_15_mixed_portfolio | A larger portfolio mixes all possession types, buffer classes, priorities, routes and selected dependencies. Tests whole-model robustness rather than one isolated rule. | 18 | 54 | 162 | 5 | 6 | 2 |

## How to use

Upload all eight CSV files from one set together. Run Scenarios A, B and C independently and compare feasibility, overrun, excess access nights, ECLO use and hard-rule diagnostics.

These packs are stress tests, not benchmark answers. They intentionally create congestion and competing constraints, so a weak solver may return long delays or no solution within its time limit.

Source schema: official NebulaX Hackathon Problem Statement repository, PS1 `main` branch, commit `966c976`.
