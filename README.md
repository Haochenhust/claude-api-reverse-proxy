# Claude API Reverse Proxy

一个部署在 Fly.io 上的 Claude 官方 API 反向代理服务，使用 Caddy 作为反向代理服务器。

## 功能

- 反向代理 `https://api.anthropic.com`
- 支持 Server-Sent Events (SSE) 流式响应
- 自动 HTTPS 重定向
- Fly.io 自动扩缩容

## 部署

本项目已配置为 Fly.io 部署，使用 `fly.toml` 配置文件。

### 快速开始

1. 安装 [flyctl](https://fly.io/docs/hands-on/install-flyctl/)
2. 登录 Fly.io: `flyctl auth login`
3. 部署: `flyctl deploy`

## 文件说明

- `Dockerfile` - 基于 Caddy 2 的 Docker 镜像
- `Caddyfile` - Caddy 反向代理配置
- `fly.toml` - Fly.io 部署配置

## License

MIT
