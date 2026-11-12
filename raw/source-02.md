# Source 2: ReAct: Synergizing Reasoning and Acting in Language Models
- **作者**：Shunyu Yao, Jeffrey Zhao, Dian Yu, Nan Du, Izhak Shafran, Karthik Narasimhan, Yuan Cao
- **發表年份**：2022 年（ICLR 2023）
- **原始連結**：https://arxiv.org/abs/2210.03629
- **核心貢獻**：
  1. 解決傳統「純推理（Chain-of-Thought）容易產生事實幻覺」以及「純行動（Acting）缺乏高階規劃目標」的雙重缺陷。
  2. 提出交錯執行迴圈：`Thought（思考推理） → Action（執行工具行動） → Observation（觀察環境回傳結果）`。
  3. **Thought（思考）**：追蹤當前進度、拆解下一步計畫、處理異常狀況。
  4. **Action（行動）**：向外部環境或工具（如搜尋引擎、計算機）發出結構化指令。
  5. **Observation（觀察）**：接收外部工具回傳的真實數據，作為下一輪 Thought 的依據，大幅降低幻覺率。
