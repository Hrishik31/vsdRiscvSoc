# vsdRiscvSoc
# ⚙️ RISC-V Toolchain Setup & Validation on Rocky Linux using WSL

![Architecture](https://img.shields.io/badge/Architecture-RISC--V-blue.svg)
![Toolchain](https://img.shields.io/badge/Toolchain-GCC--RISC--V-purple.svg)
![Platform](https://img.shields.io/badge/Platform-Rocky%20Linux-10B981.svg)
![Status](https://img.shields.io/badge/Setup-Passed-brightgreen.svg)

A complete step-by-step guide to setting up the RISC-V development toolchain on **Rocky Linux (via WSL)**. This documentation includes detailed solutions to common issues encountered during installation.

---

## 🗂️ Contents

- [System Requirements](#system-requirements)
- [Initial Setup](#initial-setup)
- [RISC-V Toolchain Installation](#risc-v-toolchain-installation)
- [Simulator & Proxy Kernel Build](#simulator--proxy-kernel-build)
- [Icarus Verilog & GTKWave](#icarus-verilog--gtkwave)
- [Validation Tests](#validation-tests)
- [Troubleshooting Summary](#troubleshooting-summary)
- [Directory Overview](#directory-overview)

---

## 🧰 System Requirements

- **Operating System**: Rocky Linux (64-bit, WSL or native)
- **RAM**: Minimum 4 GB (8 GB recommended)
- **Storage**: ~30 GB free space
- **CPU**: 2 cores or more
- **Privileges**: `sudo` access required

---

## 🚀 Initial Setup

Install essential development libraries:

```bash
sudo dnf groupinstall "Development Tools"
sudo dnf install git vim wget curl bison flex texinfo ncurses-devel \
mpfr-devel gmp-devel libmpc-devel zlib-devel expat-devel dtc \
gtkwave make autoconf automake libtool patch bc
