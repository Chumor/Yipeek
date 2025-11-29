# Yipeek · 一瞥

[![Version](https://img.shields.io/github/v/release/Chumor/yipeek?color=007ACC)](https://github.com/Chumor/yipeek/releases)  
[![Android Friendly](https://img.shields.io/badge/platform-Android-brightgreen.svg)](#)  
[![UserScript](https://img.shields.io/badge/type-UserScript-yellow.svg)](#)  
[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)  
[![Stars](https://img.shields.io/github/stars/Chumor/yipeek?style=social)](https://github.com/Chumor/yipeek/stargazers)

> **指尖轻触，万象凝于一瞥。**  
> *A tap, a glimpse — the world in focus.*

Yipeek 是一款 **网页专用脚本**，专注移动端手势图片预览：开箱即用，无需初始化或框架，极简流畅。

---

## 🎬 3 秒上手

![Demo]()  
**操作方式：** 点击 → 高斯模糊背景 → 手势缩放 → 下滑关闭  

**安装方式：**  
1. Tampermonkey / ScriptCat → 添加脚本  
2. 打开网页，点击图片即可预览  

---

## 🌟 核心特性

- ⚡ **开箱即用** — 安装即可生效，无需任何配置  
- 🤌 **移动端手势友好** — 双击缩放、双指捏合、单指拖拽、下滑/背景点击关闭  
- 🎯 **智能初始尺寸 & 居中** — 自动适配屏幕，防止裁切或过度缩放  
- 🫧 **沉浸式预览体验** — 高斯模糊背景，禁用底层交互，避免误触  
- 🔄 **动态图片自动绑定** — 支持异步加载的图片，实时监控 DOM 变化  
- 🛠️ **可扩展性** — 可定制 `normalizeImageUrl()` 适配其他网站  

---

## 🌐 已优化适配网站

- **GitHub** — 自动将 `/blob/` 地址转换为 raw URL，点击即可预览原图  
- **其他网站** — 可通过修改脚本 `normalizeImageUrl()` 增加自定义规则  

---

## 🖐️ 手势操作指南

| 手势 / 操作 | 功能 |
|------------|------|
| 点击图片 | 打开预览 |
| 双击 | 切换缩放（放大 ↔ 原始大小） |
| 双指捏合 | 平滑缩放（自由比例 0.5× ~ 4×） |
| 拖拽 | 查看放大后的图片细节 |
| 下滑或点击背景 | 关闭预览 |
| 放大时拖拽 + 缩放边界限制 | 防止图片溢出屏幕 |

---

## ⚙️ 脚本内部设计

- **`setPerfectInitialSize()` + `applyTransform()`**：自动计算最佳尺寸和居中位置  
- **手势识别 + touch-action / pointer-events**：保证移动端流畅体验  
- **GitHub URL normalize**：自动处理 blob → raw，避免跳页  

---

## 📄 许可证

MIT License — 免费用于个人和商业项目  
详见 [LICENSE](./LICENSE)

---

## ❤️ 致谢

- 灵感来源 [ImageViewer.js](https://github.com/mrhuo/image-viewer)  
- Yipeek 更专注 **移动端 + 极简 + 手势体验**  
- 特别感谢早期测试者提供的手势反馈与优化建议  

> **一瞥**，不仅是预览——它是专注、尊重与轻盈的用户体验。  
> 欢迎 Star ⭐、Issue、PR —— 让每一次指尖轻触，都更接近完美。
