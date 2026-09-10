---
layout: page
title: Projects
permalink: /projects/
---

## wgfx

A C++ real-time renderer with dual **OpenGL** and **Vulkan** backends.

The OpenGL renderer is the full-featured backend and includes:

- PBR scene rendering with image-based lighting
- Cascaded shadow maps for directional lights, perspective shadow maps for spotlights, and cubemap shadow maps for point lights
- HDR rendering with exposure tone mapping and Gaussian-blurred bloom
- Runtime-selectable 8x MSAA
- A dockable Dear ImGui panel for toggling VSync, MSAA, bloom, exposure, and bloom threshold

The Vulkan backend right now only provides device initialization, swap chain management, render passes, graphics pipelines, command buffers, and synchronized presentation.

![wgfx screenshot](https://raw.githubusercontent.com/husseinhafez1/wgfx/main/images/bloom.png)
> Sponza scene rendered with PBR lighting and HDR bloom

![wgfx screenshot](https://raw.githubusercontent.com/husseinhafez1/wgfx/main/images/msaa.png)
> 8x MSAA enabled

**Stack:** C++, OpenGL, Vulkan, GLFW, GLAD, GLM, Dear ImGui

[View on GitHub →](https://github.com/husseinhafez1/wgfx)

<!-- -->

## 3D Gaussian Splatting Renderer (3dgs-rs)

A real-time 3D Gaussian Splatting renderer written in Rust. It uses [wgpu](https://github.com/gfx-rs/wgpu) for rendering and [rust-gpu](https://github.com/Rust-GPU/rust-gpu) to write the GPU shaders in pure Rust. The current implementation handles around **200k Gaussian splats** in real time.

Splats are sorted back-to-front on the CPU. The next step is moving the sorting to the GPU with compute shaders to avoid per-frame CPU/GPU synchronization.

![3DGS screenshot](https://raw.githubusercontent.com/husseinhafez1/3dgs-rs/main/images/tomatoes.png)
> Gaussian splatting render of tomatoes

**Stack:** Rust, wgpu, rust-gpu

[View on GitHub →](https://github.com/husseinhafez1/3dgs-rs)

<!-- -->

## CUDA Edge Detection

A Sobel edge detector implemented in CUDA, validated bit-for-bit against a CPU reference before benchmarking.

**Stack:** C++, CUDA

[View on GitHub →](https://github.com/husseinhafez1/CUDA-Edge-Detection)

<!-- -->

## Software Rasterizer

A software rasterizer built from scratch in Rust, using the CPU only.

Key features:

- MVP and viewport transformation pipeline
- Barycentric coordinate rasterization with a z-buffer for depth
- Back-face culling
- TGA texture sampling from interpolated UVs
- Look-at camera and OBJ model loader

**Stack:** Rust

[View on GitHub →](https://github.com/husseinhafez1/rustraster)
