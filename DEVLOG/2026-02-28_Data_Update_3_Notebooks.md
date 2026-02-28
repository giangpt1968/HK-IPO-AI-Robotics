# DEVLOG: 2026-02-28

## Project: Update Real Data for Biren, MiniMax, Zhipu Notebooks

### Summary
Cập nhật dữ liệu thực tế cho 3 notebooks phân tích IPO. Tất cả đều đang dùng dữ liệu template từ Edge Medical (02675.HK) - sai hoàn toàn.

---

## Vấn đề phát hiện

Cả 3 notebooks dùng chung dữ liệu Edge Medical:

| Thông số | Template cũ (SAI) | Biren (THẬT) | MiniMax (THẬT) | Zhipu (THẬT) |
|----------|-------------------|--------------|----------------|--------------|
| **IPO Price** | HKD 43.24 | HKD 19.60 | HKD 165.00 | HKD 116.20 |
| **IPO Date** | 08/01/2026 | 02/01/2026 | 09/01/2026 | 08/01/2026 |
| **Proceeds** | $144M | $717M | $619M | $558M |
| **Market Cap** | $2.15B | $6.0B | $6.6B | $6.6B |
| **Revenue FY24** | RMB 160M | RMB 3,368M | $30.5M | RMB 312M |
| **Founder** | N/A | Zhang Wen | Yan Junjie | Tang Jie |
| **Cornerstone** | Tencent/ADIA | 23 investors ($372M) | 14 investors ($350M) | 11 investors (HKD 2.98B) |

---

## Dữ liệu đã cập nhật

### Biren Technology (06082.HK)
- **Founded:** Sep 2019, by Zhang Wen (Ex-SenseTime President)
- **IPO:** Jan 2, 2026 @ HKD 19.60, raised $717M
- **Day 1:** +75.8% (close HKD 34.46), retail oversubscribed 2,347x
- **Financials:** Revenue RMB 3,368M (FY24, +443% YoY), Net Loss -RMB 1.54B
- **Products:** BR100 GPU (7nm, >1 PFLOPS FP16), BR104
- **Risk:** US Entity List (Oct 2023)
- **Pre-IPO funding:** ~$1.2B (11 rounds), Qiming, IDG, Hillhouse

### MiniMax (00100.HK)
- **Founded:** Dec 2021, by Yan Junjie (Ex-SenseTime)
- **IPO:** Jan 9, 2026 @ HKD 165, raised $619M
- **Day 1:** +109% (close HKD 345), retail oversubscribed 1,837x
- **Financials:** Revenue $53.4M (9M25), Net Loss -$512M
- **Products:** Hailuo AI (video), Talkie, MiniMax-01 LLM, ABAB 6.5
- **200M+ users, 70%+ revenue from overseas**
- **Pre-IPO funding:** ~$850M, Tencent, Alibaba, IDG, miHoYo

### Zhipu AI (02513.HK)
- **Founded:** Jun 2019, by Tang Jie (Tsinghua Prof)
- **IPO:** Jan 8, 2026 @ HKD 116.20, raised $558M
- **Day 1:** +13.2% (close HKD 131.50), retail oversubscribed 1,159x
- **Financials:** Revenue RMB 312M (FY24), Net Loss -RMB 2.96B
- **Products:** GLM models, ChatGLM (30M downloads), bigmodel.cn (700K users)
- **World's first listed AGI company**
- **Pre-IPO funding:** ~$1.5B (12 rounds), Saudi Aramco, Alibaba, Tencent

---

## Edge Medical template remnants removed
- Replaced surgical robot references with industry-specific terms
- Replaced Intuitive Surgical/MicroPort peers with appropriate AI peers
- Replaced medical terminology (bệnh viện, phẫu thuật) with AI terms
- Updated all IPO terms, financial data, funding history, cornerstone investors

## Files Modified
- `IPO_Analysis_Biren_06082HK_v1.ipynb`
- `IPO_Analysis_MiniMax_00100HK_v1.ipynb`
- `IPO_Analysis_Zhipu_02513HK_v1.ipynb`

---

---

## Axera v1 & v2: Data Verification & Fix

### Lỗi phát hiện khi verify với prospectus

| Thông số | Notebook (SAI) | Prospectus (ĐÚNG) |
|----------|---------------|-------------------|
| **Năm thành lập** | 2017 | **2019** |
| **Revenue FY2022** | RMB 85M | **RMB 50.2M** |
| **Revenue FY2023** | RMB 180M | **RMB 230.1M** |
| **Revenue FY2024** | RMB 340M | **RMB 472.9M** |
| **Net Loss FY2022** | -RMB 350M | **-RMB 611.6M** |
| **Net Loss FY2023** | -RMB 550M | **-RMB 743.1M** |
| **Net Loss FY2024** | -RMB 920M | **-RMB 904.2M** |
| **OmniVision** | $100M | **$35M** |
| **Youngor** | $85M | **$35M** |
| **Cornerstone count** | 2 investors | **16 investors** |

### Files fixed
- `IPO_Analysis_Axera_00600HK_v1.ipynb` - 4 cells
- `IPO_Analysis_Axera_00600HK_v2.ipynb` - 17 fixes + 1 markdown

