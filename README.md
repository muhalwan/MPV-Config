# MPV Configuration

High quality MPV configuration optimized for visual fidelity and smooth playback.

## Features
- High quality video upscaling with FSRCNNX shader
- Optimal chroma upscaling with KrigBilateral
- HDR/SDR tone mapping optimization
- Motion interpolation for smooth playback
- Extended subtitle support
- Efficient cache management for streaming
- Custom OSC/OSD configuration

## Requirements
- Modern GPU supporting Vulkan
- MPV shaders:
  - FSRCNNX_x2_8-0-4-1.glsl
  - KrigBilateral.glsl

## Installation
1. Place config in: `~/.config/mpv/mpv.conf`
2. Create shaders directory: `~/.config/mpv/shaders/`
3. Install required shaders in the shaders directory

## Keyboard Shortcuts
- 1/2: Adjust contrast
- 3/4: Adjust brightness
- 5/6: Adjust gamma
- 7/8: Adjust saturation
- SHIFT+BS: Reset all image adjustments
- F: Clear all filters

## Notes
- Uses hardware decoding with quality preservation
- Optimized for anime and high quality video content
- Network streaming optimized with extended cache
