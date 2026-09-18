# Solver smoke-test results for sets 16-45

These results were produced locally with the team's current backend solver. They are not organiser reference scores.

Scenario A was tested across all 30 packs with a 3-second limit per pack. Selected high-stress packs also received 8-second Scenario B/C trials. `Time limit` means the solver returned `UNKNOWN`; it does not prove infeasibility.

| Dataset | Scenario A | Focused B/C result |
| --- | --- | --- |
| set_16_ultra_congestion | Infeasible | B: time limit; C: feasible |
| set_17_live_interchange_surge | Time limit | B/C: time limit |
| set_18_deep_dependency_chains | Optimal | Not separately tested |
| set_19_cross_contract_dependency_web | Optimal | Not separately tested |
| set_20_deadline_priority_crunch | Feasible | Not separately tested |
| set_21_minimum_supply_network | Feasible | Not separately tested |
| set_22_alpha_line_supply_failure | Feasible | Not separately tested |
| set_23_eastbound_supply_failure | Time limit | Not separately tested |
| set_24_hub_platform_bottleneck | Feasible | Not separately tested |
| set_25_hub_tunnel_bottleneck | Feasible | Not separately tested |
| set_26_maximum_co_share_packing | Feasible | Not separately tested |
| set_27_pc_host_shortage | Feasible | Not separately tested |
| set_28_pm_monopoly_conflict | Feasible | Not separately tested |
| set_29_multi_workfront_burst | Optimal | Not separately tested |
| set_30_single_contract_megaprogram | Feasible | Not separately tested |
| set_31_many_tiny_contracts | Optimal | Not separately tested |
| set_32_long_route_occupancy | Time limit | Not separately tested |
| set_33_point_job_swarm | Optimal | Not separately tested |
| set_34_staggered_demand_waves | Optimal | Not separately tested |
| set_35_simultaneous_start_burst | Feasible | Not separately tested |
| set_36_deadline_ladder | Feasible | Not separately tested |
| set_37_mixed_buffer_adjacency | Time limit | Not separately tested |
| set_38_eclo_continuity_window | Time limit | B/C: time limit |
| set_39_cross_line_live_lock | Time limit | B/C: time limit |
| set_40_rigid_deadline_failure | Infeasible | B: optimal; C: time limit |
| set_41_priority_inversion_trap | Infeasible | Not separately tested |
| set_42_co_share_mix_limit | Optimal | Not separately tested |
| set_43_four_c_packing_limit | Optimal | Not separately tested |
| set_44_alternating_bound_corridors | Time limit | Not separately tested |
| set_45_deterministic_mega_case | Time limit | B/C: time limit |

Every feasible result passed the backend's generated-solution consistency checks. The time-limit and infeasible outcomes are retained deliberately because these packs are intended to expose search-performance, fallback and explanation behaviour as well as ordinary feasibility.
