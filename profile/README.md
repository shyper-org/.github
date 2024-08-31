# Rust-Shyper

A Reliable Embedded Hypervisor Supporting VM Migration and Hypervisor Live-Update

## Introduction

**Rust-Shyper** is an embedded type-1 hypervisor built with Rust, which has both high performance and high reliability. Designed for embedded platform, Rust-Shyper provides a small TCB and ensures isolation between different VMs. Furthermore, it can offer differentiated services for VMs such that the real-time performance of critical VMs are guaranteed. We have proposed low overhead VM migration and hypervisor live-update mechanisms to enable Rust-Shyper to tolerate hardware faults at runtime and dynamically fix hypervisor bugs.

## Supported Platforms

The list of supported (and work in progress) platforms is presented below:

**aarch64**
- [x] NVIDIA Jetson TX2
- [x] Raspberry Pi 4 Model B
- [x] QEMU (note that VM migration and Hypervisor Live-update is not supported on QEMU)
- [x] Firefly ROC-RK3588S-PC (note that VM migration and Hypervisor Live-update is not supported on ROC-RK3588S-PC)
- [x] QEMU (for RISCV64)

## How to Build

Tools for compiling: please install:
- [Rust](https://www.rust-lang.org/tools/install)
- [aarch64-none-elf toolchain](https://developer.arm.com/downloads/-/gnu-a)
- [cargo-binutils](https://crates.io/crates/cargo-binutils/0.3.6) (optional)
- QEMU, or qemu-system-aarch64 (optional)
- u-boot-tools (optional)

Simply run `make`

```bash
make <platform>
```

For example, `make tx2` is to build Rust-Shyper for TX2.

Note that please edit the MVM profile in src/config/\<plat\>_def.rs according to your requirements.

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
