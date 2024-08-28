# TensorRT Setup Guide
**By: Kha Van**

## Prerequisite
- Nvidia **RTX** GPU

## Getting Started

### Step 1: Install the Latest Nvidia Driver
- Download and install the latest Nvidia driver from [Nvidia's website](https://www.nvidia.com/download/index.aspx). Ensure that the driver version is `v545` or newer.

### Step 2: Activate the Python Virtual Environment
- Activate your Python virtual environment where you will be installing TensorRT.

### Step 3: Install Required Packages
- Run the following commands one by one to install the necessary packages:

    ```bash
    python -m pip install nvidia-cudnn-cu11==8.9.4.25 --no-cache-dir
    python -m pip install --pre --extra-index-url https://pypi.nvidia.com/ tensorrt==9.0.1.post11.dev4 --no-cache-dir
    python -m pip uninstall -y nvidia-cudnn-cu11
    ```

### Step 4: Launch the WebUI
- Start your WebUI application.

> For instructions on how to install Extensions, refer to the [Extensions section](../README.md#extensions).

### Step 5: Install the TensorRT Extension
- Install the `Stable-Diffusion-WebUI-TensorRT` extension by following the link to its [GitHub repository](https://github.com/NVIDIA/Stable-Diffusion-WebUI-TensorRT).

### Step 6: Access the TensorRT Tab
- After restarting the WebUI, a new **TensorRT** tab should be visible.

### Step 7: Modify a Preset (Optional)
- If necessary, select and modify a preset within the TensorRT tab according to your needs.

### Step 8: Generate an Optimized Engine
- Press the **Export Default Engine** button to generate an optimized engine.
    - Note: The conversion process took approximately 3 minutes on an RTX 3060 GPU.

### Step 9: Update WebUI Settings
- Navigate to **Settings** -> **User Interface**.
- Add **`sd_unet`** to the **`Quicksettings list`**, then restart the WebUI.

### Step 10: Enjoy the Speed Boost!
- You can now choose the **[TRT]** Unet option to benefit from increased processing speeds.
    - Example: Performance improved from `~7 it/s` to `~15 it/s` on an RTX 3060.

## Important Notes
- The optimized engine only works for the specified resolution, batch size, and token count.
- If you intend to use `Hires. fix`, export a **dynamic** engine with the resolution covering both the original and the upscaled resolution.
- LoRA must be baked in separately (this is **not recommended**).