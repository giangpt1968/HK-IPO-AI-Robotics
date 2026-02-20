# DEVLOG: 2026-02-19

## Project: IPO Analysis Template for AI & Robotics Stocks

### Summary
Hoàn thành xây dựng IPO Analysis Template dạng Research Report, sử dụng Edge Medical (02675.HK) làm case study.

---

## Tasks Completed

### 1. Bug Fixes
- [x] Fixed length mismatch error trong KPI cell (`revenue_yoy` list có 3 elements nhưng DataFrame có 4 rows)

### 2. Template Enhancement - New Sections Added
| Section | Description |
|---------|-------------|
| Pre-IPO Funding History | Track valuation trajectory từ Series A → IPO |
| Cornerstone Investors | Danh sách investors, lock-up schedule |
| Sector-Specific KPIs | Templates cho AI Chips, LLM, Surgical Robotics |
| Cash Burn & Runway | Tính toán runway dựa trên burn rate |
| Geopolitical Risk | US sanctions, Entity List assessment |
| Trading Signals | Technical levels, catalysts calendar |

### 3. Edge Medical Data Filled
- **Pre-IPO Funding**: Series A ($15M) → Series B ($92M) → Series C ($200M) → IPO ($154M)
- **Cornerstone Investors**: Tencent, ADIA, UBS AM, OrbiMed, Huaxia Fund, LYFE Capital (13-15 total)
- **Surgical Robotics KPIs**: >4,000 procedures, 4 products, CE Mark obtained
- **Trading Levels**: IPO HKD 43.24, ATH HKD 73.70, Support 48.00/43.24
- **Key Dates**: 6M Lock-up Jul 8, 2026 | 12M Lock-up Jan 8, 2027

### 4. Report Format Conversion
Chuyển notebook từ technical analysis tool → Educational Research Report:

- [x] Added Methodology section (Framework 10 bước)
- [x] Added glossary (thuật ngữ IPO cho người mới)
- [x] Added detailed explanations trước mỗi code block
- [x] Improved display formatting với box drawing, color-coded assessments
- [x] Added IC Memo template với decision framework
- [x] Added Appendix hướng dẫn sử dụng cho IPO khác
- [x] Added Disclaimer

---

## Files Modified
- `IPO_Analysis_Template_Edge_Medical_02675HK_v3.ipynb` - Main notebook

## Data Sources Used
- HKEX Prospectus
- AAStocks (cornerstone investors)
- Crunchbase (funding history)
- Yahoo Finance, Investing.com (trading data)
- PMC/ScienceDirect (clinical trial data)
- MedRobot.tech (industry news)

---

## Investment Conclusion for Edge Medical

| Item | Value |
|------|-------|
| **Recommendation** | WATCH / Accumulate on dips |
| **Entry Zone** | HKD 50-55 |
| **Target Range** | HKD 70-80 |
| **Stop Loss** | HKD 40 |
| **Key Catalyst** | 1H26 Earnings (Aug-Sep 2026) |
| **Key Risk Date** | Jul 8, 2026 (6M Lock-up expiry) |

---

## Next Steps (Tomorrow)
- [ ] Create separate notebooks for other IPOs: Biren, Zhipu, Minimax, Axera
- [ ] Build peer comparison table with live data
- [ ] Add automated data fetching (optional)
- [ ] Test template with another IPO

---

## Notes
- Template designed to be reusable for HK/SG/Shanghai IPOs
- Focus on AI & Robotics sector (different risk profile vs traditional IPOs)
- Geopolitical risk section critical for China tech companies

---

*Session ended: 2026-02-19*
