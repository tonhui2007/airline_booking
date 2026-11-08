# Mẫu viết insight

**Yêu cầu:** tối thiểu **6 insight** từ **ít nhất 4 chủ đề khác nhau**; mỗi insight **80–120 từ**.
Chủ đề gợi ý: hãng hàng không · mùa vụ nhu cầu · lead time · quốc gia · phân khúc thị trường · chính sách giá vé · giá vé (giá vé bình quân) · thời gian chuyến đi · đổi hạng ghế · chất lượng dữ liệu.

---

## Bảng tổng hợp (điền trước khi viết)

| # | Chủ đề | Bằng chứng (Câu / Bảng / Hình) | Phát hiện chính (1 câu) |
|---|---|---|---|
| 1 | Hãng hàng không | Câu 2 · `outputs/tables/q02_airline_cancel.csv` · `outputs/figures/fig01_airline_cancel.png` | Trong 6.522 đặt chỗ của Aurora Air, 27,11% bị hủy; ở Horizon Wings là 27,86% trên 3.478 đặt chỗ, cao hơn 0,75 điểm phần trăm. |
| 2 | Mùa vụ nhu cầu | Câu 3 · `outputs/tables/q03_monthly_departures_2025.csv` · `outputs/figures/fig02_monthly_departures_2025.png` | Trong 12 tháng năm 2025, tháng 12 có nhiều chuyến khởi hành nhất (592), còn tháng 10 ít nhất (404), chênh 188 đặt chỗ (46,5% so với tháng 10). |
| 3 | Lead time | Câu 4 · `outputs/tables/q04_leadtime_cancel.csv` · `outputs/figures/fig03_leadtime_cancel.png` | Nhóm đặt trước từ 181 ngày có tỷ lệ hủy cao nhất (44,63%; 266/596), cao hơn nhóm 0–7 ngày (22,22%; 172/774) 22,41 điểm phần trăm. |
| 4 | Quốc gia hành khách | Câu 5 · `outputs/tables/q05_top10_country.csv` · `outputs/figures/fig04_top10_country.png` | Trong 10.000 đặt chỗ sạch, VNM đứng đầu với 2.080 đặt chỗ (20,80%), gấp khoảng 3,14 lần JPN (663; 6,63%); 105 đặt chỗ thiếu quốc gia. |
| 5 | Phân khúc thị trường | Câu 6 · `outputs/tables/q06_segment_cancel.csv` · `outputs/figures/fig05_segment_cancel.png` | Online OTA có tỷ lệ hủy cao nhất (29,43%; 1.152/3.915), cao hơn Corporate (21,44%; 199/928) 7,99 điểm phần trăm. |
| 6 | Chất lượng dữ liệu | Câu 1 · `outputs/tables/q01_before_after.csv` · `outputs/quality_report.csv` | Sau làm sạch và gộp 325 record phụ, số dòng giảm từ 10.325 xuống 10.000 đặt chỗ; đây là gộp bản ghi, không phải bằng chứng rằng các đặt chỗ bị loại bỏ. |

---

## Insight 1 — [Tiêu đề ngắn nêu phát hiện]

- **Câu hỏi / chủ đề:**
- **Phát hiện chính:** (1 câu)
- **Số liệu, đơn vị và mẫu số:** … trên … đặt chỗ; điều kiện lọc: …; đã loại … đặt chỗ vì …
- **So sánh làm rõ phát hiện:** (chênh … điểm phần trăm / gấp … lần / so với hãng hàng không, tháng, nhóm …)
- **Ý nghĩa trong phạm vi dữ liệu:** (hai hãng hàng không, giai đoạn 2024–2026)
- **Giới hạn hoặc thông tin cần kiểm chứng:**
- **Bằng chứng:** Bảng `outputs/tables/…` · Hình `outputs/figures/…`

**Đoạn hoàn chỉnh (80–120 từ):**

> …

*Nhân bản cấu trúc này cho Insight 2 đến 6.*

---

## Ví dụ giả định (KHÔNG phải kết quả của bộ dữ liệu này)

> Trong 1.000 đặt chỗ có trạng thái của hãng hàng không A, 400 bị hủy (40%), cao hơn hãng hàng không B (25% trên 800 đặt chỗ) 15 điểm phần trăm. Khoảng cách xuất hiện ở hầu hết các tháng, nên không chỉ do một mùa cao điểm. Tuy nhiên, hai hãng hàng không khác loại hình và cơ cấu kênh bán; cần dữ liệu về lý do hủy và chính sách giá để giải thích chênh lệch. *(Nguồn: Bảng q02, Hình 1)*

| Cách viết | Đánh giá |
|---|---|
| “Hãng hàng không A bị hủy nhiều.” | Yếu — không số liệu, không mẫu số, không so sánh |
| “Hãng hàng không A nên bắt buộc chính sách giá vé để giảm hủy đặt chỗ.” | Vượt bằng chứng — dữ liệu không chứng minh quan hệ nhân quả |
| Đoạn ví dụ ở trên | Tốt — có số liệu, mẫu số, so sánh, ý nghĩa, giới hạn, nguồn |

---

## Tự kiểm tra từng insight

- [ ] Có số liệu **và** mẫu số; nêu rõ điều kiện lọc (ví dụ “chỉ đặt chỗ không hủy, avg_ticket_fare > 0”)
- [ ] Có ít nhất một phép so sánh (điểm phần trăm, số lần, giữa hãng hàng không/tháng/nhóm)
- [ ] Nêu ý nghĩa **trong phạm vi hai hãng hàng không của mẫu** (không suy rộng ra toàn ngành)
- [ ] Nêu ít nhất một giới hạn cụ thể
- [ ] Trỏ tới đúng tên bảng/hình
- [ ] Không dùng từ nhân quả (“khiến”, “dẫn đến”, “nhờ … nên”); không gọi `avg_ticket_fare`/`booking_value_est` là doanh thu thực tế
- [ ] Nêu cỡ mẫu khi so sánh nhóm nhỏ
- [ ] Không lặp lại cùng một thông tin với insight khác

**Nhắc lại:** Một tỷ lệ chỉ có ý nghĩa khi nêu đối tượng được tính và điều kiện lọc. Không điền số giả định vào báo cáo.
