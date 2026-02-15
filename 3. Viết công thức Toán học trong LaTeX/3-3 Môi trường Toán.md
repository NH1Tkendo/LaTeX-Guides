### Khái niệm

Khác với **Toán tử trên dòng (Inline Math)** được hiển thị cùng dòng với văn bản, **Toán tử hiển thị khối (Display Math)** sẽ hiển thị công thức toán học trên một dòng riêng biệt, tách biệt với đoạn văn bản trước và sau nó.

### Cú pháp

Thay vì sử dụng dấu `$` (dùng cho inline math), ta sử dụng cặp ký hiệu `\[` và `\]`.

**Ví dụ mã nguồn:**
```
% Inline math (hiển thị cùng dòng)
This is an inline expression: $x + y = z$

% Display math (hiển thị dòng riêng)
This is a display math expression:
\[
    x + y = z
\]
Continuing text...
```

---

## Chỉ số trên và Chỉ số dưới (Superscripts & Subscripts)
### 1. Chỉ số trên (Superscripts) - Số mũ

Dùng để biểu diễn lũy thừa hoặc các ký hiệu ở phía trên bên phải.

- **Ký hiệu:** Dấu mũ `^` trên bàn phím.
    
- **Ví dụ:** Để viết $x^2$, ta nhập `x^2`.

**Công thức tổng quát:**

$$f(x) = ax^2 + bx + c$$

**Mã nguồn LaTeX:**
```
\[
    f(x) = a x^2 + b x + c
\]
```

### 2. Chỉ số dưới (Subscripts)

Dùng để biểu diễn các chỉ số phụ hoặc đánh số thứ tự biến/hệ số.

- **Ký hiệu:** Dấu gạch dưới `_` (underscore).
    
- **Ví dụ:** Thay thế các hệ số $a, b, c$ bằng $a_2, a_1, a_0$.
    

**Công thức sau khi thay đổi:**

$$f(x) = a_2 x^2 + a_1 x + a_0$$

**Mã nguồn LaTeX:**
```
\[
    f(x) = a_2 x^2 + a_1 x + a_0
\]
```

### 3. Quy tắc nhóm (Grouping) với ngoặc nhọn `{}`

Đây là quy tắc quan trọng nhất khi làm việc với chỉ số trong LaTeX.

- **Ký tự đơn:** Nếu chỉ số chỉ có 1 ký tự, không bắt buộc dùng ngoặc nhọn (Ví dụ: `a_1` ra $a_1$).
    
- **Nhiều ký tự:** Nếu chỉ số có từ 2 ký tự trở lên, **bắt buộc** phải bao quanh bởi ngoặc nhọn `{}`.
    
    - _Sai:_ `a_00` $\rightarrow$ LaTeX hiểu là $a_0$ rồi thêm số 0 bình thường bên cạnh ($a_00$).
        
    - _Đúng:_ `a_{00}` $\rightarrow$ Hiển thị đúng là $a_{00}$.
        

> **Lưu ý thực hành (Best Practice):** Luôn sử dụng ngoặc nhọn `{}` cho cả chỉ số trên và dưới, ngay cả khi chỉ có một ký tự (ví dụ: `x^{2}` thay vì `x^2`). Điều này giúp tránh lỗi khi chỉnh sửa sau này và giữ mã nguồn nhất quán.

**Ví dụ so sánh:**

Đoạn mã

```
% Cách viết rủi ro (chỉ đúng với 1 ký tự)
a_0

% Cách viết chuẩn (đúng cho mọi trường hợp)
a_{0}
a_{00}
x^{2}
x^{10}
```