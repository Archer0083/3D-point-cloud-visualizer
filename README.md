# 三维点云/模型可视化器 (3D Point Cloud/Model Visualizer)

**开发者: Archer0083**

一个基于Web的、功能强大的、交互式三维点云和模型可视化分析工具。无需安装任何软件，直接在浏览器中运行。

[**在线访问 (Live Demo)**](https://Archer0083.github.io/3D-point-cloud-visualizer/)

---

### 项目演示

![应用截图](https://raw.githubusercontent.com/Archer0083/3D-point-cloud-visualizer/main/example.jpg)

*点击上方图片可跳转至YouTube观看操作演示视频*

[![操作演示视频封面](https://raw.githubusercontent.com/Archer0083/3D-point-cloud-visualizer/main/example.jpg)](https://www.youtube.com/watch?v=4n_GEKv2YSo)


### 核心功能特点

#### 1. 广泛的文件格式支持
- **文本点云**: 完美兼容 `.txt`, `.xyz` 等通用文本格式。
- **标准三维格式**: 支持 `.ply` (ASCII) 和 `.obj` 模型。
- **带纹理模型**: 完整加载带 `.mtl` 材质和 `.jpg`/`.png` 纹理的 `.obj` 模型。

#### 2. 智能的数据预处理系统
- **可视化列映射**: 交互式地为数据列指派含义（X, Y, Z, R, G, B），解决格式不标准问题。
- **实时3D预览**: 在预处理时实时看到调整效果。
- **操作可撤销**: 支持撤销操作，防止误操作。

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

### 如何使用

1.  **在线使用**: 直接访问上方的 [Live Demo](https://Archer0083.github.io/3D-point-cloud-visualizer/) 链接。
2.  **本地运行**:
    * 下载本仓库中的 `index.html` 文件。
    * 用您的网页浏览器（如Chrome, Edge, Firefox）直接打开该文件即可。
    * **注意**: 运行时需要网络连接。

### 开源许可证

本项目基于 [MIT License](LICENSE) 开源。
