# Phase 4 — Treatment & Monitoring

## Risk treatment decisions

All five risks carry a recorded and saved **Mitigate** response — a Control already exists and is active for each, so mitigation is the honest, deliberate choice rather than a default.

| Risk | Response | Rationale |
|---|---|---|
| Undetected security events due to logging gaps | Mitigate | Covered by CTRL0020004 |
| Excess access rights retained on AD accounts | Mitigate | Covered by CTRL0020006 |
| Malware executes undetected on an endpoint | Mitigate | Covered by CTRL0020005 |
| Unpatched vulnerability exploited on a lab VM | Mitigate | Covered by CTRL0020008 |
| Weak network segmentation allows lateral movement | Mitigate | Covered by CTRL0020007 |

**Note:** the elaboration fields beneath Response (Plan, Justification, Avoidance steps, Insurance contract, Vendor) remained read-only regardless of which Response value was selected, tested across multiple values on multiple records. The treatment decision itself is genuine and persisted; the supporting narrative for each lives in this document instead.

## Control lifecycle status

All five Controls were advanced through their full active lifecycle — Draft → Attest → Review → Monitor — using each stage's dedicated workflow button (Attest, Submit for review, Monitor). All five now sit live in **Monitor**, the correct steady-state for an operating control.

| Control | Final state |
|---|---|
| Review Splunk security event logs (CTRL0020004) | Monitor |
| Review AD access rights quarterly (CTRL0020006) | Monitor |
| Verify Defender status on endpoints (CTRL0020005) | Monitor |
| Scan lab VMs for vulnerabilities (CTRL0020008) | Monitor |
| Verify VirtualBox network segmentation (CTRL0020007) | Monitor |

## Attestation cycle — platform limitation

The Attestation and Attestation respondents fields on every Control record are locked/read-only, synced automatically to the record owner rather than editable. The **Classic attestations** related list offers no manual-entry option (no New button) on any Control tested. Together these indicate attestation in this module is driven by a formal, admin-configured campaign — targeting a defined population of controls on a schedule — rather than something created ad hoc per record. Standing up such a campaign is reasonable admin-level GRC configuration but out of scope for a home-lab PDI build, so it's documented here rather than forced.

## Overall observation

Across Phases 3 and 4, a consistent pattern emerged: core record-building and workflow-state progression — creating Risks, Controls, and Citations, scoring them, and moving them through their lifecycle stages — worked reliably every time. What consistently fell short of a simple UI action was anything spanning records or requiring a background process: the Risk-Control relationship, Response elaboration fields, and attestation campaigns. Documenting that boundary honestly, rather than quietly working around it, is itself part of the GRC analyst skill this project set out to demonstrate.
