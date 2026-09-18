# PS1 fabricated solver test datasets

This collection contains 45 complete PS1 input packs. Every set has the same eight canonical CSV files and follows the official PS1 schema, dual-line topology, buffer definitions and 30-week horizon. Demand, dates and selected supply values are synthetic.

## How to use the collection

- Upload all eight CSV files from one set together.
- Run Scenarios A, B and C independently against the same input set.
- Compare feasibility, planned-date overrun, excess access nights, ECLO use and hard-rule diagnostics.
- Treat `UNKNOWN` from a time-bounded trial as a search timeout, not proof of infeasibility.
- Use sets 01-05 for core behaviour, 06-15 for focused rule tests, and 16-45 for heavier stress and scaling tests.

## Official public-data baseline

The official public PS1 instance has 14 contracts, 54 activities, 192 required access-nights, 2 Live contracts and 6 predecessor links. Location supply ranges from 1 to 4. Differences below are measured against that instance.

## Comparison index

| Set | Profile | Contracts | Activities | Accesses | Live | Predecessors | Supply changes |
| --- | --- | ---: | ---: | ---: | ---: | ---: | ---: |
| set_01_timing_collisions | Timing collisions | 12 | 36 | 108 | 0 | 0 | 0 |
| set_02_capacity_bottleneck | Capacity bottleneck | 10 | 30 | 120 | 0 | 0 | 8 |
| set_03_predecessor_cascade | Predecessor cascade | 10 | 40 | 100 | 0 | 35 | 0 |
| set_04_live_mirroring_interchange | Live mirroring and interchange | 10 | 30 | 75 | 6 | 0 | 0 |
| set_05_co_sharing_workfronts | Co-sharing and workfront limits | 14 | 42 | 105 | 1 | 0 | 8 |
| set_06_priority_competition | Priority competition | 15 | 30 | 75 | 0 | 0 | 8 |
| set_07_workfront_saturation | Workfront saturation | 6 | 48 | 72 | 0 | 0 | 0 |
| set_08_weekly_access_caps | Weekly access caps | 8 | 40 | 160 | 2 | 0 | 52 |
| set_09_buffer_separation | Buffer separation | 12 | 24 | 60 | 4 | 0 | 0 |
| set_10_opposite_bound_independence | Opposite-bound independence | 12 | 24 | 60 | 2 | 0 | 0 |
| set_11_interchange_line_independence | Interchange line independence | 12 | 24 | 60 | 2 | 0 | 8 |
| set_12_eclo_deadline_pressure | ECLO deadline pressure | 8 | 24 | 132 | 0 | 0 | 0 |
| set_13_activity_priority_nudges | Activity-priority nudges | 9 | 27 | 81 | 0 | 0 | 8 |
| set_14_horizon_edge | Horizon edge | 8 | 16 | 40 | 0 | 8 | 0 |
| set_15_mixed_portfolio | Mixed portfolio | 18 | 54 | 162 | 5 | 6 | 12 |
| set_16_ultra_congestion | Ultra congestion | 18 | 54 | 189 | 0 | 0 | 8 |
| set_17_live_interchange_surge | Live interchange surge | 10 | 30 | 75 | 10 | 0 | 0 |
| set_18_deep_dependency_chains | Deep dependency chains | 8 | 40 | 96 | 0 | 32 | 0 |
| set_19_cross_contract_dependency_web | Cross-contract dependency web | 12 | 36 | 72 | 0 | 32 | 0 |
| set_20_deadline_priority_crunch | Deadline and priority crunch | 18 | 36 | 108 | 0 | 0 | 8 |
| set_21_minimum_supply_network | Minimum-supply network | 12 | 36 | 108 | 0 | 0 | 64 |
| set_22_alpha_line_supply_failure | Alpha line supply failure | 14 | 42 | 105 | 0 | 0 | 58 |
| set_23_eastbound_supply_failure | Eastbound supply failure | 14 | 42 | 105 | 3 | 0 | 58 |
| set_24_hub_platform_bottleneck | Hub platform bottleneck | 12 | 36 | 90 | 0 | 0 | 12 |
| set_25_hub_tunnel_bottleneck | Hub tunnel bottleneck | 12 | 36 | 90 | 0 | 0 | 40 |
| set_26_maximum_co_share_packing | Maximum co-share packing | 20 | 40 | 100 | 0 | 0 | 8 |
| set_27_pc_host_shortage | PC host shortage | 16 | 32 | 80 | 0 | 0 | 8 |
| set_28_pm_monopoly_conflict | PM monopoly conflict | 14 | 28 | 84 | 0 | 0 | 12 |
| set_29_multi_workfront_burst | Multi-workfront burst | 6 | 60 | 90 | 0 | 0 | 52 |
| set_30_single_contract_megaprogram | Single-contract megaprogram | 1 | 30 | 60 | 0 | 0 | 52 |
| set_31_many_tiny_contracts | Many tiny contracts | 40 | 40 | 100 | 4 | 0 | 0 |
| set_32_long_route_occupancy | Long-route occupancy | 10 | 30 | 75 | 0 | 0 | 0 |
| set_33_point_job_swarm | Point-job swarm | 30 | 60 | 120 | 0 | 0 | 0 |
| set_34_staggered_demand_waves | Staggered demand waves | 15 | 45 | 112 | 0 | 0 | 0 |
| set_35_simultaneous_start_burst | Simultaneous-start burst | 20 | 40 | 100 | 0 | 0 | 8 |
| set_36_deadline_ladder | Deadline ladder | 15 | 30 | 75 | 0 | 0 | 8 |
| set_37_mixed_buffer_adjacency | Mixed-buffer adjacency | 15 | 30 | 75 | 5 | 0 | 0 |
| set_38_eclo_continuity_window | ECLO continuity window | 8 | 32 | 144 | 8 | 0 | 0 |
| set_39_cross_line_live_lock | Cross-line Live lock | 12 | 24 | 60 | 12 | 0 | 12 |
| set_40_rigid_deadline_failure | Rigid-deadline rescue | 10 | 30 | 120 | 0 | 0 | 8 |
| set_41_priority_inversion_trap | Priority inversion trap | 14 | 28 | 116 | 0 | 0 | 8 |
| set_42_co_share_mix_limit | Co-share mix limit | 24 | 24 | 72 | 0 | 0 | 8 |
| set_43_four_c_packing_limit | Four-C packing limit | 24 | 24 | 72 | 0 | 0 | 8 |
| set_44_alternating_bound_corridors | Alternating-bound corridors | 16 | 48 | 120 | 4 | 0 | 0 |
| set_45_deterministic_mega_case | Deterministic mega case | 30 | 120 | 420 | 6 | 15 | 12 |

