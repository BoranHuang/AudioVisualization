# 🌌Y2K PARTICLE CORE

![ Boran Badge](https://img.shields.io/badge/BORAN-00f3ff?)

> **"Experience the Geometry of Sound."**
> 
> 一个深度优化的 WebGL 交互式音频可视化引擎。结合 **Google MediaPipe** 手势识别与 **Three.js** 高性能渲染，在浏览器中重现《星际穿越》般的四维空间体验。专为 Apple Silicon (M-Series) 芯片优化。

---

## ⚡️ 核心功能 (Key Capabilities)

### 1. 🧬 全频段独立物理引擎 (Independent Audio Physics)
区别于传统的整体缩放，本引擎采用分频驱动算法：
* **LOW (0-60Hz):** 驱动 **Radial Explosion (径向爆发)**。低音越重，粒子向外扩散的动能越大。
* **MID (250-2000Hz):** 驱动 **Vortex Torque (涡流扭矩)**。人声与旋律会产生旋转引力，扭曲空间几何。
* **HIGH (2000Hz+):** 驱动 **High-Freq Shimmer (高频微颤)**。高音不改变形态，仅触发粒子表面的高光闪烁。

### 2. 🤖 上帝之手 (AI Gesture Control)
集成 **MediaPipe Vision (GPU Accelerated)**，实现零延迟手势追踪：
* **🖐 Expand (张开手掌):** 宇宙膨胀系数提升至 1.6x。
* **✊ Collapse (握紧拳头):** 触发引力坍缩，所有粒子被吸入奇点。
* *状态反馈：HUD 界面实时显示 "SCANNING", "HAND DETECTED", "COLLAPSING".*

### 3. 📐 9种超验数学形态 (Transcendental Geometries)
内置 9 套参数化方程生成器，支持一键无缝变形 (Morphing)：

| 快捷键 | 形态名称 | 数学原理 |
| :--- | :--- | :--- |
| `Space` | **WORMHOLE** | 动态时空隧道 |
| `Space` | **DATA_HELIX** | 破碎的 DNA 双螺旋 |
| `Space` | **CYBER_GRID** | 正弦波地形矩阵 |
| `Space` | **STARGATE** | 复杂多层环面结构 |
| `Space` | **NEBULA_KNOT** | 高维扭结投影 |
| `Space` | **MOBIUS_STRIP** | 单面拓扑循环 |
| `Space` | **LORENZ_ATTRACTOR** | 混沌吸引子 (蝴蝶效应) |
| `Space` | **HYPER_TORUS** | 4D 环面 3D 投影 |
| `Space` | **FIBONACCI_SPHERE** | 黄金分割点阵球体 |

### 4. 🎛️ 玻璃态 HUD 控制台
* **Mixer Console:** 独立调节高中低频的物理反馈强度。
* **Spectrum Analyzer:** 实时三波段频谱可视化。
* **Visual Style:** 采用 "Share Tech Mono" 字体与全息磨砂玻璃材质。

---

## 📂 项目结构 (Structure)

```text
Boran_Visualizer/
├── AudioVisualization.html  # 核心入口 (包含所有 Logic, Shader, UI)
├── README.md                # 说明文档
└── assets/                  # (可选) 存放音频文件的目录
````

> **注意**: 为保持极致的便携性，已将 HTML, CSS (UI), JS (Three.js Logic), GLSL (Shaders) 全部封装在单一的 `AudioVisualization.html` 文件中，**开箱即用**。

-----

## ⚙️ 高级配置 (Configuration)

在 `AudioVisualization.html` 代码中，您可以修改顶部的常量来定制体验：

```javascript
// 修改粒子总数 (建议 M1/M2: 30000, M3/M4: 60000+)
const COUNT = 36000; 

// 修改辉光强度
bloomPass.strength = 1.8;
bloomPass.radius = 0.6;

// 修改摄像头灵敏度阈值 (0.0-1.0)
if(avg < 0.2) { /* 判定为握拳 */ }
```

-----

## ❓ 常见问题 (Troubleshooting)

**Q: 画面是黑的，没有粒子？**

  * **A:** 检查浏览器控制台 (F12)。如果是 `CORS` 错误，请确保使用了上述的 "Local Server" 方式运行，而不是直接打开文件。

**Q: 摄像头不工作/没有反应？**

  * **A:** 1. 确保浏览器已授予**摄像头权限**。
    2\. 确保在 `localhost` 或 `https` 环境下运行（浏览器安全限制）。
    3\. 等待 HUD 显示 "SYSTEM READY"。首次加载 AI 模型可能需要 5-10 秒。

**Q: 上传音乐后没有声音？**

  * **A:** 现代浏览器禁止自动播放音频。上传文件后，尝试点击一下屏幕任意位置以激活 AudioContext。

-----

## 🛠 技术栈 (Tech Stack)

  * **Render Engine:** [Three.js r160](https://threejs.org/)
  * **Computer Vision:** [MediaPipe Vision Tasks](https://developers.google.com/mediapipe)
  * **Post-Processing:** UnrealBloomPass (High Performance)
  * **Shader Language:** WebGL GLSL (Custom Vertex/Fragment Shaders)
  * **UI Design:** CSS3 Glassmorphism & Share Tech Mono Font

-----

## 📜 版权 (License)

**MIT License**

Copyright (c) 2025 **Boran Made**

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

```

### 💡 小贴士：
因为您改名了，如果您使用 Python 启动服务器，记得在浏览器地址栏输入完整路径 `http://localhost:8000/AudioVisualization.html`，否则默认可能会显示文件列表目录。
```
