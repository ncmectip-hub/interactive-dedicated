# Interactive-Dedicated
A bootable Linux disk image with a Minecraft Dedicated Server baked in, plus a small installer (idc) that fetches, verifies, and deploys it.

# What is this?
Interactive-Dedicated ships a self-contained, bootable .img that runs a Minecraft Java Edition dedicated server on a minimal Linux base. No distro install, no Docker, no config hell. Flash it to a disk, boot it in a VM, or deploy it to bare metal — the server comes up and starts accepting players.

It also ships idc — the Interactive-Dedicated Client — a small C program that downloads the latest base image from GitHub Releases, verifies it, decompresses it, and provisions a Minecraft server on top.

# Features
🐧 Minimal Linux base — Alpine, ~50 MB userspace, boots in seconds

☕ OpenJDK 17 — headless JRE, no GUI bloat

🎮 Minecraft Java server — Paper or Vanilla, your choice of version

📦 zstd-compressed image — 2 GB image ships as ~150 MB (14:1 ratio thanks to sparse-aware archiving)

🔐 SHA-256 verified downloads — no truncated .img ever boots

🖥️ Runs anywhere — QEMU/KVM, Proxmox, VMware, VirtualBox, or bare-metal USB

🧩 No bootloader drama — syslinux by default, GRUB optional

📡 SSH out of the box — root@<host>:2222

🛠️ idc installer — libcurl + libzstd, cross-platform (Linux + Windows via MinGW)
________________________________________________________
# Installation

```bash
curl -LO https://github.com/YOURUSER/interactive-dedicated/releases/latest/download/idc
chmod +x idc
./idc
