# 03. Agent 的記憶系統：短期記憶與長期記憶

## 一句話白話定義
短期記憶是 AI 當下處理任務的「工作桌面」，長期記憶則是可隨時翻閱的「外部知識庫」，兩者搭配讓 Agent 能執行跨步驟長任務 `[Source 1]`。

## 生活化類比
- **短期記憶（Short-Term Memory）**：就像你書桌上的「便利貼與草稿紙」，拿取速度最快，但桌面空間有限（Context Window 上限），放太多東西會擠掉舊的筆記。
- **長期記憶（Long-Term Memory）**：就像身後的「大型圖書館書架」，平時不佔用桌面空間，需要時透過索引目錄（向量檢索）把相關資料抽出來放到桌上看 `[Source 1]`。

## 核心運作機制
```text
[當前對話 / ReAct 歷史紀錄] ──► 短期記憶 (Context Window)
                                     ▲   │
                         檢索相關知識 │   │ 存入重要經驗
                                     │   ▼
                            長期記憶 (外部向量資料庫 / Wiki)
```
1. **短期記憶（In-Context Learning）** `[Source 1]`：
   - 存放在模型的上下文視窗（Context Window）中，包含目前的對話歷史、剛執行的 Thought/Action/Observation 軌跡，以及錯誤反思筆記 `[Source 5]`。
2. **長期記憶（External Vector Store）** `[Source 1]`：
   - 將大量文件或歷史經驗轉換為向量嵌入（Embeddings）存入外部資料庫，在執行任務時透過語意相似度檢索（Retrieval）動態載入短期記憶中。

## 資料來源依據
- `[Source 1]` Lilian Weng (2023), *LLM Powered Autonomous Agents* — 短期與長期記憶架構分類。
- `[Source 5]` Shinn et al. (2023), *Reflexion* — 將反思經驗存入情景記憶（Episodic Memory）供後續回合參考。

## 延伸閱讀連結
- 了解記憶如何支援反思修正：[[05-reflection-loop]]
- 回到核心架構公式：[[01-agent-overview]]