## Detailed set descriptions

### set_01_timing_collisions — Timing collisions

Many projects become eligible in Weeks 2-3 on overlapping central corridors. Tests conflict resolution, priority ordering, buffers and schedule slip.

- **Scale:** 12 contracts, 36 activities and 108 required access-nights.
- **Possession mix:** C: 6, PC: 3, PM: 3.
- **Work type and buffers:** Non-live (Consist): 3, Non-live (Others): 9.
- **Contract priorities:** 1: 4, 2: 4, 3: 4.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 2-3; planned completion targets span Weeks 13-16.
- **Supply:** Uses the public location-supply table unchanged; range 1-4.
- **Difference from public baseline:** contracts -2, activities -18, access-nights -84, Live contracts -2, predecessor links -6.

### set_02_capacity_bottleneck — Capacity bottleneck

Central interchange and adjacent locations are reduced to one slot while demand concentrates there. Tests Scenario A delay, Scenario B excess supply and Scenario C trade-offs.

- **Scale:** 10 contracts, 30 activities and 120 required access-nights.
- **Possession mix:** C: 6, PC: 2, PM: 2.
- **Work type and buffers:** Non-live (Consist): 2, Non-live (Others): 8.
- **Contract priorities:** 1: 4, 2: 4, 3: 2.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 1-3; planned completion targets span Weeks 11-14.
- **Supply:** 8 of 76 location capacities differ from the public instance; range 1-4.
- **Difference from public baseline:** contracts -4, activities -24, access-nights -72, Live contracts -2, predecessor links -6.

### set_03_predecessor_cascade — Predecessor cascade

Long within-contract and cross-contract finish-to-start chains create knock-on delay. Tests precedence, priority nudges and deadline propagation.

- **Scale:** 10 contracts, 40 activities and 100 required access-nights.
- **Possession mix:** C: 5, PC: 3, PM: 2.
- **Work type and buffers:** Non-live (Consist): 4, Non-live (Others): 6.
- **Contract priorities:** 1: 4, 2: 3, 3: 3.
- **Dependencies:** 35 predecessor links.
- **Timing:** planned starts span Weeks 1-3; planned completion targets span Weeks 14-18.
- **Supply:** Uses the public location-supply table unchanged; range 1-4.
- **Difference from public baseline:** contracts -4, activities -14, access-nights -92, Live contracts -2, predecessor links +29.

### set_04_live_mirroring_interchange — Live mirroring and interchange

Live possessions overlap the shared H01-H02 corridor and flank sectors. Tests opposite-bound mirroring, cross-line Live closures, buffers and weekly caps.

- **Scale:** 10 contracts, 30 activities and 75 required access-nights.
- **Possession mix:** C: 2, PC: 5, PM: 3.
- **Work type and buffers:** Live: 6, Non-live (Consist): 2, Non-live (Others): 2.
- **Contract priorities:** 1: 4, 2: 3, 3: 3.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 3-6; planned completion targets span Weeks 14-18.
- **Supply:** Uses the public location-supply table unchanged; range 1-4.
- **Difference from public baseline:** contracts -4, activities -24, access-nights -117, Live contracts +4, predecessor links -6.

### set_05_co_sharing_workfronts — Co-sharing and workfront limits

