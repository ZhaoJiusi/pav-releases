# PAV Releases

PAV（个人资产版本管理器）的公开发布仓库。本仓库只存放公开版本说明和稳定通道更新清单；程序文件通过 GitHub Releases 分发，源码位于 [personal-asset-version-manager](https://github.com/ZhaoJiusi/personal-asset-version-manager)。

## 当前版本

- `0.2.9`：Windows 10/11 x64 免安装便携版。
- 完整解压 ZIP 后运行 `PAV_Client.exe`，不要只复制 EXE，也不要直接在压缩包内运行。
- 首次使用所需的工作区、仓库、作者和百度网盘 API 配置说明随包提供。
- 0.2.9 新增始终可用的网络中断，可停止当前请求、后续操作链和自动刷新；软件更新完整内嵌设置页。
- 新工作区只需填写项目名，仓库路径自动使用 `/apps/PAV/`；仓库和工作区使用不同来源色。
- 三维预览固定为白模、AO 和默认视角；模型仓库缩略图更大，并保留多级灰度结构。

## 未签名提示

0.2.9 是未签名版本。`PAV_Client.exe` 和 `PAVUpdater.exe` 没有 Windows 公共可信代码签名，因此 Windows 可能显示“未知发布者”或 SmartScreen 警告。

只有从本仓库 Release 下载、且 ZIP 的 SHA-256 与同一 Release 附带的 `.sha256` 文件一致时才应运行。SHA-256 可以检查文件是否与发布内容一致，但不能替代发布者数字签名。后续取得代码签名证书后，将使用新的版本号发布签名版，不会替换已经发布的文件。

## 更新

客户端仅在用户主动点击“检查软件更新”后读取仓库根目录的 `update.json`，不自动联网检查。更新清单必须在对应 Release 资产上传并完成匿名下载校验后才更新。

发布包不包含百度 App Key、Secret Key、Token、工作区数据或用户设置。
