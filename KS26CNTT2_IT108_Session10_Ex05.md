## Phần 1. Phân tích
### Input/Output
- Input (Đầu vào): Tín hiệu nhiệt độ và độ ẩm không khí thu thập từ cảm biến thời tiết đặt tại vườn lan.

- Output (Đầu ra): Lệnh kích hoạt rơ-le điều khiển máy bơm nước và hệ thống phun sương tự động khi độ ẩm xuống thấp hoặc nhiệt độ vượt ngưỡng.
### Sơ đồ phối hợp phần cứng
Cảm biến->Vi điều khiển (SoC)->Hệ thống van bơm/Phun sương tưới
## Phần 2. Triển khai

# 🚀Dự án Smart-Farm (Hệ thống Tự động hóa Chăm sóc Vườn Lan)
**Giải pháp nông nghiệp thông minh tích hợp IoT ứng dụng vi điều khiển và cảm biến thời gian thực.**
## 1. Mô tả hệ thống
Hệ thống **Smart-Farm** tự động theo dõi môi trường và điều khiển tưới nước cho vườn lan, giúp cây phát triển tối ưu mà không cần can thiệp thủ công liên tục.
## 2. Sơ đồ phần cứng & Input/Output
- Sơ đồ: Cảm biến DHT22 $\rightarrow$ Vi điều khiển (SoC) $\rightarrow$ Rơ-le van bơm/Phun sương.
- Input: Tín hiệu nhiệt độ, độ ẩm từ cảm biến.
- Output: Lệnh bật/tắt máy bơm nước và phun sương.
## 3. Quy trình xử lý lệnh CPU (Fetch–Decode–Execute)
- **Fetch (Đọc lệnh)**: CPU lấy mã lệnh bật bơm từ bộ nhớ thông qua Program Counter.
- **Decode (Giải mã)**: Bộ giải mã xác định lệnh kích hoạt cổng GPIO cho rơ-le van nước.
- **Execute (Thực thi)**: Phát tín hiệu điện áp điều khiển mở van cấp nước cho vườn lan.
## 4. Mô hình DIKW
- **Data (Dữ liệu thô)**: Điện áp cảm biến (ADC value = 712).
- **Information (Thông tin)**: Nhiệt độ 36.5°C, độ ẩm 55% lúc 12:00 trưa.
- **Knowledge (Tri thức)**: Nhiệt độ > 35°C và độ ẩm < 60% $\rightarrow$ Cần phun sương hạ nhiệt.
- **Wisdom (Trí tuệ)**: Tối ưu hóa chu kỳ sinh trưởng của lan theo từng mùa.
## 5. Tính năng hệ thống
- [x] Giám sát nhiệt độ & độ ẩm 24/7 thời gian thực.
- [x] Tự động phun sương khi trời nắng gắt.
- [x] Cảnh báo thông số bất thường qua giao diện.
- [ ] Điều khiển thủ công từ xa qua mạng.
## 6. Bảng thông số kỹ thuật thiết bị
|Thiết bị|Model|Chức năng chính|Thông số cơ bản|
|:-|:-|:-|:-|
|Vi điều khiển|ESP32 NodeMCU|Xử lý & Kết nối Wi-Fi|Dual-Core 240MHz, Flash 4MB|
|Cảm biến|DHT22 (AM2302)|Đo nhiệt độ & độ ẩm|Sai số nhiệt độ chênh nhau 0,5°C|
|Cơ cấu chấp hành|Relay Module 5V|Đóng/mắt máy bơm|Tải AC 250V/10D hoặc DC 30V/10A|
## 7. Hướng dẫn cài đặt & Vận hành
1. **Kết nối phần cứng**: Cắm nguồn Adapter 5V cho bo mạch trung tâm và kiểm tra đèn báo nguồn.
2. **Lắp đặt cảm biến**: Đặt cảm biến DHT22 ở vị trí trung tâm thoáng khí trong vườn lan.
3. **Kiểm tra van tưới**: Kết nối đường ống và nhấn nút thử nghiệm để đảm bảo van phun sương hoạt động tốt.
## Phần 3. Kiểm thử
## 8. Lưu ý xử lý sự cố (Đầy RAM)
 ### ⚠️ Xử lý tràn bộ nhớ nhật ký (RAM Overflow):
   1. Ngắt kết nối các tiến trình ghi log tạm thời.
   2. Khởi động lại thiết bị (Reboot) để xóa bộ nhớ đệm RAM.
   3. Giảm tần suất ghi nhật ký hệ thống (ví dụ: từ mỗi giây thành mỗi 5 phút) để tránh lặp lại lỗi. 