# 认识AI六兄弟 — 幻灯片源（中文，适合直接转换为 PPTX）

说明：
- 这是为你准备的完整幻灯片源，按页分节（每页一个一级标题 Slide 1、Slide 2...），包含：幻灯片要点、演讲备注（备注区内容）、配图建议（搜索关键词）。
- 我已把它放在仓库：presentations/认识AI六兄弟-source/README.md
- 你可以用 Pandoc 或其他工具将其转换为 PPTX，也可以让我再次尝试生成二进制 PPTX（如果你愿意我可以再试一次）。

---

# Slide 1 — 封面

标题：认识AI六兄弟：Agent、LLM、Skills、MCP、RAP、向量数据库（小白友好）

要点：简短副标题 + 作者与日期

备注（演讲稿）：大家好，我是你们的讲解员，今天半小时把复杂概念做成易懂的三明治。

配图建议：搜索关键词 “AI cartoon robot laptop” （Unsplash / Pexels）

---

# Slide 2 — 议程（Agenda）

要点：为什么学？我们会看：概念、原理、工程接入、案例、最佳实践、速查卡

备注：像吃自助餐——先看菜单再动筷。

配图：流程图、清单；关键词 “agenda checklist illustration”

---

# Slide 3 — Agent 是什么？

要点：Agent = 带目标与工具的大脑；关键元素：策略（policy）、模型（LLM）、工具（skills）、记忆（DB）

备注：想象“带工具箱的小帮手”。

配图关键字："robot with tools illustration"

---

# Slide 4 — 大模型（LLM）概览

要点：预测下一个词的模型；Transformer 基本流程（编码/注意力/解码）；能力：生成/理解/抽取/翻译

备注：把 LLM 当作超级联想引擎。

配图："transformer architecture illustration"

---

# Slide 5 — Prompting 基础

要点：prompt 是说明；好 prompt = 目标清晰 + 示例 + 输出格式；常用技巧：few-shot、Chain-of-Thought、system prompt

备注：点菜例子——别只说“来点吃的”。

配图：聊天气泡/菜谱；关键词 "prompt illustration"

---

# Slide 6 — Skills（工具）

要点：Skills = 外部功能模块（读写文件、调用 API、控制设备）；内置 vs 外部；要有参数规范和安全校验

备注：技能就是 Agent 的“手脚”。

配图：工具图标；关键词 "api integration illustration"

---

# Slide 7 — MCP（桥梁）是什么？

要点：Model-Call Protocol / stdio bridge：把模型的调用意图变成 API/系统命令；常见形式：JSON-RPC、stdio tagged、HTTP

备注：MCP 是“翻译官”。

配图：桥梁连接图；关键词 "bridge connecting systems illustration"

---

# Slide 8 — RAP（检索增强提示）

要点：通过检索外部知识（向量 DB）增强 prompt；流程：query → 检索 → 拼接 prompt → LLM 生成

备注：先找资料再答题，不用凭空编。若“RAP”代表别的概念，请告知。

配图：放大镜 + 文档；关键词 "document retrieval illustration"

---

# Slide 9 — 向量数据库（Vector DB）基础

要点：文本→embedding→向量空间；相似度检索（ANN）；常见产品：Pinecone、Milvus、Weaviate、Qdrant

备注：每段文字变成“指纹”。

配图：向量空间可视化；关键词 "vector space illustration"

---

# Slide 10 — 端到端架构图

要点：用户 → 前端 → Agent → LLM；Agent 调用：Skills / MCP / Vector DB；回传后处理 → 前端

备注：像厨房：客人点菜 → 厨师（Agent）看菜谱（RAP）→ 用工具（skills）做菜 → 上菜。

配图：系统架构图；关键词 "system architecture ai agent diagram"

---

# Slide 11 — 示例：客服知识库 Agent

要点：用户问 → 向量检索相关文档 → 拼 prompt → LLM 生成并引用出处；示例 skills：open ticket、send email

备注：Agent 是勤快客服。

配图：客服聊天图；关键词 "customer support chatbot illustration"

---

# Slide 12 — 示例：代码生成 + 自动化部署

要点：prompt→LLM 生成代码→skill:run tests→skill:commit/deploy；注意：沙箱、权限、审计

备注：别把生产环境交给没加氧的 AI。

配图：代码 + 流程图；关键词 "code automation illustration"

---

# Slide 13 — MCP 与参数校验的坑

