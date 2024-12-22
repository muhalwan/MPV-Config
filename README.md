# Modern MPV Configuration

A modern, high-quality MPV configuration focused on quality video playback with optimized settings for subtitle handling, video processing, and HDR content.

## Features

- 🎮 Vulkan GPU API support
- 🎥 High-quality video upscaling and processing
- 📝 Clean, Netflix-style subtitles
- 🎨 HDR/tone-mapping support
- 🖼️ Advanced motion interpolation
- 🔊 Enhanced audio settings
- 📸 High-quality screenshot configuration

## Requirements

### Base Requirements
- MPV (latest version recommended)
- Vulkan-capable GPU
- Modern Linux distribution (Arch Linux recommended)

### Required Shaders
Place these shaders in `~/.config/mpv/shaders/`:
- FSRCNNX_x2_16-0-4-1.glsl
- SSIM_Downscaler.glsl
- KrigBilateral.glsl

### Required Fonts
- Arial (or your preferred sans-serif font)
- Inter Tight Medium (for OSD)

## Installation

1. Clone this repository:
```bash
git clone https://github.com/YOUR_USERNAME/mpv-config.git ~/.config/mpv
```

2. Create required directories:
```bash
mkdir -p ~/.config/mpv/shaders
```

3. Download required shaders:
```bash
cd ~/.config/mpv/shaders
# Download shaders from their respective sources
```

## Configuration Structure

The configuration is organized into several sections:

- Graphics Engine
- Playback Behavior
- Screenshots
- On-Screen Display
- Subtitle Configuration
- Audio Settings
- Video Processing
- Streaming & Protocols

## Screenshot Location

Screenshots are saved to: `[video_directory]/Screens/`
Format: PNG with metadata and high bit depth

## Subtitle Preferences

- Font: Arial
- Size: 45
- Style: Clean, Netflix-like appearance with subtle shadow
- No background or outline
- Supports multiple subtitle paths

## Performance Notes

This configuration is optimized for modern hardware with a focus on quality over performance. If you experience playback issues:

1. Remove or comment out high-quality shaders
2. Disable interpolation
3. Switch from Vulkan to OpenGL if necessary

## Customization

To customize settings:

1. Create a `script-opts` directory for script configurations
2. Modify values in mpv.conf as needed
3. Create an `input.conf` for custom keybindings

### Debug Information

For debugging, run:
```bash
mpv --msg-level=all=debug [filename]
```

## Credits

- FSRCNNX shader by igv
- SSIM downscaler by igv
- KrigBilateral shader by igv
- Original configuration structure by Tsubajashi
