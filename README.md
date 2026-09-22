# Neon Snake · 霓虹贪吃蛇

一个零依赖、单文件的 HTML5 小游戏。直接用浏览器打开 `index.html` 就能玩，也能一键发布到 GitHub Pages。

![Neon Snake](https://img.shields.io/badge/HTML5-Canvas-39ff14)

## 玩法

- 方向键 或 `W` `A` `S` `D` 控制方向
- 手机端可直接在画面上滑动，或使用屏幕方向键
- 吃到食物 +10 分，每 50 分速度提升一档
- 撞墙或撞到自己即结束，最高分保存在本地（localStorage）

## 运行

方式一：双击 `index.html`。

方式二：起一个本地服务器（推荐，避免个别浏览器限制）。

```bash
python -m http.server 8000
# 然后访问 http://localhost:8000
```

## 发布到 GitHub Pages

```bash
git init
git add .
git commit -m "feat: neon snake game"
git branch -M main
git remote add origin https://github.com/<你的用户名>/<仓库名>.git
git push -u origin main
```

然后在仓库 **Settings → Pages** 中，把 Source 设为 `main` 分支的 `/ (root)`，保存后访问
`https://<你的用户名>.github.io/<仓库名>/` 即可。

## 项目结构

```
.
├── index.html   # 全部游戏逻辑、样式与渲染
├── LICENSE
└── README.md
```

## 许可

MIT