要点：参数标签污染（tag pollution）、编码/转义、并发问题；建议：严格校验、回显、日志

备注：MCP 是快递员，要写清楚门牌号。

配图：警告图；关键词 "bug alert illustration"

---

# Slide 14 — RAP + Vector DB 检索策略

要点：chunking、semantic vs keyword、top-k、hybrid rerank、token budget

备注：别把货架全搬上来，挑最相关的几件。

配图：超市挑选图；关键词 "shopping select items illustration"

---

# Slide 15 — 技术实现要点

要点：Embedding API、Vector DB 选型（性能/持久化/功能）、LLM 调用（同步/流式）、skill 接入（超时/幂等）

备注：选车比喻。

配图：齿轮/API 图；关键词 "api gears illustration"

---

# Slide 16 — 数据隐私与安全

要点：敏感数据屏蔽、加密、审计；幻觉风险与可验证性；权限边界

备注：别把身份证号扔模型里。

配图：锁/盾牌；关键词 "data security illustration"

---

# Slide 17 — 性能/成本与监控

要点：成本构成（embedding、retrieval、LLM token、API）、延迟优化（缓存、预取、异步）、关键指标（latency、success rate、cost）

备注：监控像车仪表盘。

配图：监控仪表盘；关键词 "monitoring dashboard illustration"

---

# Slide 18 — 故障排查清单（Cheatsheet）

要点：1) 检查 prompt 格式 2) skills 参数完整性 3) MCP tag 污染 4) 向量检索结果 5) 日志回放

备注：按厨房 SOP 检查。

配图：放大镜清单；关键词 "debug checklist illustration"

---

# Slide 19 — 最佳实践（10 条速记）

要点（示例）：清晰 prompt、skills 校验、向量检索小规模实验、审计日志、权限沙箱、版本控制、度量与告警、缓存策略、降级策略、示例数据

备注：稳妥的工程习惯。

配图：清单图；关键词 "best practices checklist illustration"

---

# Slide 20 — 小白速查卡（关键词解释）

内容表：Agent / LLM / Skill / MCP / RAP / Vector DB 各一句话解释

备注：考试前一翻。

配图：速查卡；关键词 "cheat sheet card illustration"

---

# Slide 21 — 案例研究与效果衡量

要点：部署前后对比（响应时间、正确率、工单关闭率），度量指标与成功因素

备注：数据说话。

配图：增长曲线；关键词 "case study growth chart illustration"

---

# Slide 22 — 资源与后续（Takeaways）

要点：推荐资源（Pinecone/Milvus/Qdrant/Weaviate、Embedding 服务、LLM 文档、MCP 示例仓库）、想要我生成 PPTX 或 Google Slides 则回复

备注：需要我再做 PPTX 吗？我可以再尝试或给你可直接转换的源。

配图：链接/书籍堆；关键词 "resources links illustration"

---

# 附录 A — 伪代码示例

```
# 伪代码：用户问 -> 检索 -> LLM -> 调用 skill -> 返回
query = user_input
embedding = embed_api(query)
candidates = vector_db.search(embedding, top_k=5)
prompt = build_prompt(query, candidates)
llm_response = llm.generate(prompt)
if llm_response.requests_tool_call:
    tool_result = mcp.call_tool(llm_response.tool_name, llm_response.tool_args)
    final = llm.generate(build_prompt_with_tool_result(query, candidates, tool_result))
else:
    final = llm_response.text
return final
```

备注：示例包含错误处理/超时/审计等在真实工程中必须添加。

---

# 附录 B — 图片资源与转换说明

图片来源建议：Unsplash、Pexels、Pixabay（免费）。在转换为 PPTX 时将图片放在同级 images/ 目录，并使用 Pandoc 的 --resource-path 指定。

示例 Pandoc 命令：
```
pandoc -t pptx -o "认识AI六兄弟.pptx" README.md --resource-path=images
```

如果你希望我现在把图片下载并一起放入仓库 images/ 目录，我可以继续做（请回复“下载图片并上传”）。

---

如果你现在仍要求我直接生成二进制 PPTX（我会再试一次），请回复 “再次尝试 PPTX”，我会立刻执行并把结果上传（如果成功会替换之前的占位文件）。

谢谢你，抱歉之前给你带来不便——我现在已经把完整幻灯片源写入仓库并准备继续按你的偏好完成后续操作。