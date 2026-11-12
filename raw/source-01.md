# Source 1: LLM Powered Autonomous Agents
- **作者**：Lilian Weng (OpenAI Applied AI Research)
- **發表年份**：2023 年 6 月
- **原始連結**：https://lilianweng.github.io/posts/2023-06-23-agent/
- **核心貢獻**：
  1. 提出大型語言模型自主代理的經典系統架構公式：`Agent = LLM（核心大腦） + Planning（規劃） + Memory（記憶） + Tool Use（工具使用）`。
  2. **Planning（規劃）**：包含「子目標拆解（Subgoal Decomposition，如 Chain-of-Thought）」與「自我反思修正（Self-Reflection）」。
  3. **Memory（記憶）**：區分為「短期記憶（In-Context Learning，受限於 Context Window 長度）」與「長期記憶（外部向量資料庫與快速檢索機制）」。
  4. **Tool Use（工具使用）**：讓模型學會呼叫外部 API 獲取即時資訊、執行程式碼或操作外部系統，突破預訓練權重的知識截止限制。