PC and C work competes for one-slot central locations while PM work blocks sharing. Tests legal mixes, co-share packing, workfront caps and access-night allocation.

- **Scale:** 14 contracts, 42 activities and 105 required access-nights.
- **Possession mix:** C: 8, PC: 4, PM: 2.
- **Work type and buffers:** Live: 1, Non-live (Consist): 1, Non-live (Others): 12.
- **Contract priorities:** 1: 5, 2: 5, 3: 4.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 2-2; planned completion targets span Weeks 12-16.
- **Supply:** 8 of 76 location capacities differ from the public instance; range 1-4.
- **Difference from public baseline:** contracts 0, activities -12, access-nights -87, Live contracts -1, predecessor links -6.

### set_06_priority_competition — Priority competition

Equal-start, equal-deadline work competes at central bottlenecks across contract tiers. Tests whether Priority 1 delay is protected ahead of Priority 2 and 3.

- **Scale:** 15 contracts, 30 activities and 75 required access-nights.
- **Possession mix:** PM: 15.
- **Work type and buffers:** Non-live (Others): 15.
- **Contract priorities:** 1: 5, 2: 5, 3: 5.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 2-2; planned completion targets span Weeks 12-12.
- **Supply:** 8 of 76 location capacities differ from the public instance; range 1-4.
- **Difference from public baseline:** contracts +1, activities -24, access-nights -117, Live contracts -2, predecessor links -6.

### set_07_workfront_saturation — Workfront saturation

A few contracts own many simultaneous activities but only one workfront. Tests per-night concurrent-team limits independently of network capacity.

- **Scale:** 6 contracts, 48 activities and 72 required access-nights.
- **Possession mix:** C: 6.
- **Work type and buffers:** Non-live (Others): 6.
- **Contract priorities:** 1: 2, 2: 2, 3: 2.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 1-1; planned completion targets span Weeks 3-3.
- **Supply:** Uses the public location-supply table unchanged; range 1-4.
- **Difference from public baseline:** contracts -8, activities -6, access-nights -120, Live contracts -2, predecessor links -6.

### set_08_weekly_access_caps — Weekly access caps

Location capacity is deliberately generous while each contract has many active jobs. Tests the flat two-night Live and three-night non-Live weekly allocation caps.

- **Scale:** 8 contracts, 40 activities and 160 required access-nights.
- **Possession mix:** C: 4, PC: 4.
- **Work type and buffers:** Live: 2, Non-live (Others): 6.
- **Contract priorities:** 1: 3, 2: 3, 3: 2.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 1-1; planned completion targets span Weeks 9-10.
- **Supply:** 52 of 76 location capacities differ from the public instance; range 4-4.
- **Difference from public baseline:** contracts -6, activities -14, access-nights -32, Live contracts 0, predecessor links -6.

### set_09_buffer_separation — Buffer separation

Live, Non-live Consist and buffer-free work starts together on neighbouring sectors. Tests two-sector, one-sector and zero-sector exclusion behaviour.

- **Scale:** 12 contracts, 24 activities and 60 required access-nights.
- **Possession mix:** C: 4, PC: 4, PM: 4.
- **Work type and buffers:** Live: 4, Non-live (Consist): 4, Non-live (Others): 4.
- **Contract priorities:** 1: 4, 2: 4, 3: 4.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 3-3; planned completion targets span Weeks 14-16.
- **Supply:** Uses the public location-supply table unchanged; range 1-4.
- **Difference from public baseline:** contracts -2, activities -30, access-nights -132, Live contracts +2, predecessor links -6.

### set_10_opposite_bound_independence — Opposite-bound independence

Paired EB/WB non-Live jobs should coexist, while late Live jobs must mirror closures. Tests that the solver couples bounds only when required.

- **Scale:** 12 contracts, 24 activities and 60 required access-nights.
- **Possession mix:** C: 6, PC: 4, PM: 2.
- **Work type and buffers:** Live: 2, Non-live (Others): 10.
- **Contract priorities:** 1: 4, 2: 4, 3: 4.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 2-2; planned completion targets span Weeks 13-15.
- **Supply:** Uses the public location-supply table unchanged; range 1-4.
- **Difference from public baseline:** contracts -2, activities -30, access-nights -132, Live contracts 0, predecessor links -6.

### set_11_interchange_line_independence — Interchange line independence

Non-Live ALP and BET H01-H02 work should remain independent, while Live work couples both lines. Tests the interchange exception precisely.

- **Scale:** 12 contracts, 24 activities and 60 required access-nights.
- **Possession mix:** C: 7, PC: 3, PM: 2.
- **Work type and buffers:** Live: 2, Non-live (Consist): 4, Non-live (Others): 6.
- **Contract priorities:** 1: 4, 2: 4, 3: 4.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 2-2; planned completion targets span Weeks 13-16.
- **Supply:** 8 of 76 location capacities differ from the public instance; range 1-4.
- **Difference from public baseline:** contracts -2, activities -30, access-nights -132, Live contracts 0, predecessor links -6.

