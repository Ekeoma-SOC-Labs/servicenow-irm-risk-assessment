# ServiceNow IRM — IT Risk Assessment & Management (Home Lab Project)

## Overview
A hands-on IT risk assessment and management project built on ServiceNow's Integrated Risk Management (IRM) module. The environment under assessment is my own home lab, giving this project a real, defensible scope rather than generic demo data — the same approach used in my [SOC Alert Triage Lab](https://github.com/Ekeoma-SOC-Labs).

## Author
Ekeoma Eneogwe

## Environment
- **Platform:** ServiceNow Personal Developer Instance (PDI) — Zurich release
- **Module:** Integrated Risk Management (IRM), installed with demo data (36 dependent applications)
- **Scope (assessed environment):** Home lab on VirtualBox, host-only network `192.168.56.x`
  - `DC01` — Windows Server 2019, Domain Controller
  - Windows 10 endpoint
  - Ubuntu Server — Splunk (SIEM/log management)
  - Kali Linux 2025.4 — security testing tool

## Project Phases

- [x] **Phase 1 — Foundation:** PDI provisioning, IRM plugin installation, RBAC setup, CMDB/CI creation for lab assets
- [X] **Phase 2 — Framework Mapping:** Authority Documents → Citations → Control Objectives, mapped to a chosen standard (ISO 27001 / NIST CSF)
- [ ] **Phase 3 — Risk Assessment:** Risk Register build-out, likelihood × impact scoring, risk-to-control linking
- [ ] **Phase 4 — Treatment & Monitoring:** Remediation tasks for high-scoring risks, attestation cycle, compliance dashboard/reporting
- [ ] **Phase 5 — Documentation:** Final written IT Risk Assessment Report (methodology, findings, remediation plan)

## Repository Structure
