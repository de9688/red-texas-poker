# Browser Tools MCP 配置指南

## 配置方法

将以下配置添加到您的 `.cursor/mcp.json` 文件中：

```json
{
  "mcpServers": {
    "github-mcp": {
      "command": "cmd",
      "args": [
        "/c",
        "npx",
        "-y",
        "@modelcontextprotocol/server-github"
      ],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "你的GitHub令牌"
      },
      "disabled": false,
      "autoApprove": []
    },
    "browser-tools": {
      "command": "cmd",
      "args": [
        "/c",
        "npx",
        "-y",
        "@modelcontextprotocol/server-browser"
      ],
      "env": {
        "BROWSER_API_KEY": "你的浏览器API密钥(如果有)"
      },
      "disabled": false,
      "autoApprove": ["search", "navigate", "screenshot", "read_page"]
    }
  }
}
```

## 浏览器工具功能

Browser Tools MCP服务器提供以下功能：

1. **网页搜索** - 在网络上搜索信息
2. **网页浏览** - 访问特定网址
3. **网页截图** - 捕获网页快照
4. **读取网页内容** - 提取网页文本内容

## 注意事项

- 部分功能可能需要额外的API密钥
- `autoApprove` 数组包含无需手动确认的操作
- 首次使用时可能需要接受浏览器权限提示
- 确保Cursor有适当的网络访问权限

## 使用示例

配置完成后，可以在Cursor中使用以下命令：

- "搜索关于德州扑克的信息"
- "访问 https://github.com/de9688/red-texas-poker"
- "查看德州扑克规则页面"