### set_12_eclo_deadline_pressure — ECLO deadline pressure

High workloads start late against tight planned dates. Tests when B/C use ECLO or extra access and when A accepts schedule slip.

- **Scale:** 8 contracts, 24 activities and 132 required access-nights.
- **Possession mix:** C: 5, PC: 3.
- **Work type and buffers:** Non-live (Consist): 2, Non-live (Others): 6.
- **Contract priorities:** 1: 3, 2: 3, 3: 2.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 6-8; planned completion targets span Weeks 11-12.
- **Supply:** Uses the public location-supply table unchanged; range 1-4.
- **Difference from public baseline:** contracts -6, activities -30, access-nights -60, Live contracts -2, predecessor links -6.

### set_13_activity_priority_nudges — Activity-priority nudges

Each contract contains otherwise similar activities at priorities 1, 2 and 3. Tests the within-contract priority multiplier without crossing contract-tier bands.

- **Scale:** 9 contracts, 27 activities and 81 required access-nights.
- **Possession mix:** PM: 9.
- **Work type and buffers:** Non-live (Others): 9.
- **Contract priorities:** 1: 3, 2: 3, 3: 3.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 2-2; planned completion targets span Weeks 12-12.
- **Supply:** 8 of 76 location capacities differ from the public instance; range 1-4.
- **Difference from public baseline:** contracts -5, activities -27, access-nights -111, Live contracts -2, predecessor links -6.

### set_14_horizon_edge — Horizon edge

Late starts and predecessor chains approach Week 30. Tests horizon-boundary feasibility, completion accounting and clear no-solution handling.

- **Scale:** 8 contracts, 16 activities and 40 required access-nights.
- **Possession mix:** C: 5, PC: 3.
- **Work type and buffers:** Non-live (Consist): 3, Non-live (Others): 5.
- **Contract priorities:** 1: 3, 2: 3, 3: 2.
- **Dependencies:** 8 predecessor links.
- **Timing:** planned starts span Weeks 24-26; planned completion targets span Weeks 28-29.
- **Supply:** Uses the public location-supply table unchanged; range 1-4.
- **Difference from public baseline:** contracts -6, activities -38, access-nights -152, Live contracts -2, predecessor links +2.

### set_15_mixed_portfolio — Mixed portfolio

A larger portfolio mixes all possession types, buffer classes, priorities, routes and selected dependencies. Tests whole-model robustness rather than one isolated rule.

- **Scale:** 18 contracts, 54 activities and 162 required access-nights.
- **Possession mix:** C: 9, PC: 5, PM: 4.
- **Work type and buffers:** Live: 5, Non-live (Consist): 5, Non-live (Others): 8.
- **Contract priorities:** 1: 6, 2: 6, 3: 6.
- **Dependencies:** 6 predecessor links.
- **Timing:** planned starts span Weeks 1-8; planned completion targets span Weeks 16-20.
- **Supply:** 12 of 76 location capacities differ from the public instance; range 2-4.
- **Difference from public baseline:** contracts +4, activities 0, access-nights -30, Live contracts +3, predecessor links 0.

### set_16_ultra_congestion — Ultra congestion

PM possessions with identical starts and central routes saturate one-slot locations. Tests heavy schedule slip, excess supply and search performance.

- **Scale:** 18 contracts, 54 activities and 189 required access-nights.
- **Possession mix:** PM: 18.
- **Work type and buffers:** Non-live (Others): 18.
- **Contract priorities:** 1: 6, 2: 6, 3: 6.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 1-1; planned completion targets span Weeks 10-10.
- **Supply:** 8 of 76 location capacities differ from the public instance; range 1-4.
- **Difference from public baseline:** contracts +4, activities 0, access-nights -3, Live contracts -2, predecessor links -6.

### set_17_live_interchange_surge — Live interchange surge

A surge of Live work repeatedly touches H01-H02. Tests opposite-bound mirroring, cross-line closures, two-sector buffers and Live weekly caps.

- **Scale:** 10 contracts, 30 activities and 75 required access-nights.
- **Possession mix:** PC: 5, PM: 5.
- **Work type and buffers:** Live: 10.
- **Contract priorities:** 1: 4, 2: 3, 3: 3.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 2-4; planned completion targets span Weeks 15-16.
- **Supply:** Uses the public location-supply table unchanged; range 1-4.
- **Difference from public baseline:** contracts -4, activities -24, access-nights -117, Live contracts +8, predecessor links -6.

### set_18_deep_dependency_chains — Deep dependency chains

Five-step chains within each contract create long finish-to-start critical paths across varied routes.

- **Scale:** 8 contracts, 40 activities and 96 required access-nights.
- **Possession mix:** C: 5, PC: 3.
- **Work type and buffers:** Non-live (Consist): 3, Non-live (Others): 5.
- **Contract priorities:** 1: 3, 2: 3, 3: 2.
- **Dependencies:** 32 predecessor links.
- **Timing:** planned starts span Weeks 1-1; planned completion targets span Weeks 18-20.
- **Supply:** Uses the public location-supply table unchanged; range 1-4.
- **Difference from public baseline:** contracts -6, activities -14, access-nights -96, Live contracts -2, predecessor links +26.

