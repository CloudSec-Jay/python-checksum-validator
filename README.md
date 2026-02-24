# 🧮 Python Checksum Validator

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Hash](https://img.shields.io/badge/Security-SHA256_%7C_MD5-black?style=for-the-badge)

**Automated Data Integrity & Secure Supply Chain Verification**

</div>

---

## 🎯 Overview

In modern DevOps and Security workflows, **data integrity is paramount.** Downloading binary assets, ISOs, or software packages from untrusted or public mirrors introduces significant supply chain risk. This utility provides a **lightweight, repeatable methodology** for verifying the integrity of large-scale assets, ensuring that what you download matches the original source's cryptographic signature.

## 🎯 Research Goals

- **Risk Mitigation:** Detects bit-rot and malicious tampering in critical infrastructure assets (ISO, AMI, .deb) before deployment.
- **Operational Efficiency:** Automates the manual task of checksum comparison, reducing human error in security validation.
- **Supply Chain Security:** Provides a foundational tool for verifying third-party software as part of a "Zero-Trust" ingestion pipeline.

## 🏗️ Architecture

```text
       ┌───────────────────────────┐
       │     DOWNLOADED ASSET      │
       │ (ISO, Binary, Script)     │
       └─────────────┬─────────────┘
                     │ (File Stream)
       ┌─────────────┴─────────────┐
       │  SHA256 / MD5 ALGORITHM    │
       │ (Cryptographic Hashing)   │
       └─────────────┬─────────────┘
                     │ (Computed Hash)
       ┌─────────────┴─────────────┐
       │    EXPECTED CHECKSUM      │
       │ (Official Source String)  │
       └─────────────┬─────────────┘
                     │ (Match/Fail)
       ┌─────────────┴─────────────┐
       │      INTEGRITY VERIFIED    │
       │ (Deployment Green-Light)  │
       └───────────────────────────┘
```

---

## 🚀 Quick Start

### Installation
```bash
git clone https://github.com/CloudSec-Jay/python-checksum-validator.git
cd python-checksum-validator
```

### Usage
```bash
python3 checksum.py --file <path-to-file> --checksum <expected-checksum-string> --algo sha256
```

---

## 🛡️ Skills Demonstrated

- **Python Development:** Standard library usage for cryptographic hashing (`hashlib`, `argparse`).
- **Data Integrity:** Understanding of MD5, SHA1, and SHA256 collision risks vs. performance.
- **Secure Supply Chain:** Implementing automated verification in delivery pipelines via exit codes.

---

## 🛠️ Tooling & Engineering Workflow

- **Scripting:** Python.
- **AI Tooling:** Gemini CLI is utilized as a technical partner for research acceleration, Python script scaffolding, and exploring secure supply chain methodologies.
