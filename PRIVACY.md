# 隐私说明

## 本机保存的数据

- 普通设置：`%APPDATA%\DeepSeekDesktopPet\settings.json`
- 电脑助手允许列表：`%APPDATA%\DeepSeekDesktopPet\assistant-apps.json`
- 电脑助手操作日志：`%APPDATA%\DeepSeekDesktopPet\assistant-actions.log`
- 崩溃诊断：`%APPDATA%\DeepSeekDesktopPet\crash.log`
- DeepSeek API Key：Windows 凭据管理器中的 `DeepSeekDesktopPet.ApiKey`
- 可选开机启动项：当前用户注册表 `HKCU\Software\Microsoft\Windows\CurrentVersion\Run` 中的 `DeepSeekDesktopPet`

操作日志包含时间、操作结果、应用名称、EXE 路径和进程编号或失败类型，不记录聊天全文。由于 EXE 路径可能包含 Windows 用户名，分享日志前应先检查和脱敏。

## 网络访问

- 只有用户主动发送普通聊天消息时，程序才向设置中的 API 地址发送对话历史。
- 本地“打开应用”指令不会发送给模型。
- 只有用户主动检查或安装更新时，程序才访问配置的 GitHub 仓库和 Release。
- 本版本没有遥测、广告、后台账户同步或静默上传功能。

未来的 OpenClaw 连接器若启用，可能引入独立的 Gateway、模型提供商、消息频道和插件数据流；必须在实现时提供单独的权限和隐私说明，不能沿用本文件笼统授权。

## 删除数据

退出桌宠后删除 `%APPDATA%\DeepSeekDesktopPet` 可清除普通设置、允许列表和日志。API Key 需要在桌宠设置中清除，或从 Windows 凭据管理器删除对应条目。开机启动项应先在主控台或完整设置中取消勾选，也可从 Windows“启动应用”或上述当前用户注册表位置移除。删除程序文件夹不会自动删除这些用户数据和启动项。
