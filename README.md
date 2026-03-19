# 🛠️ 开发工具包 (Dev Toolkit)

一个面向开发者的网络调试工具集，基于纯 HTML + JavaScript 实现，无需安装，打开即用。

## 功能模块

### 📡 网络

| 工具 | 说明 |
|------|------|
| [WebSocket 调试](network/websocket.html) | WebSocket 连接调试工具，支持连接/断开、发送消息、消息日志、历史接口记录 |
| [SSE 调试](network/sse.html) | Server-Sent Events 调试工具，支持 GET/POST/PUT 请求方式、自定义 Headers、请求体配置、历史记录 |

## 特性

- **零依赖**：纯 HTML + CSS + JavaScript，无需构建，无需安装任何依赖
- **历史记录**：基于 `localStorage` 保存历史接口，方便快速复用
- **移动端适配**：响应式侧边栏，支持移动端使用
- **多标签页**：支持通过 ↗ 按钮在新窗口独立打开单个工具

## 使用方式

直接用浏览器打开 `index.html` 即可，无需启动任何服务器。

```bash
# 克隆仓库
git clone https://gitee.com/candy/dev-toolkit.git

# 用浏览器打开入口页
open index.html
```

## 项目结构

```
dev-toolkit/
├── index.html          # 主入口，带侧边栏导航
└── network/
    ├── websocket.html  # WebSocket 调试工具
    └── sse.html        # SSE 调试工具
```

## WebSocket 调试工具

- 输入 WebSocket 服务器地址（如 `ws://localhost:8080`）
- 支持连接、断开、发送消息
- 消息日志按类型区分显示（发送/接收/错误/信息）
- `Ctrl+Enter` 快速发送消息
- 自动保存最近 10 条历史地址

## SSE 调试工具

- 支持 GET / POST / PUT 请求方式
- 支持自定义请求头（Headers）
- 支持请求体（Body）配置
- 历史记录按 URL 分组，同一 URL 下保存多套请求配置
- 实时展示服务端推送的事件消息
