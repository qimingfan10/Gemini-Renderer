Gemini Advanced Renderer (Gemini 高级渲染器)

![alt text](https://img.shields.io/badge/版本-v1.0-blue.svg)
![alt text](https://img.shields.io/badge/平台-Tampermonkey-yellow.svg)
![alt text](https://img.shields.io/badge/许可证-MIT-green.svg)
![alt text](https://img.shields.io/badge/状态-活跃-brightgreen.svg)

一个强大的油猴脚本，旨在将您的 Gemini 交互体验提升至全新高度。它整合了代码渲染与图片链接解析两大核心功能，让 Gemini 不再只是一个文本生成器，更是一个强大的可视化工具。

✨ 项目简介

在日常使用 Gemini 时，我们经常会遇到以下场景：

Gemini 生成了一段 HTML 或 ECharts 代码，但您必须手动复制到本地文件或在线编辑器才能看到效果。

Gemini 给了您一段 Mermaid 流程图或甘特图的代码，但这堆文本对不熟悉其语法的人来说极不直观。

Gemini 生成了 pollinations.ai 的 AI 绘画链接，您需要手动点击跳转才能查看图片。

Gemini Advanced Renderer 正是为解决这些痛点而生。它通过一个高效的 MutationObserver 实时监控页面变化，智能地将代码块和特定链接转换为丰富的可视化内容。

🚀 核心功能

📊 一键渲染 HTML & ECharts:

在 html 语言的代码块右上角生成一个 “▶️ 渲染 HTML” 或 “📈 渲染 ECharts” 按钮。

点击后直接在页面内生成一个安全的 iframe 沙箱，用于预览网页和图表效果。

自动处理并内联外部 CSS 和 JavaScript 资源，实现零依赖的自包含预览。

<img width="1523" height="1058" alt="image" src="https://github.com/user-attachments/assets/69de0d48-71c9-4198-b65a-2b1d913aa4d4" />


🎨 智能渲染与修正 Mermaid 图表:

自动识别 mermaid 语言代码块，并添加 “📊 渲染图表” 按钮。

调用 Kroki.io API 将代码实时渲染为 SVG 矢量图。

内置语法修正引擎：能自动修复常见的 gantt（甘特图）、quadrantChart（四象限图）和 requirementDiagram（需求图）中的语法错误（如缺少引号、格式错误等），大幅提高渲染成功率。

<img width="1511" height="1072" alt="image" src="https://github.com/user-attachments/assets/769374e6-3c88-4735-b347-4314511f878c" />


🖼️ 自动解析 Pollinations AI 图像:

自动识别指向 image.pollinations.ai 的链接（包括 Google 搜索重定向链接）。

将这些文本链接直接替换为渲染后的图片，提供无缝的图文浏览体验。

异步加载图片，并在加载完成前显示占位符，不阻塞页面交互。

<img width="736" height="988" alt="image" src="https://github.com/user-attachments/assets/5437258f-8030-4d80-8c84-2649e90ad2ea" />


🛠️ 安装指南

安装浏览器扩展:
首先，你需要在你的浏览器（如 Chrome, Firefox, Edge）中安装一个用户脚本管理器。推荐使用：

Tampermonkey (最为流行)

Greasemonkey (Firefox)

安装本脚本:

访问脚本的安装页面（例如 GreasyFork 或 GitHub）。

点击此处安装 [GreasyFork](https://greasyfork.org/zh-CN/scripts/544783-gemini-advanced-renderer-html-mermaid-pollinations)

在打开的页面中，点击 “安装” 按钮。

开始使用:

刷新或重新打开 Gemini 网站。

当 Gemini 生成符合条件的代码块或链接时，脚本将自动生效。

🤝 如何贡献

我们欢迎任何形式的贡献！无论是提交 Bug 反馈、提出功能建议还是直接贡献代码。

报告问题: 请通过 GitHub Issues 提交详细的问题描述。

开发: Fork 本仓库，创建你的功能分支 (git checkout -b feature/AmazingFeature)，完成修改后提交 Pull Request。脚本内置 DEBUG 模式，方便开发调试。

📄 许可证

本项目基于 MIT 许可证 发布。
