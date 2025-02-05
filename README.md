# High-Quality mpv Configuration

This repository contains a high-quality `mpv.conf` configuration file for the mpv media player, optimized for excellent video and audio playback. The configuration is designed to enhance your viewing experience, especially when watching high-resolution content.

## Features

* **Advanced Video Scaling**: Utilizes high-quality scalers like `ewa_lanczos` for upscaling and `catmull_rom` for downscaling.
* **Hardware Decoding**: Leverages NVIDIA's `nvdec-copy` for efficient hardware-accelerated decoding.
* **Shader Enhancements**:
   * **FSRCNNX_x2_16-0-4-1.glsl**: Neural network upscaling for improved detail.
   * **KrigBilateral.glsl**: Enhanced chroma scaling to reduce artifacts.
* **Debanding and Dithering**: Configured to reduce visual artifacts and improve color gradients.
* **Motion Interpolation**: Enabled for smoother motion rendering.
* **HDR Tone Mapping**: Uses `bt.2390` tone mapping for accurate HDR to SDR conversion.
* **Customized Subtitles and OSD**: Personalized subtitle styling and on-screen display settings.
* **Streaming Optimization**: Settings optimized for high-quality streaming content.

## Requirements

* **mpv Media Player**: Ensure you have the latest version installed for full compatibility.
* **NVIDIA GPU**: Recommended for hardware decoding and performance (e.g., GTX 1650 Ti or better).
* **Shaders**: Download the required shader files and place them in the designated folder:
   * `FSRCNNX_x2_16-0-4-1.glsl`
   * `KrigBilateral.glsl`

## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/muhalwan/MPV-Config.git
   ```

2. **Copy Configuration File**:
   Place the `mpv.conf` file into your mpv configuration directory:
   * **Linux/macOS**: `~/.config/mpv/`
   * **Windows**: `%APPDATA%\mpv\`

3. **Place Shader Files**:
   Create a `shaders` folder inside the mpv configuration directory if it doesn't exist and place the shader files there:
   * **Linux/macOS**: `~/.config/mpv/shaders/`
   * **Windows**: `%APPDATA%\mpv\shaders\`

4. **Verify File Paths**:
   Ensure that the file paths in `mpv.conf` match the location of your shader files.

## Usage

Launch mpv as you normally would, and it will automatically use the provided configuration:

```bash
mpv /path/to/your/video_file.mkv
```

## Notes

* **Performance Considerations**:
   * This configuration prioritizes quality and may be demanding on your system.
   * If you experience high CPU/GPU usage, consider adjusting settings:
      * Reduce `deband-iterations` in the debanding section.
      * Disable motion interpolation by setting `interpolation=no`.
* **Compatibility**:
   * Ensure your GPU drivers are up to date for the best performance.
   * Some settings may require the latest version of mpv.
* **Customization**:
   * Feel free to adjust the configuration to suit your preferences and system capabilities.

## Configuration Highlights

### Graphics Engine
* **API**: Vulkan for modern GPUs.
* **Video Output**: `gpu-next` enables advanced rendering features.
* **Hardware Decoding**: `nvdec-copy` utilizes NVIDIA hardware decoding.

### Video Processing
* **Scaling Algorithms**:
   * **Upscaling**: `ewa_lanczos` for high-quality image enlargement.
   * **Downscaling**: `catmull_rom` for smooth image reduction.
* **Shaders**:
   * **FSRCNNX**: Enhances upscaling using neural networks.
   * **KrigBilateral**: Improves chroma scaling and reduces color bleeding.
* **Debanding**:
   * Removes banding artifacts with multiple iterations and controlled parameters.
* **Motion Interpolation**:
   * Provides smoother playback for videos with lower frame rates.

### HDR and Tone Mapping
* **Tone Mapping Algorithm**: `bt.2390` for accurate HDR to SDR conversion.
* **Dynamic Peak Computation**: Adjusts brightness dynamically based on content.

### Subtitles and On-Screen Display
* Customized fonts and styling for better readability.
* Positioning and scaling optimized for various screen sizes.

## Credits
* FSRCNNX shader by **igv**
* KrigBilateral shader by **igv**
* Original configuration structure by **Tsubajashi**
