# Elytra Argus

**Argus** is the Defensive SAR (Security Attack Resistance) platform by Elytra Security.
It models what AI-driven adversaries can discover, chain, and weaponize, then converts
that intelligence into deterministic Fix Packs with validation proof.

Argus runs as an on-premises appliance. No data leaves the network.
No cloud dependency. No agentic AI at runtime.

---

## System Requirements

- Ubuntu 22.04+ or Debian 12+
- 2 GB RAM minimum (4 GB recommended)
- 10 GB free disk on /var/lib/argus
- x86-64 architecture
- systemd
- Internet access for initial package installation only

---

## Download

Download the latest release from the
[Releases](https://github.com/Elytra-Security/argus/releases) page.

Current release: **2026.01**

    curl -LO https://github.com/Elytra-Security/argus/releases/download/2026.01/argus-2026.01.tar.gz
    curl -LO https://github.com/Elytra-Security/argus/releases/download/2026.01/argus-2026.01.tar.gz.sha256

---

## Verify

Always verify the checksum before installing:

    sha256sum --check argus-2026.01.tar.gz.sha256

Expected output: `argus-2026.01.tar.gz: OK`

Do not proceed if the checksum fails.

---

## Install

    tar xzf argus-2026.01.tar.gz
    cd argus-2026.01
    ./scripts/install.sh

The install script:

- Runs as a regular OS user with sudo access
- Installs all system dependencies automatically
- Creates the argus system user and directory structure
- Sets up PostgreSQL and applies the database schema
- Configures and starts the argusd service via systemd
- Sets up nginx as a TLS reverse proxy on ports 80 and 443
- Writes operator credentials to ~/operator_credentials.txt

Installation takes approximately 2-5 minutes on a fresh system.

---

## First Login

After installation, open a browser and navigate to:

    https://APPLIANCE_IP

Accept the self-signed certificate warning. Log in with the
credentials written to ~/operator_credentials.txt during install.

---

## License

Argus requires a license to run scans. Without a license the dashboard
is accessible but scanning is disabled.

To obtain a license contact: sales@elytrasecurity.com

Once you have a license file (.ela), install it via:
Configuration > License > Upload new license file

No restart is required. The daemon reloads the license immediately.

---

## Superadmin Setup

The install script creates an operator account automatically.
To activate the superadmin account, SSH into the appliance after
the service is running and contact support@elytrasecurity.com
for the activation procedure.

---

## Support

- General: support@elytrasecurity.com
- Security issues: see SECURITY.md

---

## Version History

| Version | Date       | Notes               |
|---------|------------|---------------------|
| 2026.01 | 2026-05-09 | Initial GA release  |
