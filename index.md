# AI Agents 運作原理 — LLM Wiki 知識庫總索引

> 本 Wiki 採用「先討論架構、後批量生成」方式建立，嚴格依據 5 篇核心技術文獻進行 Ingest 與概念融合（規範詳見 `AGENTS.md`）。

## 一、 核心概念條目（`wiki/`）

| 編號 | 條目名稱 | 檔案路徑 | 核心教學重點 | 對應文獻來源 |
| :--- | :--- | :--- | :--- | :--- |
| 01 | 什麼是 AI Agent？ | `wiki/01-agent-overview.md` | 四大元件公式、Chatbot / Workflow / Agent 差異 | `[Source 1, Source 3]` |
| 02 | 任務規劃與 ReAct 迴圈 | `wiki/02-planning-and-react.md` | 子目標拆解、Thought → Action → Observation 循環 | `[Source 1, Source 2, Source 4]` |
| 03 | Agent 的記憶系統 | `wiki/03-memory-system.md` | 短期記憶（Context Window）與長期記憶（向量檢索） | `[Source 1, Source 5]` |
| 04 | 工具使用（Tool Use） | `wiki/04-tool-use.md` | Function Calling 運作三步驟、工具介面設計（ACI） | `[Source 1, Source 3, Source 4]` |
| 05 | 自我反思與多代理協作 | `wiki/05-reflection-loop.md` | Reflexion 評估修正迴圈、四大 Agentic 設計模式 | `[Source 4, Source 5]` |

## 二、 原始文獻資料庫（`raw/` — 已完成 5 篇 Ingest）

1. **`raw/source-01.md`**：Lilian Weng (2023) — *LLM Powered Autonomous Agents*
2. **`raw/source-02.md`**：Shunyu Yao et al. (2022) — *ReAct: Synergizing Reasoning and Acting in Language Models*
3. **`raw/source-03.md`**：Anthropic Engineering (2024) — *Building Effective Agents*
4. **`raw/source-04.md`**：Andrew Ng (2024) — *Agentic Design Patterns*
5. **`raw/source-05.md`**：Noah Shinn et al. (2023) — *Reflexion: Language Agents with Verbal Reinforcement Learning*

## 三、 概念關聯地圖
```text
[[01-agent-overview]] (總覽：LLM + Planning + Memory + Tool Use)
   ├──► [[02-planning-and-react]] (大腦如何拆解任務並交替思考與行動)
   ├──► [[03-memory-system]]      (短期工作桌面 vs. 長期知識圖書館)
   ├──► [[04-tool-use]]           (透過 API 與外部真實世界互動)
   └──► [[05-reflection-loop]]    (透過 Evaluator 檢查與反思實現自我修正)
```
