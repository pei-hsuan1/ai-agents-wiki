# 01. 什麼是 AI Agent？（與 Chatbot、Workflow 的差異）

## 一句話白話定義
AI Agent 是以大型語言模型（LLM）為大腦，能自主拆解目標、使用外部工具並根據結果修正行動的智能系統 `[Source 1, Source 3]`。

## 生活化類比
- **傳統 Chatbot（聊天機器人）**：像是一位「只能隔著玻璃回答問題的顧問」，你問一句它答一句，但無法幫你實際操作電腦或查即時資料。
- **Workflow（固定工作流）**：像是「照著標準食譜步驟運作的自動化生產線」，第一步切菜、第二步下鍋，順序事先寫死。
- **AI Agent（自主代理）**：像是一位「專業主廚」，你只要說「準備一桌三人晚餐」，主廚會自己看冰箱食材（觀察）、決定菜單（規劃）、使用爐具（工具）並試吃調整口味（反思）`[Source 1, Source 3]`。

## 核心運作機制
根據 Lilian Weng 的經典架構定義，一個完整的 AI Agent 由四大核心元件組成 `[Source 1]`：
```text
                  ┌─────────────────┐
                  │   Planning      │ ◄── 任務拆解、子目標規劃
                  │    (規劃能力)    │
                  └────────┬────────┘
                           │
┌─────────────────┐        ▼        ┌─────────────────┐
│     Memory      │ ◄───► LLM ◄───► │    Tool Use     │
│    (短期/長期)   │     (核心大腦)    │   (API / 搜尋)   │
└─────────────────┘                 └─────────────────┘
```
- **Chatbot vs. Workflow vs. Agent 比較** `[Source 3]`：
  - **控制路徑**：Workflow 由開發者預先寫死程式碼路徑；Agent 由 LLM 根據每一步結果動態決定下一步。
  - **適用時機**：步驟固定且可預測時用 Workflow；步驟無法預先窮舉、需靈活應變時才用 Agent。

## 資料來源依據
- `[Source 1]` Lilian Weng (2023), *LLM Powered Autonomous Agents* — 核心四大元件公式。
- `[Source 3]` Anthropic Engineering (2024), *Building Effective Agents* — Workflow 與 Agent 的邊界定義。

## 延伸閱讀連結
- 下一步了解大腦如何逐步決策：[[02-planning-and-react]]
- 了解記憶如何支撐長任務：[[03-memory-system]]
- 了解 Agent 如何呼叫外部工具：[[04-tool-use]]