### set_19_cross_contract_dependency_web — Cross-contract dependency web

Three-contract dependency groups link one programme's finish to the next programme's start. Tests cross-contract predecessor handling without cycles.

- **Scale:** 12 contracts, 36 activities and 72 required access-nights.
- **Possession mix:** C: 8, PC: 4.
- **Work type and buffers:** Non-live (Others): 12.
- **Contract priorities:** 1: 4, 2: 4, 3: 4.
- **Dependencies:** 32 predecessor links.
- **Timing:** planned starts span Weeks 1-2; planned completion targets span Weeks 17-17.
- **Supply:** Uses the public location-supply table unchanged; range 1-4.
- **Difference from public baseline:** contracts -2, activities -18, access-nights -120, Live contracts -2, predecessor links +26.

### set_20_deadline_priority_crunch — Deadline and priority crunch

All priority tiers compete for PM slots before the same early deadline. Tests tier-weighted sacrifice decisions under unavoidable delay.

- **Scale:** 18 contracts, 36 activities and 108 required access-nights.
- **Possession mix:** PM: 18.
- **Work type and buffers:** Non-live (Others): 18.
- **Contract priorities:** 1: 6, 2: 6, 3: 6.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 1-1; planned completion targets span Weeks 8-8.
- **Supply:** 8 of 76 location capacities differ from the public instance; range 1-4.
- **Difference from public baseline:** contracts +4, activities -18, access-nights -84, Live contracts -2, predecessor links -6.

### set_21_minimum_supply_network — Minimum-supply network

Every location is reduced to one slot while demand remains network-wide. Tests global packing and propagation of widespread capacity scarcity.

- **Scale:** 12 contracts, 36 activities and 108 required access-nights.
- **Possession mix:** C: 4, PC: 4, PM: 4.
- **Work type and buffers:** Non-live (Consist): 6, Non-live (Others): 6.
- **Contract priorities:** 1: 4, 2: 4, 3: 4.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 1-4; planned completion targets span Weeks 18-18.
- **Supply:** 64 of 76 location capacities differ from the public instance; range 1-1.
- **Difference from public baseline:** contracts -2, activities -18, access-nights -84, Live contracts -2, predecessor links -6.

### set_22_alpha_line_supply_failure — Alpha line supply failure

Alpha capacity drops to one while Beta remains generous and most work sits on Alpha. Tests asymmetric line pressure and route-specific delay.

- **Scale:** 14 contracts, 42 activities and 105 required access-nights.
- **Possession mix:** C: 5, PC: 5, PM: 4.
- **Work type and buffers:** Non-live (Consist): 4, Non-live (Others): 10.
- **Contract priorities:** 1: 5, 2: 5, 3: 4.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 2-2; planned completion targets span Weeks 15-17.
- **Supply:** 58 of 76 location capacities differ from the public instance; range 1-4.
- **Difference from public baseline:** contracts 0, activities -12, access-nights -87, Live contracts -2, predecessor links -6.

### set_23_eastbound_supply_failure — Eastbound supply failure

Eastbound capacity collapses while westbound remains high. Tests bound independence and asymmetric congestion.

- **Scale:** 14 contracts, 42 activities and 105 required access-nights.
- **Possession mix:** C: 5, PC: 6, PM: 3.
- **Work type and buffers:** Live: 3, Non-live (Others): 11.
- **Contract priorities:** 1: 5, 2: 5, 3: 4.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 2-4; planned completion targets span Weeks 15-15.
- **Supply:** 58 of 76 location capacities differ from the public instance; range 1-4.
- **Difference from public baseline:** contracts 0, activities -12, access-nights -87, Live contracts +1, predecessor links -6.

### set_24_hub_platform_bottleneck — Hub platform bottleneck

H01/H02 platform capacity is one while tunnel capacity is increased. Tests whether platform occupancy, not only tunnel occupancy, constrains routes.

- **Scale:** 12 contracts, 36 activities and 90 required access-nights.
- **Possession mix:** C: 4, PC: 4, PM: 4.
- **Work type and buffers:** Non-live (Others): 12.
- **Contract priorities:** 1: 4, 2: 4, 3: 4.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 1-1; planned completion targets span Weeks 13-13.
- **Supply:** 12 of 76 location capacities differ from the public instance; range 1-4.
- **Difference from public baseline:** contracts -2, activities -18, access-nights -102, Live contracts -2, predecessor links -6.

### set_25_hub_tunnel_bottleneck — Hub tunnel bottleneck

The H01-H02 tunnel is one slot while hub platforms are widened. Tests tunnel-sector capacity independently of platform availability.

