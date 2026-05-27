# 變更紀錄（Changelog）

本專案版本格式採語意化版本（SemVer）。

## [0.1.0] - 2026-05-27

第一版：把 Anthropic 官方 [`anthropics/financial-services`](https://github.com/anthropics/financial-services) 在地化成台灣台股教學版。

### 新增
- 8 個外掛 + `marketplace.json`：
  - `taiwan-finance-context`（繁中／台股／T-IFRS／民國年／新台幣 風格規則層，必裝）
  - 核心：`market-researcher-tw`、`earnings-reviewer-tw`、`equity-research-tw`、`financial-analysis-tw`
  - 進階：`model-builder-tw`、`pitch-agent-tw`、`valuation-reviewer-tw`
- `老師操作手冊.md`（零基礎安裝／驗證／疑難排解 + FinMind 進階附錄）
- `台股代號小抄.md`（各產業常用台股代號）

### 在地化內容
- 5 個 agent、18 個指令、`taiwan-finance-context` 全文繁體中文。
- 55 個 skill 加上繁中描述與「台灣在地化」說明標頭（保留原版方法論細節）。
- 術語替換：10-K→年報、10-Q→季報、US GAAP→T-IFRS、SEC/EDGAR→公開資訊觀測站（MOPS）、CapIQ/FactSet→TWSE MCP、$→新台幣（萬／億／兆）、ticker→股票代號。
- 規則：強制繁中、民國年、台股代號格式、查不到的數字標 `[需查證]` 不杜撰、結尾免責。

### 資料來源
- 預設改為免費 **TWSE MCP**（`twstock`，`https://TW-Stock-MCP-Server.fastmcp.app/mcp`）；所有外掛 `.mcp.json` 已指向此來源，agent 工具由 `mcp__capiq__*`／`mcp__factset__*` 換成 `mcp__twstock__*`。
- 進階補充：FinMind 官方 Agent Skill／`llms.txt`（深度 DCF 多年現金流、總經數據）。

### 排除（非本版範圍）
- 會計法遵類：`gl-reconciler`、`month-end-closer`、`statement-auditor`、`kyc-screener`（PDPA／需真實帳本）。
- 合作夥伴外掛 `partner-built`（LSEG、S&P，需付費金鑰）。
- 其他 vertical（investment-banking、private-equity、wealth-management、fund-admin、operations）。

### 已知缺口
- 法說會逐字稿（需老師從 MOPS 貼上）。
- 多年期完整現金流量表、總體經濟數據（改用 FinMind）。
- 即時報價深度不如付費源（TWSE MCP 含 MIS 盤中報價，但有限）。
