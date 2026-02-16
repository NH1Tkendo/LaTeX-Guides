Để biến tài liệu PDF tĩnh thành một tài liệu tương tác với các liên kết có thể nhấp chuột (clickable links), chúng ta sử dụng gói `hyperref`.

### 1. Khai báo gói (Package Import)

Thêm lệnh sau vào phần mở đầu (preamble) của tài liệu:

Đoạn mã

```
\usepackage{hyperref}
```

> **⚠️ Lưu ý quan trọng:**
> 
> Gói `hyperref` nên được khai báo là **gói cuối cùng** trong danh sách các gói (preamble). Lý do là `hyperref` sẽ định nghĩa lại (redefine) nhiều lệnh cơ bản của LaTeX để thêm tính năng liên kết. Nếu khai báo trước các gói khác, có thể gây xung đột lệnh.

### 2. Liên kết nội bộ (Internal Links)

Ngay khi gói `hyperref` được kích hoạt, các thành phần sau trong tài liệu sẽ tự động trở thành liên kết có thể nhấp chuột:

- **Mục lục (Table of Contents):** Nhấp vào tên mục sẽ nhảy đến trang tương ứng.
    
- **Tham chiếu chéo (`\ref`, `\eqref`):** Nhấp vào số mục hoặc số phương trình sẽ nhảy đến vị trí gốc của nó.
    
- **Danh sách hình ảnh/bảng biểu.**
    

**Mẹo ngắt trang:**

Sử dụng lệnh `\newpage` (không có tham số) để ngắt trang cưỡng bức. Điều này giúp kiểm tra tính năng nhảy trang của các liên kết trong các tài liệu ngắn.

### 3. Liên kết đến Website bên ngoài (External Links)

`hyperref` cung cấp 2 lệnh chính để chèn liên kết web:

#### A. Hiển thị nguyên đường dẫn (`\url`)

Dùng khi bạn muốn hiển thị rõ địa chỉ URL cho người đọc. URL sẽ được định dạng bằng font chữ đơn sắc (monospace).

- **Cú pháp:** `\url{địa_chỉ_web}`
    
- **Ví dụ:**
    ```
You can find more information on Overleaf: \url{https://www.overleaf.com}
    ```
    
- **Kết quả:** Hiển thị dòng chữ `https://www.overleaf.com` và có thể nhấp vào được.
    

#### B. Gán liên kết cho văn bản (`\href`)

Dùng khi đường dẫn quá dài hoặc bạn muốn chèn liên kết vào một từ/cụm từ cụ thể (tương tự thẻ `<a>` trong HTML).

- **Cú pháp:** `\href{địa_chỉ_web}{văn_bản_hiển_thị}`
    
- **Ví dụ:**
    
    Đoạn mã
    
    ```
    You can find more information on \href{https://www.overleaf.com}{Overleaf homepage}.
    ```
    
- **Kết quả:** Hiển thị chữ "Overleaf homepage". Khi nhấp vào chữ này sẽ mở ra trang web.
    

---

### Tổng kết lệnh

| **Lệnh**                | **Chức năng**                                    | **Ví dụ**                   |
| ----------------------- | ------------------------------------------------ | --------------------------- |
| `\usepackage{hyperref}` | Kích hoạt tính năng liên kết (đặt cuối preamble) | N/A                         |
| `\url{...}`             | Hiển thị URL trực tiếp                           | `\url{google.com}`          |
| `\href{url}{text}`      | Ẩn URL dưới văn bản                              | `\href{google.com}{Google}` |
| `\newpage`              | Ngắt sang trang mới                              | N/A                         |