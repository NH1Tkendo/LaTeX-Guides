### 1. Khai báo gói màu sắc
```
\usepackage{xcolor}
```

### 2. Cách tô màu văn bản

#### Ví dụ 1: Tô màu tiêu đề mục (Section)
```
% Lưu ý cách đặt dấu ngoặc để khoanh vùng phạm vi màu
\section{
    {\color{red} Manipulating Text} % Chỉ dòng chữ này màu đỏ
}
```

#### Ví dụ 2: Tô màu một từ cụ thể
```
Đây là văn bản thường, nhưng { \color{blue} từ này màu xanh }, còn lại vẫn màu đen.
```

### 3. Mở rộng bảng màu (Extended Colors)

Mặc định, gói `xcolor` chỉ cung cấp các màu cơ bản (primary/secondary colors) như `red`, `blue`, `green`, `black`, `white`... Để sử dụng các màu phong phú hơn (như `OliveGreen`, `RoyalBlue`...), ta cần thêm tùy chọn khi khai báo gói.

- **Tùy chọn:** `dvipsnames` (Transcript gọi là "PS names" - PostScript names).
    
- **Cú pháp:**
    ```
    \usepackage[dvipsnames]{xcolor}
    ```
    
- **Ví dụ sử dụng màu mở rộng:**
    ```
    { \color{OliveGreen} Văn bản này có màu xanh ô-liu. }
    ```
