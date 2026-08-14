# Cisco Enterprise Network Engineering Portfolio

## Overview

This repository documents hands-on engineering work focused on enterprise campus architecture, Layer 2 and Layer 3 redundancy, dynamic routing, encrypted WAN connectivity, network resiliency, and operational visibility using Cisco routing and switching platforms.

The repository is built around a complete multi-site Cornerstone Lab, with incident case studies extending that environment through focused troubleshooting and failure analysis.

All scenarios are executed within an EVE-NG virtual lab environment modeled on production-style topologies.

The work is documented as validated engineering case notes focused on observable behavior, failure analysis, and verified outcomes rather than configuration walkthroughs.

---

## Featured Lab

### Cisco Cornerstone Lab - Multi-Site Campus and WAN Architecture

[View Cisco Cornerstone Lab](Cisco-Cornerstone-Lab-Multi-Site-Campus-and-WAN-Architecture/)

A complete multi-site enterprise network demonstrating:

- Three-tier campus architecture with a redundant distribution pair
- Rapid-PVST root placement aligned with HSRP gateway ownership
- Layer 2 and Layer 3 LACP port-channel aggregation
- OSPF Area 0 with per-SVI cost tuning for preferred and alternate paths
- Route-based IPsec to a remote branch with eBGP route exchange
- IP SLA and object tracking driving campus and WAN edge failover
- Centralized syslog collection and SNMPv3 monitoring

This lab establishes the reference architecture for the repository and demonstrates how Layer 2 forwarding, first-hop redundancy, interior routing, WAN path selection, failure recovery, and monitoring operate together as one system.

---

## Capability Areas Demonstrated

### Campus Switching and First-Hop Redundancy

- Three-tier access, distribution, and core design
- VLAN segmentation by traffic function
- Rapid-PVST with deliberate root bridge placement
- HSRP gateway ownership aligned with spanning tree
- Layer 2 and Layer 3 LACP port-channel aggregation
- IP SLA-based HSRP tracking tied to distribution uplink reachability

### Routing and Path Selection

- OSPF Area 0 across the campus backbone
- Per-SVI OSPF cost tuning for deterministic path preference
- Preferred and alternate distribution paths
- Default route propagation through the campus
- eBGP route exchange between autonomous systems
- Interaction between interior and exterior routing domains

### WAN and Inter-Site Connectivity

- Route-based IPsec
- Dual encrypted paths between sites
- Dynamic routing across encrypted transport
- Primary and failover WAN edge paths
- NAT overload for internet-bound traffic
- Inter-site traffic excluded from internet NAT

### Resiliency and Failure-State Validation

- IP SLA probe design and object tracking
- HSRP gateway transition during distribution failure
- OSPF convergence through the alternate distribution path
- WAN edge failure with automatic default-route relocation
- Tracking decrement sizing verified against standby priority
- Controlled failure introduction and recovery validation

### Network Operations and Visibility

- Centralized Graylog syslog
- LibreNMS monitoring through SNMPv3
- Device, interface, health, and routing protocol visibility
- Event correlation across failure conditions
- Failure sequence reconstruction
- Dedicated management network separation

---

## Approach

These projects are not configuration walkthroughs.

The focus is on understanding how the network behaves during normal operation and when something fails:

- Where traffic should flow
- Which component owns the forwarding path
- What takes over when that component becomes unavailable
- Whether the alternate path is already known to the network
- How the transition can be verified
- How the event can be reconstructed afterward

Each scenario emphasizes verification over configuration. Recovery mechanisms are validated through controlled failure rather than assumed from configuration state.

---

## Incident Case Studies

Each incident is documented as a structured engineering case note covering observable symptoms, investigation path, root cause, corrective action, and post-remediation validation.

Incident case studies will be added as they are completed.
