### 1. Họ Phông chữ (Font Families)

LaTeX cung cấp 3 họ phông chữ chính. Để thay đổi phông chữ cho một đoạn văn bản cụ thể, ta đặt lệnh thay đổi phông bên trong một nhóm dấu ngoặc nhọn `{ ... }`.
#### Các loại họ phông:
1. **Serif (Có chân):** Phông chữ mặc định của LaTeX. Có các nét gạch trang trí nhỏ ở cuối nét chữ. Mang phong cách cổ điển.
2. **Sans-serif (Không chân):** Không có các nét gạch trang trí. Mang phong cách hiện đại, thường thấy trên web.
3. **Monospace / Typewriter (Đơn không / Máy đánh chữ):** Tất cả các ký tự có độ rộng bằng nhau. Thường dùng để hiển thị mã code hoặc tạo cảm giác cổ điển kiểu máy đánh chữ.
#### Cách thực hiện:
```
% Văn bản mặc định (thường là Serif)
Đây là văn bản mặc định.

% Đổi sang Sans-serif (Không chân)
{ \sffamily Đoạn văn bản này được định dạng không chân }

% Đổi sang Monospace (Máy đánh chữ)
{ \ttfamily Đoạn văn bản này trông giống mã code }
```

### 3. Kích thước Phông chữ (Font Sizes)
#### Các lệnh kích thước phổ biến:

Hệ thống kích thước của LaTeX trải dài từ rất nhỏ đến rất lớn. Dưới đây là một số lệnh tiêu biểu được nhắc đến và danh sách tham khảo theo thứ tự tăng dần:
- `\tiny` (Nhỏ nhất)
- `\scriptsize`
- `\footnotesize`
- `\small` (Nhỏ hơn chuẩn một chút)
- `\normalsize` (Kích thước chuẩn mặc định)
- `\large`
- `\Large`
- `\LARGE`
- `\huge` (Rất lớn)
- `\Huge` (Lớn nhất - chú ý chữ H viết hoa)
#### Ví dụ minh họa:
```
Đây là kích thước chuẩn.
{ \small Đoạn này nhỏ hơn một chút để làm chú thích. }
{ \huge Đoạn này rất lớn để làm tiêu đề nổi bật. }
```