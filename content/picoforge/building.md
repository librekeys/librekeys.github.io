---
title: Building
---

This document will help you building and running the PicoForge app from its source code.  
Refer to the [Installation](../installation/) section if you would rather install the application from pre-built binaries.


<!--more-->

{{< toc >}}

## Prerequisites

Before building, ensure you have the following requirements installed:

- **[Rust](https://www.rust-lang.org/)** - System programming language (1.90+)
- **PC/SC Middleware**:
  - Linux: `pcscd` (usually pre-installed)
  - macOS: Built-in
  - Windows: Built-in

## Building from Source

### 1. Build the Application

#### Development Build

```bash
cargo run
```

#### Production Build

```bash
cargo build --release
```

The compiled binary will be available in `target/release/picoforge` (Linux/macOS) or `target/release/picoforge.exe` (Windows).

## Building and Development with Nix

[Nix](https://nixos.org/) provides developers with a complete and consistent development environment.

You can use Nix to build and develop picoforge painlessly.

### 1. Install Nix

Follow the [Installation Guide](https://nixos.org/download/#download-nix) and [NixOS Wiki](https://wiki.nixos.org/wiki/Flakes#Setup) to install Nix and enable Flakes.

### 2. Build & Run

#### a. with Flakes

You can build and run PicoForge with a single command:

```bash
nix run github:librekeys/picoforge
```

Or simply build it and link to the current directory:

```bash
nix build github:librekeys/picoforge
```

> [!TIP]
> You can use our binary cache to save build time by allowing Nix to set extra-substitutes.

#### b. without Flakes

Download the package definition:

```bash
curl -LO https://raw.githubusercontent.com/librekeys/picoforge/main/package.nix
```

Run the following command in the directory containing `package.nix`:

```bash
nix-build -E 'with import <nixpkgs> {}; callPackage ./package.nix { }'
```

The compiled binary will be available at: `result/bin/picoforge`

### 3. Develop

You can enter a developement environement with all the required dependencies.

#### a. with Flakes

```bash
nix develop github:librekeys/picoforge
```

#### b. without Flakes

You can use the `shell.nix` file that is at the root of the repository by running:

```bash
nix-shell
```

Then you can build from source and run the application with:

```bash
cargo run
```


