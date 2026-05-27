# 貢獻說明（Contributing）

歡迎老師、助教與學生一起讓這套台灣版財經教學外掛更好用。

## 你可以怎麼幫忙
- **回報問題**：用 GitHub Issues 回報哪個指令、哪檔台股回答怪怪的（附上你問的問題與 Claude 的回答截圖最有幫助）。
- **補充在地化**：把還是英文的方法論段落翻成繁中、或修正台灣術語。
- **更新範例公司**：產業代表股有變動時，更新 `taiwan-finance-context` 的「推薦同業比較組」與 `台股代號小抄.md`。
- **新增外掛**：把上游 `anthropics/financial-services` 其他 vertical 在地化後加進來。

## 專案結構
```
.claude-plugin/marketplace.json   # 市集清單（新增外掛要在這裡登記）
<外掛>-tw/
  .claude-plugin/plugin.json      # 外掛資訊（name 需與資料夾、marketplace 一致）
  .mcp.json                       # 資料來源（一律 twstock TWSE MCP）
  agents/  skills/  commands/     # 內容；skill 需有 name + description frontmatter
taiwan-finance-context/           # 共同風格規則層（必裝）
```

## 在地化原則（重要）
1. 一律**繁體中文（台灣用語）**；專業名詞第一次出現給一句白話解釋。
2. 金額用**新台幣萬／億／兆**；會計準則用 **T-IFRS**；期間並陳**民國年**。
3. 公司用「**簡稱（四碼代號）**」格式，例：台積電（2330）。
4. 資料優先用 **TWSE MCP（`twstock`）**；查不到的數字標 `[需查證]`，**不可編造**。
5. 每份產出結尾標「※ 僅供學術討論與教學示範，非投資建議」。

## 開發小提醒
- 在 Windows 用指令碼批次替換含中文的字串時，**請用 Python 並指定 `encoding="utf-8"`**；不要用 `perl -CSD -i`，會造成雙重編碼亂碼。
- 改完後，確認所有 `*.json` 仍為合法 JSON、每個 `SKILL.md` 都有 `name`／`description` frontmatter。
- 本機測試安裝：`/plugin marketplace add <你 clone 的本機路徑>`。

## 授權
本專案為 `anthropics/financial-services` 的改作，依 **Apache License 2.0** 釋出。送出貢獻即表示同意以相同授權釋出，並保留上游與本專案的著作權與授權聲明（見 `LICENSE`、`NOTICE`）。
