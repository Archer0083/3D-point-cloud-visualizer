# 三维点云/模型可视化器 (3D Point Cloud/Model Visualizer)

**开发者: Archer0083**  
**Developer: Archer0083**

一个基于Web的、功能强大的、交互式三维点云和模型可视化分析工具。无需安装任何软件，直接在浏览器中运行。  
A powerful, web-based, interactive tool for 3D point cloud and model visualization and analysis. No installation required—runs directly in your browser.

[**在线访问 (Live Demo) - 最新版 v3.9**](https://Archer0083.github.io/3D-point-cloud-visualizer//index.html)

---

### 项目演示 (Project Demo)

*点击下方可跳转至YouTube观看操作演示视频*  
*Click the image below to watch the demo video on YouTube*

[![操作演示视频封面 (Demo Video Thumbnail)](https://raw.githubusercontent.com/Archer0083/3D-point-cloud-visualizer/main/example.jpg)](https://www.youtube.com/watch?v=4n_GEKv2YSo)

---

### 核心功能特点 (Key Features)

#### 1. 广泛的文件格式支持  
#### 1. Wide File Format Support
- **文本点云**: 完美兼容 `.txt`, `.xyz`, `.ply` 等通用文本格式。  
  **Text-based Point Clouds**: Fully supports `.txt`, `.xyz`, `.ply` and other plain-text formats.  
- **标准三维格式**: 支持 `.obj` 模型。  
  **Standard 3D Models**: Supports `.obj` model files.  
- **带纹理模型**: 完整加载带 `.mtl` 材质和 `.jpg`/`.png` 纹理的 `.obj` 模型。  
  **Textured Models**: Fully loads `.obj` models with `.mtl` materials and `.jpg`/`.png` textures.

#### 2. 智能的数据预处理系统  
#### 2. Intelligent Data Preprocessing System
- **可视化列映射**: 交互式地为数据列指派含义（X, Y, Z, R, G, B），解决格式不标准问题。  
  **Visual Column Mapping**: Interactively assign meaning to each column (X, Y, Z, R, G, B) to fix non-standard formats.  
- **实时3D预览**: 在预处理时实时看到调整效果。  
  **Real-time 3D Preview**: See changes instantly during preprocessing.  
- **操作可撤销**: 支持撤销操作，防止误操作。  
  **Undo Support**: Allows rollback of operations to prevent mistakes.  
- **点云稀疏化**: 在预处理大文件时，可设置稀疏度（例如每 N 个点保留 1 个），在不牺牲整体形态的前提下，极大降低内存占用和提升加载性能。  
  **Point Cloud Downsampling**: Retain every Nth point during preprocessing to reduce memory use while preserving shape.

#### 3. 专业的地理坐标系处理  
#### 3. Advanced Geospatial Coordinate Handling
- **自动坐标归一化**: 解决大坐标（经纬度）点云的浮点数精度问题。  
  **Auto Coordinate Normalization**: Resolves floating-point precision issues with large coordinates (e.g., GPS).  
- **自适应轴向缩放**: 自动校正经纬度和高程间的尺度差异，保证模型不变形。  
  **Adaptive Axis Scaling**: Automatically corrects scale differences between lat/lon and elevation to avoid distortion.
- **可选坐标系**: 用户可在预处理阶段明确指定数据是 **地理坐标** (WGS84)还是 **笛卡尔坐标**。  
  **Selectable Coordinate Systems**: Users can specify whether the data is in **Geographic** (WGS84) or **Cartesian** coordinates during preprocessing.  
- **智能坐标转换**: 对地理坐标数据，应用会进行专业转换，保证模型不变形；对笛卡尔坐标数据，则仅进行中心化处理，保留原始尺寸和比例。  
  **Intelligent Transformation**:  Correctly transforms geographic data to a local meter-based system for distortion-free viewing, or simply centers Cartesian data while preserving its original scale.

#### 4. 精确的数据拾取与分析  
#### 4. Accurate Data Picking and Analysis
- **双坐标系显示**: 同时显示点的**真实世界坐标**（经纬度、高程）和**局部坐标**（米）。  
  **Dual Coordinate Display**: Shows both **real-world coordinates** (lat/lon/alt) and **local coordinates** (meters).  
- **精确颜色读取**: 精确读取并显示所选点位的RGB颜色值。  
  **Precise Color Reading**: Accurately displays RGB color values of selected points.

#### 5. 丰富的可视化交互控制  
#### 5. Rich Visualization & Interaction Controls
- **显示参数调整**: 实时调整点大小和模型透明度。  
  **Display Tuning**: Adjust point size and model transparency in real-time.  
- **场景环境切换**: 一键切换深/浅色背景。  
  **Scene Themes**: Toggle between light/dark backgrounds.  
- **双重交互模式**: 提供“指针模式”（拾取）和“手指模式”（导航）。  
  **Dual Interaction Modes**: Use "Pointer Mode" (pick) and "Finger Mode" (navigate).  
- **完善的模型管理**: 支持一键清空当前场景。  
  **Scene Management**: Easily clear current scene with one click.

---

### 更新日志 (Changelog)
**v3.9** - [点击访问该版本 (View Version)](https://archer0083.github.io/3D-point-cloud-visualizer/index.html)  
- **【功能增强】** 增强了解析器的鲁棒性，现在可以正确处理带 `#`注释行的`.xyz`和 `.txt` 文件。  
  **[Feature]** Improved parser robustness to correctly handle `.xyz` and `.txt` files with comment lines starting with `#`.  
- **【核心升级】** 新增**坐标系选择**功能！用户现在可以在预处理时指定数据是地理坐标(WGS84)还是笛卡尔坐标，解决了非地理坐标数据（如CAD模型）的变形问题。。  
  **[Core Update]** Added **Coordinate System Selection!** Users can now specify data as Geographic (WGS84) or Cartesian, fixing distortion issues for non-geographic data (e.g., CAD models).

**v3.8** - [点击访问该版本 (View Version)](https://archer0083.github.io/3D-point-cloud-visualizer/v3.8.html)  
- **【功能增强】** 新增**在线示例加载器**，提供一个包含大、小两种点云的列表供用户选择，实现一键在线体验。  
  **[Feature]** Added **online demo loader** with a list of large/small point clouds for one-click experience.  
- **【核心升级】** 在预处理窗口中加入了点云稀疏化功能，通过流式处理和顺序抽稀，增强了文件解析器，现在能够智能识别在线案例.obj文件中的顶点数据，并将其作为点云进行预处理。  
  **[Core Update]** Introduced point cloud downsampling in preprocessing window with streaming-based sequential thinning. OBJ files in demo mode now auto-convert to point cloud format.

**v3.2** - [点击访问该版本 (View Version)](https://archer0083.github.io/3D-point-cloud-visualizer/v3.2.html)  
- **【重要修复】** 修复了因浏览器安全策略导致的文件上传功能在某些环境下（如嵌入式预览）失效的问题。  
  **[Fix]** Fixed file upload failures in embedded views due to browser security policies.  
- **【核心升级】** 回归并优化了基于标准文件输入的**文件流式处理引擎**，在预处理窗口中加入了**点云稀疏化**功能，彻底解决了浏览器内存限制导致的大文件加载失败问题。  
  **[Update]** Rebuilt the file streaming engine using standard `<input type="file">`, added point cloud thinning to support large files (>500MB).

**v2.8** - [点击访问该版本 (View Version)](https://archer0083.github.io/3D-point-cloud-visualizer/v2.8.html)  
- 引入了专业的地理坐标转换功能，支持双坐标系显示。  
  Introduced professional geospatial coordinate transformation with dual coordinate display.

---

### 示例数据 (Demo Data)

本仓库包含一个小体积点云文件示例和一个大体积点云文件示例，用于测试应用处理大型数据的能力。  
This repository includes small and large point cloud samples to test the application’s handling of large datasets.

- **[large_example.txt] 762 MB**  
  [https://github.com/Archer0083/3D-point-cloud-visualizer/blob/main/large_example.txt](https://github.com/Archer0083/3D-point-cloud-visualizer/blob/main/large_example.txt)
- **[small_example.obj] 24 MB**  
  [https://archer0083.github.io/3D-point-cloud-visualizer/small_example.obj](https://archer0083.github.io/3D-point-cloud-visualizer/small_example.obj)

*注意: 此文件通过 Git LFS 存储。*  
*Note: These files are stored via Git LFS.*

---

### 如何使用 (How to Use)

1. **在线使用**: 直接访问上方的 [Live Demo](https://Archer0083.github.io/3D-point-cloud-visualizer/) 链接。  
   **Online**: Visit the [Live Demo](https://Archer0083.github.io/3D-point-cloud-visualizer/) link above.
2. **本地运行**:  
   **Local Use**:
   - 下载本仓库中的 `index.html` 文件。  
     Download the `index.html` file from this repository.
   - 用您的网页浏览器（如 Chrome, Edge, Firefox）直接打开该文件即可。  
     Open it directly with your browser (Chrome, Edge, Firefox, etc.).
   - **注意**: 运行时需要网络连接。  
     **Note**: Requires internet connection at runtime.

---

### 开源许可证 (License)

本项目基于 [MIT License](LICENSE) 开源。  
This project is open-sourced under the [MIT License](LICENSE).
