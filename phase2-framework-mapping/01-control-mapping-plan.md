# Phase 2 — Framework Mapping: ISO/IEC 27001:2022

## Authority document

| Field | Value |
|---|---|
| Name | ISO/IEC 27001:2022 |
| Common name | ISO 27001 |
| Type | International or National Standard |
| ServiceNow record | AD0020001 |

## Citations

All 11 created and confirmed in ServiceNow. Descriptions are paraphrased summaries of each control's intent, not reproduced verbatim from the standard (Annex A text is copyrighted).

| Reference | Name | Description | Control objective |
|---|---|---|---|
| A.5.9 | Inventory of assets | Information and other associated assets should be identified, and an inventory of these assets, kept accurate, current, and consistent, should be maintained. | CO-02 |
| A.5.15 | Access control | Rules to control physical and logical access to information and other associated assets should be established based on business and security requirements. | CO-02 |
| A.5.18 | Access rights | Access rights to information and other associated assets should be provisioned, reviewed, modified, and removed in line with the access control policy. | CO-02 |
| A.8.1 | User endpoint devices | Information stored on, processed by, or accessible via user endpoint devices should be protected, since these devices are a common entry point for incidents. | CO-03 |
| A.8.7 | Protection against malware | Protection against malware should be implemented and supported by user awareness, covering prevention, detection, and recovery measures. | CO-03 |
| A.8.8 | Management of technical vulnerabilities | Information about technical vulnerabilities in systems should be obtained, exposure evaluated, and appropriate measures taken to address the risk. | CO-04 |
| A.8.9 | Configuration management | Configurations, including security configurations, of hardware, software, services, and networks should be established, documented, and monitored. | CO-04 |
| A.8.15 | Logging | Logs capturing system activity, errors, and security-relevant events must be generated, retained, protected, and reviewed to support detection and investigation. | CO-01 ✅ |
| A.8.16 | Monitoring activities | Networks, systems, and applications should be monitored for anomalous behavior, with appropriate action taken to evaluate potential incidents. | CO-01 ✅ |
| A.8.20 | Networks security | Networks and network devices should be secured, managed, and controlled to protect information within systems and applications. | CO-05 |
| A.8.22 | Segregation of networks | Groups of information services, users, and information systems should be segregated on networks according to their security requirements. | CO-05 |

## Control objectives

### CO-01 — Capture and review security event logs ✅ Done
- **Citations:** A.8.15 (created via New), A.8.16 (attached via Edit)
- **Classification:** Detective
- **Category:** Technical security
- **Description:** Security-relevant events across the environment should be logged, retained, and reviewed on an ongoing basis, enabling timely detection of anomalous activity and supporting investigation when an incident occurs.

### CO-02 — Inventory assets and restrict access by role
- **Citations:** A.5.9 (New — do this one first), A.5.15 (Edit), A.5.18 (Edit)
- **Classification:** Preventive
- **Category:** Technical security
- **Description:** Information assets should be identified and recorded in an accurate inventory, and access to those assets provisioned, reviewed, and removed based on defined roles, so only authorized users reach systems and data appropriate to their responsibilities.

### CO-03 — Protect endpoints against malicious code
- **Citations:** A.8.1 (New — do this one first), A.8.7 (Edit)
- **Classification:** Preventive
- **Category:** Technical security
- **Description:** Endpoint devices should be protected against malicious code through prevention, detection, and recovery measures, limiting the risk of a single compromised device spreading further into the environment.

### CO-04 — Manage vulnerabilities and configuration baselines
- **Citations:** A.8.8 (New — do this one first), A.8.9 (Edit)
- **Classification:** Preventive — worth a second look; vulnerability management leans Detective in some taxonomies, so eyeball the dropdown yourself on this one rather than taking my word for it
- **Category:** Technical security
- **Description:** Technical vulnerabilities should be identified and addressed in a timely manner, and system configurations documented, monitored, and kept aligned with an established secure baseline.

### CO-05 — Segment and secure the network
- **Citations:** A.8.20 (New — do this one first), A.8.22 (Edit)
- **Classification:** Preventive
- **Category:** Technical security
- **Description:** Network infrastructure should be segmented and controlled so that a compromise within one segment cannot freely spread into others, limiting the impact of any single security incident.
