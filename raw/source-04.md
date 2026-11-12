# Source 4: Agentic Design Patterns (四大代理設計模式)
- **作者**：Andrew Ng (DeepLearning.AI)
- **發表年份**：2024 年 3 月
- **原始連結**：https://www.deeplearning.ai/the-batch/how-agents-can-improve-llm-performance/
- **核心貢獻**：
  1. 指出「反覆迭代的 Agentic 工作流（Iterative Workflow）」能讓較輕量的模型超越單次提示（Zero-Shot）的大型模型表現。
  2. 歸納出四大核心設計模式（Agentic Design Patterns）：
     - **Reflection（自我反思）**：讓模型審查自己產出的草稿或程式碼，找出邏輯漏洞與錯誤並自行改寫。
     - **Tool Use（工具使用）**：賦予模型網路搜尋、程式碼直譯器、資料庫查詢等外部能力。
     - **Planning（任務規劃）**：面對複雜指令時，先產出多步驟執行計畫，再逐步落實。
     - **Multi-Agent Collaboration（多代理協作）**：將不同角色（如「研究員」、「撰稿者」、「審查員」）分配給不同 Agent 分工合作。
