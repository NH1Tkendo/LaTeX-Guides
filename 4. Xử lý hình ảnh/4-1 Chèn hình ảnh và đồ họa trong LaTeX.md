## Khai báo gói lệnh (Pre-requisites)

Để sử dụng các tính năng chèn ảnh, bắt buộc phải khai báo gói `graphicx` trong phần đầu tài liệu (preamble), trước `\begin{document}`.

Đoạn mã

```
\usepackage{graphicx}
```

## Lệnh chèn hình ảnh cơ bản

Sử dụng lệnh `\includegraphics` để chèn hình vào vị trí mong muốn trong văn bản.

Đoạn mã

```
\includegraphics{tên_tệp_hình_ảnh}
```

- **Ví dụ:** `\includegraphics{cosine_plot}`
    
- **Lưu ý:** Phần mở rộng của tên tệp (như `.png`, `.jpg`, `.pdf`) là tùy chọn, LaTeX thường tự động nhận diện.
    

## Điều chỉnh kích thước ảnh (Resizing)

Nếu hình ảnh quá lớn hoặc cần kích thước cụ thể, sử dụng các tham số tùy chọn đặt trong ngoặc vuông `[]` ngay sau lệnh `\includegraphics`.

### 1. Tỷ lệ (Scale)

Thu phóng ảnh theo tỷ lệ phần trăm so với kích thước gốc.

Đoạn mã

```
% Thu nhỏ còn 90% kích thước gốc
\includegraphics[scale=0.9]{tên_tệp}

% Thu nhỏ còn 50% kích thước gốc (một nửa)
\includegraphics[scale=0.5]{tên_tệp}
```

### 2. Kích thước tuyệt đối (Absolute Dimensions)

Đặt chiều rộng hoặc chiều cao cố định bằng các đơn vị đo lường (cm, inches, pt...).

Đoạn mã

```
% Đặt chiều rộng là 12cm
\includegraphics[width=12cm]{tên_tệp}

% Đặt chiều rộng là 2 inches
\includegraphics[width=2in]{tên_tệp}

% Đặt chiều cao là 2 inches
\includegraphics[height=2in]{tên_tệp}
```

### 3. Kích thước tương đối (Relative Sizes)

Đặt kích thước dựa trên các tham số của tài liệu, phổ biến nhất là dựa trên chiều rộng của khối văn bản (`\textwidth`).

Đoạn mã

```
% Ảnh rộng bằng 50% chiều rộng văn bản
\includegraphics[width=0.5\textwidth]{tên_tệp}

% Ảnh rộng bằng toàn bộ chiều rộng văn bản
\includegraphics[width=\textwidth]{tên_tệp}
```

## Quản lý tệp hình ảnh (Tổ chức thư mục)

Đối với các dự án lớn, nên tổ chức hình ảnh vào các thư mục con (ví dụ: tạo thư mục tên là `pictures` và di chuyển ảnh vào đó).

Nếu chỉ di chuyển tệp, lệnh `\includegraphics` sẽ báo lỗi không tìm thấy tệp. Cần khai báo cho LaTeX biết nơi tìm kiếm hình ảnh.

### Sử dụng `\graphicspath`

Thêm lệnh này vào phần khai báo (preamble) để chỉ định các thư mục chứa ảnh.

**Cú pháp quan trọng:**

- Đường dẫn phải nằm trong **hai cặp** ngoặc nhọn `{{ ... }}`.
    
- Bắt đầu bằng `./` (thư mục hiện tại) và kết thúc đường dẫn bằng dấu gạch chéo `/`.
    

Đoạn mã

```
% --- Trong Preamble ---

% Chỉ định LaTeX tìm ảnh trong thư mục "pictures"
\graphicspath{{./pictures/}}

% --- Trong thân tài liệu ---
% Bây giờ có thể gọi tên tệp trực tiếp mà không cần ghi đường dẫn
\includegraphics{tên_tệp_trong_thư_mục_pictures}
```