# Source 5: Reflexion: Language Agents with Verbal Reinforcement Learning
- **作者**：Noah Shinn, Federico Cassano, Edward Berman, Ashwin Gopinath, Karthik Narasimhan, Shunyu Yao
- **發表年份**：2023 年（NeurIPS 2023）
- **原始連結**：https://arxiv.org/abs/2303.11366
- **核心貢獻**：
  1. 提出不需更新模型權重（無需微調），僅透過「語言自我反思（Verbal Reinforcement）」即可讓 Agent 從失敗中學習的框架。
  2. 核心三模組迴圈：
     - **Actor（行動者）**：根據當前狀態與記憶生成行動或解答。
     - **Evaluator（評估器）**：對 Actor 的產出進行品質評分或規則檢查（判斷通過與否）。
     - **Self-Reflection（自我反思模組）**：當評估未通過時，分析失敗原因並寫成自然語言經驗摘要，存入短期記憶（Episodic Memory），引導下一輪 Actor 避開相同錯誤。
