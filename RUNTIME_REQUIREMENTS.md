# 精简版运行要求

精简版没有把微软 .NET 和 WPF 运行时复制进程序文件夹，因此 DLL 数量与压缩包体积会明显减少。桌宠自身仍采用外置 DLL、素材和配置，`DeepSeek桌宠.exe` 只作为启动入口。

## 必需环境

- Windows 11 x64；
- `.NET 8 Desktop Runtime x64`，不能只安装普通 `.NET Runtime`；
- 官方下载页：<https://dotnet.microsoft.com/zh-cn/download/dotnet/8.0>

在下载页面找到“.NET 桌面运行时”，选择 Windows x64 安装程序。安装完成后重新双击 `DeepSeek桌宠.exe`。

可以在 PowerShell 中执行以下命令检查：

```powershell
dotnet --list-runtimes
```

输出中出现 `Microsoft.WindowsDesktop.App 8.0.x` 表示运行条件已经满足。

## 应该选择哪个版本

- 希望解压即用、离线使用或给不熟悉运行库的用户：选择离线完整版。
- 已经安装 .NET 8 Desktop Runtime，希望文件更少、体积更小：选择精简版。

两个版本的功能、素材、存档目录和版本号相同，可以保留现有 `%APPDATA%\DeepSeekDesktopPet` 数据直接切换。
