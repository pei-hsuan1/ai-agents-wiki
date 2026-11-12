# 02. 大腦如何思考與行動？任務規劃與 ReAct 迴圈

## 一句話白話定義
Planning 讓 AI 把大任務切成小步驟，而 ReAct 則讓 AI 透過「思考 → 行動 → 觀察」的循環一步步驗證並完成任務 `[Source 1, Source 2]`。

## 生活化類比
想像你在陌生城市找一間評價最好的拉麵店：
1. **Thought（思考）**：「我需要先查這附近有哪些拉麵店，再比較評分。」
2. **Action（行動）**：打開地圖 App 搜尋「附近拉麵」。
3. **Observation（觀察）**：看到 A 店 4.8 星但公休、B 店 4.5 星營業中。
4. **下一輪 Thought（思考）**：「A 店公休，所以我應該導航去 B 店。」
這個不斷「想一下 → 做一步 → 看結果」的過程，就是 ReAct `[Source 2]`。

## 核心運作機制
1. **任務拆解（Task Decomposition）** `[Source 1, Source 4]`：
   - 面對複雜指令，LLM 會先運用思維鏈（Chain-of-Thought）將大目標拆解為多個可執行的子目標（Subgoals）。
2. **ReAct 推理行動迴圈（Reasoning + Acting Loop）** `[Source 2]`：
```text
   ┌──────────────────────────────────────────┐
   │                                          ▼
   │   [1. Thought 思考]：分析現況，決定下一步要做什麼
   │          │
   │          ▼
   │   [2. Action 行動]：呼叫外部工具或 API 發出指令
   │          │
   │          ▼
   │   [3. Observation 觀察]：取得工具回傳的真實數據
   │          │
   └──────────┴──► (任務未完成則繼續下一輪；完成則輸出最終答案)
```
   - **為什麼需要交替？** 純思考容易憑空捏造事實（幻覺）；純行動缺乏方向。將兩者結合能讓每一步推理都建立在真實觀察結果上 `[Source 2]`。

## 資料來源依據
- `[Source 1]` Lilian Weng (2023), *LLM Powered Autonomous Agents* — 子目標拆解機制。
- `[Source 2]` Shunyu Yao et al. (2022), *ReAct: Synergizing Reasoning and Acting in Language Models* — Thought-Action-Observation 迴圈。
- `[Source 4]` Andrew Ng (2024), *Agentic Design Patterns* — Planning 設計模式。

## 延伸閱讀連結
- 回到整體架構總覽：[[01-agent-overview]]
- 了解 Action 如何與外部工具對接：[[04-tool-use]]
