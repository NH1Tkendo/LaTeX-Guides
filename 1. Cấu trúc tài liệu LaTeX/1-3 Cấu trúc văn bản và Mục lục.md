
Để tài liệu khoa học hoặc báo cáo trở nên chuyên nghiệp, việc phân chia nội dung thành các phần (sections) và mục con (subsections) là bắt buộc. LaTeX hỗ trợ việc này hoàn toàn tự động.
### 1. Tạo phần và mục con (Sections & Subsections)

#### Lệnh cơ bản

LaTeX sử dụng các lệnh sau để tạo tiêu đề cho từng phần nội dung:

- **Tạo phần chính (Section)**:
    ```
    \section{Tên tiêu đề phần}
    ```
    
    _Kết quả_: Tạo ra tiêu đề lớn, in đậm và tự động đánh số (ví dụ: **1. Introduction**).
    
- **Tạo mục con (Subsection)**:
    ```
    \subsection{Tên tiêu đề mục con}
    ```
    
    _Kết quả_: Tạo ra tiêu đề nhỏ hơn, nằm trong phần chính và đánh số phân cấp (ví dụ: **1.1. Motivation**).
    

#### Tắt chức năng đánh số

Nếu bạn muốn tạo một tiêu đề nhưng **không muốn** LaTeX đánh số thứ tự (ví dụ: lời cảm ơn, tài liệu tham khảo), hãy thêm dấu sao `*` vào sau tên lệnh:

- **Cú pháp**:
    
    Đoạn mã
    
    ```
    \section*{Tiêu đề không đánh số}
    \subsection*{Mục con không đánh số}
    ```
    
- **Lưu ý**: Khi sử dụng lệnh có dấu `*`, phần đó sẽ không làm ảnh hưởng đến thứ tự đánh số của các phần tiếp theo (bộ đếm số tự động bỏ qua phần này).
    

### 2. Tạo mục lục tự động (Table of Contents)

LaTeX tự động thu thập tất cả các phần được đánh số để tạo thành mục lục kèm theo số trang tương ứng.

- **Cách thực hiện**: Đặt lệnh sau vào vị trí bạn muốn hiển thị mục lục (thường là sau `\maketitle`):
    ```
    \tableofcontents
    ```
    
- **Cơ chế**: Nó liệt kê các `\section`, `\subsection`... và số trang của chúng.
    
#### Nguyên tắc đánh số (Numbering Philosophy)

- **Không tự điền số thủ công**: Đừng bao giờ viết thủ công như "1. Mở đầu" hay "2. Nội dung".
    
- **Hãy để LaTeX quản lý**: Chỉ cần dùng lệnh `\section{}`, LaTeX sẽ tự động tính toán thứ tự. Nếu bạn chèn thêm một phần mới vào giữa hoặc đảo vị trí đoạn văn, hệ thống sẽ tự động cập nhật lại toàn bộ số thứ tự và mục lục chính xác.