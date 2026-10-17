# 🦉 OMySqlX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OScan-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OMySqlX** — MySQL / MariaDB Configuration Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Offline MySQL / MariaDB configuration auditor (CIS / CWE / ATT&CK)

---

## ✨ Features

- Faithful my.cnf / my.ini option-file parser ([group] scoping, !include / !includedir chains, loose- / skip- / disable- / enable- prefixes, dash-underscore equivalence, quoting & escapes, last-wins semantics, per-option file:line origin)
- Server-group model — [mysqld] [server] [mariadb]
- Network exposure — bind-address, skip-networking, mysqlx / admin interfaces, skip-name-resolve
- TLS review — ssl / have_ssl, require_secure_transport, certificate material, tls_version, cipher strength
- Authentication — mysql_native_password defaults, old_passwords, secure_auth, skip-grant-tables, validate_password / simple_password_check / cracklib
- Dangerous features — local_infile, symbolic-links, secure_file_priv, allow-suspicious-udfs, plugin_dir
- Logging & forensics — log_bin, general_log secrets, log-raw, error log, audit plugins, binlog encryption
- Replication & Galera — SSL on channels, plaintext master-password / wsrep_sst_auth, info repositories
- File-permission audit — option files, ~/.my.cnf, datadir, TLS keys, log files (--root aware)
- CIS MySQL / MariaDB Benchmark + CWE + MITRE ATT&CK
- Export TXT / Markdown / JSON / CSV / SARIF 2.1.0
- Self-test --demo, CI gates --fail-on / --min-severity

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OMySqlX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
