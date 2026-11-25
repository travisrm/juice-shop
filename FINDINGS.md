# Security Findings Triage

Pipeline: `.github/workflows/security-scan.yml` (Semgrep SAST, gitleaks secret scanning, Trivy SCA)
Target: fork of [OWASP Juice Shop](https://github.com/juice-shop/juice-shop), an intentionally vulnerable web app

## Summary

| Scanner | Total findings | Triaged | True positive | False positive / accepted |
|---|---|---|---|---|
| Semgrep (SAST) | | | | |
| gitleaks (secrets) | | | | |
| Trivy (SCA) | | | | |

## Triaged findings

<!-- Copy this block for each finding. Aim for 10-15, mixing all three scanners
     and including at least 3 false positives. -->

### F-01: <short title, e.g. "SQL injection in login route">

- **Scanner / rule:** Semgrep `<rule id>`
- **Location:** `routes/login.ts:34`
- **Severity (scanner):** High
- **Verdict:** True positive | False positive | Accepted risk
- **Evidence:** What in the code proves the verdict. Does user input actually reach this line? Is it sanitized first?
- **Impact:** What an attacker could do if this is real.
- **Remediation:** The specific code change (e.g. "use a parameterized query instead of string concatenation"), with a snippet if short.

## What I learned

- Where the scanners overlapped or disagreed
- Most common causes of false positives
- What I'd tune in the pipeline next (rule exclusions, severity thresholds, failing the build on High)
