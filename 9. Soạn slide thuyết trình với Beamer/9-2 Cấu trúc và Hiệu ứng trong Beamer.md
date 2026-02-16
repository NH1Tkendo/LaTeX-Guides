### 1. Các Khối nội dung (Blocks)

Trong Beamer, **Block** được dùng để nhóm các đoạn văn bản, ví dụ hoặc định lý thành các hộp riêng biệt để làm nổi bật chúng so với văn bản thường.

Có 3 loại khối chính thường được sử dụng:

- **Khối tiêu chuẩn (Standard Block):**
    
    - Môi trường: `block`
        
    - Đặc điểm: Thường có màu xanh dương (tùy giao diện), dùng cho nội dung tổng quát.
        
    - Cú pháp: `\begin{block}{Tiêu đề}... \end{block}`
        
- **Khối cảnh báo (Alert Block):**
    
    - Môi trường: `alertblock`
        
    - Đặc điểm: Thường có màu đỏ, dùng cho các thông tin quan trọng hoặc cảnh báo.
        
    - Cú pháp: `\begin{alertblock}{Tiêu đề}... \end{alertblock}`
        
- **Khối ví dụ (Example Block):**
    
    - Môi trường: `exampleblock`
        
    - Đặc điểm: Thường có màu xanh lá cây, chuyên dùng để trình bày ví dụ.
        
    - Cú pháp: `\begin{exampleblock}{Tiêu đề}... \end{exampleblock}`
        

**Mã nguồn mẫu:**

Đoạn mã

```
\begin{frame}{Các loại Block trong Beamer}
    
    % Khối tiêu chuẩn (Thường màu xanh dương)
    \begin{block}{Tiêu đề khối thường}
        Đây là nội dung của một khối bình thường.
    \end{block}

    % Khối cảnh báo (Thường màu đỏ)
    \begin{alertblock}{Quan trọng}
        Đây là thông tin quan trọng cần chú ý!
    \end{alertblock}

    % Khối ví dụ (Thường màu xanh lá)
    \begin{exampleblock}{Ví dụ minh họa}
        Ví dụ: $2 + 2 = 4$
    \end{exampleblock}

\end{frame}
```

### 2. Hiệu ứng xuất hiện tuần tự (`\pause`)

Để tránh việc hiển thị toàn bộ nội dung cùng lúc làm khán giả bị "ngợp", bạn có thể chia nhỏ nội dung để chúng xuất hiện lần lượt sau mỗi lần bấm chuột.

- **Lệnh sử dụng:** `\pause`
    
- **Cách hoạt động:**
    
    - Khi biên dịch, Beamer sẽ tạo ra nhiều trang PDF cho cùng một slide.
        
    - Nội dung đặt sau lệnh `\pause` sẽ bị ẩn ở trang đầu tiên và chỉ xuất hiện ở trang tiếp theo.
        

**Ví dụ áp dụng:**

Đoạn mã

```
\begin{frame}{Hiệu ứng Pause}
    Đây là dòng đầu tiên xuất hiện.
    
    \pause % Dừng lại, đợi click chuột
    
    Sau khi bấm chuột, dòng này mới hiện ra (Block ví dụ).
    \begin{exampleblock}{Ví dụ}
        Nội dung ví dụ...
    \end{exampleblock}
    
    \pause % Dừng lại lần nữa
    
    Cuối cùng là dòng kết luận này.
\end{frame}
```

### 3. Nhấn mạnh từ khóa (`\alert`)

Để làm nổi bật một từ hoặc cụm từ cụ thể trong đoạn văn (thay vì cả một khối), bạn sử dụng lệnh `\alert`.

- **Lệnh:** `\alert{nội dung}`
    
- **Hiệu ứng:** Văn bản bên trong sẽ đổi màu (thường là màu đỏ) để thu hút sự chú ý.
    

**Ví dụ:**

Đoạn mã

```
Từ khóa này rất \alert{quan trọng} trong câu.
```