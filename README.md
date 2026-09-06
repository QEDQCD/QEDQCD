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
- 主导设计并实现智能汽车多源采集：内部 API / 公告附件 / Playwright 渲染分流、登录态与滑块对抗、LLM 字段归类与画像宽表、墓表防回采、开放 API 对外只读。
- 主导设计并实现 RAG / Agent 相关系统：文档解析、混合检索、GraphRAG、LangGraph 工作流与工具调用。
- 有 Kubernetes 与 OpenStack 背景，能从部署、观测和资源成本角度看 AI 系统。

## 技术栈

- AI：`RAG`、`LangGraph`、`LangChain`、`GraphRAG`、`MCP`、`Weaviate`、`RAGFlow`、`vLLM`
- AI Coding：`Claude Code`、`Codex CLI`、`Cursor`、`Skills`、`stream-json`
- 后端：`Python`、`Go`、`Django`、`DRF`、`Flask`、`Gin`、`gRPC`、`MySQL`、`PostgreSQL`、`Redis`、`Elasticsearch`
- 平台与前端：`Docker`、`Kubernetes`、`Kubebuilder`、`KubeVirt`、`Istio`、`Prometheus`、`OpenStack`、`Vue 3`、`React`、`TypeScript`

## 代表性项目

### 企业级AI网关管理平台

企业内部接入多家模型时，不宜把上游凭据直接交给业务方，也不宜把鉴权、路由、观测、审计和知识库拆成互不相关的系统。

主导架构与核心开发：用 `Go`、`Python`、`React`、`PostgreSQL`、`Redis`、`RabbitMQ` 拆成 `gateway`、`rag-service`、`web` 三个服务，覆盖平台 API Key 生命周期、模型代理路由、调用统计审计和 RAG，并提供 Compose 部署方案。

- 控制台：`http://8.162.21.158:31873`（安全组 IP 白名单，访问前需申请放行）
- [项目地址](https://github.com/QEDQCD/ai_gateway)

### 多源信息采集与智能处理平台（情报工坊）

面向智能汽车的多源采集与分析：汽车情报（参数 / 动力 / 销量）与汽车场景库（口碑 / 质量舆情 / 新车资讯）同源入库、清洗、互联，再经开放 API 只读对外。

主导整体方案与核心采集链路：`Django`、`DRF`、`Vue 3`、`TypeScript`、`PostgreSQL`、`Redis`；后端线程池调度 + cron，统一执行器做去重、日上限、容错与墓表（硬删后永不采回）。

**采集技术能力（汽车情报）**

- 三源新能源乘用车参数：汽车之家（增量采集 + LLM 品牌预筛）、懂车帝（内部 JSON API，禁 HTML 防安全墙）、工信部公告 / 能耗 / 型号主档（批次维度 + 失败重试 / 下架判 `unavailable`）
- 编码与字段治理：GB18030 乱码修复、选装包 LLM 归类（`other_params` 从 46% 压到约 0.1%）、扁平化 / JSONB / 妙搭 CSV 多形态导出（gzip）
- 动力系统：发动机 / 电驱动 / 电池子库 + 动力系统集成库；三源车系互联确认后物化统一车系

**采集技术能力（汽车场景库）**

- 汽车之家口碑：评论维度拆列导出；懂车帝口碑 / 车友圈：短信登录态常态化、OpenCV 自动解滑块、cookie 探活、动态待采队列 + flock 轮转、142 标签画像宽表与用户画像分群
- 质量舆情：车质网 / 12315 / 中汽质量网投诉（requests 免登或双编码解析）、召回 / 质量报告（Playwright 浏览器复用 + 正文清洗）、看板聚合与群体预警
- 新车资讯：周度采集 / Markdown 导入、关联本地参数库补齐、官网定向检索 + Playwright 渲染补全

另有只读开放数据 API（API Key + 限流配额 + 审计，约 20 个资源）、多引擎翻译与 PDF OCR 等模块。

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
- [dsh-token-stats](https://github.com/QEDQCD/dsh-token-stats)：DeepSeek Harness 插件，监听 session 用量写入 JSONL，提供 `token_report` 按天/周/月聚合（`claude-token-stats` 的 DSH 对应实现）
- [claude-auto-approve](https://github.com/QEDQCD/claude-auto-approve)：Claude Code `PreToolUse` hook，白名单自动放行、危险命令强制确认
- [claude-ocr-vision](https://github.com/QEDQCD/claude-ocr-vision)：给纯文本模型「看图」——`PreToolUse` 拦截读图，改走本地 RapidOCR，支持 Claude Code / Codex CLI
- [dsh-ocr-vision](https://github.com/QEDQCD/dsh-ocr-vision)：DeepSeek Harness 插件，提供 `ocr_image` 工具，本地 RapidOCR 提文字给纯文本模型（`claude-ocr-vision` 的 DSH 对应实现）
- [claude-secret](https://github.com/QEDQCD/claude-secret)：本地加密 Claude Code token（AES-256-CBC），每次启动解密注入，退出后清掉明文
- [智能分类服务](https://github.com/QEDQCD/inis_classify)：基于 LangGraph 的分类 Agent（检索、验证、格式约束与失败兜底）
- AI cloud：基于 Kubernetes 的算力调度与资源治理（`Kubebuilder`、`KubeVirt`、`Istio` 等）

## 联系方式

- Email: `594253850@qq.com`
- GitHub: [QEDQCD](https://github.com/QEDQCD)
- OpenStack Review: [liwenjian](https://review.opendev.org/q/liwenjian)
