
```markdown
# Open Source Audit: LibreOffice

## 📋 Project Overview
This repository contains the complete capstone project for the Open Source Software course (CSE0002) at VIT Bhopal University. The project conducts a comprehensive audit of **LibreOffice Office Suite**, examining its origin story, licensing model (MPL 2.0 / LGPLv3+), philosophical foundations, Linux footprint, and its role within the Free and Open Source Software (FOSS) ecosystem.

## 🎯 Project Objectives
- Analyze the historical context and motivations behind LibreOffice's fork from OpenOffice.org
- Examine the legal and ethical implications of MPL 2.0 and LGPLv3+ licensing
- Document LibreOffice's installation, directory structure, and system integration on Linux
- Map the FOSS dependencies and community governance structure
- Compare LibreOffice against proprietary alternatives (Microsoft Office, Google Workspace)
- Demonstrate practical Linux automation skills through five shell scripts

## 📁 Repository Structure
```
oss-audit-24BCE11017/
├── script1_system_identity.sh          # System information and LibreOffice version report
├── script2_package_inspector.sh        # FOSS package verification with philosophy notes
├── script3_disk_permission_auditor.sh  # Directory permissions and disk usage audit
├── script4_log_analyzer.sh             # Log file analysis with keyword search
├── script5_manifesto_generator.sh      # Interactive open-source philosophy generator
├── README.md                           # Project documentation and setup instructions
└── OSS_Audit_ArnabKumar_24BCE11017.pdf # Complete project report (12+ pages)
```

## 🛠️ Technical Requirements
- **Operating System:** Ubuntu 22.04 LTS or any Debian-based Linux distribution
- **Shell:** Bash 4.0+
- **Software:** LibreOffice 7.x (for verification)
- **Permissions:** Sudo access for log file analysis

## 🚀 Quick Start
```bash
# Clone the repository
git clone https://github.com/[username]/oss-audit-24BCE11017.git

# Navigate to project directory
cd oss-audit-24BCE11017

# Make scripts executable
chmod +x *.sh

# Run the system identity report
./script1_system_identity.sh
```

## 📊 Scripts Summary
| Script | Purpose | Key Concepts Demonstrated |
|--------|---------|--------------------------|
| Script 1 | System Identity Report | Command substitution, variables, formatted output |
| Script 2 | FOSS Package Inspector | Conditional logic, case statements, package management |
| Script 3 | Disk Permission Auditor | For loops, file permissions, disk usage analysis |
| Script 4 | Log File Analyzer | While-read loops, arrays, file I/O, error handling |
| Script 5 | Manifesto Generator | Interactive input, file creation, string concatenation |

## 🔍 Key Findings
- **Origin:** LibreOffice emerged from a community revolt against Oracle's acquisition of Sun Microsystems in 2010
- **License:** Hybrid MPL 2.0/LGPLv3+ ensures both openness and commercial viability
- **Impact:** Used by governments worldwide (Germany, France, Brazil) for digital sovereignty
- **Comparison:** LibreOffice offers superior privacy, zero cost, and full offline capability compared to proprietary alternatives

## 👨‍🎓 Author
**Arnab Kumar**  
Registration Number: 24BCE11017  
Course: CSE0002 — Open Source Software  
Institution: VIT Bhopal University  
Slot: D11  
Date: 25 March 2026

## 📚 References
- [The Document Foundation](https://www.documentfoundation.org/)
- [LibreOffice Official Site](https://www.libreoffice.org/)
- [MPL 2.0 License](https://www.mozilla.org/en-US/MPL/2.0/)
- [GNU LGPL v3](https://www.gnu.org/licenses/lgpl-3.0.html)

## 📄 License
This project is created for educational purposes as part of the VIT Bhopal Open Source Software course. All scripts are freely available for learning and modification.

---
*"Standing on the shoulders of giants — contributing back to the open source ecosystem."*
```

