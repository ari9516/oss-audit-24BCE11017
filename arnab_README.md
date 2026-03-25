# OSS Audit — LibreOffice
**Student Name:** Arnab Kumar  
**Registration Number:** 24BCE11017  
**Course:** CSE0002 — Open Source Software | VIT Bhopal University  
**Software Audited:** LibreOffice Office Suite (MPL 2.0 / LGPLv3+)  
**Repository:** `oss-audit-24BCE11017`

---

## About This Project

This repository contains the five shell scripts for the Open Source Software Capstone Project — *The Open Source Audit*. The project audits **LibreOffice**, examining its origin story (community fork from OpenOffice.org in 2010 when Oracle acquired Sun Microsystems), its hybrid MPL 2.0 / LGPLv3+ license, philosophy, Linux footprint, FOSS ecosystem, and a comparison with proprietary alternatives (Microsoft Office and Google Workspace).

---

## Repository Contents

| File | Description |
|------|-------------|
| `script1_system_identity.sh` | Displays system info: LibreOffice version, distro, kernel, uptime, user, and MPL 2.0 / LGPLv3+ license details |
| `script2_package_inspector.sh` | Checks if a FOSS package is installed, shows version/metadata, and prints a philosophy note (case statement) |
| `script3_disk_permission_auditor.sh` | Audits system directories and LibreOffice-specific paths: permissions, ownership, and disk usage using a for loop |
| `script4_log_analyzer.sh` | Reads a log file line by line, counts keyword matches, and displays the last 5 matches |
| `script5_manifesto_generator.sh` | Interactively generates and saves a personalised open-source philosophy statement |
| `README.md` | This file |

The project report PDF is submitted separately via the VITyarthi portal.

---

## Environment Requirements

- **OS:** Ubuntu 22.04 LTS or any Debian-based Linux
- **Shell:** Bash (version 4.0+)
- **Dependencies:** `libreoffice`, `uname`, `whoami`, `uptime`, `dpkg`, `apt-cache`, `ls`, `du`, `grep`, `awk`, `cut`, `date` — install LibreOffice with `sudo apt install libreoffice`
- **Permissions:** Script 4 may require `sudo` to read `/var/log/syslog`

---

## Setup Instructions

### Step 1 — Clone the repository
```bash
git clone https://github.com/[your-github-username]/oss-audit-24BCE11017.git
cd oss-audit-24BCE11017
```

### Step 2 — Install LibreOffice (if not already installed)
```bash
sudo apt update && sudo apt install libreoffice
libreoffice --version    # Confirm installation
```

### Step 3 — Make all scripts executable
```bash
chmod +x *.sh
```

---

## Running Each Script

### Script 1 — System Identity Report
Displays system info and LibreOffice license details.
```bash
./script1_system_identity.sh
```
**Expected output:** LibreOffice version, distribution name, kernel, uptime, user info, date/time, and MPL 2.0 / LGPLv3+ license statement.

---

### Script 2 — FOSS Package Inspector
Checks if a package is installed and prints a philosophy note.
```bash
# Inspect libreoffice (default)
./script2_package_inspector.sh

# Inspect specific LibreOffice components
./script2_package_inspector.sh libreoffice-writer
./script2_package_inspector.sh libreoffice-calc
./script2_package_inspector.sh libreoffice-impress

# Inspect other packages
./script2_package_inspector.sh python3
./script2_package_inspector.sh git
```
**Expected output:** Package install status, version, and a philosophy note about the package.

---

### Script 3 — Disk and Permission Auditor
Audits system directories and LibreOffice-specific installation paths.
```bash
./script3_disk_permission_auditor.sh
```
**Expected output:** Formatted table of directories with permissions, owner, group, and size. Also checks `/usr/bin/libreoffice`, `/usr/lib/libreoffice`, `/usr/lib/libreoffice/program`, `/usr/share/libreoffice`, and `~/.config/libreoffice`.

---

### Script 4 — Log File Analyzer
Reads a log file and counts keyword matches.
```bash
# Analyse syslog for 'libreoffice' entries (default)
sudo ./script4_log_analyzer.sh /var/log/syslog libreoffice

# Search for LibreOffice Snap updates
sudo ./script4_log_analyzer.sh /var/log/syslog snap

# Search for document conversion events
sudo ./script4_log_analyzer.sh /var/log/syslog convert

# Search for ODF-related events
sudo ./script4_log_analyzer.sh /var/log/syslog odf
```
**Expected output:** Match count and the last 5 matching lines.

> **Note:** May require sudo or `adm` group membership: `sudo usermod -aG adm $USER` (then log out and back in).

---

### Script 5 — Open Source Manifesto Generator
Interactive — asks three questions and saves a personalised manifesto.
```bash
./script5_manifesto_generator.sh
```
**Follow the prompts:**
1. Enter a tool you use every day (e.g., `LibreOffice`, `bash`, `git`)
2. Enter one word for what document freedom means (e.g., `sovereignty`, `ownership`)
3. Enter something you would build and share (e.g., `a college management system`)

**Expected output:** A manifesto printed to the terminal and saved as `manifesto_[yourusername].txt`.

---

## Troubleshooting

| Issue | Solution |
|-------|----------|
| `Permission denied` on script | Run `chmod +x scriptname.sh` |
| `libreoffice: command not found` | Install with `sudo apt install libreoffice` |
| Script 1 shows "LibreOffice not found" | LibreOffice may be installed as Snap — try `snap run libreoffice --version` |
| LibreOffice crashes on launch | Reset user profile: `mv ~/.config/libreoffice ~/.config/libreoffice.bak` |
| Log file not found (Script 4) | Script auto-detects fallbacks; or try `./script4_log_analyzer.sh /var/log/dpkg.log libreoffice` |
| `dpkg: not found` (Script 2) | Replace `dpkg -l` with `rpm -qa` for RPM-based systems |
| Script outputs nothing | Ensure Bash is your shell: `echo $SHELL` should show `/bin/bash` |

---

## License

These scripts are written for educational purposes as part of the VIT Bhopal OSS course. They may be freely used and modified.

---

*VIT Bhopal University | CSE0002 — Open Source Software | Capstone Project*
