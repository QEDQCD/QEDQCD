# 李文健

<div align="center">

后端与 AI 应用工程 · 近期主要做模型接入治理与情报采集

[![GitHub](https://img.shields.io/badge/GitHub-QEDQCD-181717?style=flat-square&logo=github)](https://github.com/QEDQCD)
[![Email](https://img.shields.io/badge/Email-594253850%40qq.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:594253850@qq.com)
[![OpenStack Review](https://img.shields.io/badge/OpenStack-Review-ED1944?style=flat-square&logo=openstack&logoColor=white)](https://review.opendev.org/q/liwenjian)

</div>

## 关于我

5 年开发经验，主要做 AI 应用工程、后端系统与云原生平台。主导过 AI 网关、情报采集平台、远程编码工具、RAG 助理、智能分类与算力平台等项目，从架构设计到核心开发与交付。

## 能力要点

- 主导设计并实现企业侧多模型接入：统一鉴权、路由、调用观测、API Key 与费用配额（AI 网关）。
- 主导设计并实现 RAG / Agent 相关系统：文档解析、混合检索、GraphRAG、LangGraph 工作流与工具调用。
- 有 Kubernetes 与 OpenStack 背景，能从部署、观测和资源成本角度看 AI 系统。

## 技术栈

- AI：`RAG`、`LangGraph`、`LangChain`、`GraphRAG`、`MCP`、`Weaviate`、`RAGFlow`、`vLLM`
- AI Coding：`Claude Code`、`Codex CLI`、`Cursor`、`Skills`、`stream-json`
- 后端：`Python`、`Go`、`Django`、`DRF`、`Flask`、`Gin`、`gRPC`、`MySQL`、`PostgreSQL`、`Redis`、`Elasticsearch`
- 平台与前端：`Docker`、`Kubernetes`、`Kubebuilder`、`KubeVirt`、`Istio`、`Prometheus`、`OpenStack`、`Vue 3`、`React`、`TypeScript`

## 代表性项目

### AI Gateway

企业内部接入多家模型时，不宜把上游凭据直接交给业务方，也不宜把鉴权、路由、观测、审计和知识库拆成互不相关的系统。

主导架构与核心开发：用 `Go`、`Python`、`React`、`PostgreSQL`、`Redis`、`RabbitMQ` 拆成 `gateway`、`rag-service`、`web` 三个服务，覆盖平台 API Key 生命周期、模型代理路由、调用统计审计和 RAG，并提供 Compose 部署方案。

- 控制台：`http://8.162.21.158:31873`（安全组 IP 白名单，访问前需申请放行）
- [项目地址](https://github.com/QEDQCD/ai_gateway)

### 多源信息采集与智能处理平台（情报工坊）

多源情报（Web Search、爬虫、结构化数据源、社交平台）接入方式不同，需要统一入库、翻译、质量监控与业务域分析。

主导整体方案与核心模块开发：用 `Django`、`DRF`、`Vue 3`、`TypeScript`、`PostgreSQL`、`Redis` 做中心编排，采用「中心配置 + 边缘执行」——中心维护采集任务、Web Search Provider、`push-data` 入库与状态机；边缘 `crawler_agent` 跑 RSS / Sitemap / Playwright。另有多引擎翻译（LLM + Google/Baidu 兜底）、PDF OCR（MinerU + 视觉 LLM）、汽车情报（MIIT / 懂车帝 / CPCA / CAAM）与场景库（小红书 MCP + B 站 → LLM → 飞书推送）等模块。汽车场景库链路已实测通过。

[项目地址](https://github.com/QEDQCD/ai_translate)

### cc-go / codex-go

Claude Code、Codex 交互通常绑在本机终端，离开电脑后不便审批工具权限、看回复和切会话。

主导设计并实现两套工具及共用的远程桥接架构：`Go` + `React` + `Gin` + WeChat Bot API，经 `stream-json` 对接 CLI，覆盖微信收发、权限审批、会话管理、Web 控制台与多平台发版；cc-go 另支持 Skills 自动注入，codex-go 侧重 Docker 化部署。

- cc-go Web：`http://8.162.21.158:18080`（IP 白名单，需申请放行）· [项目地址](https://github.com/QEDQCD/cc-go)
- codex-go Web：`http://8.162.21.158:44262`（IP 白名单，需申请放行）· [项目地址](https://github.com/QEDQCD/codex-go)

### 基于 RAG 的智能助理平台（INIS）

复杂文档解析、知识索引、混合检索、答案生成与图谱增强需要收在同一套能力里。

主导设计并实现：用 `Python`、`Flask`、`React 18`、`TypeScript`、`Elasticsearch`、`GraphRAG`、`MCP` 打通文档解析、分块、索引、混合检索、图谱增强与 Web 管理台，做成可复用的 RAG 平台组件，而不是单点问答接口。

[项目地址](https://github.com/QEDQCD/INIS)

### 其他

- [claude-token-stats](https://github.com/QEDQCD/claude_token_stats)：本机统计 Claude Code / Codex CLI 的 token 用量（按天/周/月）
- [claude-auto-approve](https://github.com/QEDQCD/claude-auto-approve)：Claude Code `PreToolUse` hook，白名单自动放行、危险命令强制确认
- [智能分类服务](https://github.com/QEDQCD/inis_classify)：基于 LangGraph 的分类 Agent（检索、验证、格式约束与失败兜底）
- AI cloud：基于 Kubernetes 的算力调度与资源治理（`Kubebuilder`、`KubeVirt`、`Istio` 等）

## 联系方式

- Email: `594253850@qq.com`
- GitHub: [QEDQCD](https://github.com/QEDQCD)
- OpenStack Review: [liwenjian](https://review.opendev.org/q/liwenjian)
