# 台灣版財經外掛（financial-services-tw）

把 Anthropic 官方的 [`anthropics/financial-services`](https://github.com/anthropics/financial-services) 外掛**在地化成台灣台股教學版**：全程**繁體中文**、用**台股代號**、**新台幣（萬／億／兆）**、**T-IFRS** 與**民國年**，資料來自**免費的台灣證交所開放資料（TWSE MCP）**。

> 給經濟／通識／財金老師上課用。不用寫程式、不用架伺服器——裝好後用中文跟 Claude 對話即可。
> ⚠️ 本外掛僅供**學術討論與教學示範，非投資建議**。

---

## 快速安裝（Claude Code，一行搞定）

```
/plugin marketplace add cwstedctw/financial-services-tw
/plugin install taiwan-finance-context@financial-services-tw
/plugin install market-researcher-tw@financial-services-tw
/plugin install earnings-reviewer-tw@financial-services-tw
/plugin install equity-research-tw@financial-services-tw
/plugin install financial-analysis-tw@financial-services-tw
```

桌面版 / Cowork：**Settings → Plugins → Add marketplace**，貼上
`https://github.com/cwstedctw/financial-services-tw`，再安裝各外掛。

> **務必先裝 `taiwan-finance-context`**，它是讓所有回答變台灣風格的規則層。
> 進階再裝：`model-builder-tw`、`pitch-agent-tw`、`valuation-reviewer-tw`（需 Excel／PowerPoint）。

完整圖文步驟與課堂用法見 **[老師操作手冊.md](老師操作手冊.md)**，常用代號見 **[台股代號小抄.md](台股代號小抄.md)**。

---

## 包含的外掛

| 外掛 | 用途 | 等級 |
|------|------|------|
| `taiwan-finance-context` | 繁中／台股／T-IFRS／民國年／新台幣 回答風格（**必裝**） | 核心 |
| `market-researcher-tw` | 產業概覽、競爭格局、同業比較、選股清單 | 核心★ |
| `earnings-reviewer-tw` | 財報／法說會分析 → 模型更新 → 研究筆記 | 核心 |
| `equity-research-tw` | 個股研究指令：選股、產業、論點、財報分析 | 核心 |
| `financial-analysis-tw` | DCF、同業比較、LBO、三表模型、競爭分析 | 核心 |
| `model-builder-tw` | Excel 三表／DCF／LBO 模型 | 進階 |
| `pitch-agent-tw` | 投資簡報（pitch deck） | 進階 |
| `valuation-reviewer-tw` | 估值範本、報酬分析、投資備忘錄 | 進階 |

## 資料來源

- **預設**：免費 [TWSE MCP](https://github.com/twjackysu/TWSEMCPServer)（`https://TW-Stock-MCP-Server.fastmcp.app/mcp`，免註冊、免金鑰），涵蓋股價、本益比、財報、月營收、三大法人等。
- **進階補充（選用）**：FinMind（官方 Agent Skill / `llms.txt`）用於深度 DCF 多年現金流量表與總體經濟數據。
- 找不到的數字一律標 `[需查證]`，不杜撰。

## 試用（裝好後問問看）

1. 請用台股的方式介紹台積電（2330）最近一季的綜合損益表重點。
2. 列出半導體前 5 大公司的本益比與股價淨值比，做成表格。
3. 比較 2330 與 2454 過去一年的股價走勢，並推測原因（學術討論）。

---

## 授權與致謝

本專案改作自 Anthropic 的 [`anthropics/financial-services`](https://github.com/anthropics/financial-services)，依 **Apache License 2.0** 授權釋出（見 [LICENSE](LICENSE) 與 [NOTICE](NOTICE)）。可自由修改、Fork、分享，請保留授權與來源聲明。

> 原始倉庫聲明：本倉庫所有內容不構成投資、法律、稅務或會計建議，所有產出皆需由人簽核。
