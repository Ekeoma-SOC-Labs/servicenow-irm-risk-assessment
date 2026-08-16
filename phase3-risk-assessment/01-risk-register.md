# Phase 3 — Risk Register

## Entity

All five risks are scoped to **Home Lab Environment** (the same Entity created in Phase 3 for the Controls), owned by Ekeoma Eneogwe.

## Risks and scoring

Risk model in this instance is quantitative: **SLE** (Single Loss Expectancy, cost of one occurrence) × **ARO** (Annualized Rate of Occurrence, expected times per year) = **ALE** (Annualized Loss Expectancy). Residual currently mirrors Inherent for all five — see linking note below for why.

| Risk | SLE | ARO | ALE | Score |
|---|---|---|---|---|
| Undetected security events due to logging gaps | $500 | 2 | $1,000 | 1 - Very Low |
| Excess access rights retained on AD accounts | $300 | 1 | $300 | 1 - Very Low |
| Malware executes undetected on an endpoint | $800 | 2 | $1,600 | 1 - Very Low |
| Unpatched vulnerability exploited on a lab VM | $1,000 | 1 | $1,000 | 1 - Very Low |
| Weak network segmentation allows lateral movement | $600 | 1 | $600 | 1 - Very Low |

**Note on scoring:** every risk lands on "1 - Very Low" because this instance's built-in Risk Criteria thresholds are enterprise-calibrated — the Very Low band alone extends to $1,000,000 ALE. That ceiling is shared config also used by the bundled SOX demo data (Accounts Payable, Fixed Assets, etc.) and wasn't rescaled for a four-VM home lab. The dollar figures above are still meaningful relative to each other; only the qualitative label compresses at this scale.

## Intended risk-to-control mapping

| Risk | Control |
|---|---|
| Undetected security events due to logging gaps | Review Splunk security event logs (CTRL0020004) |
| Excess access rights retained on AD accounts | Review AD access rights quarterly (CTRL0020006) |
| Malware executes undetected on an endpoint | Verify Defender status on endpoints (CTRL0020005) |
| Unpatched vulnerability exploited on a lab VM | Scan lab VMs for vulnerabilities (CTRL0020008) |
| Weak network segmentation allows lateral movement | Verify VirtualBox network segmentation (CTRL0020007) |

**Note on linking:** the native ServiceNow Risk↔Control relationship (Controls related list on Risk, Risks related list on Control) did not persist in this PDI. Tested across two independent Risk-Control pairs (CO-01/Logging and CO-02/Access rights) to rule out a fault specific to a single record, from both relationship directions, with confirmed checkbox selection each time, full page reloads, and a private browser session with extensions disabled to rule out client-side interference. Every attempt failed to save despite the UI visually confirming a valid selection. This mirrors the `security_admin` elevation limitation from Phase 1 and is documented here as a genuine environment-specific constraint rather than a configuration error or an incomplete troubleshooting pass. The mapping above reflects the intended linkage and is what the finished Risk Register report treats as authoritative.
