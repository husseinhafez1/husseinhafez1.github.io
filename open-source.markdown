---
layout: page
title: Open Source
permalink: /open-source/
---

A collection of my contributions to open-source projects and tools I build in the open.

## Mesa (Zink)

[Mesa](https://www.mesa3d.org/) is the open-source implementation of OpenGL and Vulkan drivers on Linux. I contributed to [Zink](https://docs.mesa3d.org/drivers/zink.html), the OpenGL-over-Vulkan driver, by migrating line rasterization code from the `EXT`/`KHR`-suffixed API to the promoted Vulkan 1.4 core names (`VK_EXT_line_rasterization` → `VK_KHR_line_rasterization` → core).

This covered `VkLineRasterizationMode`, `VkPhysicalDeviceLineRasterizationFeatures`, `VkPipelineRasterizationLineStateCreateInfo`, the `VK_LINE_RASTERIZATION_MODE_*` modes, `VK_DYNAMIC_STATE_LINE_STIPPLE`, and related structure types, while deliberately leaving `CmdSetLineRasterizationModeEXT` / `CmdSetLineStippleEnableEXT` on their `EXT` names since those come from `VK_EXT_extended_dynamic_state3`.

**Stack:** C, Vulkan, Zink

[View merge request →](https://gitlab.freedesktop.org/mesa/mesa/-/merge_requests/44612)

<!-- -->

## Google Filament

[Filament](https://github.com/google/filament) is Google's real-time physically-based rendering engine for Android, iOS, Windows, Linux, macOS, and WebGL2, with 20k+ stars. I contributed `to_string()` conversions for public enums across the codebase, improving debuggability and developer experience.

**Stack:** C++

[View on GitHub →](https://github.com/google/filament)

<!-- -->

*More open-source work coming soon. This section will grow as I contribute to more graphics and rendering projects.*
