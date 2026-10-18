<!-- Header -->
<p align="center">
  <img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:3b0764,100:7c3aed&height=220&section=header&text=Leff&fontSize=80&fontColor=ffffff&fontAlignY=38&animation=fadeIn&desc=Systems%20%C2%B7%20Kernel%20%C2%B7%20Virtualization%20%C2%B7%20Game%20Security&descSize=18&descAlignY=60" />
</p>

<p align="center">
  <a href="https://leffloard.wtf">
    <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=20&duration=3200&pause=900&color=C084FC&center=true&vCenter=true&width=640&lines=Dual-vendor+hypervisor+%E2%80%94+Intel+VT-x+%2B+AMD-V;EPT%2FNPT+hooking+on+a+live+Windows+kernel;Kernel+drivers+%26+Windows+internals;Game+security+%26+anti-cheat+research;ESP32+firmware%2C+BLE+%26+ESP-NOW" />
  </a>
</p>

<p align="center">
  <a href="https://leffloard.wtf"><img src="https://img.shields.io/badge/leffloard.wtf-0d1117?style=for-the-badge&logo=googlechrome&logoColor=C084FC" /></a>
  <a href="https://discord.leffloard.wtf"><img src="https://img.shields.io/badge/leffloard-0d1117?style=for-the-badge&logo=discord&logoColor=C084FC" /></a>
  <a href="https://sense.leffloard.wtf"><img src="https://img.shields.io/badge/Sense%20server-0d1117?style=for-the-badge&logo=discord&logoColor=C084FC" /></a>
  <a href="mailto:hello@leffloard.wtf"><img src="https://img.shields.io/badge/hello@leffloard.wtf-0d1117?style=for-the-badge&logo=maildotru&logoColor=C084FC" /></a>
</p>

---

### About

I've been writing code for about eight years, and most of it lives below the application layer. I build hypervisors, kernel-mode drivers and
the tooling around them, and I spend a lot of time on how games and their anti-cheats work at the memory, driver and virtualization level.
Outside of that I ship real products for clients: native apps, Discord platforms, backends and ESP32 hardware.

Most of my serious work is in private repositories, so what you see here is a curated sample.

---

### Flagship: `hv`, a dual-vendor hypervisor

A thin hypervisor written from scratch in C++ that **virtualizes an already-running Windows system** (blue-pill style). It is loaded at runtime
and moves the live OS into a guest without a reboot.

- **Intel VT-x and AMD-V (SVM)** behind one abstraction layer: VMCS/VMCB setup, per-core virtualization, VM-exit and #VMEXIT dispatch
- **Second-level address translation hooks** with EPT on Intel and NPT on AMD, which give the guest different read/write and execute views of the same page
- **External memory read/write** through a hypercall interface. It is stable under real workloads and crash-free in daily use
- **In progress:** boot-chain integration, so the hypervisor is present from early boot instead of being loaded at runtime

---

### What I work on

<table>
<tr>
<td width="50%" valign="top">

**Game security & reversing**
Anti-cheat internals, kernel ↔ user communication channels, memory introspection, DLL injection and manual mapping, and
in-game overlays with Dear ImGui (custom widgets, theming, animation, render-loop tuning).

</td>
<td width="50%" valign="top">

**Windows internals & kernel**
WDM drivers, PE loading, process/module enumeration, paging and physical memory, IRQL-aware code
and debugging in the kernel when it all goes wrong.

</td>
</tr>
<tr>
<td valign="top">

**Engines & graphics**
A game engine written from scratch: window and input loop, renderer, scene management and an asset pipeline.

</td>
<td valign="top">

**Embedded & backend**
ESP32 firmware (BLE scanning, ESP-NOW meshes, Wi-Fi CSI presence sensing) and Python services and Discord
platforms for licensing, ticketing and reseller management, deployed behind Cloudflare.

</td>
</tr>
</table>

---

### Selected projects

| Project | Description |
|---|---|
| **`hv`** · *private* | Dual-vendor (VT-x / AMD-V) blue-pill hypervisor with EPT/NPT hooks and hypercall-based memory access |
| **[cs2KernelExample](https://github.com/leffloard/cs2KernelExample)** | Counter-Strike 2 external tool driven by a kernel driver. It shows the full driver ↔ client memory read path |
| **[lightInjector](https://github.com/leffloard/lightInjector)** | `LoadLibraryExW` injector for Unreal Engine titles, kept minimal so the mechanics stay readable |
| **[MiniEngine](https://github.com/leffloard/MiniEngine)** | A game engine in C++, built from first principles |
| **Airsoft BLE radar** · *in progress* | ESP32 nodes sniff BLE advertisements and relay them over ESP-NOW to a phone that renders a live radar with friend/foe identification |
| **[JarvisCore](https://github.com/leffloard/JarvisCore)** | Voice assistant pipeline: speech in, LLM reasoning, ElevenLabs TTS out |
| **[CardTrack](https://github.com/leffloard/CardTrack)** | Native Android app in Kotlin for tracking credit card limits |
| **[discord-select-menu-ticket](https://github.com/leffloard/discord-select-menu-ticket)** | A support ticket system built on Discord select menus |

---

### Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=cpp,c,py,ts,kotlin,cmake,visualstudio,vscode,windows,linux,arduino,cloudflare,discord,git&theme=dark&perline=14" />
</p>
<p align="center">
  <img src="https://img.shields.io/badge/x86--64%20ASM-0d1117?style=flat-square&logo=intel&logoColor=C084FC" />
  <img src="https://img.shields.io/badge/WinDbg-0d1117?style=flat-square&logo=windows&logoColor=C084FC" />
  <img src="https://img.shields.io/badge/IDA%20Pro-0d1117?style=flat-square&logo=hackaday&logoColor=C084FC" />
  <img src="https://img.shields.io/badge/Ghidra-0d1117?style=flat-square&logo=ghidra&logoColor=C084FC" />
  <img src="https://img.shields.io/badge/Dear%20ImGui-0d1117?style=flat-square&logo=cplusplus&logoColor=C084FC" />
  <img src="https://img.shields.io/badge/ESP--IDF-0d1117?style=flat-square&logo=espressif&logoColor=C084FC" />
</p>

---

### Activity

<p align="center">
  <img height="170" src="https://github-readme-stats.vercel.app/api?username=leffloard&show_icons=true&count_private=true&include_all_commits=true&hide_border=true&bg_color=0d1117&title_color=c084fc&icon_color=a855f7&text_color=c9d1d9&ring_color=7c3aed" />
  <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=leffloard&layout=compact&langs_count=8&hide_border=true&bg_color=0d1117&title_color=c084fc&text_color=c9d1d9" />
</p>
<p align="center">
  <img src="https://streak-stats.demolab.com?user=leffloard&hide_border=true&background=0d1117&ring=7c3aed&fire=c084fc&currStreakLabel=c084fc&sideLabels=c9d1d9&currStreakNum=ffffff&sideNums=ffffff&dates=8b949e" />
</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/leffloard/leffloard/output/github-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/leffloard/leffloard/output/github-snake.svg" />
    <img alt="contribution snake" src="https://raw.githubusercontent.com/leffloard/leffloard/output/github-snake-dark.svg" />
  </picture>
</p>

---

### Work with me

I take on contract work in low-level tooling, native apps, Discord platforms, backends and embedded prototypes.
The fastest way to reach me is Discord at **leffloard**, or email at **hello@leffloard.wtf**.

<p align="center">
  <img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:7c3aed,50:3b0764,100:0d1117&height=120&section=footer" />
</p>
