### Khái niệm cơ bản

- **Cơ sở dữ liệu BibTeX:** Là một tệp tin văn bản thuần túy chứa toàn bộ danh sách tài liệu tham khảo.
    
- **Định dạng tệp:** Tệp phải có phần mở rộng là `.bib`.
    
- **Ví dụ:** Tạo một file mới tên là `biblio.bib`.

### Cấu trúc một mục từ BibTeX

#### 1. Khai báo loại tài liệu

Bắt đầu bằng ký tự `@` theo sau là loại tài liệu (entry type).

- Ví dụ: `@book` (sách), `@article` (bài báo), `@thesis` (luận văn)...

#### 2. Khóa định danh và trường thông tin

Nội dung chi tiết được bao quanh bởi cặp dấu ngoặc nhọn `{ }`.

**Cú pháp tổng quát:**
```
@Loại_Tài_Liệu{Khóa_Định_Danh,
    Trường_1 = "Giá trị",
    Trường_2 = "Giá trị",
    ...
}
```

**Ví dụ thực tế (Sách Frankenstein):**

Đoạn mã

```
@book{Shelley,
    author    = "Mary Shelley",
    title     = "Frankenstein",
    publisher = "Tên Nhà Xuất Bản",
    year      = "1818"
}
```

**Các thành phần:**

- **Khóa định danh (Citation Key):** Tên ngắn gọn dùng để gọi trích dẫn trong LaTeX (ví dụ: `Shelley`). Theo sau khóa này phải có dấu phẩy `,`.
    
- **Các trường thông tin (Fields):**
    
    - `author`: Tác giả
        
    - `title`: Tiêu đề sách/bài viết
        
    - `publisher`: Nhà xuất bản
        
    - `year`: Năm xuất bản
        

### Các quy tắc cú pháp quan trọng

1. **Dấu bao quanh giá trị:** Bạn có thể sử dụng dấu ngoặc kép `""` hoặc dấu ngoặc nhọn `{}` cho giá trị của các trường thông tin. Cả hai đều hợp lệ.
    
    - Cách 1: `title = "Frankenstein"`
        
    - Cách 2: `title = {Frankenstein}`
        
2. **Ngăn cách trường:** Cuối mỗi dòng thông tin (trừ dòng cuối cùng có thể bỏ qua) cần có dấu phẩy `,` để ngăn cách.
    
3. **Nhiều tác giả (Multiple Authors):** Trong BibTeX, các tác giả được ngăn cách bằng từ khóa `and` (không dùng dấu phẩy hay ký tự `&`).
    
    - Ví dụ: `author = "Tác giả A and Tác giả B and Tác giả C"`
        

### Lấy trích dẫn từ Google Scholar

Thay vì gõ thủ công, bạn có thể sao chép mã BibTeX chuẩn từ các nguồn học thuật như Google Scholar.

**Các bước thực hiện:**

1. Tìm kiếm tài liệu trên Google Scholar (ví dụ: "The LaTeX Companion").
    
2. Nhấn vào nút **Trích dẫn (Cite)** (biểu tượng dấu ngoặc kép dưới bài viết).
    
3. Chọn định dạng **BibTeX**.
    
4. Sao chép toàn bộ đoạn mã hiện ra và dán vào file `.bib` của bạn.
    

> **Ghi chú:** Khi sao chép từ Google Scholar, định dạng mặc định thường sử dụng dấu ngoặc nhọn `{}` cho các giá trị thay vì dấu ngoặc kép. Điều này hoàn toàn bình thường và hợp lệ.