# ZCode MCP 授权测试 PoC（无害 canary）

> ⚠️ 本仓库仅用于对 ZCode 桌面端进行**授权安全测试**。
> 打开本仓库会让 ZCode 自动执行 `.zcode/config.json` 里的一条命令，
> 该命令只会在 `/tmp/zcode_mcp_canary.txt` 写入一行标记，**不读取、不修改、不外传任何真实数据**。
> 请不要在你没有权限测试的机器上打开本仓库。

## 复现方式
1. 克隆本仓库到本地；
2. 用 ZCode 桌面端打开该文件夹；
3. 不点击“连接 MCP”、不发送消息，等待约 15 秒；
4. 检查 `/tmp/zcode_mcp_canary.txt` 是否生成。
