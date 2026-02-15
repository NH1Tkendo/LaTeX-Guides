### Môi trường Itemize

Để tạo danh sách không thứ tự, ta sử dụng môi trường **itemize**.

- **Cú pháp khai báo**:
    ```
    \begin{itemize}
        % Các mục sẽ nằm ở đây
    \end{itemize}
    ```
- **Thêm mục (Item)**: Sử dụng lệnh `\item` để tạo một dấu chấm tròn (bullet point) mới.
    

### Ví dụ cơ bản

Dưới đây là mã nguồn để tạo một danh sách mua sắm đơn giản:
```
\begin{itemize}
    \item Bread
    \item Milk
    \item Apples
    \item Pasta
\end{itemize}
```

$\rightarrow$ **Kết quả**: Một danh sách gồm 4 mục với các dấu chấm tròn đầu dòng.

### Danh sách Lồng nhau 

Bạn có thể lồng một môi trường `itemize` vào bên trong một mục của danh sách khác để tạo danh sách cấp con. LaTeX hỗ trợ lồng nhau tối đa **4 cấp độ**.

- **Cách thực hiện**: Khai báo một môi trường `itemize` mới ngay sau lệnh `\item` của danh sách cha.
    
- **Ví dụ**: Liệt kê nguyên liệu làm Pasta nằm bên dưới mục Pasta.

```
\begin{itemize}
    \item Bread
    \item Milk
    \item Pasta
    \begin{itemize}  % Bắt đầu danh sách con
        \item Flour
        \item Eggs
        \item Salt
    \end{itemize}    % Kết thúc danh sách con
\end{itemize}
```

$\rightarrow$ **Kết quả**: Các mục con (Flour, Eggs, Salt) sẽ được thụt đầu dòng và ký hiệu đầu dòng sẽ tự động thay đổi (thường là dấu gạch ngang) để phân biệt với cấp cha.

### Tùy chỉnh Ký hiệu đầu dòng 

Lệnh `\item` có thể nhận một **tham số tùy chọn** (optional argument) trong dấu ngoặc vuông `[ ]` để thay đổi ký hiệu hiển thị mặc định.

- **Cú pháp**: `\item[ký_hiệu_mới]`
    
- **Ví dụ**: Thay dấu chấm tròn bằng dấu gạch ngang.
    
    Đoạn mã
    
    ```
    \begin{itemize}
        \item[-] Bread  % Mục này sẽ có dấu gạch ngang (-) thay vì chấm tròn
        \item Milk      % Mục này vẫn giữ chấm tròn mặc định
    \end{itemize}
    ```