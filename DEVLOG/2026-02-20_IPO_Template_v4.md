# DEVLOG: 2026-02-20

## Project: IPO Analysis Template V4

### Tóm tắt
Tạo phiên bản V4 hoàn chỉnh của template phân tích IPO, sửa các vấn đề cấu trúc của V3.

---

## Vấn đề với V3

V3 có cấu trúc lộn xộn:
- Trộn lẫn tiếng Anh và tiếng Việt
- Đánh số không nhất quán (2.1, 2.2... xen lẫn BƯỚC 1, 2, 3...)
- Các section cũ không liên kết với framework 10 bước
- Thiếu Executive Summary

**Ví dụ vấn đề:**
```
## BƯỚC 3: PHÂN TÍCH TÀI CHÍNH  ← Mới (tiếng Việt)
### 2.1 KPI helpers              ← Cũ (tiếng Anh, số lạc)
### 2.2 Quick charts             ← Cũ (tiếng Anh)
## 3) Deal terms & proceeds      ← Cũ (tiếng Anh)
## BƯỚC 5: CORNERSTONE           ← Mới (nhảy số, thiếu BƯỚC 4)
```

---

## Giải pháp V4

### Cấu trúc mới (hoàn toàn tiếng Việt)

```
PHẦN 0: TÓM TẮT ĐIỀU HÀNH (Executive Summary)
PHẦN 1: PHƯƠNG PHÁP PHÂN TÍCH (Framework 10 bước)
THIẾT LẬP MÔI TRƯỜNG (Import libraries)
BƯỚC 1: THÔNG TIN CÔNG TY
BƯỚC 2: LỊCH SỬ GỌI VỐN
BƯỚC 3: PHÂN TÍCH TÀI CHÍNH
  └── 3B: Biểu đồ tài chính
BƯỚC 4: ĐIỀU KHOẢN IPO & SỬ DỤNG VỐN
BƯỚC 5: CORNERSTONE & LOCK-UP
BƯỚC 6: SẢN PHẨM & LỢI THẾ CẠNH TRANH
BƯỚC 7: CHỈ SỐ NGÀNH
BƯỚC 8: SO SÁNH & ĐỊNH GIÁ
BƯỚC 9: ĐÁNH GIÁ RỦI RO
BƯỚC 10: KẾT LUẬN ĐẦU TƯ
PHỤ LỤC: THEO DÕI SAU IPO
HƯỚNG DẪN SỬ DỤNG TEMPLATE
```

### Cải tiến

| Hạng mục | V3 | V4 |
|----------|----|----|
| Ngôn ngữ | Trộn lẫn Anh/Việt | 100% tiếng Việt |
| Cấu trúc | Lộn xộn | 10 bước liên tục |
| Executive Summary | Không có | Có (Phần 0) |
| Variable names | Tiếng Anh | Tiếng Việt (cong_ty, tai_chinh...) |
| Logic flow | Nhảy bước | Liên tục từ 1-10 |

---

## Files

- **Đã tạo:** `IPO_Analysis_Template_Edge_Medical_02675HK_v4.ipynb`
- **Giữ nguyên:** `_v3.ipynb` (để tham khảo)

---

## Hướng dẫn sử dụng V4

1. **Duplicate** notebook cho công ty mới
2. **Update** các dictionary: `cong_ty`, `tai_chinh`, `cornerstone`...
3. **Run All** cells
4. **Review** đánh giá và kết luận
5. **Export** PDF nếu cần báo cáo

---

## Next Steps

- [ ] Test template với Biren (AI chips)
- [ ] Test template với Zhipu (LLM)
- [ ] Thêm templates KPI cho các ngành khác

---

*Session ended: 2026-02-20*