- **Scale:** 12 contracts, 36 activities and 90 required access-nights.
- **Possession mix:** C: 4, PC: 4, PM: 4.
- **Work type and buffers:** Non-live (Others): 12.
- **Contract priorities:** 1: 4, 2: 4, 3: 4.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 1-1; planned completion targets span Weeks 13-13.
- **Supply:** 40 of 76 location capacities differ from the public instance; range 1-4.
- **Difference from public baseline:** contracts -2, activities -18, access-nights -102, Live contracts -2, predecessor links -6.

### set_26_maximum_co_share_packing — Maximum co-share packing

PC and C jobs crowd one-slot locations. Tests efficient PC plus three-C and four-C possession packing.

- **Scale:** 20 contracts, 40 activities and 100 required access-nights.
- **Possession mix:** C: 15, PC: 5.
- **Work type and buffers:** Non-live (Others): 20.
- **Contract priorities:** 1: 7, 2: 7, 3: 6.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 1-1; planned completion targets span Weeks 8-8.
- **Supply:** 8 of 76 location capacities differ from the public instance; range 1-4.
- **Difference from public baseline:** contracts +6, activities -14, access-nights -92, Live contracts -2, predecessor links -6.

### set_27_pc_host_shortage — PC host shortage

Many PC possessions compete with only a few C workers, preventing efficient sharing. Tests that PC cannot illegally share with another PC.

- **Scale:** 16 contracts, 32 activities and 80 required access-nights.
- **Possession mix:** C: 4, PC: 12.
- **Work type and buffers:** Non-live (Others): 16.
- **Contract priorities:** 1: 6, 2: 5, 3: 5.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 1-1; planned completion targets span Weeks 9-9.
- **Supply:** 8 of 76 location capacities differ from the public instance; range 1-4.
- **Difference from public baseline:** contracts +2, activities -22, access-nights -112, Live contracts -2, predecessor links -6.

### set_28_pm_monopoly_conflict — PM monopoly conflict

PM work monopolises each possession and cannot co-share. Tests sole-possession enforcement under dense central demand.

- **Scale:** 14 contracts, 28 activities and 84 required access-nights.
- **Possession mix:** PM: 14.
- **Work type and buffers:** Non-live (Consist): 4, Non-live (Others): 10.
- **Contract priorities:** 1: 5, 2: 5, 3: 4.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 1-1; planned completion targets span Weeks 10-10.
- **Supply:** 12 of 76 location capacities differ from the public instance; range 2-4.
- **Difference from public baseline:** contracts 0, activities -26, access-nights -108, Live contracts -2, predecessor links -6.

### set_29_multi_workfront_burst — Multi-workfront burst

Six contracts each launch ten activities with three workfronts. Tests correct use of parallel teams without exceeding access-night budgets.

- **Scale:** 6 contracts, 60 activities and 90 required access-nights.
- **Possession mix:** C: 6.
- **Work type and buffers:** Non-live (Others): 6.
- **Contract priorities:** 1: 2, 2: 2, 3: 2.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 1-1; planned completion targets span Weeks 4-4.
- **Supply:** 52 of 76 location capacities differ from the public instance; range 4-4.
- **Difference from public baseline:** contracts -8, activities +6, access-nights -102, Live contracts -2, predecessor links -6.

### set_30_single_contract_megaprogram — Single-contract megaprogram

One contract owns thirty activities across both lines but has only two workfronts and three weekly nights. Tests contract-level scaling and allocation accounting.

- **Scale:** 1 contracts, 30 activities and 60 required access-nights.
- **Possession mix:** C: 1.
- **Work type and buffers:** Non-live (Others): 1.
- **Contract priorities:** 1: 1.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 1-4; planned completion targets span Weeks 12-12.
- **Supply:** 52 of 76 location capacities differ from the public instance; range 4-4.
- **Difference from public baseline:** contracts -13, activities -24, access-nights -132, Live contracts -2, predecessor links -6.

### set_31_many_tiny_contracts — Many tiny contracts

Forty one-activity contracts stress model size, contract indexing and priority ordering with little intra-contract complexity.

- **Scale:** 40 contracts, 40 activities and 100 required access-nights.
- **Possession mix:** C: 12, PC: 12, PM: 16.
- **Work type and buffers:** Live: 4, Non-live (Others): 36.
- **Contract priorities:** 1: 14, 2: 13, 3: 13.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 1-6; planned completion targets span Weeks 10-14.
- **Supply:** Uses the public location-supply table unchanged; range 1-4.
- **Difference from public baseline:** contracts +26, activities -14, access-nights -92, Live contracts +2, predecessor links -6.

### set_32_long_route_occupancy — Long-route occupancy

Activities span nearly entire lines, generating large platform and tunnel footprints. Tests occupancy expansion and widespread closure conflicts.

