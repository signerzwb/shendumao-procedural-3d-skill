# 用代码做 3D 游戏：程序化场景 Skill 与江南水乡 Demo

一份面向 AI 编程智能体的制作 Skill，加一个单 HTML 的交互式 3D 漫游案例。由神都猫整理分享，帮助创作者理解如何用程序化几何、Three.js 和 WebGL 组织一个可交互的网页 3D 场景。

## 包含什么

- `build-procedural-3d-game-skill.zip`：Skill 原始压缩包，解压后包含 `build-procedural-3d-game/SKILL.md`、参考资料和静态检查脚本。
- `jiangnan.html`：《听雨·江南水巷》交互场景示例，约 790 KiB；包括水巷、桥、建筑、天气切换、漫游操作与音效代码。它是演示场景，不是完整商业游戏。
- `third-party-notices/threejs.txt`：示例内嵌的 Three.js 上游 MIT 许可证。HTML 源码保留了原有 Three.js 版权和 SPDX 说明。

## 安装 Skill

1. 下载 `build-procedural-3d-game-skill.zip` 并解压。
2. 将解压出的 `build-procedural-3d-game` 文件夹放入你的 Codex 用户技能目录；Windows 示例为 `C:\Users\<你的用户名>\.codex\skills\`。其他支持 `SKILL.md` 的智能体按其实际文档安装。
3. 新开或刷新会话，按环境提示启用技能。示例任务：

   > 使用 `build-procedural-3d-game`，制作一个可漫游的雨夜小镇。请先说明范围与操作方式，再生成、运行、检查画面和交互。

4. 对生成结果进行实际浏览器测试和人工验收。Skill 是方法和检查清单，不能保证生成一次就完成，不能替代性能、交互与安全测试。

## 本地体验案例

下载 `jiangnan.html`，使用支持 WebGL 的现代桌面浏览器打开。进入后可用 WASD 移动、鼠标拖动环视，Q/E 转向，Shift 加速；界面提供天气、画质、声音、地图和重置控件。声音通常需要用户点击后才可播放。设备性能、浏览器和实际兼容性不同，体验会有差异。

单 HTML 不自动等于完全离线：文件内含打包的 JavaScript，但是否能在特定浏览器完全断网运行需以实际测试为准。

## 技术思路

用程序化规则生成建筑组件、材质与场景布局，用 WebGL/Three.js 实时渲染，再通过输入、相机、天气和音频系统组合出可交互体验。HTML 打包是交付形式，不意味着全部内容都天然简单，也不意味着不需要引擎；此案例内嵌 Three.js r180。

代码生成 3D 场景、WebGL 和程序化内容都早于 AI 智能体。智能体的价值在于协助把需求拆分成任务，生成和修改代码、协助测试和迭代；创意、事实核对、审美选择与最终验收仍需要人参与。

## 来源与使用边界

- Three.js 官方项目：<https://github.com/mrdoob/three.js>；案例内嵌部分遵循其 MIT 许可，详见 `third-party-notices/threejs.txt`。
- WebGL 介绍：<https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API>。
- Skill 与示例作为学习材料分享；本仓库没有对其余自有内容额外指定开源许可证。复用、改造或商业使用前，请确认相应权利和许可。
- 本仓库不附带账号、密钥、私有项目或用户聊天内容。