---

---

## Session 6: Steps 1-10 Full Data Update

### Problem
Cells 0-1 (header/summary) were updated in Session 5, but Steps 1-10 (Cells 6-29) still contained Edge Medical template data:
- IPO price 43.24 throughout
- Medical terminology (clinical validation, surgical, NMPA)
- Wrong financial data, cornerstone investors, products, risks

### Solution
Created comprehensive update scripts:
1. `_update_steps_all.py` - Updated cells 6, 8, 10, 13, 15, 17, 19, 23, 27, 29 (70 changes)
2. `_fix_cell13.py` - Regex-based fix for Cell 13 IPO terms (whitespace mismatch)
3. Global 43.24 replacement in markdown cells and outputs
4. NaN-safe chart code fix for Biren/Zhipu Cell 13

### Cells Updated per Notebook

| Cell | Content | Changes |
|------|---------|---------|
| 2 | Methodology markdown | Replaced 43.24 with correct IPO price |
| 6 | Step 1 - Company Overview | Company name, sector, founded, products |
| 8 | Step 2 - Financials | Revenue, losses, margins, growth rates |
| 10 | Step 3 - Growth Metrics | KPIs, TAM, market position |
| 13 | Step 4 - IPO Terms | Price, proceeds, use of funds, shares |
| 15 | Step 5 - Pre-IPO Funding | Rounds, investors, valuation history |
| 17 | Step 6 - Cornerstone | Investor names, amounts, lock-up |
| 19 | Step 7 - Day 1 Performance | Returns, oversubscription, volume |
| 23 | Step 8 - Competitive | Peers, moat, regulatory landscape |
| 27 | Step 9 - KPIs | Tracking metrics for each company |
| 29 | Step 10 - Verdict | Final assessment and price targets |

### Key Data Corrections
- **Biren revenue** was 10x wrong: RMB 336.8M -> RMB 3,368M (FY24)
- All medical terminology replaced with AI-specific terms
- NaN-unsafe `v*100` fixed to `(v * 100 if pd.notna(v) else np.nan)`
- Output cells cleaned of stale medical references

### Verification
Final grep confirms zero matches for: 43.24, clinical, NMPA, surgical, Edge Medical, 02675, MicroPort, Intuitive Surgical, vật tư tiêu hao, hệ thống mới lắp đặt

---

## Session 7: Axera v2 Data Verification & Fix

### Issues Found & Fixed

| Cell | Issue | Fix |
|------|-------|-----|
| **Cell 1** | Gross margin ~30% (wrong) | Changed to ~21-26% (verified from prospectus) |
| **Cell 1** | EV/Sales ~6x (wrong) | Changed to ~32x (HKD 16.58B / RMB 472.9M) |
| **Cell 10** | Gross profit values wrong | Recalculated from verified margins: 25.9%, 25.7%, 21.0%, 21.2% |
| **Cell 11** | Chart divided by 1e6 (data already in millions) | Removed /1e6 - values now display correctly |
| **Cell 11** | Comments referenced "1H2025" | Fixed to "9M2025" |
| **Cell 13** | Use of proceeds 45/25/15/15 (wrong) | Fixed to 60/15/5/10/10 per prospectus |
| **Cell 15** | Only 2 cornerstone investors ($70M) | Added all 16 investors ($185M total) |
| **Cell 19** | Black Sesame market share "~80%" | Fixed to ~5% (realistic) |
| **Cell 21** | IPO proceeds used 1,116.6M (wrong) | Fixed to 2,790M HKD net proceeds |
| **Cell 21** | Burn rate from "1H2025" 89M (wrong) | Fixed to 9M2025 855.7M / 3 quarters |
| **Cell 21** | Gross margin "~63%" in peer table | Fixed to ~21% |
| **Cell 21** | EV/Sales "10-15x" in peer table | Fixed to ~32x |

### Verified Financial Data (from prospectus)

| Period | Revenue (RMB) | Gross Margin | Net Loss (RMB) |
|--------|--------------|-------------|----------------|
| FY2022 | 50.2M | 25.9% | -611.6M |
| FY2023 | 230.1M | 25.7% | -743.1M |
| FY2024 | 472.9M | 21.0% | -904.2M |
| 9M2024 | 254M | ~21% | -691M |
| 9M2025 | 269M | 21.2% | -856M |

### Use of Proceeds (from prospectus)
- 60% Technology platform optimization & new products
- 15% New technology R&D
- 5% Sales expansion
- 10% M&A / acquisitions
- 10% Working capital

### 16 Cornerstone Investors ($185M total)
WILL Semiconductor (OmniVision) $35M, Youngor $35M, JSC International $15M, Desay SV $15M, NGS Super $10M, Factorial Master Fund $10M, Joyson Electronics $10M, Hel Ved $8M, Valliance $8M, Mingshan Capital $8M, Jupiter Global $5M, GRANITE ASIA IX $5M, Haowell+CICC $5M, NonaVerse $5M, Qingdao Guanlan+Guotai Junan $5M, Jinyi Capital $5M

*Session ended: 2026-02-28*
