# Optimizing NVIDIA GPU Performance on Ubuntu for Gaming

*Authored by: Richard Gerard Marcoux III*

## Introduction

As a user with high-end hardware, including an i9 10800k processor, 80GB of RAM, and an NVIDIA 2080 Ti graphics card, the expectation is a seamless and high-performance experience across all applications, whether it's modern gaming, using creative software like Unreal Engine, Digital Audio Workstations (DAWs), or even emulating retro games. However, a perplexing issue presented itself: applications felt "chunky" and inconsistent. The symptoms were clear—microstutters, random hitches, severe slowdowns of several seconds, and while using RetroArch for retro gaming, there were instances of audio cracking paired with video stuttering and slowdowns. These performance hiccups were especially noticeable and unwarranted when running less demanding tasks, such as playing classic SNES titles. This led to the realization that there was likely an underlying issue with the system settings or drivers that needed attention.

After thorough investigation and experimentation, which involved toggling various settings within the NVIDIA driver settings, a significant breakthrough was made. By adjusting specific NVIDIA settings, every graphics and audio application began to run perfectly smooth, completely devoid of any stutter or slowdown. What follows is a compilation of the adjustments that were made to achieve this level of performance.

## Overview

NVIDIA GPUs are powerful, but certain settings in Ubuntu can cause performance issues like frame stuttering. This guide will help you optimize these settings.

## Prerequisites

* **Ubuntu OS** : Ensure you have the latest updates installed.
* **NVIDIA GPU** : This guide is specifically for NVIDIA graphics cards.
* **NVIDIA Drivers** : Make sure you have the latest NVIDIA drivers installed.

## Step 1: Disabling VSync in NVIDIA Settings

VSync (Vertical Sync) can cause stuttering in games when enabled globally. Here's how to disable it:

1. Open `nvidia-settings` from your terminal or application menu.
2. Click on your monitor, then find the `OpenGL Settings`.
3. Disable `Sync to VBlank`.
4. Apply the changes.

 **Note** : While VSync is disabled globally, games can still enable it individually without issues.

## Step 2: Disabling Composition Pipeline Options

The Composition Pipeline settings in NVIDIA can lead to performance issues, especially with the Vulkan API. Here's how to disable them:

1. Open `nvidia-settings`.
2. Go to `X Server Display Configuration`.
3. Select `Advanced`.
4. Disable any options related to `Force Composition Pipeline` and `Force Full Composition Pipeline`.
5. Apply and save the configuration.

## Step 3: Managing Vulkan API and OpenGL Settings

For games using Vulkan API instead of OpenGL, certain settings can cause slowdowns or stuttering. To optimize:

1. Open `nvidia-settings`.
2. Navigate to the `OpenGL Settings`.
3. Ensure that the settings are optimized for performance rather than quality. This might vary depending on the game.
4. For Vulkan-specific settings, it's often best to leave them at their default unless you're experiencing issues.

## Additional Tips

* **Game-Specific Settings** : Some games have their own settings that can override global NVIDIA settings. Adjust these in-game for better performance.
* **System Monitoring** : Use tools like `htop` and `nvidia-smi` to monitor system performance and GPU usage.
* **Regular Updates** : Keep your system, drivers, and games updated for the best performance and compatibility.

## Conclusion

By adjusting these settings, you should experience a noticeable improvement in gaming performance on your Ubuntu system with an NVIDIA GPU. Remember, each game might have unique requirements, so some tweaking might be necessary for optimal performance.
