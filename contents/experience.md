### **研知 - 基于 Multi-Agent 与 RAG 的考研知识系统**
**2026年2月 – 2026年4月 | 核心开发者**

**技术栈：** Python, FastAPI, Qwen2.5-7B, BGE-small-zh, LangChain, ChromaDB

#### 主要贡献:
- **混合检索架构：** 采用结构化 Markdown 与递归字符结合的切片策略，设计"向量 + BM25"双路召回。集成查询扩展、语义重排序与 MMR 算法，显著提升文档召回精度与多样性。
- **条件性 RAG 优化：** 使用置信度驱动的动态检索机制，仅在模型低置信时触发 RAG。经近 400 题目测试验证，该策略成功规避了传统 RAG 对高置信知识的负面干扰，将整体问答准确率稳定在 **87.3%**。
- **多智能体协同：** 构建基于 **Router Agent** 路由分发的智能体架构，协同 QA、Chat 与 Tool Caller 智能体（支持代码生成、检索等 6 种工具）处理复杂任务；结合并发安全机制与持久化记忆，实现高质量多轮对话。
- **业务闭环落地：** 开发笔记管理模块，利用大模型从对话中自动提取高频考点，并结合**间隔重复算法**为用户动态生成个性化复习计划。

---

### **基于 vLLM 的大模型异步推理服务**
**2025年11月 – 2026年1月 | 独立开发**

**技术栈：** Python, PyTorch, vLLM, GPTQ, FastAPI, Docker, Qwen3, CUDA

#### 主要贡献:
- **全链路量化部署：** 针对 32B 参数大模型实施 **GPTQ W4A16** 量化方案，将显存占用从 64GB 压缩至 **18GB** (-72%)，成功在单卡 A40 (48GB) 上实现高性能部署，解决了显存瓶颈。
- **生产级服务架构：** 开发兼容 OpenAI 协议的 **FastAPI** 服务端，支持流式输出 (Streaming)。优化首字延迟 (TTFT) 至 **<80ms**，满足生产环境对实时交互的严苛要求。
- **自动化评测体系：** 构建包含 **TTFT**、**TPOT**、**Latency** 等多维指标的自动化评测工具链，通过压力测试精准定位 Memory-bound 瓶颈，为推理加速提供数据支撑。

---

### **Skills | 技能**
**编程与基础:** Python, PyTorch，数据结构、算法与代码工程能力；熟练应用 AI Coding 辅助开发

**RAG 技术:** 掌握 RAG 完整链路，熟悉 Indexing/Retrieval/Generation 核心模块，掌握混合检索与查询扩展等优化策略

**Agent 架构:** 熟悉 Multi-Agent 系统设计，理解基于 LLM + Planning + Memory + Tool/Function 的智能体实现机制

**LLM与推理:** 熟悉 LLM 基本原理，包括 Transformer、Attention 等；熟悉 LLM 推理加速与服务化技术（KV Cache、PagedAttention、Continuous Batching）；熟练使用 vLLM 进行大模型部署

**其他技能:** 熟悉 LoRA 微调、GPTQ 模型量化、CUDA 基础编程、Git 与 Docker 容器化部署