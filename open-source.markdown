---
layout: page
title: Open Source
permalink: /open-source/
---

A collection of my contributions to open-source projects and tools I build in the open.

## Mesa (zink driver)

Mesa is the open-source implementation of OpenGL, Vulkan, and other graphics API specifications, powering GPU drivers across Linux, including AMD, Intel, and virtual/translation drivers like zink (Vulkan-based OpenGL). I contributed to zink, renaming Vulkan API calls and structures from their extension-suffixed names (EXT/KHR) to their promoted, unsuffixed core names following Vulkan 1.4's promotion of VK_EXT_line_rasterization, verifying each rename against Mesa's own extension registry to correctly distinguish promoted symbols from those in a separate, non-promoted extension (VK_EXT_extended_dynamic_state3) that needed to keep their suffix.

**Stack:** C, Vulkan

[View MR →](https://gitlab.freedesktop.org/mesa/mesa/-/merge_requests/44612)

<!-- -->

## Google Filament

[Filament](https://github.com/google/filament) is Google's real-time physically-based rendering engine for Android, iOS, Windows, Linux, macOS, and WebGL2, with 20k+ stars. I contributed `to_string()` conversions for public enums across the codebase, improving debuggability and developer experience.

**Stack:** C++

[View on GitHub →](https://github.com/google/filament)

<!-- -->

*More open-source work coming soon. This section will grow as I contribute to more graphics and rendering projects.*
