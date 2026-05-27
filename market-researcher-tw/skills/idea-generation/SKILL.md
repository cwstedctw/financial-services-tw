---
name: idea-generation
description: 系統化選股與投資點子發想：結合量化篩選、主題研究與型態辨識，找出新的作多／放空點子。觸發詞：選股、找點子、screen、有什麼值得看、新點子。
---

> 🇹🇼 **台灣在地化**：本技能屬「台灣版財經外掛」，產出一律**繁體中文（台灣用語）**並遵循 `taiwan-finance-context` 規則。台股量化數據優先用 **TWSE MCP（`twstock`）**；術語對照：10-K→年報、10-Q→季報、US GAAP→T-IFRS、SEC/EDGAR→公開資訊觀測站(MOPS)、$→新台幣(萬/億/兆)、ticker→股票代號；範例用台股（如台積電 2330）；查不到的數字標 `[需查證]`，不可編造；結尾標「※ 僅供學術討論與教學示範，非投資建議」。以下為原版方法論，請依上述規則以繁中產出。

# Idea Generation

## Workflow

### Step 1: Define Search Criteria

Ask the user for parameters:
- **Direction**: Long ideas, short ideas, or both
- **Market cap**: Large, mid, small, micro
- **Sector**: Specific sector or cross-sector
- **Style**: Value, growth, quality, special situation, event-driven
- **Geography**: US, international, global
- **Theme**: Any specific thematic angle (AI, reshoring, aging demographics, etc.)

### Step 2: Quantitative Screens

Run screens based on the style:

**Value Screen**
- P/E below sector median
- EV/EBITDA below historical average
- Free cash flow yield >5%
- Price/book below 1.5x
- Insider buying in last 90 days
- Dividend yield above market average

**Growth Screen**
- Revenue growth >15% YoY
- Earnings growth >20% YoY
- Revenue acceleration (growth rate increasing)
- Expanding margins
- High return on invested capital (>15%)
- Strong net retention (>110% for SaaS)

**Quality Screen**
- Consistent revenue growth (5+ years)
- Stable or expanding margins
- ROE >15%
- Low debt/equity
- High free cash flow conversion
- Insider ownership >5%

**Short Screen**
- Declining revenue or decelerating growth
- Margin compression
- Rising receivables / inventory vs. sales
- Insider selling
- Valuation premium to peers without justification
- High short interest with deteriorating fundamentals
- Accounting red flags (auditor changes, restatements)

**Special Situation Screen**
- Recent IPOs / SPACs with lockup expirations
- Spin-offs in last 12 months
- Companies emerging from restructuring
- Activist involvement
- Management changes at underperforming companies

### Step 3: Thematic Sweep

For thematic ideas, research the theme and identify beneficiaries:

1. Define the thesis (e.g., "AI infrastructure spending accelerates through 2026")
2. Map the value chain — who benefits directly vs. indirectly?
3. Identify pure-play vs. diversified exposure
4. Assess which names are already "priced in" vs. under-appreciated
5. Look for second-order beneficiaries that the market hasn't connected to the theme

### Step 4: Idea Presentation

For each idea that passes the screen, present:

**[Company Name] — [Long/Short] — [One-Line Thesis]**

| Metric | Value | vs. Peers |
|--------|-------|-----------|
| Market cap | | |
| EV/EBITDA (NTM) | | |
| P/E (NTM) | | |
| Revenue growth | | |
| EBITDA margin | | |
| FCF yield | | |

**Thesis (3-5 bullets):**
- Why this is mispriced
- What the market is missing
- Catalyst to realize value

**Key Risks:**
- What would make this wrong

**Suggested Next Steps:**
- Build full model? Deep-dive diligence? Expert call?

### Step 5: Output

- Shortlist of 5-10 ideas with one-page summaries
- Screening criteria and methodology documented
- Comparison table across all ideas
- Prioritized list: which ideas to research first

## Important Notes

- Screens surface candidates, not conclusions — every screen output needs fundamental work
- The best ideas often come from intersections (e.g., quality company at value price due to temporary headwind)
- Avoid crowded trades — check ownership data, short interest, and how many analysts cover the name
- Contrarian ideas need a catalyst — being early without a catalyst is the same as being wrong
- Track idea hit rates over time — which screens and approaches produce the best ideas?
- Short ideas need higher conviction — timing is harder and risk is asymmetric
