# 数字侦探：四数推理游戏

一个无需安装、无需构建的纯 HTML + CSS + JavaScript 网页小游戏。玩家通过大小关系逐步推理电脑隐藏的四个数字。

**在线试玩：** [https://jiangyuanjiegoforwind-glitch.github.io/guessnumberABCD/](https://jiangyuanjiegoforwind-glitch.github.io/guessnumberABCD/)

## 游戏规则

- 玩家使用 `A / B / C / D`，电脑使用 `甲 / 乙 / 丙 / 丁`。
- 双方各有四个 `1–20` 的整数，不能为 `0`，也不能出现重复数字。
- 双方四个数字的总和都必须为 `20`。
- 可以比较一个玩家数字与一个电脑数字，也可以比较双方各自两个不同数字之和。
- 比较结果只显示 `>`、`<` 或 `=`，不会展示电脑的具体数字。
- 最终猜测错误时只提示“猜错了”，不会透露正确位置数量；完全正确后公布答案和总猜测次数。

## 功能

- 玩家数字实时校验，只有总和等于 `20` 才能开始。
- 使用 Web Crypto API 随机生成电脑数字，并自动保证数字为正数、互不重复且总和为 `20`。
- 两种提问模式可无限使用，完整保留可滚动历史记录。
- 猜错后可以继续尝试，重新开始会保留玩家数字并生成新答案。
- 支持键盘操作、减少动态效果偏好以及桌面和移动端响应式布局。
- 所有页面样式与逻辑都包含在一个 `index.html` 中，不依赖第三方库。

## 本地运行

克隆仓库后直接双击 `index.html`，或使用浏览器打开该文件即可运行。

```bash
git clone git@github.com:jiangyuanjiegoforwind-glitch/guessnumberABCD.git
cd guessnumberABCD
open index.html
```

## 部署

仓库通过 GitHub Actions 自动部署到 GitHub Pages。推送到 `main` 分支后，Pages 工作流会发布仓库根目录中的静态页面。

## 许可证

本项目使用 [MIT License](LICENSE)。
