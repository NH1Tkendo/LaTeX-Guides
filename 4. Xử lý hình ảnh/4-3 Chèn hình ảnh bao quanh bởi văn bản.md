### 1. Khai báo gói lệnh

Trước khi sử dụng, cần thêm gói `wrapfig` vào phần khai báo (preamble) của tài liệu.

Đoạn mã

```
\usepackage{wrapfig}
```

### 2. Môi trường `wrapfigure`

Thay vì dùng môi trường `figure` thông thường, ta sử dụng môi trường `wrapfigure`. Môi trường này yêu cầu **hai tham số bắt buộc** để định dạng đúng (nếu thiếu sẽ gây lỗi biên dịch).

**Cú pháp:**

Đoạn mã

```
\begin{wrapfigure}{vị_trí}{chiều_rộng}
    ...
\end{wrapfigure}
```

**Giải thích tham số:**

1. **Vị_trí (Alignment):** Xác định hình ảnh nằm bên trái hay phải.
    
    - `l`: Trái (Left)
        
    - `r`: Phải (Right)
        
2. **Chiều_rộng (Width):** Độ rộng mà khung hình sẽ chiếm dụng.
    
    - Ví dụ: `0.5\textwidth` (chiếm 50% chiều rộng văn bản).
        

**Ví dụ mã nguồn đầy đủ:**

Đoạn mã

```
\begin{wrapfigure}{l}{0.5\textwidth} % Căn trái, rộng 50% trang
    \centering
    \includegraphics[width=0.45\textwidth]{image_filename}
    \caption{Đây là chú thích hình ảnh}
\end{wrapfigure}
```

_Lưu ý: Bên trong `wrapfigure`, bạn vẫn sử dụng `\centering`, `\includegraphics` và `\caption` như bình thường._

---

## Tạo danh sách Hình ảnh và Bảng biểu (Lists of Figures/Tables)

Trong các bài báo khoa học hoặc luận văn, việc tạo mục lục tự động cho hình ảnh và bảng biểu là rất cần thiết.

### 1. Danh sách hình ảnh

Lệnh này sẽ liệt kê tất cả các hình ảnh có sử dụng lệnh `\caption` trong tài liệu.

Đoạn mã

```
\listoffigures
```

### 2. Danh sách bảng biểu

Tương tự như hình ảnh, lệnh này liệt kê tất cả các bảng.

Đoạn mã

```
\listoftables
```