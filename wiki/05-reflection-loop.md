# 05. 自我反思（Reflection）與多代理協作

## 一句話白話定義
Reflection 讓 AI 在交出最終答案前，先扮演「審查員」檢查自己的草稿與錯誤，透過多輪迭代大幅提升輸出準確率 `[Source 4, Source 5]`。

## 生活化類比
寫期末報告時，很少人能「從第一個字直接寫到最後一個字且完全不修改（Zero-Shot）」。真正高品質的做法是：先寫初稿 → 對照評分標準自己檢查一遍 → 發現某段偏題或缺少佐證 → 修正後再交卷。這就是 Reflection 迴圈 `[Source 4]`。

## 核心運作機制
1. **Reflexion 語言強化學習迴圈** `[Source 5]`：
```text
   ┌───────────────────────────────────────────────────┐
   │                                                   ▼
   │   [Actor 行動者] ──► 產出初版內容或行動軌跡
   │         ▲                    │
   │         │                    ▼
   │   [短期記憶庫]        [Evaluator 評估器] ──► 檢查是否符合規則？
   │         ▲                    │ (未通過)
   │         │                    ▼
   └── [Self-Reflection 自我反思]：分析錯誤原因並寫下改進規則
```
   - **關鍵價值**：不需要重新訓練模型權重，只要把「失敗原因」轉成文字提示寫入記憶，下一輪生成就能避開同樣的錯誤 `[Source 5]`。
2. **四大 Agentic 設計模式與多代理協作** `[Source 4]`：
   - Andrew Ng 指出，結合 **Reflection（反思）**、**Tool Use（工具）**、**Planning（規劃）** 與 **Multi-Agent（多代理分工，如讓「生成者」與「批評者」分開）**，能讓系統穩定度產生質變。

## 資料來源依據
- `[Source 4]` Andrew Ng (2024), *Agentic Design Patterns* — Reflection 與 Multi-Agent 設計模式。
- `[Source 5]` Shinn et al. (2023), *Reflexion: Language Agents with Verbal Reinforcement Learning* — Actor / Evaluator / Self-Reflection 三元架構。

## 延伸閱讀連結
- 了解反思筆記存放在哪裡：[[03-memory-system]]
- 回到架構總覽：[[01-agent-overview]]
