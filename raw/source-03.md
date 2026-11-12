# Source 3: Building Effective Agents
- **作者**：Anthropic Engineering Team (Erik Schluntz, Barry Zhang)
- **發表年份**：2024 年 12 月
- **原始連結**：https://www.anthropic.com/research/building-effective-agents
- **核心貢獻**：
  1. 明確區分 **Workflows（工作流）** 與 **Agents（自主代理）** 的定義邊界：
     - **Workflows**：透過預先寫好的程式碼路徑（Predefined Code Paths）串接 LLM 與工具，執行順序固定可控。
     - **Agents**：由 LLM 動態自主決定執行流程、選擇工具與判斷何時結束任務，具備高度彈性。
  2. 提出實務設計原則：優先使用最簡單的解決方案（如單次 LLM 呼叫或固定 Workflow），僅在任務步驟無法預先窮舉、需要動態決策時才導入自主 Agent。
  3. 強調「工具介面設計（Agent-Computer Interface, ACI）」的重要性：清楚的工具說明與防呆參數能大幅減少 Agent 呼叫出錯。
