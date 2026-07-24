# Changelog

本仓库的 CHANGELOG 由私有仓发布脚本脱敏后自 private 自动同步，仅含对外可见的提交。
开发细节与内部文档保留在私有仓库。

## v2.7.46 (2026-07-25)

- Initial commit (f0b15d7)
- docs: add README with v2.0 changelog (8261b60)
- feat: switch compilation framework to Nuitka for secure anti-reverse distribution on macOS and Windows (b076193)
- refactor: reorganize project structure into src, packaging, tests, and docs (32ec9be)
- fix: support Nuitka compiled check (__compiled__) for user log directory redirection (de4156f)
- style: rename application to '欧希 (myoc)' and update slogan/prompts (e277646)
- style: simplify first screen prompt and rename title to MyOC (bcaa385)
- fix: route API screenshot calls to main GUI thread and use QOpenGLWidget.grabFramebuffer() (be45c52)
- fix: force include PIL package in Nuitka options for Mac and Windows to prevent black screens (5a030c5)
- fix: bundle live2d FrameworkShaders using --include-data-dir on Mac and Windows to fix black rendering screen (92e7e82)
- docs: add diagnostics and agent automation interface design specification (532e1ab)
- fix: import QColor to prevent NameError in setup_bg_color_menu (1a4c912)
- fix: background color clearing order in paintGL, and change welcome version button to ClickableLabel subclass to avoid hover cursors (516101c)
- fix: add logging and 20px padding to ClickableLabel in first screen to expand click hitbox (d979f41)
- feat: configure and compile application window and bundle icons using user provided icon.png (8edefd4)
- chore: add imageio to windows build dependency list for icon conversion (84f8453)
- docs: upgrade README.md with user-facing features, installation guidelines, and bypass instructions (0280bfe)
- fix: resolve UnboundLocalError by moving urllib.parse to top-level imports in telemetry.py (8a25774)
- style: process icon.png to standard macOS squircle size and padding to ensure consistent round-corner rendering across Finder, Dock, and Windows (03c6004)
- release: add final Myoc.pkg v2.1 for macOS, update README.md version history, and update .gitignore to track release deliverables (e882f15)
- docs: add VERSION_2_1_REVIEW.md summarizing upgrade changes and development experience pitfalls (5db4872)
- build(win): 引入 PowerShell 一键打包与绿色化整理流水线并修复构建 bug (709bd01)
- feat: 统一版本管理, 增加GitHub异步更新检测, 修复重置时清除表情与视线追踪脖子死锁问题 (85b968a)
- feat: 实现关于面板线上 JSON 配置同步与过滤白名单机制, 升级版本为 v2.1.2 (9a262b5)
- fix: 显式开启 paintGL 每帧的 model.Update() 物理及参数更新，彻底解锁物理级联与脖子不转问题，升级版本为 v2.1.4 (1a26f90)
- fix: 修复 model.Update(dt) 缺失参数类型导致黑屏不显示问题，升级版本为 v2.1.5 (81eebd5)
- fix: 彻底拿掉 paintGL 外观覆写缓存与 Update 帧重置, 恢复滑块/追踪/表情物理并动态同步首屏版本号, 升级版本为 v2.1.6 (f056195)
- fix: 彻底移除白名单校验重塑缓存因果源头，结合物理Update完美解决追踪/滑块/表情失效问题，同步首屏版本号 (b5458c4)
- fix: 回滚核心渲染引擎至 v2.1.0 交付大版本，仅在视线跟随中增加级联偏转参数解决转头，彻底消除闪眼和失效，升级版本为 v2.1.7 (4c8c231)
- docs: 沉淀项目特有 Live2D 渲染与参数缓存防崩塌红线规约到 .agents/AGENTS.md (5d55746)
- build(win): 增加 icon.ico 文件并将 Windows 打包脚本更新为标准 .ico 图标 (3cbab7c)
- release: add Myoc v2.2.0 release packages and documentation (b6e7771)
- docs: 添加 Live2D 模型数据库技术方案文档与版本管理脚本 (1980c39)
- feat(v2.3.0): 集成模型数据库客户端 (425e81a)
- feat(v2.4.0): 模型预处理工具 - 明暗牌标记嵌入 (fb1002d)
- feat(v2.5.0): 服务端基础设施 - Cloudflare Workers + Supabase (96e8d59)
- fix(v2.5.1): 修复暗牌读取逻辑，支持子目录纹理 (647af33)
- fix(v2.5.2): 修复 Worker 联表查询，Supabase 一对一关系返回对象而非数组 (ee75559)
- docs(v2.5.2): 添加模型数据库配置文档，录入 Yomi 模型数据 (f8f5bfc)
- test(v2.5.2): 明暗牌端到端测试 10/10 全部通过 (29cfbd8)
- feat(v2.5.2): 场景17 - 模型归属与篡改检查技能 (b1560f5)
- refactor(v2.6.0): 模型运营工具从客户端剥离为独立 ops 模块 (4daadba)
- refactor(v2.6.0): 整理项目结构，按 5 分区归档 (0679dc2)
- docs(v2.6.0): 追加场景17到技术方案文档 (5d19df6)
- docs(v2.6.0): 更新 README，补充完整目录结构与职能说明 (34b83c3)
- fix: 代码审查修复 - API随机化、路径同步、架构解耦 (86b9fcd)
- docs: define official model access design (5e3e830)
- chore: ignore local worktrees (2b1e3af)
- chore: 版本清理 - 合并 v2.7.0-v2.7.4 为空 bump，统一为 v2.7.0 (b7d7a18)
- feat: implement background official model authorization gate and supplier redirection UI (ee526df)
- chore: organize and clean up v2.7.0 UI refactoring files (fbc7e01)
- v2.7.7: UI 优化与授权信息展示修复 (b717a32)
- v2.7.8: 应用内置截图功能 (5d2c219)
- v2.7.9: 反馈整合截图功能 (a319b34)
- v2.7.11: 安全审查修复 + UI 优化 (5fe7457)
- docs: update architecture, agent guide, API docs + add model_registry tool (8cc0af7)
- fix: clear __pycache__ on startup to prevent cross-version cache conflicts (ce6c61c)
- v2.7.12: 模型注册表 + Supabase 同步 + 鼠标追踪修复 (b56ef2a)
- v2.7.13: Mac 构建包 + Windows 脚本 + 版本整理 (269a5f3)
- v2.7.14: 安全加固 - API鉴权 + 反馈防护 + 模糊查询移除 (b6ce355)
- security: Workers IP 限流 + API Key 配置 (3cc27f2)
- docs: 更新 SECURITY_PLAN 执行记录 (4e2ab50)
- docs: feedback 表已创建完成 (cb1f59f)
- docs: Workers 已部署，安全加固全部完成 (1d9e878)
- v2.7.14: Mac 构建包 + 安全策略文档 (0e5fcce)
- chore: 构建脚本不再生成无版本号 Myoc.pkg 别名 (54a7e2e)
- fix: 构建包含 settings.json + 移除无版本号别名 (7bd1187)
- fix: 修复 bundle identifier + 包含 settings.json (bbc846e)
- fix: 修复 live2d Python 文件未包含在 .pkg 的问题 (910c3d2)
- fix: 修复参数名 NameError - ParamAngleX 等应为字符串 (ad6af6b)
- fix: feedback_api_base 默认值改为 Workers URL (a636f21)
- chore: 清理旧版本构建包，更新版本记录 (055078c)
- docs: 创建维护规则文档，更新坑点记录 (410adb3)
- docs: 明确公开仓库推送规则 (57fabf8)
- fix: 修复模型 5bcf57 MID 不匹配 + Supabase 数据修复 (0bc63a7)
- fix: 客户端查询端点添加 API Key 认证 (96e63cf)
- fix: 修复 model_load 拼写错误导致启动闪退 (470b27d)
- docs: 更新项目文档到 v2.7.23 (a444d35)
- docs: 更新文档到 v2.7.24 (67ee082)
- chore: 添加 server/node_modules/ 到 .gitignore，防止大文件入库 (3b6e2cf)
- docs: 记录 git 大文件导致 push 被拒的坑 (8ad4fc1)
- fix: 广告语为空时不显示，分隔线自适应 (cd1c143)
- fix: 反馈统一走 Bot API 发送文本+图片 (364fa3a)
- feat: WebSocket welcome 消息增加使用说明 (d71b8df)
- docs: 新增 WebSocket 使用手册 (2dd8d37)
- docs: WebSocket 使用手册更新到 v2.7.28 (ee66416)
- v2.7.28: WebSocket API 完整实现别名+随机范围+随机方案 (7ea563d)
- v2.7.29: 修复翻译不全+WebSocket欢迎消息+ApiCommand枚举 (e6135dc)
- fix: Windows 构建脚本补充 settings.json 和 remote_config.json 数据文件 (90da21e)
- chore: 统一版本号引用到 v2.7.29 (c7b85ba)
- docs: 修正 PROJECT_INDEX.md v2.7.29 版本描述 (c3a8887)
- chore: add v2.7.31 Windows build artifact (93aef43)
- fix: v2.7.36 验收问题修复 — 语言持久化、移除功能受限文案、全量语言切换 (f8907d8)
- chore: release v2.7.46 with clean remote config, proxy retry chain and Windows launcher fix (4ed5bc5)
- chore: track v2.7.46 mac release artifacts and remove old release binaries (43fdccc)
- docs: update README.md with concise developer dashboard, version evolution timeline and clean structure (3b048ba)
- v2.7.46: 网络稳定性专项修复 - vclaw域名统一 + 公共网络模块 + 代理自寻找全覆盖 + 授权信息修复 + README编码修复 (ddbcb75)
- v2.7.46: 添加 Windows 构建产物 (b6eb7c6)

