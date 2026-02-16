### Khái niệm và Lợi ích

- **Template là gì?** Là đoạn mã nguồn LaTeX đã được người khác viết sẵn cấu trúc và định dạng.
    
- **Lợi ích:**
    
    - Không cần viết tài liệu từ con số 0.
        
    - Tiết kiệm thời gian đáng kể, đặc biệt với các định dạng phức tạp như CV (Sơ yếu lý lịch), bài thuyết trình, hoặc Poster khoa học.
        
    - Chỉ cần tập trung thay đổi nội dung, giữ nguyên thiết kế chuyên nghiệp.
        

### Nguồn tìm kiếm Template

1. **Overleaf Templates:**
    
    - Truy cập thông qua menu trên tài khoản Overleaf hoặc tìm kiếm trên Google.
        
    - Cung cấp nhiều danh mục: Bài báo học thuật, Thư từ, CV, Poster, v.v.
        
2. **Các nguồn khác:**
    
    - Google Search cho các nhu cầu cụ thể.
        
    - **GitHub:** Nơi chứa các phiên bản mới nhất của nhiều mẫu mã nguồn mở.
        

### Nghiên cứu tình huống 1: Poster Khoa học (Scientific Poster)

Quy trình làm việc với một mẫu Poster (ví dụ: mẫu của Đại học Melbourne):

1. **Xem trước (Preview):** Tải xuống file PDF để xem bố cục chung (Tiêu đề căn giữa, Logo, cấu trúc nhiều cột, hình ảnh chèn vào).
    
2. **Xem mã nguồn (View Source):**
    
    - Kiểm tra `\documentclass`: Có thể là các lớp lạ như `poster` (kích thước font chữ lớn, ví dụ 20pt).
        
    - Kiểm tra gói lệnh (Packages): Có thể chứa các gói lạ như `adjustbox` bên cạnh các gói quen thuộc (`amsmath`, `amsfonts`).
        
    - **Lưu ý quan trọng:** Bạn **không cần hiểu từng dòng lệnh**. Mục tiêu là nắm bắt cấu trúc tổng thể.
        
3. **Mở mẫu (Open as Template):** Nhấn nút này để tạo một dự án mới trong tài khoản Overleaf của bạn dựa trên mẫu đó.
    
4. **Chỉnh sửa (Modification):**
    
    - Tìm các môi trường chứa nội dung, ví dụ: môi trường `block`.
        
    - Thử thay đổi các tham số (arguments) để xem kết quả.
        
    
    _Ví dụ mô phỏng cách sửa nội dung trong block:_
    
    Đoạn mã
    
    ```
    % Thay đổi tiêu đề và nội dung của khối
    \begin{block}{Vấn đề quan trọng}{Nội dung chi tiết...}
    ```
    

### Nghiên cứu tình huống 2: Thư trang trọng (Formal Letter)

Tương tự như Poster, bạn có thể tìm các mẫu thư được thiết kế đẹp mắt với màu sắc, độ mờ (opacity) và logo công ty.

- **Quy trình:** Chọn mẫu ưng ý -> `Open as Template` -> Thay thế thông tin cá nhân và nội dung thư.
    
- **Tùy biến:** Hầu hết các mẫu cho phép xóa hoặc thay thế Logo công ty bằng hình ảnh của bạn.
    

### Kết luận

Chìa khóa khi sử dụng Template là kỹ năng **đọc hiểu cấu trúc** và **thử nghiệm**. Ngay cả khi gặp các gói lệnh hoặc lớp văn bản chưa học, bạn vẫn có thể thao tác dựa trên logic của các tham số (tiêu đề, nội dung) để tạo ra tài liệu mong muốn.