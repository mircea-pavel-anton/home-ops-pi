# LDS home k8s cluster

<div align="center">

[![Discord](https://img.shields.io/discord/673534664354430999?color=7289da&label=DISCORD&style=for-the-badge&logo=discord)](https://discord.gg/k8s-at-home 'k8s at home Discord Community')
[![GitHub stars](https://img.shields.io/github/stars/lildrunkensmurf/k3s-home-cluster?color=green&style=for-the-badge)](https://github.com/lildrunkensmurf/k3s-home-cluster/stargazers 'This repo star count')
[![GitHub last commit](https://img.shields.io/github/last-commit/lildrunkensmurf/k3s-home-cluster?color=purple&style=for-the-badge)](https://github.com/LilDrunkenSmurf/k3s-home-cluster/commits/main 'Commit History')\
[![Release](https://img.shields.io/github/v/release/lildrunkensmurf/k3s-home-cluster?style=for-the-badge)](https://github.com/lildrunkensmurf/k3s-home-cluster/releases 'Repo releases')

</div>

## Overview

This repository is for my home K3s cluster, which is a lightweight version of K8s. It's based off of the k8s-at-home [flux template](https://github.com/onedr0p/flux-cluster-template).
It's supported by [k3s](https://k3s.io) cluster with [Ansible](https://www.ansible.com) backed by [Flux](https://toolkit.fluxcd.io/) and [SOPS](https://toolkit.fluxcd.io/guides/mozilla-sops/).

The purpose here is to learn k8s, while practicing Gitops.

## 🔧 Hardware

| Name        | Device         | CPU            | OS Disk   | Data Disk   | RAM   | OS       | Purpose             |
|-------------|----------------|----------------|-----------|-------------|-------|----------|---------------------|
| NAS         | HP z820        | 2x E5-2680     | 32GB USB  | ZFS 36TB    | 128GB | Unraid   | NAS/NFS/Backup      |
| Eula        | Dell 7080mff   | i7-10700T      | 480GB SSD | 1.25TB NVME | 64GB  | Ubuntu   | k8s Worker          |
| Ayaka       | Dell 7080mff   | i5-10500T      | 480GB SSD | 1.25TB NVME | 64GB  | Ubuntu   | k8s Worker          |
| Ganyu       | Dell 7050mff   | i5-7500T       | 240GB SSD | 1TB NVME    | 64GB  | Ubuntu   | k8s Worker          |
| HuTao       | Lenovo m910q   | i5-7500T       | 480GB SSD | 1TB NVME    | 64GB  | Ubuntu   | k8s Worker          |
| Yelan       | Beelink Mini-s | Celetron N5095 | 256GB SSD | 1TB M.2 SSD | 16GB  | Ubuntu   | k8s Worker          |
| Raiden      | Raspberry Pi4  | Cortex A72     | 240GB SSD | -           | 8GB   | Ubuntu   | k8s control-plane   |
| Zhongli     | Raspberry Pi4  | Cortex A72     | 240GB SSD | -           | 4GB   | Ubuntu   | k8s control-plane   |
| Nahida      | Raspberry Pi4  | Cortex A72     | 240GB SSD | -           | 4GB   | Ubuntu   | k8s control-plane   |
| Amber       | Raspberry Pi3B | Cortex A53     | 120GB mSD | -           | 1GB   | Raspbian | DNS/VPN/MeshCentral |
| Nas UPS     | Smart-UPS 750  | -              | -         | -           | -     | -        | UPS - NAS           |
| Network UPS | Back-UPS 600   | -              | -         | -           | -     | -        | UPS - K8s + Network |
| UDMB        | Unifi UDM Base | Cortex A57     | -         | -           | 2GB   | Unifi OS | Router              |
| DumbSwitch  | Netgear GS324P | -              | -         | -           | -     | -        | 24 Port PoE Switch  |

Total CPU: 50 threads (workers)

Total RAM: 272GB (workers)

## 🤝 Thanks

Big shout out to original flux template, and the k8s-at-home discord.

[@whazor](https://github.com/whazor) created [this website](https://nanne.dev/k8s-at-home-search/) as a creative way to search Helm Releases across GitHub. You may use it as a means to get ideas on how to configure an applications' Helm values.
