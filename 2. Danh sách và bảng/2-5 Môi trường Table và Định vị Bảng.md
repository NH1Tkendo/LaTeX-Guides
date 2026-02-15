### 1. Vấn đề của môi trường `tabular` đơn thuần

Khi chỉ sử dụng môi trường `tabular`, LaTeX xem bảng đó như một ký tự văn bản kích thước lớn (a big symbol). Điều này dẫn đến hai vấn đề:

- Bảng nằm chen chúc trong dòng văn bản (inline).
    
- Không thể tự động căn giữa hoặc thêm chú thích một cách chuyên nghiệp.
    

### 2. Môi trường `table` (The Table Environment)

Để giải quyết các vấn đề trên, ta cần bao bọc (wrap) môi trường `tabular` bên trong môi trường `table`. Đây là một **môi trường trôi nổi** (floating environment) giúp LaTeX tự động tính toán vị trí hiển thị tốt nhất.

Đoạn mã

```
\begin{table}[tùy_chọn_vị_trí]
    \centering          % Lệnh căn giữa
    \caption{...}       % Lệnh chú thích
    \begin{tabular}{...}
        ...
    \end{tabular}
\end{table}
```

### 3. Căn giữa bảng (Centering)

Để bảng hiển thị ở chính giữa trang giấy (thay vì mặc định lệch trái), sử dụng lệnh `\centering` ngay sau `\begin{table}` và trước `\begin{tabular}`.

### 4. Tùy chỉnh vị trí hiển thị (Placement Specifiers)

Vị trí của bảng được quy định trong ngoặc vuông `[]` sau `\begin{table}`. Các tham số phổ biến:

|**Tham số**|**Ý nghĩa (Tiếng Anh)**|**Mô tả**|
|---|---|---|
|**h**|Here|Đặt bảng ngay tại vị trí hiện tại trong mã nguồn (nếu còn đủ chỗ).|
|**t**|Top|Đặt bảng ở đầu trang.|
|**b**|Bottom|Đặt bảng ở cuối trang.|
|**!**|Override/Shout|Dấu chấm than dùng để "ép" LaTeX tuân theo tham số đi kèm (ví dụ `!h` hoặc `!t`), bỏ qua các quy tắc thẩm mỹ mặc định của LaTeX.|

**Lưu ý:** Nếu dùng `[!t]` ngay trang đầu tiên, bảng có thể bị đẩy lên trên cả tiêu đề bài viết (Title), do đó cần cân nhắc khi sử dụng.

### 5. Thêm chú thích cho bảng (Adding Captions)

Sử dụng lệnh `\caption{Nội dung chú thích}` để:

- Tạo dòng mô tả cho bảng.
    
- Tự động đánh số thứ tự (Ví dụ: Table 1: Here is my table).
    
- Lệnh này thường đặt bên trong môi trường `table`.
    

### 6. Mã nguồn tổng hợp (Full Code Example)

Ví dụ dưới đây tạo một bảng được căn giữa, đặt ở ngay vị trí mã nguồn (`h`) và có chú thích:

Đoạn mã

```
\begin{table}[h] % Đặt bảng tại vị trí này (here)
    \centering   % Căn giữa bảng
    \caption{Bảng dữ liệu mẫu của tôi} % Thêm chú thích
    
    \begin{tabular}{|c|c|}
        \hline
        Cột A & Cột B \\
        \hline
        Dữ liệu 1 & Dữ liệu 2 \\
        \hline
    \end{tabular}
\end{table}
```