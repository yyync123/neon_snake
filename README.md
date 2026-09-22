# Neon Snake · 霓虹贪吃蛇

> 一个零依赖、单文件的 HTML5 小游戏。克隆下来双击即玩，也可以直接部署到 GitHub Pages。

[![HTML5](https://img.shields.io/badge/HTML5-Canvas-39ff14?style=flat-square)](https://developer.mozilla.org/zh-CN/docs/Web/API/Canvas_API)
[![零依赖](https://img.shields.io/badge/dependencies-0-00e5ff?style=flat-square)](#)
[![License](https://img.shields.io/badge/license-MIT-7c5cff?style=flat-square)](./LICENSE)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-ready-ff2d75?style=flat-square)](#发布到-github-pages)

---

## 在线试玩

部署完成后访问：`https://<你的用户名>.github.io/<仓库名>/`

本地运行：直接双击 `index.html`，或启动一个静态服务器：

```bash
python -m http.server 8000
# 浏览器打开 http://localhost:8000
```

---

## 特性

| 特性 | 说明 |
| --- | --- |
| 零依赖 | 全部逻辑写在一个 `index.html`，无需安装任何东西 |
| 精致视觉 | 霓虹渐变、光晕、玻璃拟态面板、动态背景 |
| 平滑操作 | 键盘、屏幕方向键、手机滑动手势三种方式 |
| 等级系统 | 每 50 分升一档，速度逐步加快 |
| 本地存档 | 最高分通过 `localStorage` 自动保存 |
| 音效反馈 | Web Audio 实时生成，可一键静音 |
| 移动端友好 | 响应式布局，自动显示虚拟方向键 |

---

## 玩法

| 操作 | 键盘 | 触屏 |
| --- | --- | --- |
| 移动 | `W` `A` `S` `D` / 方向键 | 在画面上滑动 / 虚拟方向键 |
| 开始 / 暂停 | `Space` | 轻点画面 |
| 重新开始 | `R` | 点击重置按钮 |
| 静音开关 | `M` | 点击静音按钮 |

- 吃到食物 **+10 分**，每累计 **50 分**提升一个等级，蛇移动更快。
- 撞到墙壁或自己的身体则游戏结束，最高分会自动保存。

---

## 发布到 GitHub Pages

```bash
git init
git add .
git commit -m "feat: neon snake game"
git branch -M main
git remote add origin https://github.com/<你的用户名>/<仓库名>.git
git push -u origin main
```

然后在仓库页面：

1. 打开 **Settings → Pages**
2. **Source** 选择 `Deploy from a branch`
3. 分支选 `main`，目录选 `/ (root)`
4. 保存，等待一两分钟后访问上方链接即可

---

## 项目结构

```
.
├── index.html   # 页面结构、样式与全部游戏逻辑
├── LICENSE      # MIT 许可证
├── README.md    # 本说明
└── .gitignore
```

---

## 自定义

所有可调参数都集中在 `index.html` 的脚本开头，方便修改：

```js
const COLS = 24;   // 横向格子数
const ROWS = 24;   // 纵向格子数
const CELL = canvas.width / COLS;
```

速度与等级节奏位于 `reset()` 和 `step()` 中，配色集中在 CSS 顶部的 `:root` 变量里。

---

## 许可

[MIT](./LICENSE)
