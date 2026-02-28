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
| **Revenue FY24** | RMB 160M | RMB 336.8M | $30.5M | RMB 312M |
| **Founder** | N/A | Zhang Wen | Yan Junjie | Tang Jie |
| **Cornerstone** | Tencent/ADIA | 23 investors ($372M) | 14 investors ($350M) | 11 investors (HKD 2.98B) |

---

## Dữ liệu đã cập nhật

### Biren Technology (06082.HK)
- **Founded:** Sep 2019, by Zhang Wen (Ex-SenseTime President)
- **IPO:** Jan 2, 2026 @ HKD 19.60, raised $717M
- **Day 1:** +75.8% (close HKD 34.46), retail oversubscribed 2,347x
- **Financials:** Revenue RMB 336.8M (FY24), Net Loss -RMB 1.54B
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

*Session ended: 2026-02-28*
