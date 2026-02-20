# DEVLOG: 2026-02-20 (Session 2 & 3)

## Project: Axera Semiconductor (00600.HK) Data Update

### Summary
Cập nhật đầy đủ dữ liệu thực tế cho notebook phân tích IPO của Axera Semiconductor.
Loại bỏ hoàn toàn dữ liệu Edge Medical còn sót lại từ template gốc.

---

## Data Sources Used

| Nguồn | URL | Thông tin |
|-------|-----|-----------|
| Pandaily | https://pandaily.com/axera-launches-ipo-secures-185-m-cornerstone-investment-set-to-become-china-s-first-edge-ai-chip-stock | Cornerstone investors |
| Caproasia | https://www.caproasia.com/2026/01/31/china-ai-chipmaker-axera-semiconductor-hong-kong-ipo-to-raise-379-million-with-expected-ipo-listing-on-10th-february-2026-axera-semiconductor-previously-shanghai-zhiaixin-semiconductor-technology/ | Investor list |
| Asia Tech Daily | https://asiatechdaily.com/axeras-hong-kong-ipo-tests-investor-appetite-for-chinas-edge-ai-chipmakers/ | Financial data |
| Yahoo Finance | https://finance.yahoo.com/news/chinese-ai-chipmaker-axera-semiconductor-230920676.html | IPO details |
| Axera Official | https://en.axera-tech.com/ | Products, technology |
| CNX Software | https://www.cnx-software.com/2026/01/27/maixcam2-modular-4k-ai-camera-is-based-on-axera-ax630-soc-with-3-2-tops-npu/ | Product specs |

---

## Session 3: Bug Fixes & Cleanup

### Lỗi đã sửa

| Lỗi | Nguyên nhân | Fix |
|-----|-------------|-----|
| `\!=` SyntaxError | Escaped backslash trong JSON | Replace `\\!=` -> `!=` |
| Unterminated string | `print("` bị ngắt dòng | Merge broken lines |
| Edge Medical data | Template gốc chưa clean | Replace toàn bộ |

### Dữ liệu Edge Medical đã loại bỏ

| Hạng mục | Edge Medical (cũ) | Axera (mới) |
|----------|-------------------|-------------|
| **Mã CK** | 02675.HK | 00600.HK |
| **Ngành** | Robot phẫu thuật | Edge AI Chips |
| **Giá IPO** | HKD 43.24 | HKD 28.20 |
| **Ngày IPO** | 08/01/2026 | 10/02/2026 |
| **Cornerstone** | Tencent, ADIA, OrbiMed, LYFE | OmniVision, Youngor |
| **Lock-up 6M** | 08/07/2026 | 10/08/2026 |
| **Lock-up 12M** | 08/01/2027 | 10/02/2027 |
| **Peers** | Intuitive Surgical, MicroPort | Nvidia, Horizon Robotics |

### Moat examples đã cập nhật

| Loại Moat | Edge Medical (cũ) | Axera (mới) |
|-----------|-------------------|-------------|
| Regulatory | FDA, CE, NMPA | PSA Certified, automotive certs |
| Switching Cost | Bác sĩ quen dùng robot | Khách hàng đã tích hợp SDK |
| Network Effect | Bệnh viện dùng, data tốt | Developers, ecosystem mạnh |

### Peer comparison đã cập nhật

| Cũ | Mới |
|----|-----|
| Intuitive Surgical (ISRG) | Nvidia (NVDA) |
| MicroPort MedBot (2252.HK) | Horizon Robotics (9660.HK) |

---

## Sections Updated

### PHẦN 0: Executive Summary
- Rating: 3/5 (THEO DÕI / Tích lũy khi giảm)
- Entry zone: HKD 24-26
- Target: HKD 35-40
- Stop loss: HKD 20

### BƯỚC 1: Thông tin công ty
- Founder/CEO: Dr. Xiaoxin Qiu (Ex-Broadcom VP, Ex-Unisoc CTO)
- Industry: Edge AI Chips / Vision AI Processors
- Market position: #1 mid-to-high-end visual edge AI (24.1% share)

### BƯỚC 2: Lịch sử gọi vốn
| Vòng | Thời gian | Số tiền |
|------|-----------|---------|
| Seed | 2019 | $10M |
| Series A | Apr 2021 | $50M |
| Series A+ | Jul 2021 | $30M |
| Series A-IV | Jan 2022 | $126M |
| Series C | Apr 2025 | $140M |
| IPO | Feb 2026 | $379M |

**Pre-IPO Investors:** Qiming Venture Partners, Tencent, Meituan, Ningbo CTS Fund, Chongqing Industrial Fund, Weihao Chuangxin, Xfund Capital, Yuanhe Puhua

### BƯỚC 3: Phân tích tài chính
| Chỉ số | Giá trị |
|--------|---------|
| CAGR 2022-2024 | 206.8% |
| 9M2025 Revenue | RMB 269M |
| 9M2025 Net Loss | RMB 856M |
| R&D / Revenue | >200% |

### BƯỚC 4: Điều khoản IPO
| Hạng mục | Giá trị |
|----------|---------|
| Giá IPO | HKD 28.20 |
| Vốn huy động | ~$379M |
| Market Cap | ~$2.13B |
| H-shares phát hành | 104.9M |

### BƯỚC 5: Cornerstone & Lock-up
| Investor | Số tiền | Lock-up |
|----------|---------|---------|
| OmniVision (WILL Semi) | $100M | 6 tháng |
| Youngor Group | $85M | 6 tháng |

