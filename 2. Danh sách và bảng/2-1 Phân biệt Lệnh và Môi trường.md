### Lệnh (Commands)

Các lệnh trong LaTeX dùng để thực hiện một tác vụ cụ thể hoặc định dạng văn bản ngắn.

- **Cú pháp chung**:
    
    - Bắt đầu bằng dấu gạch chéo ngược `\` (backslash).
        
    - Theo sau là tên lệnh.
        
    - Có thể nhận các tham số đầu vào (inputs).
        
- **Các loại tham số**:
    
    1. **Tham số bắt buộc (Non-optional arguments)**: Đặt trong dấu ngoặc nhọn `{ }`. Lệnh sẽ không hoạt động hoặc hoạt động sai nếu thiếu tham số này.
        
    2. **Tham số tùy chọn (Optional arguments)**: Đặt trong dấu ngoặc vuông `[ ]`. Dùng để điều chỉnh hành vi mặc định của lệnh.
        
- **Ví dụ 1: Lệnh tạo tiêu đề (Section)**
    
    Đoạn mã
    
    ```
    \section{Tên của tiêu đề}
    ```
    
    - `\section`: Tên lệnh.
        
    - `{Tên của tiêu đề}`: Tham số bắt buộc, nội dung sẽ hiển thị ra văn bản.
        
- **Ví dụ 2: Lệnh tạo chú thích (Footnote)**
    
    - Sử dụng cơ bản:
        
        Đoạn mã
        
        ```
        Some text \footnote{Nội dung chú thích}
        ```
        
        $\rightarrow$ Kết quả: Tạo một số nhỏ (ví dụ: 1) ở vị trí văn bản và hiển thị nội dung chú thích ở cuối trang.
        
    - Sử dụng với tham số tùy chọn:
        
        Đoạn mã
        
        ```
        Some text \footnote[2]{Nội dung chú thích}
        ```
        
        $\rightarrow$ Kết quả: Bắt buộc số chú thích hiển thị là **2** thay vì tự động tăng theo thứ tự mặc định.
        

### Môi trường (Environments)

Môi trường được sử dụng cho các khối văn bản lớn hơn hoặc các cấu trúc đặc biệt cần điểm bắt đầu và kết thúc rõ ràng.

- **Cú pháp chung**:
    
    Luôn bao gồm một cặp lệnh mở và đóng tương ứng:
    
    Đoạn mã
    
    ```
    \begin{tên_môi_trường}
        % Nội dung bên trong môi trường
    \end{tên_môi_trường}
    ```
    
- **Ví dụ: Môi trường Tóm tắt (Abstract)**
    
    - Dùng để viết đoạn tóm tắt nội dung ở đầu một bài báo khoa học.
        
    - Cú pháp:
        
        Đoạn mã
        
        ```
        \begin{abstract}
            Đây là nội dung tóm tắt của bài báo.
        \end{abstract}
        ```
