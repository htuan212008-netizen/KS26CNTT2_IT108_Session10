# Phần 1. Thiết kế Kiến trúc Prompt
## Bối cảnh (Context)
Bạn là một gia giúp sinh viên hiểu bài một cách dễ dàng

## Nội dung (Content)
Tôi đang gặp khó khăn khi học về khái niệm "Mô hình IPO (Input - Process - Output) trong trang trại thông minh". Hãy giải thích khái niệm này dựa trên một ví dụ thực tế, gần gũi và dễ hình dung nhất.

## Yêu cầu (Task)
- [ ] Giải thích khái niệm IPO trong trang trại thông minh thật đơn giản
- [ ] Dùng ví dụ gần gũi, dễ hiểu
- [ ] Không dùng thuật ngữ phức tạp
- [ ] Có hình minh hoạ nếu cần

## Không cần
- Không sử dụng các thuật ngữ chuyên ngành quá phức tạp hoặc mã lập trình dài dòng nếu không thực sự cần thiết.
# Phần 2. Sản phẩm phản hồi từ AI
## 1. Input (Đầu vào - Dữ liệu nhận vào):
- Các cảm biến cắm ở đất sẽ đo độ ẩm và nhiệt độ không gian xung quanh.
- Thông tin thu thập được (ví dụ: đất đang khô, độ ẩm chỉ còn 30%) sẽ được gửi về bộ điều khiển trung tâm.
## 2. Process (Xử lý - Bộ não trung tâm):
- Máy tính hoặc vi điều khiển (như Arduino/Raspberry Pi) nhận số liệu độ ẩm từ cảm biến.
- Nó so sánh với mức tiêu chuẩn cài đặt sẵn (ví dụ: độ ẩm chuẩn phải từ 60% trở lên). Nếu thấy thấp hơn, nó sẽ quyết định bật máy bơm nước.
## 3. Output (Đầu ra - Kết quả thực hiện):
- Hệ thống kích hoạt van nước và máy bơm chạy.
- Nước được phun ra các béc tưới để làm ẩm đất, giúp cây trồng phát triển tốt mà không cần con người phải ra ruộng bật công tắc thủ công.