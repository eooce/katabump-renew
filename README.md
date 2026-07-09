## 🚀 katabump 自动续期（GitHub Actions）

这是一个基于 GitHub Actions 的自动化脚本，用于定时登录自动续期[katabump](https://dashboard.katabump.com) 应用。

⚠️ 有cf盾,太垃圾的机房节点可能过不了，建议用稍微干净点的节点,[B2proxy住宅代理](https://www.b2proxy.com/signup?code=0F5133)

━━━━━━━━━━━━━━━━━━━━━━

🔐 Secrets 配置说明

| Secret 名称         | 是否必填 | 说明                                              |
|---------------------|----------|---------------------------------------------------|
| KATABUMP_EMAIL     | ✅ 必填  | katabump 登录邮箱                                    |
| KATABUMP_PASSWORD  | ✅ 必填  | katabump 登录密码                                    | 
| NODE_LINK          | ❌ 可选  | 代理链接，如 vless:// vmess:// tuic:// hysteria2:// anttls:// socks5://|
| TG_BOT_TOKEN       | ❌ 可选  | Telegram Bot Token（用于发送通知）                     |
| TG_CHAT_ID         | ❌ 可选  | Telegram Chat ID（接收通知的用户或群组 ID）              |

━━━━━━━━━━━━━━━━━━━━━━
### 代理格式（确认在v2rayN里使用正常的节点）

`NODE_LINK` 支持以下任意一种代理协议的完整分享链接（不配置则直连）：

- **VLESS**：`vless://uuid@server:port?security=reality&sni=...&type=ws&...`
- **VMess**：`vmess://base64encoded...`
- **Trojan**：`trojan://password@server:port?sni=...&type=ws&...`
- **tuic**：`tuic://uuid:password@server:port...`
- **anytls**：`anytls://uuid@server:port...`
- **hysteria2**：`hysteria2://base64@server:port...`
- **SOCKS5**：`socks5://user:pass@server:port` 或 `socks://user:pass@server:port`
