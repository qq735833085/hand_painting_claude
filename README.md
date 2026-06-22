# 3D 空间手势绘画 🖐️

基于 MediaPipe Hands + Three.js 的浏览器端 3D 空间手势绘画应用。通过摄像头识别手部关键点，用手指在真实空间中绘画，笔画具有真实的深度维度。

## ✨ 特性

- **真实 3D 空间绘画** — 手指的 X/Y/Z 三维位置直接映射到 3D 世界坐标，笔画具有深度
- **摄像头 AR 叠加** — 笔画直接画在摄像头实时画面上，所见即所得
- **旋转视角** — 可旋转/缩放 3D 场景，查看笔画的深度层次
- **手势操作** — 所有功能均支持手势控制，无需触摸屏幕
- **按钮补充** — 底部工具栏提供完整的触屏/点击操作

## 🖐️ 手势说明

| 手势 | 动作 | 功能 |
|------|------|------|
| 🖊️ 食指伸出 | 仅伸直食指 | **3D 空间绘画** |
| ✌️ 食指 + 中指 | 伸直食指和中指 | **循环切换颜色**（9 色） |
| ✊ 握拳 | 五指蜷曲，保持 0.8 秒 | **暂停 / 继续** |
| 🤏 拇指食指捏合 | 两指捏合，保持 1.5 秒 | **清空画布** |

## 🎮 屏幕按钮

底部工具栏提供所有功能的触屏/点击操作：

- 🎨 颜色圆点 — 选择绘画颜色
- 🧹 橡皮擦 — 切换橡皮擦模式
- ⏯️ 暂停 — 暂停/继续绘画
- 🗑️ 清空 — 清除所有笔画
- ↩️ 撤销 — 撤销最后一笔
- 🔍 视角模式 — 切换旋转视角/绘画模式
- 🏠 重置视角 — 恢复默认视角
- 🔄 切换摄像头 — 前后摄像头切换
- 📖 说明 — 查看操作指南

## 🚀 快速开始

### 本地运行

由于浏览器摄像头 API 需要安全上下文（HTTPS 或 localhost），推荐以下方式：

**方式一：使用 serve（推荐，支持 HTTPS）**

```bash
npx serve --ssl
```

手机通过 `https://<电脑局域网IP>:3000` 访问。

**方式二：Python HTTP 服务器（仅 PC localhost）**

```bash
python -m http.server 8080
```

浏览器打开 `http://localhost:8080`。

### 部署到 GitHub Pages

1. Fork 本仓库
2. Settings → Pages → Source: Deploy from a branch → Branch: `master` → Save
3. 通过 `https://<用户名>.github.io/hand_painting_claude` 访问

## ⌨️ 键盘快捷键

| 按键 | 功能 |
|------|------|
| `E` | 切换橡皮擦 |
| `空格` | 暂停/继续 |
| `C` | 切换颜色 |
| `O` | 切换视角模式 |
| `R` | 重置视角 |
| `F` | 切换摄像头 |
| `Ctrl+Z` | 撤销 |
| `Delete` | 清空画布 |

## 🛠️ 技术栈

- [MediaPipe Hands](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker) — 手部 21 关键点实时检测
- [Three.js](https://threejs.org/) — 3D 渲染引擎，笔画以 TubeGeometry 呈现
- 纯浏览器端运行，无需后端

## 📱 兼容性

- iOS Safari 15+
- Android Chrome 90+
- 桌面 Chrome / Edge / Firefox（需摄像头）
- 需要 HTTPS 或 localhost 才能使用摄像头

## 📄 License

MIT
