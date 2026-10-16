## Phần 1. Phân tích
- **Lỗi file nhị phân (Binary File)**: File `.docx` chứa mã XML nén và dữ liệu nhị phân nên hệ thống Git không thể đọc, đối chiếu hay hiển thị trực tiếp nội dung trên trình duyệt GitHub.
- **Xung đột toàn bộ file (Merge Conflict)**: Git không thể tách nhỏ từng dòng văn bản trong file Word để so sánh, dẫn đến xung đột toàn bộ file mỗi khi có người chỉnh sửa.
- **Đặc tính Markdown (`.md`)**: Là văn bản thô (Plain Text) cực kỳ nhẹ, an toàn tuyệt đối trước lỗi hỏng cấu trúc (như mất 1 byte dữ liệu) và được hiển thị trực quan trực tiếp trên GitHub.
## Phần 2. Hoàn thiện
# 🌿 GreenTech Project

> *Giải pháp công nghệ xanh bảo vệ môi trường và phát triển bền vững.*

## 1. Giới thiệu
GreenTech là dự án ứng dụng công nghệ để bảo vệ môi trường, thúc đẩy cuộc sống xanh cho cộng đồng.

## 2. Mục tiêu
- Tạo ra giải pháp công nghệ xanh tối ưu.
- Nâng cao ý thức cộng đồng về bảo vệ môi trường.
- Giảm thiểu rác thải nhựa và phát triển bền vững.

## 3. Quy tắc làm việc nhóm với Git & Markdown
1. Luôn thực hiện `git pull` để cập nhật code mới trước khi sửa.
2. Thực hiện `git add`, `git commit`, `git push` thường xuyên.
3. Đồng bộ với nhánh chính để hạn chế xung đột.
4. Thảo luận với nhóm trước khi chỉnh sửa file quan trọng.