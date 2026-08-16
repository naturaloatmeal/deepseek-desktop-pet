# OpenClaw 可选连接器设计说明

## 当前决定

当前桌宠不捆绑、不自动安装、也不复制 OpenClaw 代码。应用启动等低风险能力由桌宠自身的安全白名单服务完成。这样可以保持 Windows 11 原生 WPF 部署，不要求普通用户安装 Node、WSL、Gateway 或额外后台服务。

## 为什么不直接把 OpenClaw 塞进 EXE

OpenClaw 是完整的个人智能代理和 Gateway，能力远超“打开一个应用”。其工具可以在获得权限后读写文件、访问网络、控制浏览器、发送消息或执行主机命令。把整套代理静默打包会扩大安装体积、供应链、后台进程、权限和隐私边界，也不符合本项目“EXE 只是启动入口、功能文件外置”的部署原则。

## 未来连接方式

建议把 OpenClaw 作为高级用户主动安装的独立后端，桌宠只实现一个可关闭的连接器：

1. 仅连接 `127.0.0.1` 回环地址，默认拒绝局域网和公网 Gateway。
2. 令牌存入 Windows 凭据管理器，不写入仓库、日志或普通配置。
3. 首次配对显示 Gateway 地址、身份和将要开放的能力。
4. 默认只开放聊天；文件、浏览器、消息、摄像头、屏幕和 `system.run` 分别授权。
5. 所有电脑执行继续经过桌宠本地允许列表和逐次确认，OpenClaw 文本不能直接变成 Shell。
6. 禁止默认 `security="full"` / `ask="off"`；建议执行为拒绝或允许列表并始终询问。
7. 提供立即断开、撤销令牌、查看操作日志和关闭连接器的入口。
8. 远程频道、插件和技能均视为独立供应链，启用前显示来源、版本和权限。

## 许可与发布

OpenClaw 当前采用 MIT License。仅通过协议连接用户独立安装的服务，和把其源代码或二进制包含进发行包，是不同的发布场景。若未来复制、修改、链接或分发 OpenClaw 代码，必须以实际采用版本为准重新审计，并保留其版权声明、MIT 许可文本和第三方通知。

参考：

- https://github.com/openclaw/openclaw
- https://github.com/openclaw/openclaw/blob/main/LICENSE
- https://docs.openclaw.ai/gateway/security
- https://docs.openclaw.ai/platforms/windows
