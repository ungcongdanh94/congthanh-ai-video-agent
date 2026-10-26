# CÔNG THẢNH AI Video Agent — Prototype

Prototype web app chạy trực tiếp trên trình duyệt, không cần cài dependencies.

## Chạy thử
1. Giải nén thư mục.
2. Mở `index.html` bằng Chrome, Edge hoặc Firefox.
3. Nhập tên dự án và prompt, chọn loại video, tải ảnh tham chiếu.
4. Nhấn **Tạo storyboard mẫu**.
5. Nhấn **Tạo cảnh (demo)** cho từng cảnh, sau đó duyệt hoặc từ chối.
6. Chỉ khi tất cả cảnh đã được duyệt, nút ghép mới hoạt động.
7. Nhấn **Xuất storyboard JSON** để tải cấu hình dự án.

## Menu Thêm API nhanh
- Nhấn **Thêm API nhanh** ở menu bên trái hoặc nút trên thanh đầu trang.
- Khai báo tên cấu hình, loại API, nhà cung cấp, endpoint và model.
- Nút **Kiểm tra biểu mẫu** chỉ kiểm tra dữ liệu nhập, không gửi request mạng và không xác minh API key.
- Cấu hình được giữ tạm trong bộ nhớ của tab hiện tại; khi tải lại trang sẽ mất. API key không được lưu trong danh sách hay xuất vào JSON.

**Bảo mật:** Đây là frontend tĩnh. Không nhập API key sản xuất hoặc key có quyền thanh toán. Không thể kết nối API thật an toàn từ GitHub Pages trực tiếp vì key sẽ bị lộ cho trình duyệt. Muốn gọi API thật cần backend (ví dụ Railway) giữ key trong biến môi trường/secret store, xác thực request và gọi nhà cung cấp từ server.

## Giới hạn hiện tại
- Chưa có backend, tài khoản, database, Redis/BullMQ hoặc triển khai Railway.
- Tạo cảnh và ghép video chỉ mô phỏng trạng thái; không tạo video AI thật và không xuất MP4.
- Ảnh chỉ được giữ trong phiên trình duyệt, không được tải lên server.
- Chưa kết nối nhà cung cấp video, mô hình ngôn ngữ, dịch vụ TTS hoặc FFmpeg.

## Để đưa lên production
Cần bổ sung Next.js API, xác thực, PostgreSQL/Prisma, Redis/BullMQ, object storage, provider adapter đã xác minh API, worker FFmpeg và các kiểm thử bảo mật.
