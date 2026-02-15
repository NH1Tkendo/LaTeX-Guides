### 1. Khởi tạo môi trường
```
\begin{tabular}{...}
    % Nội dung bảng
\end{tabular}
```

### 2. Định nghĩa cột và căn lề 

Số lượng và cách căn lề của các cột được xác định trong tham số ngay sau lệnh `\begin{tabular}`. Có 3 tùy chọn căn lề cơ bản:

- `l`: Căn lề trái (Left-aligned)
    
- `c`: Căn lề giữa (Centered)
    
- `r`: Căn lề phải (Right-aligned)
    

**Kẻ đường dọc (Vertical Lines):**

- Sử dụng ký tự gạch đứng `|` (pipe) giữa các ký tự định dạng cột để tạo đường kẻ dọc.
    
- Ví dụ: `{|c|r|l|}` sẽ tạo ra 3 cột (giữa, phải, trái) với các đường kẻ dọc ngăn cách và bao quanh.
    

### 3. Cấu trúc nội dung bảng

Nội dung bên trong bảng được tổ chức theo quy tắc sau:

- **Ngăn cách cột:** Sử dụng ký tự ampersand `&` để chuyển sang cột tiếp theo.
    
- **Ngắt dòng (Xuống hàng):** Sử dụng hai dấu gạch chéo ngược `\\` để kết thúc một hàng.
    

### 4. Các lệnh kẻ đường ngang (Horizontal Lines)

Để bảng chuyên nghiệp hơn, ta sử dụng lệnh `\hline` để tạo các đường kẻ ngang:

- `\hline`: Kẻ một đường ngang đơn.
    
- Có thể viết liên tiếp hai lệnh `\hline \hline` để tạo đường kẻ đôi.
    
- Thường được đặt ở đầu bảng, cuối bảng hoặc giữa các hàng để phân tách tiêu đề.
    

### 5. Ví dụ minh họa (Example)

Dưới đây là mã nguồn để tạo một bảng đầy đủ các đường kẻ khung và căn lề khác nhau:

Đoạn mã

```
\begin{tabular}{|r|c|l|}
    \hline
    Cột 1 (Phải) & Cột 2 (Giữa) & Cột 3 (Trái) \\
    \hline \hline
    Dữ liệu A1 & Dữ liệu A2 & Dữ liệu A3 \\
    \hline
    Dữ liệu B1 & Dữ liệu B2 & Dữ liệu B3 \\
    \hline
\end{tabular}
```
