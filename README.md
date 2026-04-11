# Hi, I'm 李文健

<div align="center">

**AI 应用工程师 / Python & Go 开发者 / 云原生工程实践者**

聚焦 **RAG、Multi-Agent、LangGraph、知识库系统、Kubernetes 平台工程、算力与调度系统**

[![GitHub](https://img.shields.io/badge/GitHub-QEDQCD-181717?style=flat-square&logo=github)](https://github.com/QEDQCD)
[![Email](https://img.shields.io/badge/Email-594253850%40qq.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:594253850@qq.com)
[![OpenStack Review](https://img.shields.io/badge/OpenStack-Review-ED1944?style=flat-square&logo=openstack&logoColor=white)](https://review.opendev.org/q/liwenjian)

</div>

## About Me

- 5 年开发经验，长期从事 **Python / Go 后端开发、AI 应用落地、云平台与 Kubernetes 相关工程建设**。
- 做过 **RAG 平台、叙词分类系统、多 Agent 情报处理平台、K8s 算力云平台、OpenStack 公有云、网络安全靶场**。
- 熟悉从 **需求分析、方案设计、接口开发、工作流编排、模型接入、部署上线、测试与文档沉淀** 的完整链路。
- 关注把 AI 能力做成可交付的工程系统，而不是只停留在 Demo 阶段。

## Focus Areas

<div align="center">

| Direction | What I Care About |
| --- | --- |
| AI Application Engineering | 把 RAG、Agent、工作流编排、多模型接入做成可落地系统 |
| Backend Architecture | 做清晰的接口边界、任务模型、权限体系和稳定的数据链路 |
| Cloud Native Platform | 在 Kubernetes 平台上建设调度、治理、可观测与自动化能力 |
| Engineering Delivery | 重视测试、文档、部署、排障和长期可维护性 |

</div>

## Tech Stack

### AI / LLM

![RAG](https://img.shields.io/badge/RAG-2F6BFF?style=flat-square)
![Multi-Agent](https://img.shields.io/badge/Multi--Agent-0F9D58?style=flat-square)
![LangGraph](https://img.shields.io/badge/LangGraph-121212?style=flat-square)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square)
![Dify](https://img.shields.io/badge/Dify-4F46E5?style=flat-square)
![MCP](https://img.shields.io/badge/MCP-FF6B35?style=flat-square)
![GraphRAG](https://img.shields.io/badge/GraphRAG-7B61FF?style=flat-square)
![RAGFlow](https://img.shields.io/badge/RAGFlow-009688?style=flat-square)
![Weaviate](https://img.shields.io/badge/Weaviate-00A98F?style=flat-square&logo=weaviate&logoColor=white)
![vLLM](https://img.shields.io/badge/vLLM-1F2937?style=flat-square)

### Backend / Infra

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![DRF](https://img.shields.io/badge/DRF-A30000?style=flat-square)
![Gin](https://img.shields.io/badge/Gin-008ECF?style=flat-square&logo=gin&logoColor=white)
![gRPC](https://img.shields.io/badge/gRPC-244C5A?style=flat-square)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Elasticsearch](https://img.shields.io/badge/Elasticsearch-005571?style=flat-square&logo=elasticsearch&logoColor=white)

### Frontend / Platform

![Vue 3](https://img.shields.io/badge/Vue%203-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![Umi](https://img.shields.io/badge/Umi-1677FF?style=flat-square)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Kubebuilder](https://img.shields.io/badge/Kubebuilder-326CE5?style=flat-square)
![KubeVirt](https://img.shields.io/badge/KubeVirt-FE6A16?style=flat-square)
![Istio](https://img.shields.io/badge/Istio-466BB0?style=flat-square&logo=istio&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![OpenStack](https://img.shields.io/badge/OpenStack-ED1944?style=flat-square&logo=openstack&logoColor=white)

## What I Build

### 1. 情报工坊 / Intelligence Workshop

> 多租户情报采集、翻译、导入导出一体化平台

- 技术栈：`Django` + `Django REST Framework` + `Vue 3` + `Vite` + `Pinia` + `PostgreSQL` + `Redis` + `Playwright` + `Docker`
- 工程特征：支持 **租户隔离、RBAC、采集任务管理、翻译任务编排、批量导入导出、质量评估、失败重放**
- 亮点：独立 `crawler_agent` 支持 **RSS / Sitemap / HTML 列表页 / 动态页面抓取**，形成“中心配置 + 边缘执行”的采集模式
- 方向：把情报采集、翻译、知识沉淀和交付流程做成可运营的平台

[Repository](https://github.com/QEDQCD/ai_translate)

### 2. RAGFlow智能知识增强平台

> 面向复杂文档理解、知识库构建、检索增强生成与图谱推理的一体化平台

- 技术栈：`Python` + `Flask` + `Peewee` + `React 18` + `Umi 4` + `TypeScript` + `Elasticsearch` + `GraphRAG` + `MCP` + `Docker Compose`
- 工程特征：统一打通 **复杂文档解析、分块构建、知识索引、混合检索、答案生成、图谱增强、Web 管理台**
- 亮点：支持 **PDF / Office / 图片等复杂文档处理**，并具备 **GraphRAG、多步推理、MCP 工具化输出**
- 方向：把 RAG 做成平台能力，而不是单点问答接口

[Repository](https://github.com/QEDQCD/INIS)

### 3. 分类与叙词服务

> 基于 LangGraph 的科技文献叙词标注与智能分类系统

- 技术栈：`Django` + `DRF` + `LangGraph` + `Weaviate` + `RAGFlow` + `Volcano Ark` + `DashScope`
- 工程特征：围绕 **关键词抽取 -> 知识库匹配 -> 联网增强 -> LLM 验证 -> 格式约束** 建立可追踪工作流
- 亮点：叙词流程与分类流程分离设计，支持 **多级分类、结果纠错、流程日志、失败兜底、多源检索融合**
- 成果：分类与叙词关键字段准确率从 **50% 提升到 85%**

[Repository](https://github.com/QEDQCD/inis_classify)

### 4.  AI cloud

> 基于 Kubernetes 的算力调度与资源治理平台

- 技术栈：`Go` + `Gin` + `GORM` + `gRPC` + `Kubernetes` + `Kubebuilder` + `KubeVirt` + `Kube-OVN` + `Istio` + `Knative` + `Crossplane`
- 工程特征：覆盖 **计算、网络、存储、商城、调度、治理、Webhook、CRD/Controller、Kustomize 交付**
- 亮点：参与 **弹性伸缩、虚拟机生命周期、网络与网关、监控告警、资源治理** 等平台能力建设
- 方向：面向企业级算力云平台的系统化工程实践

## Engineering Keywords

- **AI 应用工程化**：Prompt 设计、多模型接入、工作流编排、Agent 协作、RAG 链路落地
- **平台后端开发**：RESTful API、RPC/gRPC、权限设计、租户隔离、异步任务、状态机
- **云原生与基础设施**：Kubernetes、CRD / Operator、KubeVirt、服务治理、弹性伸缩、可观测性
- **复杂系统交付**：Docker / Compose、CI/CD、测试用例、部署文档、问题排查与线上迭代

## Experience Snapshot

- 当前主要方向是 **AI 应用 + 云平台工程** 的结合，包括知识库系统、分类标引、情报处理平台和算力云平台。
- 有 **OpenStack 公有云、网络升级、K8s 平台、网络安全攻防靶场、大数据平台** 等复杂项目经验。
- 参与过 OpenStack 社区问题修复与代码贡献，也长期重视测试、文档和工程规范。

## Contact

- Email: `594253850@qq.com`
- GitHub: [QEDQCD](https://github.com/QEDQCD)
- OpenStack Review: [liwenjian](https://review.opendev.org/q/liwenjian)

---

<div align="center">

**把 AI 能力做成稳定、可维护、可交付的工程系统。**

</div>
