Beamer là một lớp văn bản (document class) trong LaTeX dùng để tạo các bài thuyết trình (presentation/slides). Khi chuyển từ `article` sang `beamer`, tỷ lệ khung hình sẽ thay đổi và các công cụ điều hướng đặc trưng sẽ xuất hiện.

### 1. Thiết lập môi trường Beamer

Để bắt đầu, cần thay đổi khai báo lớp văn bản ở đầu tệp:
```
\documentclass{beamer}
```

### 2. Tạo trang tiêu đề (Title Page)

Cấu trúc khai báo thông tin tương tự như các tài liệu LaTeX khác, nhưng có thêm trường thông tin về tổ chức.

**Các lệnh khai báo thông tin:**

- `\title{...}`: Tiêu đề bài thuyết trình.
    
- `\author{...}`: Tên tác giả.
    
- `\date{...}`: Ngày tháng.
    
- `\institute{...}`: Tên trường đại học hoặc tổ chức (đặc trưng của Beamer).
    

**Cách hiển thị trang tiêu đề:** Có 2 cách để tạo slide tiêu đề:

1. Sử dụng lệnh `\maketitle` (tự động tạo một frame tiêu đề).
    
2. Sử dụng lệnh `\frame{\titlepage}`.

```
\title{Introduction to Beamer}
\author{Author Name}
\institute{University Name}
\date{\today}

\begin{document}
    % Cách 1:
    \frame{\titlepage} 
    % Hoặc dùng \maketitle
\end{document}
```

### 3. Tạo các Slide nội dung (Frames)

Trong Beamer, mỗi slide được gọi là một **khung (frame)**. Không nên viết văn bản trực tiếp bên ngoài môi trường frame.

**Cấu trúc một slide cơ bản:** Sử dụng môi trường `frame` để bao quanh nội dung. Tiêu đề của slide có thể được đặt làm tham số ngay sau lệnh mở môi trường.

```
\begin{frame}{Tiêu đề của Slide}
    Nội dung của slide sẽ nằm ở đây.
    Văn bản sẽ được căn chỉnh tự động theo cấu trúc của Beamer.
\end{frame}
```

### 4. Tạo Mục lục (Table of Contents)

Beamer hỗ trợ tạo mục lục tự động dựa trên các phần (`\section`) đã khai báo. Mục lục này có khả năng liên kết (clickable) để nhảy đến các phần tương ứng.

**Các bước thực hiện:**

1. Chia cấu trúc bài nói bằng lệnh `\section{Tên phần}`.
    
2. Tạo một frame riêng cho mục lục.
    
3. Sử dụng lệnh `\tableofcontents`.
    

**Mã nguồn mẫu:**

Đoạn mã

```
% Tạo một frame chứa mục lục
\begin{frame}{Nội dung chính}
    \tableofcontents
\end{frame}

% Định nghĩa các phần
\section{Giới thiệu}
\begin{frame}{Slide giới thiệu}
    ...
\end{frame}

\section{Nội dung chi tiết}
\begin{frame}{Slide chi tiết}
    ...
\end{frame}
```

**Lợi ích:** Giúp cấu trúc bài thuyết trình rõ ràng: bắt đầu bằng việc tóm tắt lộ trình (outline) và sau đó đi vào chi tiết từng phần.