# Installation Guide
**by Kha Van**

## For Automatic1111 / Forge Webui (on Windows)

### Preface
For optimal performance, it is highly recommended to install on an **SSD** instead of an HDD.

- **Apple Silicon Users:** Refer to this [Tutorial](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Installation-on-Apple-Silicon) page.
- **AMD GPU Users:** Refer to the [AMD GPU](https://github.com/lshqqytiger/stable-diffusion-webui-amdgpu) repo.

### Download

#### For Automatic1111
1. Visit the [Release](https://github.com/AUTOMATIC1111/stable-diffusion-webui/releases/tag/v1.0.0-pre) page.
2. Download the **`sd.webui.zip`** file.

#### For Forge
1. Visit the [Release](https://github.com/lllyasviel/stable-diffusion-webui-forge/releases/tag/latest) page.
2. Download the **`webui_forge_cu121_torch21.7z`** file.

### Installation
1. **Extract the Files:**
   - Extract all contents *(2x folders and 3x files)* to a folder of your choice.
   - **Do not** place them in `OneDrive` or any other cloud drives.

2. **Run the Update Script:**
   - Execute the **`update.bat`** file.

3. **Modify Commandline Arguments (for Automatic1111 only):**
   - Adjust the [commandline arguments](#commandline-args) as described below.

4. **Download a Checkpoint:**
   - Before running the WebUI, download a **checkpoint** of your choice to avoid the automatic download of the default low-quality checkpoint.
   - If you're unsure about checkpoints, refer to the [Checkpoint Guide](../README.md#checkpoint).

5. **Launch the WebUI:**
   - Run the **`run.bat`** file.
   - On the first launch, the WebUI will download and install all necessary packages. This process may take some time.

6. **Completion:**
   - The installation is complete when a browser window opens with the WebUI loaded.

### Commandline Arguments

> These memory-related arguments are specific to Automatic1111; Forge automatically manages these settings.

1. Navigate to the `webui` folder.
2. Right-click on the `webui-user.bat` file and select `Edit`.
   - **Tip:** Enable `Show > File name extensions` if you can't find this file.

3. Add the following flags after the **`COMMANDLINE_ARGS=`** line, separated by spaces:

   - **`--xformers`**: Enhances generation speed and reduces memory consumption.
   - **`--medvram-sdxl`**: Use this if you have less than **12 GB** of VRAM but wish to use **SDXL** checkpoints.
   - **`--medvram`**: Use this if you have less than **8 GB** of VRAM.
   - **`--lowvram`**: Use this instead of `--medvram` if you encounter **CUDA Out of Memory Error**.

### Advanced Arguments

- **`--api`**: Enables other programs to interact with the WebUI. Refer to the official [API Documentation](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/API) for more information.
- **`--port XXXX`**: Specify a custom port for the WebUI to use.

For a complete list of available commandline arguments, see the [Commandline Arguments Documentation](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Command-Line-Arguments-and-Settings).