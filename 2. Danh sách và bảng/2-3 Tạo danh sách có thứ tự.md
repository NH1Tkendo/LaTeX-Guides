### Môi trường Enumerate

Để tạo danh sách có thứ tự (mặc định là 1, 2, 3...), ta sử dụng môi trường **enumerate**.

- **Cú pháp cơ bản**:
    ```
    \begin{enumerate}
        \item Pizza
        \item Pasta
        \item Taco
    \end{enumerate}
    ```
### Danh sách Lồng nhau (Nested Lists)

Tương tự như danh sách không thứ tự, bạn có thể lồng ghép các loại danh sách khác nhau vào bên trong môi trường `enumerate`.

1. **Enumerate trong Enumerate**:
    
    - Tạo danh sách con có thứ tự bên trong danh sách cha.
        
    - LaTeX tự động thay đổi kiểu đánh số cho cấp con (ví dụ: cấp 1 là số, cấp 2 là chữ cái a, b...).

	```
    \begin{enumerate}
        \item Pizza
        \item Pasta
        \begin{enumerate} % Danh sách con
            \item Spaghetti
        \end{enumerate}
    \end{enumerate}
    ```
    
2. **Itemize trong Enumerate**:
    
    - Lồng danh sách gạch đầu dòng (bullet points) vào trong danh sách đánh số.

    ```
    \begin{enumerate}
        \item Taco
        \begin{itemize} % Danh sách không thứ tự con
            \item Good
        \end{itemize}
    \end{enumerate}
    ```
    

### Tùy chỉnh Kiểu đánh số (Custom Numbering)

Để thay đổi kiểu ký hiệu (ví dụ: số La Mã, bảng chữ cái) thay vì số 1, 2, 3 mặc định, bạn cần sử dụng gói lệnh (package) hỗ trợ.

#### 1. Khai báo gói lệnh

Thêm dòng sau vào phần đầu tài liệu (preamble):

Đoạn mã

```
\usepackage{enumerate}
```

#### 2. Sử dụng tham số tùy chọn

Thêm tham số vào trong ngoặc vuông `[...]` ngay sau `\begin{enumerate}` để định nghĩa kiểu hiển thị.

- **Số La Mã thường (i, ii, iii...)**:
    
    Đoạn mã
    
    ```
    \begin{enumerate}[(i)]
        \item Item 1
    \end{enumerate}
    ```
    
- **Số La Mã in hoa (I, II, III...)**:
    
    Đoạn mã
    
    ```
    \begin{enumerate}[I.]
        \item Item 1
    \end{enumerate}
    ```
    
- **Chữ cái (a, b, c...)**:
    
    Đoạn mã
    
    ```
    \begin{enumerate}[a)]
        \item Item 1
    \end{enumerate}
    ```
    

> **Ghi chú**: Các ký tự đi kèm như dấu ngoặc đơn `()` hoặc dấu chấm `.` trong tham số tùy chọn sẽ được hiển thị y hệt trong kết quả cuối cùng.