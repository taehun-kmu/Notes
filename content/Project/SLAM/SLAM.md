---
title: SLAM (Simulataneous Localization & Mapping)
alias: SLAM
---

## Spectacular AI

### Realsense

> [!info]+ Devices
> 
> - [D455](https://www.intelrealsense.com/depth-camera-d455/)
> - [D435i](https://www.intelrealsense.com/depth-camera-d435i/) [^1] 

> [!Important]+ Dependencies
> 
> - **APT**
>   ```bash
>   sudo apt update
>   sudo apt install --no-install-recommends python-is-python3 python3-pip git
>   ```
> 
> - **Pip**
>   ```bash
>   python3 -m pip install spectacularAI[full]
>   ```
> 
> - **C/C++ Develop**
>   ```bash
>   sudo apt install cmake clang build-essential
>   ```
> 
> - **FFmpeg**
>   ```bash
>   sudo apt install ffmpeg
>   
>   # Optional (FFmpeg 6)
>   sh -c "$(curl -fsSL https://raw.githubusercontent.com/taehun-kmu/auto/main/script/ffmpeg.sh)"
>   ```

> [!Example]+ 
> 
> - **Unzip**
>   ```bash
>   tar -xzvf ${Download} && cd Linux_Ubuntu_x86-64
>   ```
> - **udev**
>   ```bash
>   ./bin/3rdparty/librealsense/setup_udev_rules.strikethrough
>   ```
> 
> - **Check**
>   > Now you should see rapidly flowing JSONL text <br>
>   > press Ctrl+C to exit
>   ```bash
>   ./vio_jsonl
>   ```
> 
> - **Run**
>   ```bash
>   ./sai-record-realsense
>   ```

[^1]: D435 without the "**i**" does not work.

