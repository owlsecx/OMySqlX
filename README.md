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

OMySqlX is an offline MySQL / MariaDB configuration auditor. It faithfully parses my.cnf / my.ini option files (includes, group scoping, dash/underscore equivalence) to review bind address, TLS, auth plugins, local_infile, secure_file_priv, logging, replication/Galera, and file permissions. Findings map to CIS MySQL/MariaDB, CWE, and MITRE ATT&CK.

---

## ✨ Features

- Faithful my.cnf/my.ini parser with !include chains, group scoping, loose-/skip- prefixes, and last-wins semantics
- Network exposure: bind-address, skip-networking, mysqlx/admin interfaces, skip-name-resolve
- TLS and authentication: require_secure_transport, certs, tls_version, native password defaults, skip-grant-tables, password validators
- Dangerous features: local_infile, symbolic-links, secure_file_priv, suspicious UDFs, plugin_dir
- Logging/forensics and replication/Galera (SSL channels, plaintext master-password / wsrep_sst_auth)
- Permission audit for option files, ~/.my.cnf, datadir, TLS keys; multi-format export and CI gates

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OMySqlX -c /etc/mysql/my.cnf --scan
./OMySqlX --root ./fs --flavor mariadb --sarif -o mysql.sarif --fail-on high
./OMySqlX --demo --list-rules
./OMySqlX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
