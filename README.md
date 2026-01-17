# Elastic SIEM – Zeek Network Detections

## Overview
Built custom Elastic SIEM detection rules using Zeek DNS and network logs to identify suspicious network behavior and validate SOC alerting workflows.

This project focuses on detection engineering, rule tuning, and analyst-ready visibility using real Zeek telemetry.

---

## Environment & Tools
- Elastic SIEM (Elastic Cloud)
- Zeek network sensor
- Filebeat Zeek module
- Kibana
- KQL
- Ubuntu (Zeek sensor)

---

## Data Sources
- Zeek DNS logs (`zeek.dns`)
- Zeek connection logs (`zeek.conn`)
- Network metadata (IP, domain, query types)

---

## What Was Implemented
- Ingested Zeek network logs into Elastic SIEM via Filebeat
- Created custom detection rules using KQL
- Focused on DNS-based threat indicators and abnormal network behavior
- Validated detections using rule preview and Kibana Discover

---

## Detection Logic (Examples)
- Suspicious DNS query volume from a single source IP
- Repeated DNS requests to rare or newly observed domains
- DNS activity consistent with beaconing or C2 patterns

---

## Findings / SOC Notes
- Identified abnormal DNS query patterns indicative of potential beaconing
- Detected high-frequency DNS requests to uncommon domains
- Confirmed alerts populated correctly in Elastic SIEM with supporting network context
- Verified analyst pivot capability from alert → DNS logs → source IP activity

---

## Validation Evidence
**Elastic SIEM – Detection Rule Creation and Preview (Zeek DNS)**

![Elastic SIEM Zeek Detection Rule](screenshots/zeek-detection-rule.png)

---

## SOC Relevance
This project demonstrates:
- Network-based threat detection using Zeek telemetry
- SIEM rule creation and validation
- Alert-driven investigation aligned with SOC analyst workflows
- Practical detection engineering beyond default SIEM rules
