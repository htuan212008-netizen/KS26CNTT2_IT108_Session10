# Phần 1. Phân tích bài toán
1.Tiết kiệm Token (74%): Markdown dùng ký hiệu tối giản (**, #, |), trong khi HTML chứa nhiều thẻ rườm rà, khiến số lượng token tăng vọt (~2.350 so với ~620 tokens).

2.Tốc độ phản hồi nhanh: Ít token hơn giúp giảm tải bộ nhớ và cửa sổ ngữ cảnh (Attention Window), rút ngắn thời gian phản hồi của AI từ ~8.2 giây xuống ~1.6 giây.

3.Độ chính xác cao: Giúp AI dễ dàng bóc tách thông tin cốt lõi mà không bị nhiễu bởi mã nguồn HTML.
# Phần 2. So sánh & Đánh giá
## 1. Bảng so sánh chi tiết

|Tiêu chí so sánh|Ngôn ngữ Markdown|Ngôn ngữ HTML|
|:-|:-|:-|
|Cú pháp định dạng|Tối giản, dùng ký tự ngắn gọn|Phức tạp, nhiều thẻ đóng/mở|
|Mức độ tiêu thụ Token|Thấp (Tiết kiệm ~74%)|Cao (Lãng phí token)|
|Tốc độ phản hồi của AI|Nhanh (~1.6 giây)|Chậm (~8.2 giây)|
|Chi phí vận hành API|Thấp (~$0.0062 / lần)|Cao (~$0.0235 / lần)|
|Độ dễ đọc|Rất cao, gọn gàng|Thấp, dễ bị rối mắt|
## 2. Giải pháp tối ưu cho hệ thống "GreenTech"

**Giải pháp lựa chọn**: Sử dụng Markdown làm chuẩn định dạng phản hồi dữ liệu.

**Lập luận lý do:**
- Giúp hệ thống nông nghiệp tiết kiệm đáng kể chi phí API khi phục vụ lượng lớn truy vấn từ nông dân.
- Tốc độ phản hồi nhanh (~1.6 giây) mang lại trải nghiệm mượt mà, tức thì cho người dùng.
- Giải phóng tài nguyên tính toán để AI tập trung vào chất lượng chuyên môn tư vấn cây trồng.