# Additional fabricated PS1 solver test datasets

These 30 input packs match the eight-file schema in the official PS1 `main` branch. Each pack is structurally valid and uses the official dual-line network, buffer rules and 30-week horizon. The demand and selected supply values are synthetic.

| Set | Intended stress | Contracts | Activities | Accesses | Live contracts | Predecessor links | Minimum supply |
| --- | --- | ---: | ---: | ---: | ---: | ---: | ---: |
| set_16_ultra_congestion | PM possessions with identical starts and central routes saturate one-slot locations. Tests heavy schedule slip, excess supply and search performance. | 18 | 54 | 189 | 0 | 0 | 1 |
| set_17_live_interchange_surge | A surge of Live work repeatedly touches H01-H02. Tests opposite-bound mirroring, cross-line closures, two-sector buffers and Live weekly caps. | 10 | 30 | 75 | 10 | 0 | 1 |
| set_18_deep_dependency_chains | Five-step chains within each contract create long finish-to-start critical paths across varied routes. | 8 | 40 | 96 | 0 | 32 | 1 |
| set_19_cross_contract_dependency_web | Three-contract dependency groups link one programme's finish to the next programme's start. Tests cross-contract predecessor handling without cycles. | 12 | 36 | 72 | 0 | 32 | 1 |
| set_20_deadline_priority_crunch | All priority tiers compete for PM slots before the same early deadline. Tests tier-weighted sacrifice decisions under unavoidable delay. | 18 | 36 | 108 | 0 | 0 | 1 |
| set_21_minimum_supply_network | Every location is reduced to one slot while demand remains network-wide. Tests global packing and propagation of widespread capacity scarcity. | 12 | 36 | 108 | 0 | 0 | 1 |
| set_22_alpha_line_supply_failure | Alpha capacity drops to one while Beta remains generous and most work sits on Alpha. Tests asymmetric line pressure and route-specific delay. | 14 | 42 | 105 | 0 | 0 | 1 |
| set_23_eastbound_supply_failure | Eastbound capacity collapses while westbound remains high. Tests bound independence and asymmetric congestion. | 14 | 42 | 105 | 3 | 0 | 1 |
| set_24_hub_platform_bottleneck | H01/H02 platform capacity is one while tunnel capacity is increased. Tests whether platform occupancy, not only tunnel occupancy, constrains routes. | 12 | 36 | 90 | 0 | 0 | 1 |
| set_25_hub_tunnel_bottleneck | The H01-H02 tunnel is one slot while hub platforms are widened. Tests tunnel-sector capacity independently of platform availability. | 12 | 36 | 90 | 0 | 0 | 1 |
| set_26_maximum_co_share_packing | PC and C jobs crowd one-slot locations. Tests efficient PC plus three-C and four-C possession packing. | 20 | 40 | 100 | 0 | 0 | 1 |
| set_27_pc_host_shortage | Many PC possessions compete with only a few C workers, preventing efficient sharing. Tests that PC cannot illegally share with another PC. | 16 | 32 | 80 | 0 | 0 | 1 |
| set_28_pm_monopoly_conflict | PM work monopolises each possession and cannot co-share. Tests sole-possession enforcement under dense central demand. | 14 | 28 | 84 | 0 | 0 | 2 |
| set_29_multi_workfront_burst | Six contracts each launch ten activities with three workfronts. Tests correct use of parallel teams without exceeding access-night budgets. | 6 | 60 | 90 | 0 | 0 | 4 |
| set_30_single_contract_megaprogram | One contract owns thirty activities across both lines but has only two workfronts and three weekly nights. Tests contract-level scaling and allocation accounting. | 1 | 30 | 60 | 0 | 0 | 4 |
| set_31_many_tiny_contracts | Forty one-activity contracts stress model size, contract indexing and priority ordering with little intra-contract complexity. | 40 | 40 | 100 | 4 | 0 | 1 |
| set_32_long_route_occupancy | Activities span nearly entire lines, generating large platform and tunnel footprints. Tests occupancy expansion and widespread closure conflicts. | 10 | 30 | 75 | 0 | 0 | 1 |
| set_33_point_job_swarm | Sixty short jobs occupy single tunnel sectors. Tests high activity count, co-sharing and slot grouping without long-route expansion. | 30 | 60 | 120 | 0 | 0 | 1 |
| set_34_staggered_demand_waves | Programmes arrive in five start-date waves. Tests rolling admission, capacity reuse and avoidance of premature scheduling. | 15 | 45 | 112 | 0 | 0 | 1 |
| set_35_simultaneous_start_burst | Forty activities all become eligible in Week 10 on central corridors. Tests burst handling and prioritised displacement. | 20 | 40 | 100 | 0 | 0 | 1 |
| set_36_deadline_ladder | Contracts share the same start but have weekly-stepped deadlines. Tests deadline ordering and whether later work yields to earlier milestones. | 15 | 30 | 75 | 0 | 0 | 1 |
| set_37_mixed_buffer_adjacency | Alternating Live, Consist and buffer-free work occupies neighbouring sectors on the same bounds. Tests pairwise closure spacing. | 15 | 30 | 75 | 5 | 0 | 1 |
| set_38_eclo_continuity_window | Live workloads pressure both line-specific two-week ECLO windows in Scenario C. Tests continuity-window selection and cross-line overlap. | 8 | 32 | 144 | 8 | 0 | 1 |
| set_39_cross_line_live_lock | Live H01-H02 work on both lines competes for the same traction-power closure periods. Tests that cross-line conflicts cannot be scheduled concurrently. | 12 | 24 | 60 | 12 | 0 | 2 |
| set_40_rigid_deadline_failure | High workloads begin only two weeks before planned completion. Tests whether Scenario B can rescue the deadline with ECLO and extra supply while strict-supply Scenario A fails. | 10 | 30 | 120 | 0 | 0 | 1 |
| set_41_priority_inversion_trap | Small Priority-1 contracts compete against large Priority-3 contracts. Tests that workload size does not wrongly outweigh the contract-priority band. | 14 | 28 | 116 | 0 | 0 | 1 |
| set_42_co_share_mix_limit | PC and C programmes deliberately exceed one-PC-plus-three-C demand at the same locations. Tests legal mix limits and spillover possessions. | 24 | 24 | 72 | 0 | 0 | 1 |
| set_43_four_c_packing_limit | C-only workloads require exact groups of at most four per possession. Tests that five or more C jobs never occupy one slot. | 24 | 24 | 72 | 0 | 0 | 1 |
| set_44_alternating_bound_corridors | Mirrored EB/WB corridors carry alternating Live and non-Live programmes. Tests selective opposite-bound coupling across several route lengths. | 16 | 48 | 120 | 4 | 0 | 1 |
| set_45_deterministic_mega_case | Thirty contracts and 120 activities mix every rule at scale. This is the largest search and timeout stress test in the collection. | 30 | 120 | 420 | 6 | 15 | 2 |

## How to use

Upload all eight CSV files from one set together. Run Scenarios A, B and C independently and compare feasibility, overrun, excess access nights, ECLO use and hard-rule diagnostics.

These packs are stress tests, not benchmark answers. They intentionally create congestion and competing constraints, so a weak solver may return long delays or no solution within its time limit.

Source schema: official NebulaX Hackathon Problem Statement repository, PS1 `main` branch, commit `966c976`.
