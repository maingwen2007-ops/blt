# BÀI LÀM PHA 2 (ĐỀ LUYỆN TẬP CHỦ ĐỀ CHẠY AFFILIATE)

- **Họ tên: Lê Anh Duy**
- **Lớp:**
- **[Link repository Pha2](https://github.com/maingwen2007-ops/blt)**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini): Gemini**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đăng ký gói Affiliate ra JSON

**KET QUA AI**

```text
[
  {
    "ma_goi": "TT",
    "ngay_bat_dau": "2026-12-20",
    "creator_chinh": 2,
    "thuc_tap_sinh": 1,
    "hang_tai_khoan": "thuong",
    "ghi_chu": null
  },
  {
    "ma_goi": "SP",
    "ngay_bat_dau": "2027-01-08",
    "creator_chinh": 3,
    "thuc_tap_sinh": 0,
    "hang_tai_khoan": "thuong",
    "ghi_chu": "Có một bạn đang bó bột chân cần ngồi bàn gần cửa ra vào"
  },
  {
    "ma_goi": "PRO",
    "ngay_bat_dau": null,
    "creator_chinh": 4,
    "thuc_tap_sinh": 0,
    "hang_tai_khoan": "vip",
    "ghi_chu": "cần mượn thêm đèn trợ sáng và phông xanh để quay mẫu"
  }
]
```

**[Link trò chuyện](https://share.gemini.google/yTM9AO7FkzQ0)**

## 4.3. Báo giá gói Affiliate bằng Chain-of-Thought

**KET QUA AI**

```text
**1. Tiền Creator chính:**

* Gói được chọn: TT – Gói TikTok Affiliate với đơn giá 1.500.000 đồng/Creator chính.
* Số lượng Creator chính: 4 người.
* Tính toán: $4 \times 1.500.000 = 6.000.000$ đồng.

**2. Tiền thực tập sinh:**

* Thực tập sinh (từ 15 đến dưới 18 tuổi) tính 60% giá Creator chính: $1.500.000 \times 60\% = 900.000$ đồng/người.
* Số lượng thực tập sinh: 2 người (16 tuổi và 17 tuổi đều thuộc nhóm từ 15 đến dưới 18 tuổi).
* Bé 7 tuổi đi cùng ngồi khu chờ được miễn phí (0 đồng).
* Tính toán: $2 \times 900.000 = 1.800.000$ đồng.

**3. Tổng tiền gói:**

* Tổng tiền gói = Tiền Creator chính + Tiền thực tập sinh.
* Tính toán: $6.000.000 + 1.800.000 = 7.800.000$ đồng.

**4. Giảm giá team:**

* Team có 4 Creator chính (đạt điều kiện từ 4 Creator chính trở lên) nên được giảm 10% trên tổng tiền gói.
* Số tiền được giảm: $7.800.000 \times 10\% = 780.000$ đồng.
* Tiền gói sau giảm: $7.800.000 - 780.000 = 7.020.000$ đồng.

**5. Phụ thu thuê mic:**

* Đơn giá thuê mic: 250.000 đồng/bộ (không áp dụng giảm giá).
* Số lượng thuê: 2 bộ.
* Tính toán: $2 \times 250.000 = 500.000$ đồng.

**6. Tổng tiền:**

* Tổng tiền = Tiền gói sau giảm + Phụ thu.
* Tính toán: $7.020.000 + 500.000 = 7.520.000$ đồng.

[RESULT: 7.520.000 đồng]
```

**[Link trò chuyện](https://share.gemini.google/wkiB3DB8YZgG)**

### b) Kiểm tra kết quả AI

Kết quả của AI là đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "sai_phong",
  "so_khach": 3,
  "so_ca_bi_anh_huong": 2,
  "tom_tat": "Nhóm 3 khách bị xếp sai phòng thiếu đèn livestream và ồn trong 2 ca thực hành đầu."
}
```

**[Link trò chuyện](https://share.gemini.google/KRNyUOIINKKV)**

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
| --- | --- | --- | --- |
| **Đúng thông tin (50%)** | 3.0 / 5.0 | **Câu bị lỗi:** "Gói TikTok Affiliate bên mình giá chỉ 1.200.000đ/người thôi... Bạn báo huỷ trước 5 ngày thì được hoàn lại đủ 100% tiền nha"<br>

<br>**Lý do sai:** Không có dữ liệu chuẩn của trung tâm để đối chiếu xác thực mức giá 1.200.000đ và điều kiện hoàn tiền trước 5 ngày, nên không thể chấm trọn điểm tính chính xác. | Đối chiếu lại bảng giá và quy định hoàn hủy hiện hành của trung tâm trước khi tư vấn (ví dụ: *"Gói TikTok Affiliate bên mình có học phí là [Giá chuẩn]đ/người. Trường hợp bạn báo hủy trước [Số ngày quy định] ngày sẽ được hoàn [Tỷ lệ]% học phí theo chính sách trung tâm."*). |
| **Đầy đủ (30%)** | 1.5 / 3.0 | **Câu bị lỗi:** Toàn bộ đoạn phản hồi (thiếu thông tin kêu gọi hành động ở cuối câu).<br>

<br>**Lý do sai:** Đã trả lời được 2 ý về giá và hoàn tiền, nhưng thiếu hoàn toàn phần mời khách hàng cung cấp ngày đợt thực chiến và số lượng suất muốn đăng ký. | Bổ sung câu kêu gọi ở cuối: *"Để mình hỗ trợ giữ chỗ, bạn vui lòng cho mình xin thông tin về ngày đợt thực chiến bạn muốn tham gia và số lượng suất đăng ký nhé!"* |
| **Giọng điệu (20%)** | 0.5 / 2.0 | **Câu bị lỗi:** "Dạ hello bạn nha!", "gắn link là nổ đơn hoa hồng trăm triệu luôn ạ", "cứ chốt lẹ kẻo hết slot nè!"<br>

<br>**Lý do sai:** Sử dụng từ ngữ suồng sã, thiếu chuyên nghiệp (*hello bạn nha, chốt lẹ, nè*) và cam kết doanh thu/hoa hồng ảo (*nổ đơn hoa hồng trăm triệu*). | Sửa thành văn phong lịch sự, thực tế: *"Dạ chào bạn! Khóa học cung cấp kiến thức và kỹ năng thực chiến để bạn xây dựng kênh hiệu quả. Bạn sớm phản hồi thông tin để mình hỗ trợ đăng ký giữ suất cho bạn nhé."* |
| **Tổng điểm** | **5.0 / 10** |  |  |
```

**[Link trò chuyện](https://share.gemini.google/rjTwZk2wJpHr)** 
