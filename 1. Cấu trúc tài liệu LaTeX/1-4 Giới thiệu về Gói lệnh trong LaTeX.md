### Khái niệm cơ bản

- **Gói lệnh (Package):** Là cách để nhập thêm các chức năng bổ sung từ bên ngoài vào LaTeX, giúp mở rộng khả năng xử lý văn bản (định dạng, công thức, hình ảnh...).
    
- **Cú pháp:** Sử dụng lệnh `\usepackage{}`.
    
- **Vị trí đặt lệnh:** Đặt ngay sau khai báo `\documentclass` và trước `\begin{document}`.
    

### Phần khai báo (Preamble)

- **Định nghĩa:** Khu vực nằm trước lệnh `\begin{document}` được gọi là **Phần khai báo (Preamble)**.
    
- **Chức năng:**
    
    - Chứa các thông tin cấu hình, khai báo gói lệnh.
        
    - Nội dung tại đây **không hiển thị** trực tiếp ra văn bản đầu ra.
        
    - Khoảng trắng (whitespace) hoặc xuống dòng trong Preamble không ảnh hưởng đến văn bản hiển thị, nhưng nên sắp xếp gọn gàng để dễ quản lý.
        
- **Cấu trúc gợi ý:**
    
    1. `\documentclass{...}`
        
    2. Các lệnh `\usepackage{...}`
        
    3. Thông tin tiêu đề, tác giả
        
    4. `\begin{document}`
        

---

## Các ví dụ về Gói lệnh

### 1. Gói `csquotes` (Trích dẫn)

Dùng để tạo các định dạng trích dẫn đẹp mắt và chuẩn xác hơn so với dấu ngoặc kép thông thường.

- **Khai báo:**
    
    Đoạn mã
    
    ```
    \usepackage{csquotes}
    ```
    
- **Sử dụng:**
    
    Đoạn mã
    
    ```
    \textquote{Nội dung cần trích dẫn}
    ```
    
    _Ví dụ:_ `He said: \textquote{I love learning LaTeX}.`
    
- **Xử lý lỗi thường gặp:**
    
    - **Lỗi:** _Undefined control sequence_ (Chuỗi điều khiển chưa được định nghĩa).
        
    - **Nguyên nhân:** Thường do viết sai tên lệnh (ví dụ viết nhầm `textquotes` số nhiều thay vì `textquote`).
        
    - **Khắc phục:** Kiểm tra lại chính tả của lệnh so với tài liệu hướng dẫn.
        

### 2. Gói `blindtext` (Văn bản giả)

Dùng để tạo ra các đoạn văn bản ngẫu nhiên (tương tự _Lorem Ipsum_), giúp kiểm tra bố cục, khoảng cách giữa các phần trước khi có nội dung thật.

- **Khai báo:**
    
    Đoạn mã
    
    ```
    \usepackage{blindtext}
    ```
    
- **Mẹo:** Nên biên dịch (recompile) ngay sau khi khai báo gói để đảm bảo LaTeX nhận diện đúng và không có lỗi chính tả.
    
- **Sử dụng:**
    
    Đoạn mã
    
    ```
    \blindtext
    ```
    
- **Ứng dụng:**
    
    - Tạo nội dung nhanh để kiểm tra khoảng cách giữa các tiêu đề (Section/Subsection).
        
    - Kiểm tra bố cục khi chèn hình ảnh hoặc danh sách.
        
    - Dễ dàng xóa đi sau khi đã kiểm tra xong giao diện.
        

---

## Tóm tắt quy trình làm việc với Package

1. **Tìm gói cần dùng:** Xác định chức năng cần thêm.
    
2. **Khai báo:** Thêm `\usepackage{ten_goi}` vào Preamble.
    
3. **Kiểm tra:** Biên dịch thử để bắt lỗi cú pháp/chính tả sớm.
    
4. **Sử dụng:** Dùng các lệnh cụ thể mà gói đó cung cấp trong phần thân tài liệu (Main body).
    

> **Ghi chú:** Các gói lệnh (Packages) có thể rất đơn giản (như 2 ví dụ trên) hoặc rất phức tạp với hàng nghìn lệnh con. Khóa học sẽ bắt đầu từ các gói đơn giản và nâng cao dần.