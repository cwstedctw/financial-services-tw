---
name: model-update
description: 用新資料更新財務模型——季財報、管理層財測、總經變化或修正假設；調整預估、重算估值、標出重大變化。觸發詞：更新模型、填財報、刷新預估、新財測。
---

> 🇹🇼 **台灣在地化**：本技能屬「台灣版財經外掛」，產出一律**繁體中文（台灣用語）**並遵循 `taiwan-finance-context` 規則。台股量化數據優先用 **TWSE MCP（`twstock`）**；術語對照：10-K→年報、10-Q→季報、US GAAP→T-IFRS、SEC/EDGAR→公開資訊觀測站(MOPS)、$→新台幣(萬/億/兆)、ticker→股票代號；範例用台股（如台積電 2330）；查不到的數字標 `[需查證]`，不可編造；結尾標「※ 僅供學術討論與教學示範，非投資建議」。以下為原版方法論，請依上述規則以繁中產出。

# Model Update

## Workflow

### Step 1: Identify What Changed

Determine the update trigger:
- **Earnings release**: New quarterly actuals to plug in
- **Guidance change**: Company updated forward outlook
- **Estimate revision**: Analyst changing assumptions based on new data
- **Macro update**: Interest rates, FX, commodity prices changed
- **Event-driven**: M&A, restructuring, new product, management change

### Step 2: Plug New Data

#### After Earnings
Update the model with reported actuals:

| Line Item | Prior Estimate | Actual | Delta | Notes |
|-----------|---------------|--------|-------|-------|
| Revenue | | | | |
| Gross Margin | | | | |
| Operating Expenses | | | | |
| EBITDA | | | | |
| EPS | | | | |
| [Key metric 1] | | | | |
| [Key metric 2] | | | | |

**Segment Detail** (if applicable):
- Update each segment's revenue and margin
- Note any segment mix shifts

**Balance Sheet / Cash Flow Updates**:
- Cash and debt balances
- Share count (buybacks, dilution)
- Capex actual vs. estimate
- Working capital changes

### Step 3: Revise Forward Estimates

Based on the new data, adjust forward estimates:

| | Old FY Est | New FY Est | Change | Old Next FY | New Next FY | Change |
|---|-----------|-----------|--------|------------|------------|--------|
| Revenue | | | | | | |
| EBITDA | | | | | | |
| EPS | | | | | | |

**Key Assumption Changes:**
- What assumptions are you changing and why?
- Revenue growth rate: old → new (reason)
- Margin assumption: old → new (reason)
- Any new items (restructuring charges, one-time gains, etc.)

### Step 4: Valuation Impact

Recalculate valuation with updated estimates:

| Valuation Method | Prior | Updated | Change |
|-----------------|-------|---------|--------|
| DCF fair value | | | |
| P/E (NTM EPS × target multiple) | | | |
| EV/EBITDA (NTM EBITDA × target multiple) | | | |
| **Price Target** | | | |

### Step 5: Summary & Action

**Estimate Change Summary:**
- One paragraph: what changed, why, and what it means for the stock
- Is this a thesis-changing event or noise?

**Rating / Price Target:**
- Maintain or change rating?
- New price target (if changed) with methodology
- Upside/downside to current price

### Step 6: Output

- Updated Excel model (if user provides the existing model)
- Estimate change summary (markdown or Word)
- Updated price target derivation

## Important Notes

- Always reconcile your estimates to the company's reported figures before projecting forward
- Note any non-recurring items and whether your estimates are T-IFRS or adjusted
- Track your estimate revision history — it shows your analytical progression
- If the quarter was noisy, separate signal from noise in your estimate changes
- Check consensus after updating — how do your revised estimates compare to the Street?
- Share count matters — dilution from stock comp, converts, or buybacks can materially affect EPS
