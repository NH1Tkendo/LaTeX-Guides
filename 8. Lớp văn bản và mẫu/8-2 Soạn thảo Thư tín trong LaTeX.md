### Cấu trúc cơ bản

Khác với `article`, lớp `letter` yêu cầu một cấu trúc lồng nhau cụ thể để hiển thị đúng các thành phần như địa chỉ, lời chào và chữ ký.

1. **Khai báo lớp:** Sử dụng `\documentclass{letter}`.
    
2. **Thông tin người gửi:** Khai báo `\address` và `\signature` (thường đặt trước `\begin{document}` hoặc ngay đầu tài liệu).
    
3. **Môi trường thư:** Toàn bộ nội dung thư nằm trong môi trường `\begin{letter}{...}`.
    

### Các lệnh quan trọng

|**Lệnh**|**Ý nghĩa**|**Vị trí**|
|---|---|---|
|`\address{...}`|Địa chỉ của người gửi. Sử dụng `\\` để xuống dòng.|Preamble (Lời mở đầu)|
|`\signature{...}`|Tên người gửi (sẽ hiện bên dưới phần ký tên).|Preamble|
|`\begin{letter}{...}`|Bắt đầu bức thư. Tham số `{...}` chứa thông tin người nhận hoặc thông tin công ty.|Trong `document`|
|`\opening{...}`|Lời chào mở đầu (Ví dụ: _To whom it may concern_).|Trong `letter`|
|`\closing{...}`|Lời chào kết thúc (Ví dụ: _Yours faithfully_).|Cuối `letter`|

### Mã nguồn mẫu

Dưới đây là đoạn mã hoàn chỉnh để tạo một bức thư cơ bản:

Đoạn mã

```
\documentclass[12pt]{letter} % Thiết lập cỡ chữ 12pt

% 1. Thông tin người gửi
\signature{Kansteiner} 
\address{Fantasy Town \\ Fantasy St. \\ Fantasy House Number}

\begin{document}

    % 2. Bắt đầu thư - Tham số là thông tin người nhận/công ty
    \begin{letter}{CEO of the Business \\ Business Address}
        
        % 3. Lời mở đầu
        \opening{To whom it may concern,}

        % 4. Nội dung thư
        Đây là nội dung chính của bức thư. 
        LaTeX sẽ tự động căn chỉnh lề và bố cục dựa trên độ dài của văn bản.
        
        % 5. Lời kết
        \closing{Yours faithfully,}

    \end{letter}

\end{document}
```

### Một số lưu ý quan trọng

- **Tham số tùy chọn (Optional Arguments):**
    
    - Nên sử dụng `[12pt]` để cỡ chữ dễ đọc hơn (mặc định 10pt có thể hơi nhỏ cho thư tín).
        
    - **Cảnh báo:** Không sử dụng tham số `landscape` (khổ ngang) cho lớp `letter`. Cấu trúc dữ liệu bên dưới của lớp này không tương thích với chế độ ngang và sẽ làm hỏng bố cục thư.
        
- **Xuống dòng:** Trong phần địa chỉ (`\address`), bắt buộc dùng dấu gạch chéo ngược kép `\\` để ngắt dòng (tránh nhầm lẫn dùng dấu gạch chéo tới `/`).
    
- **Bố cục tự động:** Nếu nội dung thư quá ngắn, bố cục có thể trông rời rạc. LaTeX hiển thị tốt nhất khi thư có độ dài vừa phải (có nhiều đoạn văn).