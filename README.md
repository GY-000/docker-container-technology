---
AIGC:
    Label: "1"
    ContentProducer: 001191440300708461136T1XGW3
    ProduceID: 4c9e4784caf78ea31f553070d9c20355_7e96c4b18e1c11f1bfea525400e6dd8f
    ReservedCode1: +NfDEfJWv8rt9Fmj0t2tr6Zus4loxtg3f/Q/RoQC8XnxuEmr/I3nxUhu8n6RrmJaplZba5BEtc3v3l0SdPUkBa7Ys/NW+/ihQ/GrlrQ3RGGRdzMvZv3BBtPEsdo6lsbJ9IWOL0aZs4ilKLHYB/SRgzo2WfL2eXbE5JWeOpCzJw/0sOKpOrm7lS/iG40=
    ContentPropagator: 001191440300708461136T1XGW3
    PropagateID: 4c9e4784caf78ea31f553070d9c20355_7e96c4b18e1c11f1bfea525400e6dd8f
    ReservedCode2: +NfDEfJWv8rt9Fmj0t2tr6Zus4loxtg3f/Q/RoQC8XnxuEmr/I3nxUhu8n6RrmJaplZba5BEtc3v3l0SdPUkBa7Ys/NW+/ihQ/GrlrQ3RGGRdzMvZv3BBtPEsdo6lsbJ9IWOL0aZs4ilKLHYB/SRgzo2WfL2eXbE5JWeOpCzJw/0sOKpOrm7lS/iG40=
---

# docker-container-technology

Docker 容器技术实践项目，包含镜像管理、多阶段构建、Harbor 私有仓库部署。

## 项目简介

基于 Docker / Docker Compose 容器化部署 OpenClaw + Ollama 本地大模型微信 AI 应答系统。
实现微信消息监听、本地大模型推理、自动化 AI 回复完整链路。
项目实践容器环境隔离、内网服务访问控制、敏感信息脱敏管控，贴合云原生安全、安全运维相关实践。

## 技术栈

| 层级 | 技术 |
|------|------|
| 操作系统 | CentOS Linux 7 |
| 容器引擎 | Docker + Docker Compose |
| AI 框架 | OpenClaw（微信消息中间件） |
| 大模型 | Ollama（本地推理）+ 百炼 API（云端模型） |
| 消息通道 | 微信消息接口 |

## 项目结构

```
docker-container-technology/
├── openclaw.json         # OpenClaw 核心配置（脱敏版）
├── DEPLOY.md             # 部署文档
└── README.md
```

## 快速开始

1. 安装 Docker 和 Docker Compose
2. 部署 Ollama 并加载模型
3. 配置 `openclaw.json`（填入 API Key 和微信账号信息）
4. 启动 OpenClaw 容器
5. 扫码登录微信，测试消息响应

> 详细步骤见 [DEPLOY.md](./DEPLOY.md)

## 项目成果

- 容器化统一运行环境，部署耗时由 1 小时缩短至 10 分钟
- 接口调用成功率 99.5%，单条消息平均响应延迟 ≤ 1s
- 整理全套故障解决方案，形成标准化部署流程

## 安全说明

- `openclaw.json` 中的 API Key、auth token 等敏感信息已脱敏，部署时替换为真实凭据
- 模型文件、运行会话缓存因安全与体积因素不纳入公开仓库

## 许可证

MIT License
