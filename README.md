# 📦 Agam SDK & Toolchain Target Packs

> Part of the [agam-lang](https://github.com/agam-lang) organization.  
> Official pre-built target packs, LLVM sysroot distributions, cross-compilation toolchains, and standalone native binary bundles for the **Agam** platform.

---

## 🎯 Target Matrix & Platform Tiers

Agam provides production-grade pre-built SDK toolchain bundles:

| Platform / Target Triple | Tier | Backend Support | JIT Engine | Hardware Features |
| :--- | :--- | :--- | :--- | :--- |
| **`x86_64-pc-windows-msvc`** | **Tier 1** | Native LLVM + C11 | Cranelift JIT | AVX2, AVX-512, Direct3D |
| **`x86_64-unknown-linux-gnu`** | **Tier 1** | Native LLVM + C11 | Cranelift JIT | AVX-512, Vulkan, io_uring |
| **`aarch64-unknown-linux-gnu`** | **Tier 1** | Native LLVM + C11 | Cranelift JIT | ARM Neon, SVE/SVE2 |
| **`aarch64-linux-android`** | **Tier 2** | Native LLVM | Cranelift JIT | Android NDK 26+, Vulkan |
| **`wasm32-unknown-emscripten`** | **Tier 2** | WASM / WebAssembly | Browser VM | SIMD128, SharedArrayBuffer |

---

## 🛠️ SDK Bundle Contents

Each release artifact contains:
1. **`bin/agamc`**: Standalone native Agam compiler executable.
2. **`lib/libagam_runtime.a`**: Core runtime library (ARC memory manager, SIMD primitives, task scheduler).
3. **`include/`**: C ABI headers for zero-overhead foreign function interface (`agam_runtime.h`).
4. **`std/`**: Pre-compiled standard library interfaces (`std::tensor`, `std::gpu`, `std::ml`).

---

## 📜 License

Dual-licensed under [MIT](LICENSE-MIT) and [Apache 2.0](LICENSE-APACHE).
