

- **Họ tên:**NGUYỄN ĐỨC GIA HUY 
- **Lớp:** CNTT2 
- **Link repository Pha2:** —
- **Công cụ AI đã dùng:** Codex (đáp án tham khảo tổng hợp)

> Các kết quả dưới đây là đáp án tham khảo. Link chia sẻ chưa có vì chưa chạy prompt trong các cuộc trò chuyện độc lập có thể chia sẻ.

## 4.2. Trích xuất tin nhắn đặt vé ra JSON

**KET QUA AI**

```json
[
  {
    "ma_goi": "SVT",
    "ngay_su_kien": "2026-12-20",
    "nguoi_lon": 2,
    "tre_em": 1,
    "loai_ve": "thuong",
    "ghi_chu": null
  },
  {
    "ma_goi": "FZ",
    "ngay_su_kien": "2027-01-05",
    "nguoi_lon": 3,
    "tre_em": 0,
    "loai_ve": "thuong",
    "ghi_chu": "hỗ trợ xe lăn"
  },
  {
    "ma_goi": "VIP",
    "ngay_su_kien": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "loai_ve": "vip",
    "ghi_chu": "hỗ trợ tìm chỗ cho người khiếm thị"
  }
]
```

**Link trò chuyện:** Chưa có link chia sẻ thực tế; kết quả này là đáp án mẫu.

## 4.3. Báo giá vé bằng Chain-of-Thought

**KET QUA AI**

```text
1. Tiền người lớn: 5 × 1.200.000 = 6.000.000 đồng.
2. Tiền trẻ em: trẻ 8 tuổi = 70% × 1.200.000 = 840.000 đồng; trẻ 10 tuổi = 840.000 đồng; bé 3 tuổi dưới 5 tuổi nên miễn phí = 0 đồng. Tổng tiền trẻ em = 1.680.000 đồng.
3. Tiền vé trước giảm giá: 6.000.000 + 1.680.000 + 0 = 7.680.000 đồng.
4. Nhóm có 5 người lớn nên được giảm 5%: 7.680.000 × 5% = 384.000 đồng. Tiền vé sau giảm = 7.680.000 − 384.000 = 7.296.000 đồng.
5. Phụ thu khu ghế ưu tiên: 1 × 300.000 = 300.000 đồng. Khoản này không được giảm giá.
6. Tổng tiền: 7.296.000 + 300.000 = 7.596.000 đồng.
[RESULT: 7.596.000 đồng]
```

**Link trò chuyện:** Chưa có link chia sẻ thực tế; kết quả này là đáp án mẫu.

### b) Kiểm tra kết quả AI

Kết quả đúng. Các bước áp dụng đúng giá SVT, mức 70% cho trẻ 8 và 10 tuổi, miễn phí cho trẻ 3 tuổi, giảm 5% trên tiền vé vì nhóm có đủ 5 người lớn, và cộng phụ thu 300.000 đồng không giảm giá. Tổng đúng là **7.596.000 đồng**.

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```json
{"loai_su_co":"sai_khu_vuc","so_khach":2,"so_hiep_bi_anh_huong":2,"tom_tat":"Hai khách bị xếp sang khu không mái che trong hai hiệp đầu dù đã cam kết khu có mái."}
```

**Link trò chuyện:** Chưa có link chia sẻ thực tế; kết quả này là đáp án mẫu.

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
|---|---:|---|---|
| Đúng thông tin | 0/5 | “Vé Sân Vận Động bên em giá 1.000.000đ/người” sai; giá chuẩn là 1.200.000 đồng/người lớn. “Anh huỷ trước 3 ngày thì được hoàn tiền đầy đủ” sai; huỷ trước 3 ngày thuộc mức hoàn 50% (nhóm từ 3 đến 6 ngày). Mỗi nội dung được 0/2,5 điểm. | “Vé SVT có giá 1.200.000 đồng/người lớn. Nếu anh huỷ trước sự kiện 3 ngày, anh được hoàn 50% tiền vé.” |
| Đầy đủ | 2/3 | Câu trả lời có đề cập giá và chính sách huỷ, nhưng thiếu lời mời khách cung cấp ngày trận đấu và số lượng vé để đặt. | “Anh cho em xin ngày trận đấu và số lượng vé cần đặt để em hỗ trợ thêm nhé.” |
| Giọng điệu | 1/2 | “xem rất đã luôn ạ” và “nha anh” tạo sắc thái suồng sã, chưa chuyên nghiệp; lời chào và cách xưng hô nhìn chung lịch sự. | Dùng câu trung tính, chuyên nghiệp, ví dụ: “Vé SVT có giá 1.200.000 đồng/người lớn.” |

**Tổng điểm: 3/10**

**Link trò chuyện:** Chưa có link chia sẻ thực tế; kết quả này là đáp án mẫu.
