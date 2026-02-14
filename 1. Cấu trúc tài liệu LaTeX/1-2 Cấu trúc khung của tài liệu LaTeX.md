## Cấu trúc khung của tài liệu LaTeX 

### 1. Khai báo loại tài liệu 

Đây là câu lệnh đầu tiên bắt buộc phải có trong mọi tài liệu LaTeX. Nó định nghĩa kiểu định dạng chung cho toàn bộ văn bản.

- **Cú pháp**: `\documentclass{...}`
    
- **Ví dụ**:
    ```
    \documentclass{article}
    ```
    - `article`: Định dạng bài báo (phổ biến nhất).
    - Các tùy chọn khác: `letter` (thư từ), `report` (báo cáo), `book` (sách)...

### 2. Khai báo thông tin tài liệu 

Các thông tin này được khai báo ở phần đầu nhưng **chưa hiển thị** ngay lập tức trong văn bản.

- **Tiêu đề**:
    ```
     \title{Skeleton of a LaTeX Document}
    ```
    
- **Tác giả**:
    ```
    \author{Tên Tác Giả}
    ```
    
- **Ngày tháng**:
    - Cách 1 - Ngày cố định: `\date{20 September 2020}`
    - Cách 2 - Tự động cập nhật ngày hiện tại khi biên dịch: `\date{\today}`
        

### 3. Môi trường tài liệu 

Nội dung thực tế của văn bản phải nằm trong một khối lệnh được gọi là **môi trường** (environment).

- **Cấu trúc**
    ```
    \begin{document}
        % Nội dung văn bản được viết ở đây
    \end{document}
    ```
    
- Mọi văn bản nằm ngoài cặp lệnh `begin` và `end` này sẽ không được hiển thị hoặc gây lỗi.
    

### 4. Hiển thị tiêu đề 

Để in các thông tin metadata (Tiêu đề, Tác giả, Ngày) ra trang giấy, ta cần dùng lệnh `\maketitle` bên trong môi trường tài liệu (thường đặt ngay đầu tiên).

- **Lưu ý**: Lệnh này không cần tham số (arguments) đi kèm.
    
- **Cú pháp**:
    ```
    \begin{document}
        \maketitle
        % Nội dung khác...
    \end{document}
    ```

---

### Tổng hợp mã nguồn (Full Code Snippet)

Dưới đây là đoạn mã hoàn chỉnh cho một tài liệu LaTeX tối giản (Minimal working document):

Đoạn mã

```
% 1. Khai báo class
\documentclass{article}

% 2. Khai báo thông tin (Metadata)
\title{Skeleton of a LaTeX Document}
\author{Your Name}
\date{\today} % Tự động lấy ngày hiện tại

% 3. Môi trường nội dung
\begin{document}

    % 4. Lệnh in tiêu đề ra văn bản
    \maketitle

    % Nội dung chính
    This is where the actual text of the document is going to be placed.

\end{document}
```