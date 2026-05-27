---
name: morning-note
description: 草擬精簡的晨間會議筆記，彙整隔夜發展、交易點子與追蹤股的重大事件，緊湊、有觀點、可行動。觸發詞：晨間筆記、晨會、隔夜發生什麼、交易點子。
---

> 🇹🇼 **台灣在地化**：本技能屬「台灣版財經外掛」，產出一律**繁體中文（台灣用語）**並遵循 `taiwan-finance-context` 規則。台股量化數據優先用 **TWSE MCP（`twstock`）**；術語對照：10-K→年報、10-Q→季報、US GAAP→T-IFRS、SEC/EDGAR→公開資訊觀測站(MOPS)、$→新台幣(萬/億/兆)、ticker→股票代號；範例用台股（如台積電 2330）；查不到的數字標 `[需查證]`，不可編造；結尾標「※ 僅供學術討論與教學示範，非投資建議」。以下為原版方法論，請依上述規則以繁中產出。

# Morning Note

## Workflow

### Step 1: Overnight Developments

Scan for relevant events across coverage universe:

**Earnings & Guidance**
- Any coverage companies reporting overnight or pre-market?
- Earnings surprises (beat/miss on revenue, EPS, key metrics)
- Guidance changes (raised, lowered, maintained)

**News & Events**
- M&A announcements or rumors
- Management changes
- Product launches or regulatory decisions
- Analyst upgrades/downgrades from competitors
- Macro data or policy changes affecting the sector

**Market Context**
- Overnight futures / pre-market moves
- Sector ETF performance
- Relevant commodity or currency moves
- Key economic data releases today

### Step 2: Morning Note Format

Keep it tight — a morning note should be readable in 2 minutes:

---

**[Date] Morning Note — [Analyst Name]**
**[Sector Coverage]**

**Top Call: [Headline — the one thing PMs need to hear]**
- 2-3 sentences on the key development and why it matters
- Stock impact: price target, rating reiteration/change

**Overnight/Pre-Market Developments**
- [Company A]: One-line summary of earnings/news + our take
- [Company B]: One-line summary + our take
- [Sector/Macro]: Relevant sector-wide development

**Key Events Today**
- [Time]: [Company] earnings call
- [Time]: Economic data release (expectations vs. our view)
- [Time]: Conference or investor day

**Trade Ideas** (if any)
- [Long/Short] [Company]: 1-2 sentence thesis + catalyst
- Risk: What would make this wrong

---

### Step 3: Quick Takes on Earnings

If a coverage company reported, provide a quick reaction:

| Metric | Consensus | Actual | Beat/Miss |
|--------|-----------|--------|-----------|
| Revenue | | | |
| EPS | | | |
| [Key metric] | | | |
| Guidance | | | |

**Our Take**: 2-3 sentences — is this good or bad for the stock? Does it change our thesis?

**Action**: Maintain / Upgrade / Downgrade rating? Adjust price target?

### Step 4: Output

- Markdown text for email/Slack distribution
- Word document if formal distribution is needed
- Keep to 1 page max — PMs and traders won't read more

## Important Notes

- Be opinionated — morning notes that just summarize news without a view are useless
- Lead with the most important thing — don't bury the headline
- "No news" is a valid morning note — say "nothing material overnight, maintaining positioning"
- Distinguish between actionable events (earnings, M&A) and noise (minor analyst notes, non-events)
- Time-stamp your takes — if you're writing at 6am, note that pre-market may change by open
- If you're wrong, own it in the next morning note — credibility matters more than being right every time
