---
description: 從一個 PowerPoint 範本檔，建立可重用的 PPT 範本技能
argument-hint: "[.pptx 或 .potx 檔路徑]"
allowed-tools: ["Read", "Write", "Bash", "Glob"]
---

# PPT 範本建立指令

從使用者提供的 PowerPoint 範本，建立一個自包含的 PPT 範本技能。

## 步驟

1. **若未提供，先索取範本檔**：
   - 「請提供你的 PowerPoint 範本檔路徑（.pptx 或 .potx）」
   - 範本應包含你想用的投影片版面與品牌樣式。

2. **載入 `ppt-template-creator` 技能**：
   - 用 `skill: "ppt-template-creator"` 載入完整技能說明。
   - 依技能內的流程分析範本並產生新技能。

3. **蒐集其他資訊**：
   - 公司／範本名稱（用來命名技能）
   - 主要用途（投資簡報、董事會資料、客戶簡報等）

4. **執行技能流程**：
   - 分析範本結構（版面、佔位框、尺寸）
   - 產生含 assets/ 與 SKILL.md 的技能資料夾
   - 建立範例簡報以驗證
   - 打包技能

5. **把打包好的技能交付**給使用者。