# v2.7.13 (2026-07-21)

### 功能与体验

- **非合作模型冻结逻辑调整**：参数列表可用，仅锁定随机功能（随机/清空随机/随机方案）
- **本地模型清单就绪**：5 个模型已注册，支持 model_registry.py 管理

### 修复

- **修复鼠标跟踪失效**：修复 `_debug_lbp_history` 未初始化导致的鼠标释放/离开时 `AttributeError`
- **修复非合作模型身体跟踪**：扩展 `_detect_tracking_params` 候选列表，支持非标准参数名（`HeadAugX/Y/Z`、`BodyAugX/Y/Z`、`Eyeball_Gaze_X/Y`）
- **清理调试代码**：移除 `paintGL` 中每帧 `ctypes` 调用和冗余日志

## v2.2.0 (2026-07-07)

### 安装与分发

- **macOS 改为 .pkg 安装包**：双击安装到 /Applications，不再需要手动拖拽 .app
- **Windows 改为 .zip 压缩包**：解压后根目录直接看到 `Myoc.exe`

### 产品与体验

- **全新产品命名与品牌**：统一产品名 MyOC，配套原生圆角图标
- **关于面板**：展示当前版本号、GitHub 仓库地址、微信公众号联系方式
- **启动自动更新检测**：应用启动时自动检测 GitHub 上的新版本

### 反馈与诊断

- **一键反馈**：界面右上角「💬 反馈」按钮，填写问题描述一键上报开发者
