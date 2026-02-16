### 1. Liên kết tệp BibTeX với tài liệu chính

Để LaTeX biết lấy dữ liệu trích dẫn từ đâu, bạn cần khai báo tệp cơ sở dữ liệu trong tệp chính.

**Cú pháp:** Sử dụng lệnh `\bibliography{}` tại vị trí bạn muốn danh sách tham khảo xuất hiện (thường là cuối tài liệu).

```
\bibliography{tên_file_bib} 
```

### 2. Thiết lập kiểu trích dẫn (Bibliography Style)

Nếu chỉ liên kết tệp, tài liệu có thể sẽ không biên dịch được hoặc không hiển thị đúng vì LaTeX chưa biết định dạng hiển thị như thế nào. Bạn cần quy định kiểu trích dẫn (style).

**Cú pháp:**

Đoạn mã

```
\bibliographystyle{tên_kiểu}
```

**Ví dụ:**
```
\bibliographystyle{plain}
\bibliography{biblio}
```

### 3. Các kiểu định dạng phổ biến

Việc thay đổi tham số trong `\bibliographystyle{}` sẽ thay đổi hoàn toàn cách hiển thị trích dẫn trong văn bản và trong danh sách tham khảo mà không cần sửa đổi dữ liệu gốc.

#### Kiểu `plain`

- **Mô tả:** Đánh số thứ tự đơn giản.
    
- **Hiển thị trong văn bản:** `[1]`, `[2]`.
    
- **Danh sách tham khảo:** Sắp xếp theo tên tác giả hoặc thứ tự xuất hiện (tùy biến thể).
    

Đoạn mã

```
\bibliographystyle{plain}
```

#### Kiểu `alpha`

- **Mô tả:** Sử dụng hệ thống chữ-số (alphanumeric) dựa trên tên tác giả và năm xuất bản.
    
- **Hiển thị trong văn bản:** Dùng 3 ký tự đầu của tên tác giả + 2 số cuối của năm.
    
    - Ví dụ: `[And18]` (Anderson, 1837) hoặc `[She18]` (Shelley, 1818).
        
- **Ứng dụng:** Thường dùng trong các bài báo khoa học kỹ thuật để người đọc dễ nhận diện nguồn ngay lập tức.
    

Đoạn mã

```
\bibliographystyle{alpha}
```

### 4. Quy trình thực hiện tổng quát

1. **Tạo nội dung:** Viết văn bản và chèn trích dẫn bằng lệnh `\cite{Khóa_Định_Danh}` (ví dụ: `\cite{Shelley}`).
    
    - _Mẹo:_ Các trình biên soạn (như Overleaf, TeXShop) thường hỗ trợ gợi ý khóa định danh sau khi bạn đã liên kết tệp `.bib`.
        
2. **Khai báo cuối bài:**
    
    Đoạn mã
    
    ```
    \bibliographystyle{plain} % Hoặc alpha, abbrv, v.v.
    \bibliography{biblio}     % Tên file .bib
    ```
    
3. **Biên dịch (Compile):** LaTeX sẽ tự động lấy thông tin từ file `.bib`, định dạng theo `style` đã chọn và tạo danh sách tham khảo.