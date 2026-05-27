# 台灣版財經外掛（financial-services-tw）

把 Anthropic 官方的 [`anthropics/financial-services`](https://github.com/anthropics/financial-services) 外掛**在地化成台灣台股教學版**：全程**繁體中文**、用**台股代號**、**新台幣（萬／億／兆）**、**T-IFRS** 與**民國年**，資料來自**免費的台灣證交所開放資料（TWSE MCP）**。

> 給經濟／通識／財金老師上課用。不用寫程式、不用架伺服器——裝好後用中文跟 Claude 對話即可。
> ⚠️ 本外掛僅供**學術討論與教學示範，非投資建議**。

---

## 安裝（只要裝「一個」外掛 `taiwan-finance`）

### 方法 A：桌面版 / Cowork（用滑鼠，推薦給老師）

1. 左側 **Personal plugins** 右邊按 **`+`** → **Create plugin** → **Add marketplace**。
2. 在欄位貼上市集網址：
   ```
   https://github.com/cwstedctw/financial-services-tw
   ```
   （若欄位要的是 `owner/repo` 格式，就貼 `cwstedctw/financial-services-tw`）
3. 加好後 → **Browse plugins** → 找到 **taiwan-finance** → 安裝 / 啟用。
4. 若詢問是否啟用資料源 **`twstock`**（免費台灣證交所資料）→ 選**允許**。

所有功能（產業研究、財報法說、個股研究、估值、DCF/LBO 模型、投資簡報）與台灣風格規則都包在這一個外掛裡。

### 方法 B：命令列（Claude Code CLI）

在終端機輸入：
```
claude plugin marketplace add cwstedctw/financial-services-tw
claude plugin install taiwan-finance@financial-services-tw
```
> 在 Claude Code 終端機的對話框內，也可用 `/plugin marketplace add …` 與 `/plugin install …`（視版本而定；部分桌面版選單沒有 `/plugin`，請改用方法 A）。
>
> 更新：`claude plugin update taiwan-finance`，或 GUI 內 Browse plugins 更新。

完整圖文步驟與課堂用法見 **[老師操作手冊.md](老師操作手冊.md)**，常用代號見 **[台股代號小抄.md](台股代號小抄.md)**。

---

## 這個外掛包含什麼

裝一個 `taiwan-finance`，就同時擁有：

| 能力 | 對應指令 / 用法 | 等級 |
|------|------|------|
| 台灣風格規則層（繁中／台股／T-IFRS／民國年／新台幣） | 自動套用（提到台股代號時啟用） | 核心 |
| 產業研究（產業概覽、競爭格局、同業比較、選股） | `/sector`、`/competitive-analysis`、`/comps`、`/screen` | 核心 |
| 財報／法說分析 | `/earnings`、`/earnings-preview`、`market-researcher` 等代理 | 核心 |
| 個股研究（論點、首次評等、晨報、催化事件） | `/thesis`、`/initiate`、`/morning-note`、`/catalysts` | 核心 |
| 估值與模型（DCF、三表、LBO、競爭分析） | `/dcf`、`/3-statement-model`、`/lbo`、`/debug-model` | 進階（需 Excel） |
| 投資簡報 | `/ppt-template`、`pitch-agent` 代理 | 進階（需 PowerPoint） |

> ⚠️ **指令有命名空間**：實際要打 **`/taiwan-finance:comps`**（不是 `/comps`，後者會顯示 `Unknown command`）。最省事的方式是**直接用中文問**（見下方「試用」），或只打 `/` 從選單點 `taiwan-finance:…`。

內含 **27 個技能、5 個代理（agent）、16 個指令**，全部繁體中文、台股在地化。

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