- **Scale:** 10 contracts, 30 activities and 75 required access-nights.
- **Possession mix:** PC: 4, PM: 6.
- **Work type and buffers:** Non-live (Consist): 5, Non-live (Others): 5.
- **Contract priorities:** 1: 4, 2: 3, 3: 3.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 1-3; planned completion targets span Weeks 17-17.
- **Supply:** Uses the public location-supply table unchanged; range 1-4.
- **Difference from public baseline:** contracts -4, activities -24, access-nights -117, Live contracts -2, predecessor links -6.

### set_33_point_job_swarm — Point-job swarm

Sixty short jobs occupy single tunnel sectors. Tests high activity count, co-sharing and slot grouping without long-route expansion.

- **Scale:** 30 contracts, 60 activities and 120 required access-nights.
- **Possession mix:** C: 24, PC: 6.
- **Work type and buffers:** Non-live (Others): 30.
- **Contract priorities:** 1: 10, 2: 10, 3: 10.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 1-4; planned completion targets span Weeks 10-12.
- **Supply:** Uses the public location-supply table unchanged; range 1-4.
- **Difference from public baseline:** contracts +16, activities +6, access-nights -72, Live contracts -2, predecessor links -6.

### set_34_staggered_demand_waves — Staggered demand waves

Programmes arrive in five start-date waves. Tests rolling admission, capacity reuse and avoidance of premature scheduling.

- **Scale:** 15 contracts, 45 activities and 112 required access-nights.
- **Possession mix:** C: 5, PC: 5, PM: 5.
- **Work type and buffers:** Non-live (Consist): 4, Non-live (Others): 11.
- **Contract priorities:** 1: 5, 2: 5, 3: 5.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 1-13; planned completion targets span Weeks 10-22.
- **Supply:** Uses the public location-supply table unchanged; range 1-4.
- **Difference from public baseline:** contracts +1, activities -9, access-nights -80, Live contracts -2, predecessor links -6.

### set_35_simultaneous_start_burst — Simultaneous-start burst

Forty activities all become eligible in Week 10 on central corridors. Tests burst handling and prioritised displacement.

- **Scale:** 20 contracts, 40 activities and 100 required access-nights.
- **Possession mix:** C: 6, PC: 7, PM: 7.
- **Work type and buffers:** Non-live (Consist): 4, Non-live (Others): 16.
- **Contract priorities:** 1: 7, 2: 7, 3: 6.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 10-10; planned completion targets span Weeks 14-14.
- **Supply:** 8 of 76 location capacities differ from the public instance; range 1-4.
- **Difference from public baseline:** contracts +6, activities -14, access-nights -92, Live contracts -2, predecessor links -6.

### set_36_deadline_ladder — Deadline ladder

Contracts share the same start but have weekly-stepped deadlines. Tests deadline ordering and whether later work yields to earlier milestones.

- **Scale:** 15 contracts, 30 activities and 75 required access-nights.
- **Possession mix:** PM: 15.
- **Work type and buffers:** Non-live (Others): 15.
- **Contract priorities:** 2: 15.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 1-1; planned completion targets span Weeks 5-19.
- **Supply:** 8 of 76 location capacities differ from the public instance; range 1-4.
- **Difference from public baseline:** contracts +1, activities -24, access-nights -117, Live contracts -2, predecessor links -6.

### set_37_mixed_buffer_adjacency — Mixed-buffer adjacency

Alternating Live, Consist and buffer-free work occupies neighbouring sectors on the same bounds. Tests pairwise closure spacing.

- **Scale:** 15 contracts, 30 activities and 75 required access-nights.
- **Possession mix:** C: 5, PC: 5, PM: 5.
- **Work type and buffers:** Live: 5, Non-live (Consist): 5, Non-live (Others): 5.
- **Contract priorities:** 1: 5, 2: 5, 3: 5.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 2-2; planned completion targets span Weeks 15-15.
- **Supply:** Uses the public location-supply table unchanged; range 1-4.
- **Difference from public baseline:** contracts +1, activities -24, access-nights -117, Live contracts +3, predecessor links -6.

### set_38_eclo_continuity_window — ECLO continuity window

Live workloads pressure both line-specific two-week ECLO windows in Scenario C. Tests continuity-window selection and cross-line overlap.

- **Scale:** 8 contracts, 32 activities and 144 required access-nights.
- **Possession mix:** PC: 4, PM: 4.
- **Work type and buffers:** Live: 8.
- **Contract priorities:** 1: 3, 2: 3, 3: 2.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 4-6; planned completion targets span Weeks 11-12.
- **Supply:** Uses the public location-supply table unchanged; range 1-4.
- **Difference from public baseline:** contracts -6, activities -22, access-nights -48, Live contracts +6, predecessor links -6.

### set_39_cross_line_live_lock — Cross-line Live lock

Live H01-H02 work on both lines competes for the same traction-power closure periods. Tests that cross-line conflicts cannot be scheduled concurrently.

- **Scale:** 12 contracts, 24 activities and 60 required access-nights.
- **Possession mix:** PC: 6, PM: 6.
- **Work type and buffers:** Live: 12.
- **Contract priorities:** 1: 4, 2: 4, 3: 4.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 2-2; planned completion targets span Weeks 16-16.
- **Supply:** 12 of 76 location capacities differ from the public instance; range 2-4.
- **Difference from public baseline:** contracts -2, activities -30, access-nights -132, Live contracts +10, predecessor links -6.

