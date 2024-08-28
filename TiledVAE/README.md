# Tiled Diffusion & VAE Guide

### Author: Kha Van

## Overview
This document provides a step-by-step guide to using the Tiled Diffusion and VAE extension, which helps mitigate CUDA Out of Memory Errors when upscaling images with high resolutions, particularly when using `Hires. fix` or `img2img` in the Stable Diffusion environment.

## Usage
When upscaling an image using `Hires. fix` or `img2img`, you might encounter a **CUDA Out of Memory Error** if the resolution is set too high. The Tiled Diffusion & VAE extension can help alleviate this issue.

## Requirements

Before proceeding, ensure you understand how to install extensions in your environment. You can refer to the [Extensions Installation Guide](../README.md#extensions) for detailed instructions.

### Required Extension
To use Tiled Diffusion & VAE, install the following extension:

- **MultiDiffusion with Tiled VAE (multidiffusion-upscaler-for-automatic1111)**  
  Available on GitHub: [MultiDiffusion Upscaler](https://github.com/pkuliyi2015/multidiffusion-upscaler-for-automatic1111)

## How to Use

### Step 1: Install the Extension
1. Follow the installation guide to add the MultiDiffusion with Tiled VAE extension to your environment.
2. After installation, you should see a new sub-section named **Tiled VAE** in the **txt2img** and **img2img** tabs.

### Step 2: Enable Tiled VAE
1. Navigate to either the **txt2img** or **img2img** tab in your interface.
2. Scroll down to find the **Tiled VAE** section.
3. Check the option to **Enable** the Tiled VAE feature.
4. If necessary, adjust the `Tile Size` parameter to suit your specific needs. The default settings should work in most cases, but fine-tuning may yield better results depending on your GPU's capabilities.

### Step 3: Upscale Your Image
1. Once Tiled VAE is enabled, proceed to upscale your image as you normally would.
2. The Tiled VAE extension will manage the process, helping to avoid CUDA Out of Memory Errors.

> **Example**: Using this extension, I successfully upscaled a `1024x1024` image to `2048x2048` on an RTX 3070 Ti with only **8GB** of VRAM.

### Compatibility with ControlNet
This extension also integrates well with the **Tile Resample** module from [ControlNet](../ControlNet/README.md), allowing for even more advanced image manipulation and upscaling techniques.

