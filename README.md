# Rust Bindings for libbladeRF

## Overview

This project provides Rust bindings for the `libbladeRF` library, enabling Rust developers to interface with bladeRF hardware. The bindings are generated using `bindgen` and allow for direct use of `libbladeRF` functions within Rust programs. This README outlines how to set up and use these bindings.

## Prerequisites

Before using these bindings, ensure that you have the following installed:
- Rust toolchain (latest stable version recommended)
- `libbladeRF` library installed on your system (refer to the host build instructions)

## Structure

- `Cargo.toml`: Project configuration and dependencies.
- `build.rs`: Build script for generating Rust bindings using `bindgen`.
- `wrapper.h`: A header file that includes the `libbladeRF` shared library.
- `src/lib.rs`: The Rust library file that includes the generated bindings.
- `src/main.rs`: An example Rust application.

## Setup

The following will generate the Rust bindings using `bindgen` and compile the project.

```bash
cd hello_libbladeRF    # Navigate to one of the Rust crates
cargo build             # Navigate to the project directory and build the project using Cargo
cargo test              # Run tests (including the ones in lib.rs)
cargo run               # Runs the example application in src/main.rs
```

### Accessing `libbladeRF` Functions

You can access `libbladeRF` functions via the bindings in `src/lib.rs`. The `build.rs` script automatically generates these bindings.

# License #

This code is distributed under an [MIT License](LICENSE).

