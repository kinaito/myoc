# MyOC v2.7.54

发布日期：2026-10-11

## 本次发布亮点

* **三层弹性自适应视线与骨骼追踪体系（根治非标参数模型与物理中继模型“只有眼睛动/完全不动”）**：
  - **VTube Studio 创作者权威映射**：优先智能探测并解析模型自带的 `*.vtube.json`，直接提取官方配置的 `FaceAngleX/Y/Z`、`EyeRightX/Y`、`BodyAngleX/Y` 与 `EyeOpenLeft/Right` 驱动通道。
  - **物理中继拓扑智能反向追溯（Zero Ad-hoc）**：当视线驱动目标属于受控物理输出（如部分中继模型的 `ParamAngleX` 由输入骨骼 `Param30` 驱动、多重转向模型的 `ParamAngleX` 由 `ParamAngleX2` 驱动）时，自动反向推导物理输入源并直接驱动该输入源。不仅彻底杜绝每一帧 `UpdatePhysics` 抹零覆盖导致的头部/身体僵死，反而完美激活全局物理中继联动与惯性弹性。
  - **CDI3 语义降级匹配**：若模型采用非标 ID（如非标命名模型的 `Param`、`Param2` 或 `ParamAngle5`），自动降级使用 `.cdi3.json` 的中英文显示名称（如“Angle X / 角度 X / 脸 X”）模糊识别，彻底杜绝误判为背景道具导致不眨眼、不呼吸、不跟踪的问题。
* **自适应参数值域驱动与非标眨眼注入**：
  - **动态值域自适应 (`apply_gaze_param`)**：自动判定参数为归一化输入中继骨骼（$[-1, 1]$）还是传统角度骨骼（$[-30, 30]$），平滑限幅，杜绝参数死锁与极端共振。
  - **非标自然眨眼注入**：针对无标准 `ParamEyeLOpen` 的特殊模型（如非标命名模型 `Param5`/`Param6`），自动注入自然眨眼曲线，恢复角色鲜活生命力。

---

## 详细变更

### 渲染与驱动核心 (Render/Tracking)
- **多层解析升级**：`preview_widget.py` 中新增 `_output_to_inputs`、`_vtube_mappings` 与 `_param_display_names` 提取逻辑。
- **驱动选择算法**：重构 `_find_param` 与 `_detect_tracking_params`，支持 VTS 预设、物理反向追溯、语义识别与身体防重复碰撞保护。
- **渲染循环增强**：在 `paintGL` 中使用 `apply_gaze_param` 替代硬编码度数，支持非标眨眼注入。

### 自动化验证与测试
- **测试套件**：新增 `tests/test_tracking_adaptive.py`，覆盖标准模型、非标命名模型、多级中继物理模型等 6 大典型异构模型。

---

## 适用平台

- **macOS**：下载 `Myoc-2.7.54.pkg` 双击安装到 `/Applications`，或直接使用免安装版 `Myoc.app`
- **Windows**：（构建中，待后续同步补充上传）
