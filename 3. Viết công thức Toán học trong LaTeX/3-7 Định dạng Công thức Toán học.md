### 1. Quy tắc chọn chế độ hiển thị (Display Mode)

Khi soạn thảo, việc nhồi nhét một công thức quá dài vào dòng văn bản (inline math) sẽ làm bố cục trở nên rối mắt.

- **Vấn đề:** Công thức dài dùng dấu `$` (inline) làm xấu đoạn văn.
    
- **Quy tắc ngón tay cái (Rule of thumb):** Nếu công thức dài hơn **1/3 chiều rộng văn bản** (text width), bạn nên chuyển sang chế độ hiển thị khối (display math).
    
- **Cách thực hiện:** Thay thế cặp dấu `$` bằng cặp `\[ ... \]`.
    

### 2. Quản lý khoảng trắng (Spacing)

Trong các biểu thức có kèm điều kiện (ví dụ: $x \neq 1$), LaTeX mặc định không tạo đủ khoảng cách giữa phương trình và điều kiện, gây cảm giác chật chội.

**Các lệnh tạo khoảng cách phổ biến:**

|**Lệnh**|**Mô tả**|**Ví dụ sử dụng**|
|---|---|---|
|`\quad`|Tạo một khoảng trắng rộng (khoảng bằng chữ M)|`y = x \quad \forall x`|
|`\qquad`|Tạo khoảng trắng rộng gấp đôi `\quad`|`y = x \qquad \forall x`|
|`\,`|Khoảng trắng rất nhỏ (thin space)|Dùng trong tích phân (xem mục 4)|
|`\`|Khoảng trắng thường (như phím Space)|`a \ b`|
|`\!`|Khoảng trắng âm (negative space - thu hẹp khoảng cách)|Dùng khi các ký tự quá xa nhau|

### 3. Dấu ngoặc trên nhiều dòng (Multi-line Brackets)

Khi sử dụng môi trường `multline` để ngắt dòng một phương trình dài, cặp lệnh tự động `\left( ... \right)` sẽ **gây lỗi** nếu dấu mở và dấu đóng nằm trên hai dòng khác nhau.

**Giải pháp:** Thay thế `\left` và `\right` bằng các lệnh chỉnh kích thước thủ công (manual sizing).

**Các cấp độ kích thước (từ nhỏ đến lớn):**

1. `\big`
    
2. `\Big` (Viết hoa chữ B)
    
3. `\bigg` (Hai chữ g)
    
4. `\Bigg` (Viết hoa chữ B và hai chữ g)
    

**Ví dụ mã nguồn:**

Đoạn mã

```
\begin{multline*}
    % Dòng 1: Dùng dấu mở ngoặc thủ công kích thước lớn nhất
    \Bigg( x^2 + 3x^3 + ... \\
    % Dòng 2: Dùng dấu đóng ngoặc thủ công tương ứng
    + 5z + 6w \Bigg)
\end{multline*}
```

### 4. Tinh chỉnh Tích phân (Integrals)

Theo quy chuẩn thẩm mỹ toán học, cần có một khoảng cách nhỏ tách biệt giữa hàm số và vi phân $dx$.

- **Vấn đề:** $\int \cos x dx$ (dính liền, khó đọc).
    
- **Giải pháp:** Thêm lệnh `\,` trước $dx$.
    
- **Mã lệnh:** `\int \cos x \, dx`
    
- **Kết quả:** $\int \cos x \, dx$ (thoáng và chuẩn xác hơn).
    

---

**Tổng kết:**

- Dùng **Display Math** cho công thức dài.
    
- Dùng `\quad` hoặc `\qquad` để tách biệt điều kiện.
    
- Dùng `\Big`, `\bigg`... thay cho `\left`/`\right` khi ngắt dòng.
    
- Luôn thêm `\,` trước $dx$ trong tích phân.