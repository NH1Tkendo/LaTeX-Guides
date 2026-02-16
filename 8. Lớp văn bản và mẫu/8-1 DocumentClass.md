Lệnh `\documentclass` không chỉ xác định loại tài liệu (như `article`, `report`, `book`) mà còn chấp nhận các tham số tùy chọn (optional arguments) để thay đổi cấu trúc và định dạng chung.

### Cú pháp cơ bản

Các tham số tùy chọn được đặt trong dấu ngoặc vuông `[...]` ngay trước tên lớp văn bản.

Đoạn mã

```
\documentclass[tham_số_1, tham_số_2, ...]{tên_lớp_văn_bản}
```

### Các nhóm tham số phổ biến

#### 1. Cỡ chữ (Font Size)

Thiết lập kích thước chữ mặc định cho toàn bộ tài liệu.

- **Mặc định:** `10pt` (nếu không khai báo gì).
    
- **Các tùy chọn:** `10pt`, `11pt`, `12pt`.
    

Đoạn mã

```
% Ví dụ: Thiết lập cỡ chữ 12pt
\documentclass[12pt]{article}
```

#### 2. Định dạng Phương trình Toán học (Equation Formatting)

Mặc định, LaTeX căn giữa phương trình và đặt số thứ tự bên phải. Bạn có thể thay đổi điều này bằng các tham số sau:

- **`fleqn` (Flush Left Equations):** Căn lề trái cho toàn bộ phương trình thay vì căn giữa.
    
- **`leqno` (Left Equation Numbers):** Đặt số thứ tự (nhãn) của phương trình sang bên trái thay vì bên phải.
    

**Ví dụ minh họa:**

Với phương trình $2 + 2 = 4$:

- Mặc định: Phương trình nằm giữa, số `(1)` nằm bên phải.
    
- Dùng `[fleqn, leqno]`: Phương trình nằm bên trái, số `(1)` nằm bên trái.
    

Đoạn mã

```
\documentclass[fleqn, leqno]{article}
```

#### 3. Bố cục trang (Page Layout)

Các tham số này thay đổi đáng kể cấu trúc hiển thị của tài liệu:

- **`twocolumn`:** Chia nội dung văn bản thành 2 cột (thường dùng cho bài báo khoa học, báo cáo kỹ thuật hoặc CV).
    
- **`landscape`:** Xoay ngang khổ giấy (thay vì khổ dọc mặc định).
    

Đoạn mã

```
% Ví dụ: Tạo tài liệu xoay ngang và chia 2 cột
\documentclass[landscape, twocolumn]{article}
```

### Tổng hợp ví dụ
```
% Tài liệu cỡ chữ 12pt, xoay ngang, chia 2 cột, phương trình căn trái
\documentclass[12pt, landscape, twocolumn, fleqn]{article}
```

> **Lưu ý:** Các tham số tùy chọn này hoạt động với hầu hết các lớp văn bản chuẩn (`article`, `report`, `book`, `letter`...).