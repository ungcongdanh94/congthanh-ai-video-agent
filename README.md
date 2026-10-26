# CÔNG THẢNH AI Video Agent — Prototype

Prototype web app chạy trực tiếp trên trình duyệt, không cần cài đặt dependencies.

## Chạy thử
1. Giải nén thư mục.
2. Mở `index.html` bằng Chrome, Edge hoặc Firefox.
3. Nhập tên dự án và prompt, chọn loại video, tải ảnh tham chiếu.
4. Nhấn **Tạo storyboard mẫu**.
5. Nhấn **Tạo cảnh (demo)** cho từng cảnh, sau đó duyệt hoặc từ chối.
6. Chỉ khi tất cả cảnh đã được duyệt, nút ghép mới hoạt động.
7. Nhấn **Xuất storyboard JSON** để tải cấu hình dự án.

## Giới hạn hiện tại
- Đây là prototype frontend, chưa có backend, tài khoản, database, Redis/BullMQ hoặc triển khai Railway.
- Tạo cảnh và ghép video chỉ mô phỏng trạng thái; không tạo video AI thật và không xuất MP4.
- Ảnh chỉ được giữ trong phiên trình duyệt, không được tải lên server.
- Chưa kết nối nhà cung cấp video, mô hình ngôn ngữ, dịch vụ TTS hoặc FFmpeg.

## Để đưa lên production
Cần bổ sung Next.js API, xác thực, PostgreSQL/Prisma, Redis/BullMQ, object storage, provider adapter đã xác minh API, worker FFmpeg và các kiểm thử bảo mật.
