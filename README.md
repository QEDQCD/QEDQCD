# 李文健

<div align="center">

**AI 应用与平台工程实践者**

聚焦 **RAG、Agent Workflow、AI Coding、信息采集、知识系统、多模型治理、Kubernetes 平台工程与算力治理**

[![GitHub](https://img.shields.io/badge/GitHub-QEDQCD-181717?style=flat-square&logo=github)](https://github.com/QEDQCD)
[![Email](https://img.shields.io/badge/Email-594253850%40qq.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:594253850@qq.com)
[![OpenStack Review](https://img.shields.io/badge/OpenStack-Review-ED1944?style=flat-square&logo=openstack&logoColor=white)](https://review.opendev.org/q/liwenjian)

</div>

## 关于我

- 5 年开发经验，长期聚焦 **AI 应用工程、后端系统建设与云原生平台实践**，关注如何把模型能力落到真实业务流程中。
- 擅长把 **检索、工作流、模型调用、权限体系、任务机制、部署交付** 打通，做成可上线、可维护、可持续迭代的工程系统。
- 主导并深度参与 **AI 网关**、**编码工具微信端代理**、**token 消耗**、**智能助理**、**智能分类Agent**、**自动采集Agent**、**算力平台** 与 **开源云平台** 等系统从设计到交付的全链路工程落地。
- 工作重点是 **系统边界、链路可追踪性、质量控制、失败恢复、评估闭环与长期维护成本**。

## AI 工程能力

- **AI 应用系统化落地**：围绕 RAG、Agent Workflow、多模型接入与工具调用构建完整链路，覆盖可追踪、可回放、可干预。
- **AI Coding 与 Harness Engineering**：研读 Claude Code CLI 源码，理解 Harness Agent 架构（TAOR 循环、工具调用、MCP、Skills、Memory、Context 压缩与权限门控）；日常以 Cursor、Claude、Codex 结合 vibe coding 与 Harness/Loop Engineering 范式推进开发与交付；编码工具微信端代理将 Claude Code、Codex CLI 从本机终端扩展到微信与 Web，支持远程审批、会话管理与输出推送。
- **企业级模型接入治理**：AI 网关提供 OpenAI 兼容统一出口，覆盖租户审批、平台 API Key 生命周期、多上游路由、调用观测与费用配额。
- **后端与平台整合能力**：能够把 AI 能力嵌入权限体系、租户隔离、任务编排、异步处理与管理后台，形成可运营的业务系统。
- **生产可用性与交付质量**：重视评估、日志、失败重试、结果校验、部署文档与线上排障，把 AI 系统做成可维护资产。
- **云原生与资源治理背景**：具备 Kubernetes、资源调度、服务治理与平台工程经验，能从基础设施视角思考 AI 系统的伸缩性、可靠性与运行成本。

## 技术领域

- **AI 系统**：`RAG`、`Agent Workflow`、`LangGraph`、`LangChain`、`GraphRAG`、`MCP`、`Weaviate`、`RAGFlow`、`vLLM`
- **AI Coding / Harness**：`Claude Code`、`Codex CLI`、`Harness Engineering`、`Skills`、`Cursor`、`stream-json`、权限门控
- **后端工程**：`Python`、`Go`、`Django`、`DRF`、`Flask`、`Gin`、`gRPC`、`MySQL`、`PostgreSQL`、`Redis`、`Elasticsearch`
- **平台与基础设施**：`Docker`、`Kubernetes`、`Kubebuilder`、`KubeVirt`、`Istio`、`Prometheus`、`OpenStack`
- **前端与交付**：`Vue 3`、`React`、`TypeScript`、`Vite`、`Umi`、`Playwright`、`Docker Compose`

## 代表性项目

### 1. AI Gateway

> 面向多模型接入、统一鉴权、调用观测与 RAG 能力整合的平台型 AI 网关

- **关键问题**：企业内部接入多家模型供应商时，不能把上游凭据直接暴露给业务方，也不能把 API Key 管理、模型路由、调用观测、审计追踪和知识库能力拆成彼此割裂的孤立系统。
- **我的实现**：基于 `Go`、`Python`、`React`、`PostgreSQL`、`Redis` 与 `RabbitMQ` 组织 `gateway`、`rag-service`、`web` 三个核心服务，打通平台 API Key 生命周期、模型代理路由、调用统计审计和 RAG 服务，并提供可直接部署的 Compose 方案。
- **工程价值**：提供统一的模型接入底座，覆盖模型治理、调用管控、权限隔离与知识服务集成，支撑企业多租户 AI 能力的平台化落地。
- **公网访问**：
  - 控制台前端：`http://8.162.21.158:31873`
  - 公网入口已配置安全组来源 IP 白名单限制，访问前需要先申请放行。

[项目地址](https://github.com/QEDQCD/ai_gateway)

### 2. cc-go

> 通过微信机器人接管 Claude Code 会话，并提供 Web 管理面板与多平台发版的远程编码工具

- **关键问题**：Claude Code 交互通常绑定在本机终端，离开电脑后难以及时审批工具权限、查看回复和切换会话。
- **我的实现**：基于 `Go`、`React`、`Gin` 与 `WeChat Bot API`，通过 `stream-json` 协议桥接 Claude Code CLI，整合微信消息收发、权限审批、会话管理、Skills 自动注入、Web 控制台与 Bot API。
- **工程价值**：将 Claude Code 从本机终端扩展为可远程接入、可移动审批、可部署交付的工程化工具，与 codex-go 共用同一套远程桥接架构。
- **公网访问**：
  - Web 管理台：`http://8.162.21.158:18080`
  - 公网入口已配置安全组来源 IP 白名单限制，访问前需要先申请放行。

[项目地址](https://github.com/QEDQCD/cc-go)

### 3. codex-go

> 通过微信机器人接管 Codex 会话，并提供 Web 与 Docker 化部署能力的远程编码工具

- **关键问题**：Codex 交互通常绑定在本机终端，无法在移动端自然地审批权限、查看回复和切换会话。
- **我的实现**：基于 `Go`、`React`、`Gin`、`Docker` 与 `WeChat Bot API`，把 Codex 会话管理、微信消息收发、Web 控制台和多平台发版流程整合成一个可部署项目。
- **工程价值**：将 Codex 从本机终端扩展为可远程接入、可多端协同、可 Docker 化部署的工程化工具，覆盖 Agent 会话控制、终端接入适配与完整交付链路。
- **公网访问**：
  - Web 管理台：`http://8.162.21.158:44262`
  - 公网入口已配置安全组来源 IP 白名单限制，访问前需要先申请放行。

[项目地址](https://github.com/QEDQCD/codex-go)

### 4. 多源信息采集与智能处理平台

> 情报工坊（Intelligence Workshop），覆盖采集、解析、翻译、入库、监控与交付全链路

- **关键问题**：多源情报（Web Search、爬虫、结构化数据源、社交平台）接入方式各异，需统一入库、翻译、质量监控与业务域分析，不能拆成彼此割裂的脚本与单点工具。
- **我的实现**：基于 `Django`、`DRF`、`Vue 3`、`TypeScript`、`PostgreSQL` 与 `Redis` 搭建中心编排平台，采用"中心配置 + 边缘执行"模式——中心侧维护采集任务、Web Search Provider、`push-data` 入库与状态机，边缘侧 `crawler_agent` 独立运行 RSS/Sitemap/Playwright 抓取；落地多引擎翻译（LLM + Google/Baidu 兜底）、PDF OCR（MinerU + 视觉 LLM）、汽车情报（MIIT/懂车帝/CPCA/CAAM）与场景库（小红书 MCP + B 站 → LLM 提炼 → 飞书推送）等业务模块。
- **工程价值**：打通 Web Search / 爬虫 Agent / 结构化数据源三类采集入口，统一收敛到自动翻译与导入导出链路；汽车场景库全链路实测通过，场景卡片可沉淀为可检索、可复盘、可交付的结构化情报资产。

[项目地址](https://github.com/QEDQCD/ai_translate)

### 5. claude-token-stats

> 面向 Claude Code 的 token 用量自动记录与多维度统计 skill，支持自然语言触发查询

- **关键问题**：Claude Code 会话结束后 token 消耗分散在 transcript 中，缺少按天/周/月、按 session、按模型的可查询汇总，难以评估使用成本与优化方向。
- **我的实现**：基于 `Python` 与 Claude Code Stop hook，在每次会话结束时自动提取 assistant 消息的 `usage` 字段并去重写入 `~/.claude/token_usage.jsonl`，提供按天/周/月分桶、本地时区转换、session/模型/日期区间过滤及定价估算等统计脚本。
- **工程价值**：将 token 用量从不可见的会话细节转化为可查询、可对比、可追踪的本地数据资产，导入 skill 后可直接用自然语言问「本月用了多少 token」「哪个 session 最费 token」。

[项目地址](https://github.com/QEDQCD/claude_token_stats)

### 6. 基于RAG的智能助理平台

> 面向复杂文档理解、知识库构建、检索增强生成与图谱推理的一体化平台

- **关键问题**：复杂文档解析、知识索引构建、混合检索、答案生成与图谱增强需要收敛到同一套平台能力中。
- **我的实现**：基于 `Python`、`Flask`、`React 18`、`TypeScript`、`Elasticsearch`、`GraphRAG` 与 `MCP` 打通文档解析、分块构建、索引管理、混合检索、图谱增强和 Web 管理台。
- **工程价值**：把 RAG 能力从单点问答接口提升为可复用平台组件，支持复杂文档解析、混合检索增强、多步推理与工具化结果输出。

[项目地址](https://github.com/QEDQCD/INIS)

### 7. 智能分类服务

> 基于 LangGraph 的智能分类Agent

- **关键问题**：智能分类涵盖关键词抽取、知识库匹配、联网增强、LLM 验证、格式约束与失败兜底等多阶段工作流。
- **我的实现**：基于 `Django`、`DRF`、`LangGraph`、`Weaviate`、`RAGFlow`、`Volcano Ark` 与 `DashScope` 组织分类工作流，形成可追踪、可纠错、可扩展的链路。
- **工程价值**：通过多源检索融合、流程可观测、结果纠错与结构化约束，提升智能分类任务的关键字段准确率，并形成可扩展的质量优化闭环。

[项目地址](https://github.com/QEDQCD/inis_classify)

### 8. AI cloud

> 基于 Kubernetes 的算力调度与资源治理平台

- **关键问题**：企业级算力平台需要同时覆盖计算、网络、存储、调度、治理、Webhook、CRD/Controller 与交付体系，以平台能力建设为主。
- **我的实现**：基于 `Go`、`Gin`、`gRPC`、`Kubernetes`、`Kubebuilder`、`KubeVirt`、`Kube-OVN`、`Istio`、`Knative` 与 `Crossplane` 参与弹性伸缩、虚拟机生命周期、网络与网关、监控告警、资源治理等核心能力建设。
- **工程价值**：提供覆盖计算、网络、存储与调度的算力治理能力，为上层业务系统提供弹性伸缩、可靠性保障与成本控制基础。

## 工程判断

- 设计 AI 系统时，会同时看 **检索质量、工作流可追踪性、结果一致性与系统可控性**。
- 倾向把 AI 能力封装成 **可测试、可观测、可回放、可持续优化** 的系统组件。
- 做 AI 应用时会考虑 **任务编排、权限边界、失败恢复、评估机制与长期维护成本**。
- 交付时会覆盖 **部署、文档、排障、治理与持续交付**。

## 经验概览

- 当前主要方向是 **AI 应用工程与平台工程的结合**，包括知识系统、信息采集、情报处理平台、AI Coding 和算力治理平台。
- 具备 **OpenStack 公有云、Kubernetes 平台、网络升级、网络安全靶场与复杂业务系统** 的持续工程经验。
- 长期关注 **AI 系统如何真正进入生产环境**，以及如何在复杂基础设施中保持稳定、可维护和可演进。

## 联系方式

- Email: `594253850@qq.com`
- GitHub: [QEDQCD](https://github.com/QEDQCD)
- OpenStack Review: [liwenjian](https://review.opendev.org/q/liwenjian)

---

<div align="center">

**把 AI 能力沉淀为可评估、可运营、可持续迭代的工程系统。**

</div>