**Lock-up Schedule:**
- Aug 2026: Cornerstone expiry
- Feb 2027: Founders/VCs expiry

### BƯỚC 6: Sản phẩm
| Dòng SP | Segment | Hiệu năng |
|---------|---------|-----------|
| AX620 | Entry IPC | 3.2-12.8 TOPS |
| AX630 | Mid-range Edge | 3.2-12.8 TOPS |
| AX650 | High-end Edge | 18-72 TOPS |
| M55H/M76H | Smart Driving | TBD |

### BƯỚC 7: Chỉ số ngành (đã cập nhật)
- Peers: Nvidia (NVDA), Horizon Robotics (9660.HK)
- Metrics phù hợp với AI chips industry

### BƯỚC 8: So sánh & Định giá (đã cập nhật)
- So sánh với AI chip companies thay vì surgical robots
- Fair value range: HKD 55-75

### BƯỚC 9: Đánh giá rủi ro
- Profitability: CAO (vẫn lỗ lớn)
- Geopolitical: TRUNG BÌNH (chưa nằm trong Entity List)
- Lock-up expiry: CAO (Aug 2026, Feb 2027)
- Competition: TRUNG BÌNH (nhiều đối thủ trong ngành)

### BƯỚC 10: Kết luận đầu tư
- **Khuyến nghị:** THEO DÕI / Tích lũy khi giảm
- **Entry:** HKD 24-26
- **Target:** HKD 35-40
- **Stop Loss:** HKD 20
- **Risk/Reward:** ~1:1.7

---

## Key Insights

1. **Tăng trưởng ấn tượng** - CAGR 206.8% là con số rất cao
2. **Vẫn đang lỗ** - Typical cho chip startup, cần theo dõi runway
3. **Cornerstone mạnh** - OmniVision là strategic partner trong ngành
4. **Lock-up risk** - Cảnh giác Aug 2026 và Feb 2027
5. **Geopolitical OK** - Chưa nằm trong Entity List, nhưng cần monitor

---

## Files Modified
- `IPO_Analysis_Axera_00600HK_v1.ipynb` - Full data update & cleanup

---

## Session 4: Format Update to v2

### Mục tiêu
Cập nhật format hiển thị của Axera v1 để khớp với Edge Medical v4 template.

### Thay đổi chính

| Thành phần | v1 (cũ) | v2 (mới - giống v4) |
|------------|---------|---------------------|
| **Header Cell 1** | `# PHẦN 0:` | `# 📋 PHẦN 0:` (có emoji) |
| **Intro text** | Không có | `**Dành cho người bận rộn**...` |
| **Tổng quan** | `### TỔNG QUAN NHANH` 2 cột | `## 🎯 Tổng quan nhanh` 3 cột |
| **Bảng đánh giá** | `Hạng mục \| Chi tiết` | `Hạng mục \| Đánh giá \| Chi tiết` |
| **Điểm chính** | `### ĐIỂM CHÍNH` | `## 💡 3 điểm chính cần nhớ` |
| **Ngày quan trọng** | `### NGÀY QUAN TRỌNG` | `## 📅 Các mốc thời gian quan trọng` |
| **Phiên bản** | 4.0 | 2.0 |

### Format mới Cell 1 (Executive Summary)
```markdown
---

# 📋 PHẦN 0: TÓM TẮT ĐIỀU HÀNH (Executive Summary)

**Dành cho người bận rộn** - Đọc phần này trước...

---

## 🎯 Tổng quan nhanh

| Hạng mục | Đánh giá | Chi tiết |
|----------|----------|----------|
| **Công ty** | Axera (00600.HK) | Edge AI Chips |
| **Thesis** | 🟢 Tích cực | Dẫn đầu thị trường |
| **Tài chính** | 🟢 Tăng trưởng mạnh | CAGR 206.8% |
| **Định giá** | 🟡 Hợp lý | EV/Sales ~6x |
| **Rủi ro** | 🟡 Trung bình | Vẫn lỗ |
| **Quyết định** | 📊 THEO DÕI | HKD 24-26 |

---

## 💡 3 điểm chính cần nhớ
...

## 📅 Các mốc thời gian quan trọng
...
```

### Files
- **Input:** `IPO_Analysis_Axera_00600HK_v1.ipynb`
- **Output:** `IPO_Analysis_Axera_00600HK_v2.ipynb`

---

## Session 5: Push to GitHub

### Repository
- **URL:** https://github.com/giangpt1968/HK-IPO-AI-Robotics
- **Visibility:** Private

### Files pushed
| File | Mô tả |
|------|-------|
| `README.md` | Project overview |
| `.gitignore` | Ignore rules |
| `DEVLOG/` | 3 session logs |
| `IPO_Analysis_Template_Edge_Medical_*.ipynb` | Template v1-v4 |
| `IPO_Analysis_Axera_*.ipynb` | Axera v1, v2 |
| `IPO_Analysis_Biren_*.ipynb` | Biren v1 |
| `IPO_Analysis_MiniMax_*.ipynb` | MiniMax v1 |
| `IPO_Analysis_Zhipu_*.ipynb` | Zhipu v1 |

### Commit
```
Initial commit: HK IPO AI & Robotics Analysis
Co-Authored-By: Claude Opus 4.5 <noreply@anthropic.com>
```

---

*Session ended: 2026-02-20*
