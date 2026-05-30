# Elytra Argus

**Argus** is the Defensive SAR (Security Attack Resistance) platform by Elytra Security.

It models what AI-driven adversaries can discover, chain, and weaponize, then converts
that intelligence into deterministic Fix Packs with validation proof.

Argus runs as an on-premises appliance. No data leaves the network.
No cloud dependency. No agentic AI at runtime.

---

## What Argus Does

Argus answers the questions that matter to security teams and boards:

- What can an AI-driven attacker learn about us from the outside and inside?
- What can that attacker chain together toward crown jewels or sensitive data?
- Which findings are truly feasible to exploit?
- What should we fix first, and what exact ticket goes into ITSM?
- How do we prove the issue is fixed?
- Are we becoming harder to recon over time?

---

## Key Capabilities

- **SAR Matrix** — maps findings to AI-driven reconnaissance stages and techniques
- **Recon Resistance Score** — board-level metric for AI recon advantage reduction
- **Attacker Next-Step Simulation** — deterministic adversary path reasoning over scan evidence
- **Action Command Center** — prioritized Fix Packs with ITSM handoff and validation contracts
- **Evidence Ledger** — tamper-evident audit history for every Fix Pack state change
- **Coverage Gap Detection** — identifies weakly monitored or unmonitored critical assets
- **Connectors** — Active Directory, M365, AWS, GCP, Wazuh

All classification and scoring is deterministic. No LLM at runtime.

---

## System Requirements

- Ubuntu 22.04+ or Debian 12+
- 2 GB RAM minimum (4 GB recommended)
- 10 GB free disk on /var/lib/argus
- x86-64 architecture
- systemd

---

## Getting Argus

Argus is distributed exclusively through the Elytra Customer Portal.

Licensed customers can download the latest release and installation
documentation at:

[https://portal.elytrasecurity.com](https://portal.elytrasecurity.com)

To request access or a trial license, contact:
[info@elytrasecurity.com](mailto:info@elytrasecurity.com)

---

## License

Argus requires a valid license to run scans. Without a license the
dashboard is accessible but scanning is disabled.

License management is available under Configuration > License
in the Argus operator console. No restart is required when a new
license is installed.

---

## Support

| Channel | Contact |
|---|---|
| General | support@elytrasecurity.com |
| Security issues | See SECURITY.md |
| Sales and licensing | info@elytrasecurity.com |

---

## Version History

| Version | Date       | Notes              |
|---------|------------|--------------------|
| 2026.01 | 2026-05-09 | Initial GA release |

---

## Security

For responsible disclosure and security vulnerability reporting,
see [SECURITY.md](SECURITY.md).
