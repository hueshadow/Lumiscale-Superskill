# AI API 反代/网关/中转 工具大全（2026.05）

> 来源：[X/Twitter @laozhang2579（老张来了）](https://x.com/laozhang2579/status/2053301954286064058)
> 整理时间：2026-05-12
> 整理类型：资源聚合 + 分类索引
> 来自hueshadow

---

## 简介

@laozhang2579 整理了一份 AI API 反代/网关/中转赛道的完整清单，涵盖 **8 大类、25+ 个项目**。这份清单覆盖了从 Claude 到 Gemini、从 ChatGPT 到 Copilot 的全生态逆向方案，是当前 AI CLI 工具包装成标准化 API 的行业全景图。

---

## 一、综合型多协议网关

将多种 AI CLI 工具统一包装成 OpenAI/Gemini/Claude/Codex 兼容 API 的网关项目。

### 1. CLIProxyAPI
- **定位**：赛道标杆
- **功能**：把 Gemini CLI、Antigravity、ChatGPT Codex、Claude Code、Qwen Code、iFlow 包装成 OpenAI/Gemini/Claude/Codex 兼容的 API 服务
- **亮点**：覆盖面最广的多协议网关

### 2. AIClient-2-API
- **技术栈**：Node.js
- **功能**：通过模拟 Gemini CLI、Antigravity、Codex、Grok、Kiro 的客户端请求，封装成本地 OpenAI 兼容接口
- **亮点**：2026 年初加入 Grok 的 Cookie/SSO 逆向，目前对 Grok 支持最完整

### 3. Antigravity-Manager
- **技术栈**：Tauri + React（桌面客户端）
- **功能**：把 Google/Anthropic 的 Web Session 转成标准化 API 接口
- **特色**：带 OAuth 链接生成和账号池调度
- **适用场景**：「账号管家」类内容创作

### 4. 9router / OmniRoute
- **定位**：智能路由 + 多档 fallback
- **关系**：OmniRoute 是 9router 的 TypeScript fork
- **亮点**：iFlow、Kiro、Qwen 被标为 FREE 的为真免费无限，通过 OAuth 和 device auth 接入

### 5. ccproxy-api
- **技术栈**：Python
- **功能**：直接复用 Claude CLI SDK tokens 和 Codex CLI 的 credential store
- **亮点**：插件系统干净

### 6. CliGate
- **功能**：带可视化 Dashboard
- **支持**：ChatGPT Account Pool、Claude Account Pool OAuth PKCE login、Antigravity Account Pool
- **亮点**：一键配置 CLI 工具

---

## 二、Claude 专项

### 7. claude-relay-service
- **定位**：国内最火的 Claude 中转方案
- **功能**：集成 Anthropic 的 OAuth 授权流程，Web 界面点击 Add Account 生成授权链接，登录 Claude 账号授权后接入服务
- **适用场景**：拼车党的基础设施，教程必讲

### 8. ClewdR
- **技术栈**：Rust
- **覆盖平台**：Linux/macOS/Windows/Android（单一静态二进制）
- **功能**：支持 Claude 网页和 Claude Code
- **特色**：Docker 镜像齐全，带 React 管理界面
- **定位**：性能路线代表

### 9. claude-code-proxy
- **定位**：Claude Code 转 OpenAI 的经典实现
- **适用场景**：教程中讲「双向转换」的基础案例

### 10. claude-relay（npow）
- **思路**：直接起一个 `claude -p` 进程来代理，而不是逆向协议
- **差异点**：与主流逆向路线不同，走进程代理路线

### 11. claude-unofficial-api / unofficial-claude-api（st1vms）
- **定位**：更早期的纯 Session Key 逆向方案
- **技术栈**：前者 JS、后者 Python
- **适用场景**：教程中讲「历史演进」

### 12. Claude Code Action with OAuth
- **功能**：官方 Claude Code Action 的 fork，支持 OAuth 认证
- **亮点**：让 Claude Max 订阅者在 GitHub Actions 里使用订阅

### 13. opencode-claude-auth
- **路线**：Keychain 路线
- **功能**：从 macOS Keychain 读取 Claude Code OAuth credentials
- **亮点**：支持多账号自动检测

---

## 三、ChatGPT / Codex 专项

### 14. PawanOsman/ChatGPT
- **定位**：元老级项目
- **亮点**：把逆向成本打到几乎为零

### 15. acheong08/ChatGPT（revChatGPT）
- **定位**：逆向 ChatGPT Web 的祖师爷仓库
- **历史意义**：奠定了 ChatGPT Web 逆向的技术基础

### 16. codexProxy（J1aDong/codexProxy）
- **方向**：把 Codex 包成 Anthropic Messages 入口
- **语境**：@laozhang2579 提到"你自己做的那个方向"，说明 codexProxy 作者与发布者有交集

---

## 四、Gemini 专项

### 17. gemini-proxy（KashifKhn）
- **技术栈**：Bun + Hono + TypeScript
- **认证**：OAuth 2.0 + PKCE 浏览器登录，自动刷新 token
- **亮点**：不需要付费 API key，不需要 gcloud CLI，目前最干净的实现

### 18. 三大竞品
| 项目 | 作者 | 特点 |
|------|------|------|
| gemini-openai-proxy | Brioch | — |
| gemini-cli-proxy | ubaltaci | — |
| geminicli2api | gzzhongqi | — |

### 19. openai-gemini（PublicAffairs）
- **路线**：Serverless
- **部署**：可直接部署到 Vercel/Cloudflare Workers
- **适用场景**：讲部署的必备案例

---

## 五、Copilot 专项

### 20. copilot-proxy（hankchiutw）
- **功能**：简单 HTTP 代理，把 GitHub Copilot 的免费额度暴露成 OpenAI 兼容 API
- **亮点**：思路清晰

### 21. github-copilot-proxy（BjornMelin）
- **方向**：反向——让 Cursor 调 Copilot 的后端
- **用途**：绕过 Cursor 的 500 次 premium 限制

### 22. copilot-proxy（lutzleonhardt）
- **路线**：VS Code 插件
- **方式**：通过 Language Model API 暴露
- **亮点**：思路很野

---

## 六、Kiro / Qwen / Grok 逆向

### 23. kiro-gateway（jwadow/kiro-gateway）
- **功能**：Kiro IDE / Amazon Q Developer 的网关
- **核心价值**：免费白嫖 Claude 模型

### 24. Qwen-Copilot-Proxy（edwardgj）
- **方式**：伪装成 Ollama 接口对接 Copilot Chat
- **亮点**：思路巧妙

### 25. GrokProxy（CNFlyCat）
- **路线**：Cookie 路线
- **方式**：从开发者工具 Network 面板抓 `sso=` 开头的 cookie 配置进 cookies.yaml
- **适用场景**：教程中讲 Cookie 型反代的标本案例

---

## 七、Cursor 专项

### 26. Cursor-To-OpenAI（JiuZ-Chn/Cursor-To-OpenAI）
- **功能**：把 Cursor 编辑器的 AI Chat 包成 OpenAI
- **认证方式**：从 Cursor 客户端 cookie（`user_` 开头）提取认证，网页 cookie 不能用
- **教学价值**：「客户端 Cookie vs 网页 Cookie 差异」的绝佳案例

---

## 八、逆向号池 + 商用平台

### 27. FakeOAI/tokens
- **定位**：商用级别
- **功能**：轮训号池将各大平台的模型能力转化为 OpenAI、Anthropic、Gemini 等平台的 API 接口标准格式
- **支持**：Claude Code、Codex、GeminiCli 等终端调用

---

## 项目技术路线速查

| 路线 | 代表项目 | 核心思路 |
|------|----------|----------|
| **多协议网关** | CLIProxyAPI、AIClient-2-API | 包装多种 CLI 工具为统一 API |
| **OAuth 路线** | claude-relay-service、gemini-proxy | 通过 OAuth 授权获取合法 token |
| **Session Key 逆向** | claude-unofficial-api | 提取 Web Session Key 冒充客户端 |
| **Cookie 路线** | GrokProxy、Cursor-To-OpenAI | 从浏览器/客户端抓 Cookie 认证 |
| **Keychain 路线** | opencode-claude-auth | 从系统 Keychain 读取已存凭证 |
| **进程代理** | claude-relay（npow） | 直接起 CLI 进程来代理请求 |
| **Serverless** | openai-gemini | 部署到 Vercel/Cloudflare Workers |
| **号池商用** | FakeOAI/tokens | 轮训号池实现商业级别可用性 |

---

## 场景化内容选题建议（@laozhang2579 的提示）

| 场景 | 推荐案例 | 教学价值 |
|------|----------|----------|
| 账号管家 | Antigravity-Manager | OAuth 链接生成 + 账号池调度 |
| Cookie 型反代 | GrokProxy | 从开发者工具抓 Cookie 的完整流程 |
| 双向转换 | claude-code-proxy | Claude Code ↔ OpenAI 互转 |
| 历史演进 | claude-unofficial-api → ClewdR | Session Key 逆向 → Rust 性能路线的演进 |
| 客户端 vs 网页 Cookie | Cursor-To-OpenAI | `user_` cookie vs 网页 cookie 的差异 |

---

## 风险提示

⚠️ 本文档仅作为技术整理和行业观察，所列项目涉及 API 逆向、账号共享等行为，可能违反对应平台的服务条款。使用者需自行评估合规风险。

---

*来自hueshadow*
