# CÔNG THẢNH AI Video Agent — Prototype v2

Web app tĩnh để chuẩn bị và quản lý quy trình tạo video bằng Poiiky Studio.

## Chức năng
- Prompt song ngữ Anh–Việt theo mẫu, mặc định 15 giây/cảnh.
- Thư viện ảnh tham chiếu (giới hạn 8 MB/ảnh trong prototype).
- Storyboard nhiều cảnh, gán ảnh và ghi chú model.
- Sao chép prompt EN, VI hoặc song ngữ.
- Mở Poiiky Studio trong tab mới.
- Theo dõi trạng thái thủ công: chưa bắt đầu, sẵn sàng, đang tạo, đã tạo video, đã duyệt, cần tạo lại.
- Xuất/nhập JSON dự án.
- Lưu thông tin dự án/model trong localStorage.

## Chạy thử
Mở `index.html` bằng trình duyệt hiện đại hoặc xuất bản thư mục này bằng GitHub Pages.

## Lưu ý quan trọng
- Không gọi API tạo video.
- Không tự động thao tác Poiiky Studio.
- Không xác nhận video đã tạo thật; người dùng tự cập nhật trạng thái.
- Mẫu prompt được tạo theo template trong trình duyệt, không phải LLM.
- Ảnh tham chiếu được giữ trong bộ nhớ trang hiện tại và không được nhúng vào JSON export. Tải lại trang có thể làm mất ảnh đã thêm; hãy giữ bản gốc trên máy.
- Không nhập API key, mật khẩu hoặc token vào prototype.
- Muốn có AI prompt thật/API, cần backend và tích hợp provider sau này.
