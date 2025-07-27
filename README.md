# 三维点云/模型可视化器 (3D Point Cloud/Model Visualizer)

**开发者: Archer0083**

一个基于Web的、功能强大的、交互式三维点云和模型可视化分析工具。无需安装任何软件，直接在浏览器中运行。

[**在线访问 (Live Demo) - 最新版 v3.8**](https://Archer0083.github.io/3D-point-cloud-visualizer//v3.8.html)

---

### 项目演示

*点击下方可跳转至YouTube观看操作演示视频*

[![操作演示视频封面](https://raw.githubusercontent.com/Archer0083/3D-point-cloud-visualizer/main/example.jpg)](https://www.youtube.com/watch?v=4n_GEKv2YSo)

### 核心功能特点

#### 1. 广泛的文件格式支持
- **文本点云**: 完美兼容 `.txt`, `.xyz`, `.ply` 等通用文本格式。
- **标准三维格式**: 支持 `.obj` 模型。
- **带纹理模型**: 完整加载带 `.mtl` 材质和 `.jpg`/`.png` 纹理的 `.obj` 模型。

#### 2. 智能的数据预处理系统
- **可视化列映射**: 交互式地为数据列指派含义（X, Y, Z, R, G, B），解决格式不标准问题。
- **实时3D预览**: 在预处理时实时看到调整效果。
- **操作可撤销**: 支持撤销操作，防止误操作。
- **点云稀疏化**: 在预处理大文件时，可设置稀疏度（例如每 N 个点保留 1 个），在不牺牲整体形态的前提下，极大降低内存占用和提升加载性能。

#### 3. 专业的地理坐标系处理
- **自动坐标归一化**: 解决大坐标（经纬度）点云的浮点数精度问题。
- **自适应轴向缩放**: 自动校正经纬度和高程间的尺度差异，保证模型不变形。

#### 4. 精确的数据拾取与分析
- **双坐标系显示**: 同时显示点的**真实世界坐标**（经纬度、高程）和**局部坐标**（米）。
- **精确颜色读取**: 精确读取并显示所选点位的RGB颜色值。

#### 5. 丰富的可视化交互控制
- **显示参数调整**: 实时调整点大小和模型透明度。
- **场景环境切换**: 一键切换深/浅色背景。
- **双重交互模式**: 提供“指针模式”（拾取）和“手指模式”（导航）。
- **完善的模型管理**: 支持一键清空当前场景。

### 更新日志 (Changelog)
**v3.8** - [点击访问该版本](https://archer0083.github.io/3D-point-cloud-visualizer/v3.8.html)
- **【功能增强】** 新增**在线示例加载器**，提供一个包含大、小两种点云的列表供用户选择，实现一键在线体验。
- **【核心升级】**  在预处理窗口中加入了点云稀疏化功能，通过流式处理和顺序抽稀，增强了文件解析器，现在能够智能识别在线案例.obj文件中的顶点数据，并将其作为点云进行预处理。
  
**v3.2** - [点击访问该版本](https://archer0083.github.io/3D-point-cloud-visualizer/v3.2.html)
- **【重要修复】** 修复了因浏览器安全策略导致的文件上传功能在某些环境下（如嵌入式预览）失效的问题。
- **【核心升级】** 回归并优化了基于标准文件输入（`<input type="file">`）的**文件流式处理引擎**，在预处理窗口中加入了**点云稀疏化**功能，通过流式处理和顺序抽稀，从根本上解决了因浏览器内存限制导致的大型点云文件（>500MB）加载失败的问题。

**v2.8** - [点击访问该版本](https://archer0083.github.io/3D-point-cloud-visualizer/v2.8.html)
- 引入了专业的地理坐标转换功能，支持双坐标系显示。

### 示例数据 (Demo Data)

本仓库包含一个小体积点云文件示例和一个大体积点云文件示例，用于测试应用处理大型数据的能力。

- **[large_example.txt]762 MB(https://github.com/Archer0083/3D-point-cloud-visualizer/blob/main/large_example.txt)**
- **[small_example.obj]24 MB(https://archer0083.github.io/3D-point-cloud-visualizer/small_example.obj)** 

*注意: 此文件通过 Git LFS 存储。*

### 如何使用

1.  **在线使用**: 直接访问上方的 [Live Demo](https://Archer0083.github.io/3D-point-cloud-visualizer/) 链接。
2.  **本地运行**:
    * 下载本仓库中的 `index.html` 文件。
    * 用您的网页浏览器（如Chrome, Edge, Firefox）直接打开该文件即可。
    * **注意**: 运行时需要网络连接。

### 开源许可证

本项目基于 [MIT License](LICENSE) 开源。
