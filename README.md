# Redundant Network Design with Spanning Tree Failover

## Overview
Designed and validated a redundant Layer 2 network to eliminate single points of failure between switches. Implemented dual-path connectivity and verified failover behavior using Spanning Tree Protocol during link failure.

## Objective
Built a resilient switch topology capable of maintaining connectivity during link failure by introducing redundancy and validating automatic failover behavior.

## Network Setup
```
Devices Used
2 Cisco 2960 Switches
1 Router
2 End Devices PCs
```
Topology Design
- Switch0 connected to Switch1 using two physical links
- PCs connected across both switches
- Router connected to provide gateway functionality

Logical Design
- Primary path and secondary path established between switches
- One path active and one path blocked by Spanning Tree

Video Demonstration
![Redundancy Lab Video](https://github.com/Pelumi-Johnson/Redundant-Network-Design-with-Spanning-Tree-Failover/blob/main/Animation.gif)

## Configuration
Configured switch-to-switch connections using two links to create redundant paths
```
Enabled default Spanning Tree behavior on switches

No manual STP configuration required for initial failover validation
```
## Validation

### Initial State
Verified connectivity between devices across both switches
Confirmed network stability with redundant links present

### STP Behavior
Observed one link in forwarding state and the second link in blocking state

Used command
```
show spanning-tree
```
Confirmed loop prevention through port blocking

### Failure Simulation
Disconnected primary active link between switches

Observed behavior
Backup link transitioned to forwarding state
Traffic continued without interruption

## Key Concepts Applied
- Redundant link design to remove single points of failure
- Spanning Tree Protocol for loop prevention
- Failover validation through physical link failure simulation
- Layer 2 resilience through controlled path selection

## Outcome
Implemented a redundant switching topology capable of maintaining communication during link failure. Verified that Spanning Tree Protocol dynamically reconfigured the network path, ensuring continuous connectivity without manual intervention.
