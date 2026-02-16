### 1. Môi trường Ma trận 

Cấu trúc của ma trận tương tự như bảng (`tabular` hoặc `align`):

- Dùng ký hiệu `&` để ngăn cách các cột.
    
- Dùng ký hiệu `\\` để xuống dòng (hàng mới).
    

#### Các loại khung bao (Brackets)

Tùy thuộc vào chữ cái đầu tiên của tên môi trường, hình dáng dấu ngoặc bao quanh ma trận sẽ thay đổi:

|**Tên môi trường**|**Loại ngoặc hiển thị**|**Ví dụ sử dụng**|
|---|---|---|
|`matrix`|Không có ngoặc|Hệ phương trình không khung|
|`pmatrix`|Ngoặc tròn `( )`|Ma trận thông thường|
|`bmatrix`|Ngoặc vuông `[ ]`|Ma trận, Vector|
|`vmatrix`|Dấu gạch đứng `||
|`Vmatrix`|Hai gạch đứng `||

#### Ví dụ mã nguồn:

Đoạn mã

```
\[
    A = \begin{bmatrix}
        1 & 2 & 3 & 4 \\
        5 & 6 & 7 & 8
    \end{bmatrix}
\]
```

**Hiển thị:**

$$A = \begin{bmatrix} 1 & 2 & 3 & 4 \\ 5 & 6 & 7 & 8 \end{bmatrix}$$

> **Lưu ý về hiển thị:** Mặc dù có thể viết ma trận trong chế độ cùng dòng (inline math), nhưng không khuyến khích vì kích thước ma trận sẽ làm vỡ bố cục dòng văn bản. Nên sử dụng chế độ hiển thị khối (display math).

### 2. Môi trường Phân nhánh (Cases Environment)

Môi trường `cases` được dùng để định nghĩa các hàm số có nhiều biểu thức tùy thuộc vào điều kiện (ví dụ: hàm trị tuyệt đối, hàm dấu).

- **Cú pháp:** `\begin{cases} ... \end{cases}`
    
- **Cấu trúc:** `Biểu thức & Điều kiện \\`
    
- **Kết hợp văn bản:** Sử dụng lệnh `\text{...}` để viết các từ nối (như "khi", "với", "for") trong môi trường toán.
    

#### Ví dụ: Định nghĩa hàm trị tuyệt đối

Đoạn mã

```
\[
    |x| = \begin{cases}
        x & \text{for } x > 0 \\
        0 & \text{for } x = 0 \\
        -x & \text{for } x < 0
    \end{cases}
\]
```

**Hiển thị:**

$$|x| = \begin{cases} x & \text{for } x > 0 \\ 0 & \text{for } x = 0 \\ -x & \text{for } x < 0 \end{cases}$$

### Tóm tắt cú pháp

|**Ký hiệu**|**Chức năng**|
|---|---|
|`&`|Căn chỉnh cột (trong ma trận) hoặc tách biểu thức và điều kiện (trong cases)|
|`\\`|Xuống dòng|
|`\text{ }`|Viết văn bản thường trong môi trường toán|