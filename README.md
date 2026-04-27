# 李文健

<div align="center">

**AI 应用与平台工程实践者**

聚焦 **RAG、Agent Workflow、知识系统、分类标引、情报处理平台、Kubernetes 平台工程与算力治理**

[![GitHub](https://img.shields.io/badge/GitHub-QEDQCD-181717?style=flat-square&logo=github)](https://github.com/QEDQCD)
[![Email](https://img.shields.io/badge/Email-594253850%40qq.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:594253850@qq.com)
[![OpenStack Review](https://img.shields.io/badge/OpenStack-Review-ED1944?style=flat-square&logo=openstack&logoColor=white)](https://review.opendev.org/q/liwenjian)

</div>

## 关于我

- 5 年开发经验，长期聚焦 **AI 应用工程、后端系统建设与云原生平台实践**，关注如何把模型能力落到真实业务流程中。
- 我擅长把 **检索、工作流、模型调用、权限体系、任务机制、部署交付** 打通，做成可上线、可维护、可持续迭代的工程系统。
- 过去的实践覆盖 **RAG 平台、分类与叙词服务、多 Agent 情报处理平台、Kubernetes 算力云平台、OpenStack 公有云与复杂业务平台**。
- 相比只停留在模型接入和 Prompt 调整，我更关注 **系统边界、链路可追踪性、质量控制、失败恢复、评估闭环与长期维护成本**。

## AI 工程能力

- **AI 应用系统化落地**：围绕 RAG、Agent Workflow、多模型接入与工具调用构建完整链路，关注可追踪、可回放、可干预，而不是只追求“调用成功”。
- **后端与平台整合能力**：能够把 AI 能力嵌入权限体系、租户隔离、任务编排、异步处理与管理后台，形成真正可运营的业务系统。
- **生产可用性与交付质量**：重视评估、日志、失败重试、结果校验、部署文档与线上排障，把 AI 系统做成可维护资产，而不是一次性 Demo。
- **云原生与资源治理背景**：具备 Kubernetes、资源调度、服务治理与平台工程经验，能从基础设施视角思考 AI 系统的伸缩性、可靠性与运行成本。

## 技术领域

- **AI 系统**：`RAG`、`Agent Workflow`、`LangGraph`、`LangChain`、`GraphRAG`、`MCP`、`Weaviate`、`RAGFlow`、`vLLM`
- **后端工程**：`Python`、`Go`、`Django`、`DRF`、`Flask`、`Gin`、`gRPC`、`MySQL`、`PostgreSQL`、`Redis`、`Elasticsearch`
- **平台与基础设施**：`Docker`、`Kubernetes`、`Kubebuilder`、`KubeVirt`、`Istio`、`Prometheus`、`OpenStack`
- **前端与交付**：`Vue 3`、`React`、`TypeScript`、`Vite`、`Umi`、`Playwright`、`Docker Compose`

## 代表性项目

### 1. AI Gateway

> 面向多模型接入、统一鉴权、调用观测与 RAG 能力整合的平台型 AI 网关

- **关键问题**：企业内部接入多家模型供应商时，不能把上游凭据直接暴露给业务方，也不能把 API Key 管理、模型路由、调用观测、审计追踪和知识库能力拆成彼此割裂的孤立系统。
- **我的实现**：基于 `Go`、`Python`、`React`、`PostgreSQL`、`Redis` 与 `RabbitMQ` 组织 `gateway`、`rag-service`、`web` 三个核心服务，打通平台 API Key 生命周期、模型代理路由、调用统计审计和 RAG 服务，并提供可直接部署的 Compose 方案。
- **工程价值**：把“接模型”升级为“管模型、管调用、管权限、管知识”的平台能力，体现了 AI 基础设施、平台治理和应用落地之间做系统整合的能力。

[项目地址](https://github.com/QEDQCD/ai_gateway)

### 2. 情报工坊 / Intelligence Workshop

> 面向情报采集、翻译、导入导出与交付流程的多租户业务平台

- **关键问题**：需要同时处理租户隔离、RBAC、采集任务管理、翻译流程编排、批量导入导出与失败重放，不能只做单点功能。
- **我的实现**：基于 `Django`、`DRF`、`Vue 3`、`PostgreSQL`、`Redis` 与 `Playwright` 搭建完整平台，并通过独立 `crawler_agent` 支持 RSS、Sitemap、HTML 列表页与动态页面抓取，形成“中心配置 + 边缘执行”的采集模式。
- **工程价值**：把情报采集、翻译、知识沉淀和交付流程整合成可运营系统，而不是离散脚本和人工流程。

[项目地址](https://github.com/QEDQCD/ai_translate)

### 3. RAGFlow 智能知识增强平台

> 面向复杂文档理解、知识库构建、检索增强生成与图谱推理的一体化平台

- **关键问题**：复杂文档解析、知识索引构建、混合检索、答案生成与图谱增强需要统一在同一套平台能力中，而不是分散在多个孤立模块里。
- **我的实现**：基于 `Python`、`Flask`、`React 18`、`TypeScript`、`Elasticsearch`、`GraphRAG` 与 `MCP` 打通文档解析、分块构建、索引管理、混合检索、图谱增强和 Web 管理台。
- **工程价值**：把 RAG 从单点问答接口升级为平台能力，支持 PDF、Office、图片等复杂文档处理，以及多步推理和工具化输出。

[项目地址](https://github.com/QEDQCD/INIS)

### 4. 分类与叙词服务

> 基于 LangGraph 的科技文献叙词标注与智能分类系统

- **关键问题**：分类与叙词并不是单次模型调用，而是涉及关键词抽取、知识库匹配、联网增强、LLM 验证、格式约束与失败兜底的多阶段工作流。
- **我的实现**：基于 `Django`、`DRF`、`LangGraph`、`Weaviate`、`RAGFlow`、`Volcano Ark` 与 `DashScope` 将叙词流程与分类流程分离设计，形成可追踪、可纠错、可扩展的链路。
- **工程价值**：通过多源检索融合、流程日志、结果纠错与结构化约束，将分类与叙词关键字段准确率从 **50% 提升到 85%**。

[项目地址](https://github.com/QEDQCD/inis_classify)

### 5. AI cloud

> 基于 Kubernetes 的算力调度与资源治理平台

- **关键问题**：企业级算力平台需要同时覆盖计算、网络、存储、调度、治理、Webhook、CRD/Controller 与交付体系，重点是平台能力建设，而不是单个接口开发。
- **我的实现**：基于 `Go`、`Gin`、`gRPC`、`Kubernetes`、`Kubebuilder`、`KubeVirt`、`Kube-OVN`、`Istio`、`Knative` 与 `Crossplane` 参与弹性伸缩、虚拟机生命周期、网络与网关、监控告警、资源治理等核心能力建设。
- **工程价值**：补足了我在 AI 系统之外的资源治理与平台工程背景，使我在设计 AI 系统时更重视伸缩性、可靠性与运行成本。

### 6. huangxudong-skill

> 面向 Codex / Agent 场景的人物视角 Skill，探索 Persona Skill Engineering 的可运行封装方式

- **关键问题**：如何把公开语料、表达风格、人物时间线与决策启发式沉淀成可复用、可调用的 Agent 能力，而不是停留在提示词堆叠。
- **我的实现**：围绕角色规则、表达 DNA、场景路由、研究资料与脚本工具构建可复用 Skill 包，支持更稳定的人物风格控制和任务适配。
- **工程价值**：这是我对 Persona Modeling、Prompt Engineering 与 Agent 可交付资产化的一次工程化探索。

[项目地址](https://github.com/QEDQCD/huangxudong-skill)

### 7. zhusujin-skill

> 面向《新三国》抽象影射机制的主题 Skill，探索“文风模仿”如何工程化为可运行的生成系统

- **关键问题**：如果只是模仿几句名场面台词，很容易停留在表层口癖复读，无法稳定完成“分析台词机制”“把现实事件改写成影射体”这类真实任务。
- **我的实现**：围绕任务路由、核心生成机制、表达 DNA 与研究资料构建完整 Skill 包，让 Agent 能先判断用户是在分析台词、生成台词，还是把现实权力关系改写成《新三国》式组织影射。
- **工程价值**：把一个高语境、强梗化的互联网文风，从“像不像”升级为“能不能稳定运行”的生成系统，体现了我在 Persona / Style Skill Engineering 与任务结构化设计上的持续探索。

[项目地址](https://github.com/QEDQCD/zhusujin-skill)

### 8. free-code

> 面向终端原生 AI Coding Agent 的可构建分叉，探索多提供方接入与能力扩展

- **关键问题**：AI Coding Agent 不只是模型切换，还涉及终端交互、后端适配、能力扩展与可审计构建链路。
- **我的实现**：基于 `TypeScript`、`Bun`、`React`、`Ink` 与多模型后端接入，完成 Codex 适配、UI 推理状态对齐，以及 agent / skill / bridge 的扩展实践。
- **工程价值**：这类项目体现了我对 AI Agent 运行机制、能力封装与开发者工具链的持续深入探索。

[项目地址](https://github.com/QEDQCD/free-code)

## 工程判断

- 我关注的不只是模型能否调用成功，而是 **检索质量、工作流可追踪性、结果一致性与系统可控性**。
- 我倾向于把 AI 能力封装成 **可测试、可观测、可回放、可持续优化** 的系统组件，而不是一次性脚本。
- 我在设计 AI 应用时，会同时考虑 **任务编排、权限边界、失败恢复、评估机制与长期维护成本**。
- 我重视的不只是“做出功能”，还包括 **部署、文档、排障、治理与持续交付能力**。

## 经验概览

- 当前主要方向是 **AI 应用工程与平台工程的结合**，包括知识系统、分类标引、情报处理平台和算力治理平台。
- 具备 **OpenStack 公有云、Kubernetes 平台、网络升级、网络安全靶场与复杂业务系统** 的持续工程经验。
- 长期关注 **AI 系统如何真正进入生产环境**，以及如何在复杂基础设施中保持稳定、可维护和可演进。

## 联系方式

- Email: `594253850@qq.com`
- GitHub: [QEDQCD](https://github.com/QEDQCD)
- OpenStack Review: [liwenjian](https://review.opendev.org/q/liwenjian)

---

<div align="center">

**我关注的不只是把模型接入业务，而是把 AI 能力沉淀为可评估、可运营、可持续迭代的工程系统。**

</div>
