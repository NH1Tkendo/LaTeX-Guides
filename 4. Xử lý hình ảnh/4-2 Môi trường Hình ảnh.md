### Vấn đề và Giải pháp

Khi sử dụng lệnh `\includegraphics` trực tiếp trong văn bản, LaTeX coi hình ảnh là một "ký tự khổng lồ", dẫn đến việc bố cục văn bản xung quanh bị phá vỡ và trông không đẹp mắt.

**Giải pháp:** Bao bọc lệnh chèn ảnh bên trong môi trường `figure`. Đây là một "môi trường trôi nổi" (floating environment), tương tự như môi trường `table`, giúp LaTeX quản lý vị trí của hình ảnh tách biệt với dòng chảy văn bản chính.

### Cú pháp cơ bản

Đoạn mã

```
\begin{figure}
    % Các lệnh xử lý ảnh nằm ở đây
    \includegraphics{ten_file_anh}
\end{figure}
```

### Định vị hình ảnh (Placement Specifiers)

Sử dụng các tham số tùy chọn trong ngoặc vuông `[]` ngay sau `\begin{figure}` để gợi ý vị trí đặt hình ảnh mong muốn.

Các tham số phổ biến:

- `h` (here): Đặt hình ảnh xấp xỉ ngay tại vị trí nó xuất hiện trong mã nguồn.
    
- `t` (top): Đặt ở đầu trang.
    
- `b` (bottom): Đặt ở cuối trang (Đây thường là tùy chọn mặc định nếu không ghi gì).
    
- `!`: Dấu chấm than dùng để "ép buộc" LaTeX tuân theo vị trí chỉ định, bỏ qua một số quy tắc nội bộ về dàn trang của LaTeX.
    

**Ví dụ:** Ép buộc đặt ảnh ngay tại vị trí hiện tại.

Đoạn mã

```
\begin{figure}[h!]
    ...
\end{figure}
```

### Căn lề (Alignment)

Sử dụng các lệnh căn lề bên trong môi trường `figure` để điều chỉnh vị trí của nội dung.

- **Căn giữa (Thường dùng nhất):** Sử dụng lệnh `\centering`.
    
- **Căn phải:** Sử dụng lệnh `\flushright`.
    

**Lưu ý:** Các lệnh này cũng có thể dùng để căn lề cho văn bản thông thường, không chỉ giới hạn trong hình ảnh.

**Ví dụ căn giữa ảnh:**

Đoạn mã

```
\begin{figure}[h]
    \centering
    \includegraphics{ten_file_anh}
\end{figure}
```

### Chú thích (Captions)

Sử dụng lệnh `\caption{Nội dung chú thích}` để thêm chú thích và tự động đánh số cho hình ảnh (Ví dụ: Figure 1: Nội dung...).

Vị trí đặt lệnh `\caption` trong mã nguồn quyết định vị trí hiển thị của nó so với hình ảnh:

- **Chú thích bên dưới ảnh (Phổ biến):** Đặt `\caption` phía _sau_ lệnh `\includegraphics`.
    
- **Chú thích bên trên ảnh:** Đặt `\caption` phía _trước_ lệnh `\includegraphics`.
    

**Ví dụ tổng hợp:**

Đoạn mã

```
\begin{figure}[h!]
    \centering
    % Chú thích nằm dưới ảnh
    \includegraphics[width=0.8\textwidth]{example_plot}
    \caption{Đây là biểu đồ ví dụ.}
\end{figure}
```