### set_40_rigid_deadline_failure — Rigid-deadline rescue

High workloads begin only two weeks before planned completion. Tests whether Scenario B can rescue the deadline with ECLO and extra supply while strict-supply Scenario A fails.

- **Scale:** 10 contracts, 30 activities and 120 required access-nights.
- **Possession mix:** PM: 10.
- **Work type and buffers:** Non-live (Others): 10.
- **Contract priorities:** 1: 4, 2: 3, 3: 3.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 15-15; planned completion targets span Weeks 17-17.
- **Supply:** 8 of 76 location capacities differ from the public instance; range 1-4.
- **Difference from public baseline:** contracts -4, activities -24, access-nights -72, Live contracts -2, predecessor links -6.

### set_41_priority_inversion_trap — Priority inversion trap

Small Priority-1 contracts compete against large Priority-3 contracts. Tests that workload size does not wrongly outweigh the contract-priority band.

- **Scale:** 14 contracts, 28 activities and 116 required access-nights.
- **Possession mix:** PM: 14.
- **Work type and buffers:** Non-live (Others): 14.
- **Contract priorities:** 1: 4, 3: 10.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 1-1; planned completion targets span Weeks 10-10.
- **Supply:** 8 of 76 location capacities differ from the public instance; range 1-4.
- **Difference from public baseline:** contracts 0, activities -26, access-nights -76, Live contracts -2, predecessor links -6.

### set_42_co_share_mix_limit — Co-share mix limit

PC and C programmes deliberately exceed one-PC-plus-three-C demand at the same locations. Tests legal mix limits and spillover possessions.

- **Scale:** 24 contracts, 24 activities and 72 required access-nights.
- **Possession mix:** C: 20, PC: 4.
- **Work type and buffers:** Non-live (Others): 24.
- **Contract priorities:** 1: 8, 2: 8, 3: 8.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 1-1; planned completion targets span Weeks 7-7.
- **Supply:** 8 of 76 location capacities differ from the public instance; range 1-4.
- **Difference from public baseline:** contracts +10, activities -30, access-nights -120, Live contracts -2, predecessor links -6.

### set_43_four_c_packing_limit — Four-C packing limit

C-only workloads require exact groups of at most four per possession. Tests that five or more C jobs never occupy one slot.

- **Scale:** 24 contracts, 24 activities and 72 required access-nights.
- **Possession mix:** C: 24.
- **Work type and buffers:** Non-live (Others): 24.
- **Contract priorities:** 1: 8, 2: 8, 3: 8.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 1-1; planned completion targets span Weeks 6-6.
- **Supply:** 8 of 76 location capacities differ from the public instance; range 1-4.
- **Difference from public baseline:** contracts +10, activities -30, access-nights -120, Live contracts -2, predecessor links -6.

### set_44_alternating_bound_corridors — Alternating-bound corridors

Mirrored EB/WB corridors carry alternating Live and non-Live programmes. Tests selective opposite-bound coupling across several route lengths.

- **Scale:** 16 contracts, 48 activities and 120 required access-nights.
- **Possession mix:** C: 4, PC: 8, PM: 4.
- **Work type and buffers:** Live: 4, Non-live (Others): 12.
- **Contract priorities:** 1: 6, 2: 5, 3: 5.
- **Dependencies:** 0 predecessor links.
- **Timing:** planned starts span Weeks 2-5; planned completion targets span Weeks 14-16.
- **Supply:** Uses the public location-supply table unchanged; range 1-4.
- **Difference from public baseline:** contracts +2, activities -6, access-nights -72, Live contracts +2, predecessor links -6.

### set_45_deterministic_mega_case — Deterministic mega case

Thirty contracts and 120 activities mix every rule at scale. This is the largest search and timeout stress test in the collection.

- **Scale:** 30 contracts, 120 activities and 420 required access-nights.
- **Possession mix:** C: 12, PC: 9, PM: 9.
- **Work type and buffers:** Live: 6, Non-live (Consist): 6, Non-live (Others): 18.
- **Contract priorities:** 1: 10, 2: 10, 3: 10.
- **Dependencies:** 15 predecessor links.
- **Timing:** planned starts span Weeks 1-10; planned completion targets span Weeks 13-20.
- **Supply:** 12 of 76 location capacities differ from the public instance; range 2-4.
- **Difference from public baseline:** contracts +16, activities +66, access-nights +228, Live contracts +4, predecessor links +9.

## Validation and solver notes

All 45 packs passed schema and semantic input validation. Some stress packs are deliberately infeasible under particular policies, while others are intended to exceed short solver time limits. See the accompanying validation and smoke-test reports for measured outcomes.

Source schema: official NebulaX Hackathon Problem Statement repository, PS1 `main` branch, commit `966c976`.
