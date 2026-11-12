# 04. 工具使用（Tool Use）：讓 AI 長出手腳

## 一句話白話定義
Tool Use 讓 LLM 透過標準化介面（如 Function Calling / API）呼叫外部程式與即時資料庫，突破模型只能產生純文字的限制 `[Source 1, Source 3]`。

## 生活化類比
大型語言模型本身就像一位「博學但被關在房間裡的學者」，他讀過幾年前的書，但不知道今天外面的氣溫，也不會心算複雜財務報表。給他一支電話和計算機（Tool Use），他就能打電話問氣象局、用計算機算出精準數字，再整理成完整報告給你 `[Source 1]`。

## 核心運作機制
LLM 並不會「親自」執行程式碼，而是透過以下三步驟與工具協作 `[Source 1, Source 3]`：
```text
1. LLM 判斷需求 ──► 輸出結構化呼叫指令 (例如：get_weather(city="Taipei"))
                         │
2. 系統執行層 (Runtime) ──► 實際呼叫外部 API，取得回傳值 {"temp": 24, "rain": "20%"}
                         │
3. 回傳 Observation ──► 將 JSON 結果餵回給 LLM，由 LLM 組織成自然語言回答
```
- **工具介面設計關鍵（ACI）** `[Source 3]`：
  - Anthropic 指出，給 Agent 使用的工具必須具備清晰的功能描述、明確的參數格式與防呆錯誤提示，才能大幅降低模型傳錯參數的機率。
- **常見工具類型** `[Source 1, Source 4]`：網路即時搜尋、程式碼直譯器（Code Interpreter）、資料庫查詢、行事曆與郵件 API。

## 資料來源依據
- `[Source 1]` Lilian Weng (2023), *LLM Powered Autonomous Agents* — Tool Use 模組定義。
- `[Source 3]` Anthropic Engineering (2024), *Building Effective Agents* — Agent-Computer Interface (ACI) 工具設計原則。
- `[Source 4]` Andrew Ng (2024), *Agentic Design Patterns* — Tool Use 設計模式。

## 延伸閱讀連結
- 了解工具行動在整個迴圈中的位置：[[02-planning-and-react]]
- 回到架構總覽：[[01-agent-overview]]
