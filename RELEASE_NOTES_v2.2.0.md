# MyOC v2.2.0

发布日期：2026-07-07

## 本次发布说明

MyOC v2.2.0 是一次**安装与分发形态**的重要升级，同时补齐了产品品牌化与用户反馈通道。

### 安装形态升级

- **macOS 改为 .pkg 安装包**：以前 macOS 用户拿到的是未打包的应用bundle，需要手动拖拽；现在双击 .pkg 直接安装到 /Applications。
- **Windows 改为 .zip 压缩包**：以前 Windows 用户解压后面对一堆无从下手的依赖文件；现在解压后根目录直接看到 `Myoc.exe`，双击即启动。
- **双端正式安装包**：macOS / Windows 均提供正式安装包，通过 GitHub Releases 统一分发。

### 产品与体验

- **全新产品命名与品牌**：从 Live2D Editor 统一命名为 MyOC，配套原生圆角图标（macOS Dock / Windows 任务栏 / 开始菜单均干净圆角渲染）。
- **关于面板**：新增「关于」弹窗，展示当前版本号、GitHub 仓库地址、微信公众号联系方式。
- **启动自动更新检测**：应用启动时自动检测 GitHub 上的新版本，发现新版本时提示用户升级。

### 用户反馈通道

- **一键反馈**：界面右上角「💬 反馈」按钮，填写问题描述后一键上报开发者（HMAC-SHA256 签名的安全上报通道，自动附带最近 150 行脱敏日志，加速定位）。
- **意见与改进建议同样欢迎**：不限于问题报告。

### 工程化建设

- **版本号统一管理**：版本号唯一真源，构建产物 / 安装包名 / git tag 全流程自动同步，杜绝版本散落与覆盖。
- **私有开发 + 对外发布分离**：开发仅在私有仓库进行，公开仓只含脱敏后的产物与版本说明（即将持续同步）。

## 适用平台

- macOS：[Myoc-2.2.0.pkg](https://github.com/kinaito/myoc/releases/tag/v2.2.0) 双击安装到 /Applications
- Windows：[Myoc-Windows-v2.2.0.zip](https://github.com/kinaito/myoc/releases/tag/v2.2.0) 解压后双击 Myoc.exe

---

完整历史见本仓库根目录 [CHANGELOG](https://github.com/kinaito/myoc/blob/main/CHANGELOG.md)
