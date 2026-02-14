### Ghi chú đơn

- **Định nghĩa:** Ghi chú là các đoạn văn bản dùng để hướng dẫn hoặc giải thích cho người đọc mã nguồn (source code), nhưng **không hiển thị** trong tài liệu PDF cuối cùng sau khi biên dịch.
    
- **Cú pháp:** Sử dụng ký tự phần trăm `%`.
    
- **Cơ chế:** LaTeX sẽ bỏ qua tất cả nội dung nằm sau dấu `%` cho đến hết dòng đó.
    

**Ví dụ:**
```
% Đây là một ghi chú trên dòng riêng biệt
\section{Introduction} % Đây là ghi chú cùng dòng (inline comment)
```
### Ghi chú khối

Khi gặp các đoạn mã dài bị lỗi (ví dụ: một bảng chưa hoàn thiện hoặc mã bị sai cú pháp) khiến tài liệu không thể biên dịch, việc thêm dấu `%` vào đầu từng dòng rất mất thời gian.

Để giải quyết vấn đề này, ta sử dụng gói lệnh `comment` để vô hiệu hóa một khối văn bản lớn.

- **Khai báo gói:**  `\usepackage{comment}`

- **Cách sử dụng:** Bao quanh đoạn mã cần ẩn bằng môi trường (environment) `comment`.
    ```
    \begin{comment}
        Đoạn mã bị lỗi hoặc nội dung nháp dài.
        Tất cả nội dung nằm giữa begin và end sẽ bị LaTeX bỏ qua
        tương tự như một ghi chú khổng lồ.
    \end{comment}
    ```
