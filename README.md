# pfSense ZeroTier Experimental (Standalone Edition) - 

This repository provides a hardened, standalone distribution of ZeroTier 1.12.2 for pfSense. It is specifically designed for users who experience "Signal 4" or "Signal 6" crashes and those who require an offline-installable package.

## 🏆 Credits & Acknowledgments
The WebUI used in this package is based on the excellent work by **[ChanceM](https://github.com/ChanceM/pfSense-pkg-zerotier)**. This repository adapts his cosmetic interface to a standalone, patched binary environment suited for high-stability production firewalls.

---

## 🛠 Why this exists?
Standard pfSense ZeroTier installations often break because:
1. **Instruction Set Mismatch:** Newer binaries try to use hardware acceleration that causes `Illegal Instruction` (Signal 4) on many Intel/AMD CPUs used in firewalls.
2. **Repository Drift:** pfSense updates often try to pull incompatible FreeBSD quarterly packages.
3. **WebUI Conflicts:** The UI often loses connection to the service due to IPv6 loopback mapping issues (`ffff:127.0.0.1`).

**This package solves all three.**

---

## 🚀 Installation

1. **Download** the `.pkg` package from the [Releases](../../releases) section.
2. **Upload** the file to your pfSense box (via SCP or Diagnostics > Command Prompt).
3. **Install** via the shell:
   ```bash
   pkg add pfSense-pkg-ZeroTier-Offline-1.12.2.pkg
   
4. Refresh your WebGUI. You will find the interface under VPN > ZeroTier.

