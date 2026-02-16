### Phương pháp: Sử dụng môi trường `thebibliography`

#### 1. Thiết lập môi trường

Sử dụng môi trường _thư mục tham khảo 
```
\begin{thebibliography}{99}
    % Các mục tài liệu tham khảo sẽ nằm ở đây
\end{thebibliography}
```

**Giải thích tham số `{99}`:**
- Đây là tham số xác định độ rộng của nhãn đánh số hoặc số lượng tài liệu tham khảo tối đa dự kiến.
- `{2}` hoặc `{9}`: Dùng cho danh sách có 1 chữ số (dưới 10 tài liệu).
- `{99}`: Dùng cho danh sách có 2 chữ số (lên đến 99 tài liệu). Đây là thiết lập phổ biến và an toàn.

#### 2. Thêm mục tài liệu tham khảo (`\bibitem`)

Sử dụng lệnh `\bibitem` để định nghĩa từng tài liệu.

**Cú pháp:**
```
\bibitem{key} Thông tin chi tiết về tài liệu (Tác giả, Tên sách, Năm...)
```

- **key (khóa định danh):** Tên ngắn gọn dùng để gọi trích dẫn này trong bài viết (ví dụ: `Anderson`, `Shelley`).
- **Nội dung:** Phần văn bản hiển thị trong danh sách cuối cùng.

**Ví dụ mã nguồn:**
```
\begin{thebibliography}{99}
    \bibitem{Anderson} 
    Hans Christian Andersen. The Little Mermaid. 1837.
    
    \bibitem{Shelley} 
    Mary Shelley. Frankenstein. 1818.
\end{thebibliography}
```

### Cách trích dẫn trong văn bản (`\cite`)

Sau khi đã thiết lập danh sách `\bibitem`, bạn dùng lệnh `\cite` để trích dẫn tại bất kỳ đâu trong văn bản. LaTeX sẽ tự động đánh số `[1]`, `[2]` tương ứng.

#### Lệnh cơ bản
```
Theo tác giả Anderson \cite{Anderson}...
```

_Kết quả:_ Theo tác giả Anderson [1]...

#### Mẹo định dạng (Tilde `~`)

Nên dùng dấu ngã `~` trước lệnh `\cite` để tạo _khoảng trắng không ngắt dòng (non-breaking space)_. Việc này giúp số thứ tự trích dẫn không bị rớt xuống dòng mới một mình.

```
Tham khảo tác phẩm này~\cite{Shelley}.
```

#### Thêm tham số tùy chọn (Số trang)

Bạn có thể thêm thông tin cụ thể (như số trang) vào trong ngoặc vuông `[]`.

Đoạn mã

```
\cite[page 47]{Shelley}
```

_Kết quả:_ [2, page 47]

#### Trích dẫn nhiều tài liệu cùng lúc

Dùng dấu phẩy để ngăn cách các khóa định danh.

Đoạn mã

```
\cite{Anderson, Shelley}
```

_Kết quả:_ [1, 2]