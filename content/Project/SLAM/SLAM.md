---
title: SLAM (Simulataneous Localization & Mapping)
alias: SLAM
---

## Spectacular AI

> [!important]+ Develop
> 
> - **APT**
>   ```bash
>   sudo apt update
>   sudo apt install --no-install-recommends zlib1g libusb-1.0-0-dev python-is-python3 python3-pip python3-tk python3.10-venv git 
>   ```
> 
> - **C/C++**
>   ```bash
>   sudo apt install cmake clang build-essential gcc g++
>   ```
> 
> - **FFmpeg**
>   ```bash
>   sudo apt install ffmpeg
>   ```
> 
>   ```bash
>   # Optional (FFmpeg 6)
>   sh -c "$(curl -fsSL https://raw.githubusercontent.com/taehun-kmu/auto/main/script/ffmpeg.sh)"
>   ```

### Realsense

> [!info]+ Devices
> 
> - [D455](https://www.intelrealsense.com/depth-camera-d455/)
> - [D435i](https://www.intelrealsense.com/depth-camera-d435i/) [^1] 

> [!Important]- Dependencies
> 
> - [UV](https://docs.astral.sh/uv/)
> 
>   ```bash
>   uv tool install spectacularAI[full] --no-cache # Global
>   ```
> 
>   ```bash
>   uv pip install numpy opencv-python opencv-contrib-python spectacularAI[full] --no-cache # venv
>   ```
> 
> - [Pip](https://pip.pypa.io/en/stable/)
> 
>   ```bash
>   python3 -m pip install spectacularAI[full] # System
>   ```
> 
>   ```bash
>   pip install numpy opencv-python opencv-contrib-python spectacularAI[full] # venv
>   ```

> [!Example]- 
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
> - **Check** [^2]
>   ```bash
>   ./vio_jsonl
>   ```
> 
> - **Run**
>   ```bash
>   ./sai-record-realsense
>   ```

### OAK-D

> [!info]+ Devices
> 
> > OAK-D models with IMU sensors are supproted. This includes but is not limited to
> 
> - [OAK-D](https://shop.luxonis.com/products/oak-d)
> - [OAKD-D (Pro) W](https://shop.luxonis.com/products/oak-d-pro-w)
> - [OAK-D LR](https://shop.luxonis.com/products/oak-d-lr)
> - [OAK-D PoE](https://shop.luxonis.com/products/oak-d-poe)

> [!Important]- Dependencies
> 
> - [UV](https://docs.astral.sh/uv/)
> 
>   ```bash
>   uv tool install depthai depthai-viewer spectacularAI[full] --no-cache # Global
>   ```
> 
>   ```bash
>   uv venv 
>   source .venv/bin/activate # Exit venv: deactivate
>   uv pip install numpy matplotlib opencv-python opencv-contrib-python pygame PyOpenGL PyopenGL_accelerate depthai depthai-viewer spectacularAI[full] --no-cache # venv
>   ```
> 
> - [Pip](https://pip.pypa.io/en/stable/)
> 
>   ```bash
>   uv tool install spectacularAI[full] --no-cache # Global
>   ```
> 
>   ```bash
>   uv pip install numpy matplotlib opencv-python opencv-contrib-python pygame PyOpenGL PyopenGL_accelerate spectacularAI[full] --no-cache # venv
>   ```

> [!Example]- 
> 
> > [!info]+ Repository 
> > 
> > ```bash
> > git clone https://github.com/spectacularAI/sdk-examples && cd sdk-examples/python/oak
> > ```
> 
> </details>
> 
> 
> - **Minimal**
> 
>   > Prints 6-DoF poses as JSON text
> 
>   ```bash
>   python vio_jsonl.py
>   ```
> 
> - **Basic** 
> 
>   > Interactive 3D plot
>   > Draw in the air with the device
> 
>   ```bash
>   python vio_visu.py
>   ```
> 
> - **3D pen**
> 
>   > Draw in the air
>   > Cover the OAK-D color camera to activate the ink
> 
>   ```bash
>   python pen_3d.py
>   ```
> 
> - **3D mapping**
> 
>   > Build and visualize 3D point cloud of the environment in real-time
> 
>   ```bash
>   python mapping_visu.py
>   ```
> 
> - **3D mapping with Augmented Reality**
> 
>   > Show 3D mesh or point cloud on top of camera view, using OpenGL
> 
>   ```bash
>   python mapping_ar.py
>   ```
> 
> - **Advanced Spatial AI example**
> 
>   > Spectacular AI VIO + Tiny YOLO object detection
> 
>   ```bash
>   ./depthai_combination.py
>   ```
> 
>   ```bash
>   python depthai_combination.py
>   ```
> 
> - **Mixed reality**
> 
>   > The good old OpenGL functions like `glTranslatef` used for rendering.
> 
>   ```bash
>   python mixed_reality.py
>   ```

[^1]: D435 without the "**i**" does not work.
[^2]: Now you should see rapidly flowing JSONL text <br> press Ctrl+C to exit

