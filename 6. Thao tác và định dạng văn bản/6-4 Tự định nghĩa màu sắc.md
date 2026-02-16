### 1. Cú pháp khai báo

Lệnh khai báo màu phải được đặt trong phần mở đầu (Preamble).

**Cú pháp:**

Đoạn mã

```
\definecolor{tên_màu}{hệ_màu}{thông_số}
```

- `tên_màu`: Tên do bạn tự đặt (ví dụ: `myBlue`, `DeepRed`).
    
- `hệ_màu`: Định dạng màu sử dụng (`RGB`, `rgb`, `HTML`...).
    
- `thông_số`: Giá trị cụ thể của màu.
    

### 2. Các hệ màu phổ biến (Color Models)

Có 3 hệ màu chính thường được sử dụng trong LaTeX:

#### A. Hệ màu RGB (0-255)

Sử dụng các số nguyên từ 0 đến 255. Đây là hệ màu dễ dùng nhất nếu bạn lấy thông số từ các phần mềm đồ họa (Photoshop, Paint).

- **Hệ màu:** `RGB` (Viết hoa toàn bộ).
    
- **Ví dụ:**
    
    Đoạn mã
    
    ```
    % Màu đỏ tía (Red=187, Green=42, Blue=97)
    \definecolor{MyCustomRed}{RGB}{187, 42, 97}
    ```
    

#### B. Hệ màu rgb (0-1)

Sử dụng số thập phân chuẩn hóa từ 0 đến 1.

- **Hệ màu:** `rgb` (Viết thường toàn bộ).
    
- **Cách tính:** Lấy giá trị 0-255 chia cho 255.
    
- **Ví dụ:**
    
    Đoạn mã
    
    ```
    % Màu đỏ thuần (1, 0, 0)
    \definecolor{RedOne}{rgb}{1.0, 0.0, 0.0}
    ```
    

> **⚠️ Lưu ý quan trọng:**
> 
> LaTeX phân biệt chữ hoa/thường rất nghiêm ngặt.
> 
> - `RGB`: Dùng số nguyên (0-255).
>     
> - `rgb`: Dùng số thập phân (0.0-1.0).
>     
>     Nếu dùng nhầm (ví dụ: dùng số 255 cho hệ `rgb`), màu sẽ bị sai hoặc biến mất.
>     

#### C. Hệ màu HTML (Hex)

Sử dụng mã Hexadecimal (hệ thập lục phân) gồm 6 ký tự, thường dùng trong thiết kế web và CSS.

- **Hệ màu:** `HTML` (Viết hoa).
    
- **Ví dụ:**
    
    Đoạn mã
    
    ```
    % Màu xám đậm (Mã Hex: 665544)
    \definecolor{MyHexColor}{HTML}{665544}
    ```
    

### 3. Cách sử dụng màu đã định nghĩa

Sau khi định nghĩa trong Preamble, bạn dùng tên màu đó như các màu có sẵn.

- **Dùng lệnh `\textcolor` (cho một đoạn ngắn):**
    
    Đoạn mã
    
    ```
    \textcolor{MyCustomRed}{Đoạn văn này có màu đỏ tía.}
    ```
    
- **Dùng lệnh `\color` (thay đổi trạng thái màu):**
    
    Đoạn mã
    
    ```
    {
        \color{MyHexColor}
        Toàn bộ đoạn văn trong nhóm này sẽ có màu xám đậm.
    }
    ```
    

### 4. Lời khuyên về thiết kế (Design Best Practices)

- **Tính nhất quán:** Không nên dùng quá nhiều màu (ví dụ 25 màu) và quá nhiều font (ví dụ 15 font) trong một tài liệu. Điều này làm tài liệu trông rối mắt và thiếu chuyên nghiệp.
    
- **Số lượng:** Chỉ nên chọn một bộ (palette) gồm vài màu chủ đạo và vài font chữ chính.
    
- **Nguồn tham khảo:** Nếu không giỏi phối màu, bạn có thể tìm kiếm từ khóa "Color Templates" hoặc "Color Palettes" trên Google để lấy các mã Hex/RGB hài hòa với nhau.
    

---

**Tổng kết:**

|**Lệnh**|**Ý nghĩa**|**Ví dụ**|
|---|---|---|
|`\definecolor{name}{RGB}{r,g,b}`|Định nghĩa màu theo hệ 0-255|`\definecolor{Skin}{RGB}{255,224,189}`|
|`\definecolor{name}{HTML}{HEX}`|Định nghĩa màu theo mã Hex|`\definecolor{Gold}{HTML}{FFD700}`|
|`\textcolor{name}{text}`|Tô màu cho đoạn text cụ thể|`\textcolor{Gold}{Winner}`|