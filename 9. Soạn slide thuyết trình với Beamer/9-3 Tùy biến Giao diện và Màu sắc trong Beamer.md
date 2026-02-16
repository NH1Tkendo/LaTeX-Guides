### 1. Thay đổi Giao diện (Themes)

Giao diện (`Theme`) trong Beamer quy định bố cục tổng thể: cách hiển thị tiêu đề, thanh điều hướng, vị trí mục lục và định dạng các khối văn bản.

- **Quy tắc đặt tên:** Các theme chuẩn của Beamer thường được đặt tên theo các **thành phố**.
    
- **Lệnh sử dụng:** Đặt trong phần khai báo (preamble).
    

Đoạn mã

```
\usetheme{Tên_Thành_Phố}
```

- **Một số ví dụ phổ biến:**
    
    - `Hannover`: Có thanh điều hướng (sidebar) nằm bên trái.
        
    - `Bergen`: Bố cục đơn giản, tập trung vào nội dung.
        
    - `Berkeley`, `Madrid`, `Berlin`...
        

_Lưu ý: Khi đổi theme, cấu trúc hiển thị thay đổi nhưng màu sắc cơ bản (thường là xanh dương) có thể vẫn giữ nguyên nếu không đổi color theme._

### 2. Thay đổi Phối màu (Color Themes)

Phối màu (`Color Theme`) quy định màu sắc của nền, chữ, tiêu đề và các khối (blocks) mà không làm thay đổi bố cục.

- **Quy tắc đặt tên:** Các color theme chuẩn thường được đặt tên theo **động vật** hoặc các loài trong tự nhiên.
    
- **Lệnh sử dụng:**
    

Đoạn mã

```
\usecolortheme{Tên_Động_Vật}
```

- **Một số ví dụ:**
    
    - `beetle`: Tông màu tối (xám/xanh đậm), chữ trắng.
        
    - `fly`: Tông màu xám nhạt.
        
    - `orchid`, `wolverine`, `beaver`...
        

### 3. Kết hợp và Tìm kiếm Mẫu

Bạn có thể kết hợp bất kỳ `theme` nào với `colortheme` nào để tạo ra phong cách riêng.

**Ví dụ kết hợp:**

Đoạn mã

```
\documentclass{beamer}
\usetheme{Madrid}      % Chọn bố cục Madrid
\usecolortheme{beaver} % Chọn phối màu Beaver (tông đỏ/xám)
\begin{document}
...
\end{document}
```

**Nguồn tài nguyên tham khảo:**

1. **Beamer Theme Gallery:** Trang web liệt kê trực quan sự kết hợp giữa các themes, colors và fonts. Giúp bạn xem trước giao diện trước khi viết code.
    
2. **Overleaf Templates:**
    
    - Thư viện mẫu có sẵn trên Overleaf thường đẹp và hiện đại hơn các theme mặc định.
        
    - Nhiều trường đại học có sẵn mẫu riêng (chứa logo trường, màu sắc thương hiệu) giúp tiết kiệm thời gian thiết kế.
        
    - Cách dùng: Tìm mẫu ưng ý $\rightarrow$ Chọn "Open as Template" $\rightarrow$ Xem mã nguồn để học hỏi hoặc chỉnh sửa.
        

### Ghi chú thêm

- **Nút điều hướng (Navigation Symbols):** Ở góc dưới bên phải các slide mặc định thường có các biểu tượng nhỏ để lật trang. Bạn có thể tắt chúng nếu thấy không cần thiết (dù video không đề cập lệnh tắt, nhưng đây là tính năng mặc định được nhắc tới).