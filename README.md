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
