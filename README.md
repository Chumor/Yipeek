# Yipeek · 一瞥

> **指尖轻触，万象凝于一瞥。**  
> *A tap, a glimpse — the world in focus.*

![Yipeek 封面](https://socialify.git.ci/Chumor/Yipeek/image?description=1&font=Inter&language=1&logo=https%3A%2F%2Fgitlab.com%2Fchumoer%2FYipeek%2F-%2Fraw%2Fmain%2Fassets%2Fgoogle-photos-128.png&name=1&owner=1&pattern=Brick+Wall&theme=Auto)

<p align="center">
  <a href="https://github.com/Chumor/yipeek" title="GitHub 仓库">
    <img src="https://img.shields.io/badge/GitHub-Chumor/Yipeek-181717?logo=github&style=flat-square">
  </a>
  <a href="https://gitlab.com/chumoer/Yipeek" title="GitLab 仓库">
    <img src="https://img.shields.io/badge/GitLab-Yipeek-FC6D26?logo=gitlab&style=flat-square">
  </a>
  <a href="https://github.com/Chumor/yipeek/releases" title="Release">
    <img src="https://img.shields.io/github/v/release/Chumor/yipeek?color=007ACC&style=flat-square">
  </a>
  <a href="https://www.apache.org/licenses/LICENSE-2.0" title="Apache License 2.0">
    <img src="https://img.shields.io/badge/license-Apache%202.0-blue?style=flat-square">
  </a>
  <img src="https://img.shields.io/badge/type-UserScript-yellow?style=flat-square" title="UserScript 脚本类型">
</p>

<p align="center">
  <a href="https://greasyfork.org/zh-CN/scripts/557392-yipeek" title="Tampermonkey">
    <img src="https://img.shields.io/badge/Tampermonkey-Install-339933?style=flat-square&logo=tampermonkey">
  </a>
  <a href="https://scriptcat.org/zh-CN/script-show-page/4750" title="ScriptCat">
    <img src="https://img.shields.io/badge/ScriptCat-Install-FC6D26?style=flat-square&logo=scriptcase">
  </a>
</p>

<a href="https://www.flaticon.com/free-icons/google-photos" title="google photos icons">Google photos icons created by Freepik - Flaticon</a>

Yipeek 是一款 **网页专用脚本**，专注移动端手势图片预览：  
开箱即用，无需初始化或框架，追求**极简、顺滑、原生**的操作体验。

---

## 🎬 快速上手

[点击观看 Demo 视频](https://github.com/user-attachments/assets/55ecb6bc-71fe-419c-9529-0e0a3d2e5acd)

**操作方式**：点击 → 高斯模糊背景 → 手势缩放 → 下滑关闭  

**安装方式**：  
1. Tampermonkey / ScriptCat → 添加脚本  
2. 打开网页，点击图片即可预览

---

## 核心特性

- **开箱即用** — 安装即可生效，无需任何配置
- **移动端手势友好** — 支持双击缩放、双指捏合、拖拽，下滑或点击背景关闭
- **智能初始尺寸与居中** — 自动适配屏幕，防止裁切或过度缩放
- **沉浸式预览体验** — 高斯模糊背景，禁用底层交互，避免误触
- **动态图片自动绑定** — 支持异步加载图片，实时监控 DOM 变化
- **高度可扩展** — 可定制 `normalizeImageUrl()` 适配其他网站
- **智能图标忽略** — 自动跳过 logo、导航按钮等非内容图（无需配置）
- **链接拦截保障** — 点击 `<a><img>` 时优先预览，不跳转页面
- **显式忽略支持** — 任意元素加 `data-yipeek-ignore` 即可全局禁用预览

  
---

## 已优化适配网站

- **GitHub** — 自动将 `/blob/` 地址转换为 raw URL，点击即可预览原图  
- **其他网站** — 可通过修改脚本 `normalizeImageUrl()` 增加自定义规则  

---

## 手势操作指南

| 手势 / 操作 | 功能 |
|------------|------|
| 点击图片 | 打开预览 |
| 双击 | 切换缩放（放大 ↔ 原始大小） |
| 双指捏合 | 平滑缩放（0.5× ~ 4×） |
| 拖拽 | 查看放大后的图片细节 |
| 下滑或点击背景 | 关闭预览 |
| 放大拖拽限制 | 防止图片溢出屏幕 |

---

## 脚本内部设计

- setPerfectInitialSize() + applyTransform() — 自动计算最佳尺寸和居中位置  
- 手势识别 + touch-action / pointer-events — 保证移动端流畅体验  
- GitHub URL normalize — 自动处理 blob → raw，避免跳页

---

## 📄 许可证

Apache License 2.0 — 免费用于个人和商业项目  
详见 [LICENSE](./LICENSE)

---

## 说明

- 图标来源已在 README 上方注明官方署名  
- Yipeek 专注「指尖轻触，万象凝于一瞥」的**移动端原生**体验  

> 欢迎 Star ⭐、Issue、PR —— 让每一次指尖轻触，都更接近完美。
