### 1. Khai báo môi trường mới (`\newtheorem`)

LaTeX không có sẵn môi trường `theorem` mặc định. Bạn phải tự định nghĩa chúng trước khi sử dụng.

- **Cú pháp khai báo (trong Preamble):**
    
    Đoạn mã
    
    ```
    \newtheorem{tên_môi_trường}{Tên_hiển_thị}
    ```
    
    - `tên_môi_trường`: Tên dùng để gọi lệnh (ví dụ: `theorem`, `defn`).
        
    - `Tên_hiển_thị`: Từ sẽ xuất hiện trong văn bản PDF (ví dụ: "Theorem", "Định lý").
        
- **Ví dụ khai báo:**
    
    Đoạn mã
    
    ```
    \usepackage{amsthm} % Bắt buộc
    
    % Tạo môi trường Định lý
    \newtheorem{theorem}{Theorem}
    
    % Tạo môi trường Định nghĩa
    \newtheorem{definition}{Definition}
    ```
    

### 2. Sử dụng trong văn bản

Sau khi khai báo, bạn sử dụng chúng như các môi trường bình thường (`\begin{...} ... \end{...}`).

#### A. Cách dùng cơ bản

Đoạn mã

```
\begin{theorem}
    This is a basic theorem.
\end{theorem}
```

_Kết quả:_ **Theorem 1.** This is a basic theorem.

#### B. Thêm tên hoặc chú thích (Optional Arguments)

Bạn có thể thêm tên riêng cho định lý (ví dụ: tên người phát minh) bằng cách đặt trong ngoặc vuông `[]` ngay sau lệnh `\begin`.

Đoạn mã

```
\begin{theorem}[Pythagoras]
    $a^2 + b^2 = c^2$
\end{theorem}
```

_Kết quả:_ **Theorem 2 (Pythagoras).** $a^2 + b^2 = c^2$

### 3. Môi trường không đánh số (Unnumbered Environments)

Đôi khi bạn muốn tạo các mục như "Nhận xét" (Remarks) hoặc "Lưu ý" mà không cần số thứ tự (ví dụ: không muốn hiện "Remark 1").

- **Cách làm:** Thêm dấu sao `*` vào lệnh `\newtheorem*`.
    
- **Ví dụ:**
    
    Đoạn mã
    
    ```
    % Trong Preamble
    \newtheorem*{remark}{Remark}
    
    % Trong văn bản
    \begin{remark}
        This is a remark without a number.
    \end{remark}
    ```
    
- _Kết quả:_ **Remark.** This is a remark without a number.
    

### 4. Tham chiếu chéo (Labeling & Referencing)

Bạn có thể gắn nhãn và tham chiếu ngược lại các định lý/định nghĩa tương tự như hình ảnh hoặc phương trình.

- **Gắn nhãn:** Dùng `\label{...}` bên trong môi trường.
    
- **Gọi lại:** Dùng `\ref{...}`.
    

Đoạn mã

```
\begin{definition}
    A triangle is...
    \label{def:triangle}
\end{definition}

See Definition \ref{def:triangle} for more details.
```

### Tóm tắt cú pháp

| **Mục đích**             | **Lệnh khai báo (Preamble)** | **Cách dùng (Body)**          |
| ------------------------ | ---------------------------- | ----------------------------- |
| **Đánh số (Định lý)**    | `\newtheorem{thm}{Theorem}`  | `\begin{thm} ... \end{thm}`   |
| **Không đánh số (Note)** | `\newtheorem*{note}{Note}`   | `\begin{note} ... \end{note}` |
| **Thêm tên riêng**       | (Như trên)                   | `\begin{thm}[Tên]`            |