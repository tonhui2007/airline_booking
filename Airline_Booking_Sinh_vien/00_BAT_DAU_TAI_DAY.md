# BẮT ĐẦU TẠI ĐÂY — Bài thực hành dữ liệu đặt vé máy bay

> Đọc trong 3 phút. Tài liệu đầy đủ và **chính thức** là `De_bai_Hang_khong.docx`.

## Bạn sẽ làm gì?

Nhận một tệp dữ liệu đặt vé của hai hãng hàng không mô phỏng **có lỗi cài sẵn** (10.325 dòng × 24 cột) và biến nó thành:

| Sản phẩm | Số lượng |
|---|---|
| Bảng dữ liệu sạch có truy vết (gồm bảng đặt chỗ và bảng tổng hợp theo tháng) | 5 tệp CSV |
| Câu hỏi phân tích (hủy đặt chỗ, mùa vụ nhu cầu, lead time, giá vé, chuyến đi…) | 10 câu |
| Biểu đồ đạt chuẩn | 8 hình |
| Insight có bằng chứng | 6 insight |
| Báo cáo | 8–12 trang |

Không cần học máy. Dữ liệu và hai hãng là mô phỏng phục vụ học tập. Không cần tài khoản Kaggle. Chỉ cần Python, pandas, matplotlib.

## 5 bước khởi động (15 phút)

1. **Đọc trang 2 của đề** (“Bài tập trong một trang”) và **Mục 3** (sơ đồ quy trình).
2. **Mở notebook** `airline_student_starter.ipynb`
   - *Colab:* File → Upload notebook; bảng 📁 Files → tải `data/airline_bookings_dirty.csv` lên.
   - *Máy cá nhân:* giữ nguyên cấu trúc thư mục này, mở notebook tại đây.
3. **Chạy ô 0.1 và 0.2.** Phải thấy: `✅ Đầu vào đúng 10.325 dòng × 24 cột`.
4. **Phân công** theo Mục 14 của đề; đặt lịch 5 buổi.
5. **Bắt đầu Giai đoạn A** — khảo sát, *chưa sửa gì*.

## Quy trình 5 giai đoạn

```
A Khảo sát  →  B Làm sạch (B1–B8)  →  C Bảng sạch & kiểm tra  →  D 10 câu hỏi  →  E Insight & nộp
  ≈ 2 giờ          ≈ 3,5 giờ                ≈ 2 giờ                  ≈ 3 giờ          2–5 giờ
```

Mỗi giai đoạn trong notebook có **thẻ nhiệm vụ** (mục tiêu, các bước, bẫy thường gặp) và **ô tự kiểm tra** in ✅ / ❌.

## Ba nguyên tắc không được vi phạm

- ❌ **Không sửa tay** tệp CSV, không thay bằng bộ dữ liệu gốc sạch.
- ❌ **Không đoán dữ liệu** — không sửa được bằng bằng chứng thì để thiếu và ghi lý do; không điền trung bình.
- ❌ **Không kết luận vượt dữ liệu** — chỉ có 2 hãng hàng không ở dữ liệu mô phỏng, 2024–2026; không suy ra nguyên nhân hủy đặt chỗ; `avg_ticket_fare` là giá vé bình quân/hành khách; `booking_value_est` chỉ là ước tính giá trị vé, không phải doanh thu thực tế.

## Trước khi nộp

```bash
python tools/kiem_tra_nop_bai.py NhomXX_HangKhong
```

Nộp `NhomXX_HangKhong.zip` khi công cụ **không còn ❌**. Cấu trúc thư mục bài nộp: Mục 12 của đề.
