# DeepSeek 鲸鱼娘桌宠 v1.0.0

发布日期：2026-08-16  
平台：Windows 11 x64  
发行形式：免安装文件夹式 ZIP，提供离线完整版与依赖系统运行时的精简版

## 使用方法

1. 将 ZIP 完整解压到一个可写文件夹。
2. 双击 `DeepSeek桌宠.exe`。
3. 手动启动会打开主控台；设置为开机启动后，登录 Windows 时只显示桌宠和托盘。
4. 不要只复制 EXE。`Assets`、`Config`、DLL、运行时文件和随附文档都是程序组成部分。

### 两种压缩包的区别

- `DeepSeek桌宠-v1.0.0-Win11-x64.zip`：离线完整版，自带 .NET 8 Windows Desktop Runtime，文件较多，解压即用。
- `DeepSeek桌宠-v1.0.0-Win11-x64-精简版.zip`：不包含微软运行时，文件更少；运行前必须安装 `.NET 8 Desktop Runtime x64`，详见 `RUNTIME_REQUIREMENTS.md`。

## v1.0 主要功能

- 小鲸透明桌宠、自然待机、眨眼、随机互动和启动登场动画；
- 8 帧真实连续步态、左右镜像、柔和动作过渡和随机散步；
- 拖拽、40%–200% 缩放、多显示器、鼠标穿透、完全隐藏和拖到屏幕侧边隐藏；
- 悬停快捷喂食、饮水、擦拭和摸摸；
- 饱食度、口渴度、清洁度、疲惫度、鲸币、休息和外出打工；
- 主控台、DeepSeek API 聊天、GitHub 更新中心；
- 只允许启动白名单 EXE 的安全电脑助手。

## 发布前验证

- Release 编译：0 警告、0 错误；
- Windows 11 x64 自包含发布目录完整；
- 设置保存/备份/恢复测试通过；
- 电脑助手授权、路径阻止、白名单、审计和恢复测试通过；
- 连续步态运行测试通过，窗口保持响应且没有崩溃日志；
- 角色图集、默认配置和法律说明均作为外部文件保留。

## 重要提示

- 当前没有商业代码签名，Windows 可能显示“未知发布者”或信誉提示；请只运行来自可信来源且校验值一致的压缩包。
- ZIP 同目录提供 `.sha256.txt` 侧车文件，可使用 PowerShell 的 `Get-FileHash -Algorithm SHA256` 复核。
- 聊天需要用户自己的 DeepSeek API Key；Key 保存于 Windows 凭据管理器。
- 电脑助手不会执行任意 Shell，也不会自动获得管理员权限。
- 更新中心只有在维护者配置真实 GitHub 仓库后才可使用。
- 本项目为非官方同人项目；角色参考素材、DeepSeek 名称和相关标识的权利归相应权利人所有。公开再分发或商业使用前，实际发布者必须确认所需授权。

完整责任边界、隐私、安全和第三方说明请阅读：

- `DISCLAIMER.md`
- `SECURITY.md`
- `PRIVACY.md`
- `THIRD_PARTY_NOTICES.md`
- `DOTNET-LICENSE.txt`
- `DOTNET-THIRD-PARTY-NOTICES.txt`
- `RUNTIME_REQUIREMENTS.md`
- `PROJECT_INTRODUCTION.md`
