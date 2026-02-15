### 1. Thiết lập tiền sảnh (Preamble)

Để sử dụng đầy đủ các ký hiệu và môi trường toán học chuyên sâu, cần khai báo các gói thư viện từ Hiệp hội Toán học Hoa Kỳ (American Mathematical Society - AMS).

- **Các gói cần thiết**:
    - `amsmath`: Các cấu trúc toán học cơ bản.
    - `amssymb`: Các ký hiệu toán học (Symbols).
    - `amsthm`: Các môi trường định lý (Theorems).

**Mã nguồn khai báo:**
```
\usepackage{amsmath}
\usepackage{amssymb}
\usepackage{amsthm}
```

---

### 2. Toán học trong dòng (Inline Math)

**Khái niệm**: Là các công thức toán học nằm trực tiếp trong đoạn văn bản.

- **Cách thực hiện**: Bao quanh công thức bằng ký hiệu đô la `$ ... $`.
    
- **Đặc điểm**: Nếu không có dấu `$`, LaTeX sẽ hiểu công thức là văn bản thường, dẫn đến sai định dạng (font chữ, khoảng cách).
    
- **Ví dụ**:
    
    - Nhập: `$f(x) = 5x + 3$`
        
    - Kết quả: $f(x) = 5x + 3$
        

> [!CAUTION] Ghi chú quan trọng
> 
> Bạn **phải** đóng dấu `$` ở cuối công thức. Nếu thiếu, LaTeX sẽ báo lỗi biên dịch (Compile error).

---

### 3. Các phép toán và ký hiệu cơ bản

Hầu hết các phép tính số học cơ bản có thể dùng trực tiếp từ bàn phím, một số ký hiệu đặc biệt cần dùng lệnh (command).

|**Ký hiệu**|**Lệnh LaTeX**|**Ví dụ**|**Kết quả**|
|---|---|---|---|
|**Cộng, trừ**|`+`, `-`|`$a + b - c$`|$a + b - c$|
|**Chia**|`/`|`$a / b$`|$a / b$|
|**Dấu chấm nhân**|`\cdot`|`$5 \cdot x$`|$5 \cdot x$|
|**Khác**|`\neq`|`$2 + 2 \neq 5$`|$2 + 2 \neq 5$|

---

### 4. Lệnh căn thức (Square Root)

Lệnh `\sqrt` được sử dụng để tạo biểu tượng căn bậc hai hoặc căn bậc $n$.

- **Căn bậc hai**: Sử dụng cú pháp `\sqrt{giá_trị}`.
    
    - Ví dụ: `\sqrt{9} = 3` viết là `$\sqrt{9} = 3$` $\rightarrow$ $\sqrt{9} = 3$
        
- **Căn bậc n**: Sử dụng tham số tùy chọn trong ngoặc vuông `[ ]`.
    
    - Cú pháp: `\sqrt[n]{giá_trị}`
        
    - Ví dụ (Căn bậc 3): `$\sqrt[3]{9}$` $\rightarrow$ $\sqrt[3]{9}$
        

---

### 5. Một số quy tắc định dạng cần nhớ

- **Viết liền**: Trong môi trường toán học, việc viết sát các ký tự (như `5x`) sẽ được LaTeX tự động hiểu là phép nhân và điều chỉnh khoảng cách tối ưu.
    
- **Ký hiệu sao (`*`)**: Nếu dùng phím `*` trên bàn phím, LaTeX sẽ hiển thị dấu sao lớn. Để có dấu chấm nhân chuyên nghiệp, hãy dùng `\cdot`.