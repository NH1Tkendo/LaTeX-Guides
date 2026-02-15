### 1. Ký tự Hy Lạp (Greek Letters)

LaTeX hỗ trợ viết đầy đủ các ký tự trong bảng chữ cái Hy Lạp, thường được dùng phổ biến trong Toán học, Vật lý và Kỹ thuật (ví dụ: $\pi$, $\lambda$, $\omega$, $\epsilon$...).

- **Cú pháp cơ bản**: Sử dụng dấu gạch chéo ngược `\` + tên ký tự (viết thường).
    
    - Ví dụ: `\pi` $\rightarrow$ $\pi$
        
- **Quy tắc viết hoa - viết thường**:
    
    - LaTeX phân biệt chữ hoa và chữ thường dựa trên chữ cái đầu tiên của lệnh.
        
    - **Chữ thường**: Bắt đầu bằng chữ thường (ví dụ: `\lambda` $\rightarrow$ $\lambda$).
        
    - **Chữ hoa**: Bắt đầu bằng chữ Hoa (ví dụ: `\Lambda` $\rightarrow$ $\Lambda$).
        
---

### 2. Phân số (Fractions)

Có hai cách chính để biểu diễn phép chia hoặc phân số trong LaTeX.

#### Cách 1: Sử dụng ký hiệu gạch chéo `/`

- **Cách dùng**: Viết trực tiếp như văn bản thường hoặc trong môi trường toán.
    
- **Kết quả**: Các thành phần nằm trên cùng một dòng.
    
- **Ví dụ**: `$5x / 3$` $\rightarrow$ $5x / 3$
    

#### Cách 2: Sử dụng lệnh `\frac`

Đây là cách chuyên nghiệp để hiển thị phân số với tử số nằm trên mẫu số.

- **Cú pháp**: `\frac{tử_số}{mẫu_số}`
    
    - Tham số 1 (Numerator): Tử số.
        
    - Tham số 2 (Denominator): Mẫu số.
        
- **Ví dụ**:
    

```
\frac{5x}{3}
```

$\rightarrow$ Kết quả hiển thị: $\frac{5x}{3}$
