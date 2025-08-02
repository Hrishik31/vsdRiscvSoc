# vsdRiscvSoc
# 🚀 RISC-V Toolchain Setup on Rocky Linux using WSL

![RISC-V](https://img.shields.io/badge/Architecture-RISC--V-blue.svg)
![Platform](https://img.shields.io/badge/Platform-Rocky%20Linux-10B981.svg)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen.svg)

This guide walks you through the installation and verification of a RISC-V development environment on **Rocky Linux** via WSL. Follow the steps sequentially for a successful setup.

---

## 🧾 Table of Contents

- [Step 1: Install Development Tools](#step-1-install-development-tools)
- [Step 2: Create Workspace](#step-2-create-workspace)
- [Step 3: Download Prebuilt RISC-V GCC Toolchain](#step-3-download-prebuilt-risc-v-gcc-toolchain)
- [Step 4: Add Toolchain to PATH](#step-4-add-toolchain-to-path)
- [Step 5: Install Device Tree Compiler](#step-5-install-device-tree-compiler)
- [Step 6: Build and Install Spike (ISA Simulator)](#step-6-build-and-install-spike-isa-simulator)
- [Step 7: Build and Install RISC-V Proxy Kernel](#step-7-build-and-install-risc-v-proxy-kernel)
- [Step 8: Fix PATH for Cross Compiler Binaries](#step-8-fix-path-for-cross-compiler-binaries)
- [Step 9: Toolchain Verification Checks](#step-9-toolchain-verification-checks)
- [Step 10: Run Unique C Test Program](#step-10-run-unique-c-test-program)

---

## ✅ Step 1: Install Development Tools

Install essential tools and libraries using `dnf`.

```bash
sudo dnf groupinstall "Development Tools" -y
sudo dnf install git vim autoconf automake curl \
gmp-devel mpfr-devel libmpc-devel gawk bison flex \
texinfo gperf libtool patchutils bc zlib-devel expat-devel \
gtkwave -y
