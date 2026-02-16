### 1. Hệ thống Đánh số (Numbering Logic)

Mặc định, mỗi môi trường (Theorem, Definition) có một bộ đếm riêng biệt (Ví dụ: Theorem 1, Definition 1). Tuy nhiên, ta có thể liên kết chúng hoặc đánh số theo cấu trúc bài viết.

#### A. Đánh số chung (Shared Counter)

Khi muốn các môi trường chia sẻ chung một bộ đếm (Ví dụ: Theorem 1 $\rightarrow$ Definition 2 $\rightarrow$ Theorem 3), ta sử dụng tham số tùy chọn **nằm giữa** hai tham số bắt buộc.

- **Cú pháp:**
    
    Đoạn mã
    
    ```
    \newtheorem{tên_mới}[tên_cũ]{Tên_hiển_thị}
    ```
    
- **Ví dụ:** Muốn `definition` dùng chung bộ đếm với `theorem`:
    
    Đoạn mã
    
    ```
    \newtheorem{theorem}{Theorem}
    % [theorem] ở giữa: Báo hiệu dùng chung bộ đếm với theorem
    \newtheorem{definition}[theorem]{Definition}
    ```
    

#### B. Đánh số theo phân cấp (Section-based Numbering)

Khi muốn số thứ tự reset theo từng mục (Ví dụ: Theorem 1.1, Theorem 1.2... sang mục 2 thành Theorem 2.1), ta sử dụng tham số tùy chọn **nằm cuối cùng**.

- **Cú pháp:**
    
    Đoạn mã
    
    ```
    \newtheorem{tên_môi_trường}{Tên_hiển_thị}[cấp_độ_mẹ]
    ```
    
- **Ví dụ:** Đánh số theo `section` (hoặc `chapter`, `subsection`):
    
    Đoạn mã
    
    ```
    % [section] ở cuối: Reset số mỗi khi sang section mới
    \newtheorem{theorem}{Theorem}[section]
    ```
    

### 2. Thay đổi Giao diện (Theorem Styles)

Gói `amsthm` cung cấp lệnh `\theoremstyle{...}` để thay đổi font chữ của tiêu đề và nội dung. Lệnh này cần đặt **trước** các lệnh `\newtheorem` mà bạn muốn áp dụng.

Có 3 kiểu style chính:

|**Tên Style**|**Đặc điểm hiển thị**|**Thường dùng cho**|
|---|---|---|
|`plain` (Mặc định)|**Tiêu đề in đậm**, _Nội dung in nghiêng_|Theorem, Lemma, Proposition|
|`definition`|**Tiêu đề in đậm**, Nội dung in thẳng (Roman)|Definition, Example, Problem|
|`remark`|_Tiêu đề in nghiêng_, Nội dung in thẳng|Remark, Note, Annotation|

**Mã nguồn mẫu:**

Đoạn mã

```
% Các môi trường dùng style mặc định (plain)
\theoremstyle{plain}
\newtheorem{theorem}{Theorem}

% Các môi trường dùng style định nghĩa (definition)
\theoremstyle{definition}
\newtheorem{defn}{Definition}

% Các môi trường dùng style ghi chú (remark)
\theoremstyle{remark}
\newtheorem*{rem}{Remark} % Dùng * để không đánh số
```

### 3. Môi trường Chứng minh (Proof Environment)

Gói `amsthm` cung cấp sẵn môi trường `proof` để trình bày lời giải hoặc chứng minh toán học.

- **Đặc điểm:**
    
    - Tự động thêm chữ _Proof_ (hoặc _Chứng minh_) in nghiêng ở đầu.
        
    - Tự động thêm ký hiệu kết thúc chứng minh (QED symbol - hình vuông rỗng $\square$) ở cuối dòng cuối cùng.
        
- **Cú pháp:**
    
    Đoạn mã
    
    ```
    \begin{proof}
        Đây là nội dung chứng minh...
        Vì vậy ta có điều phải chứng minh.
    \end{proof}
    ```
    

---

**Tổng kết Cú pháp `\newtheorem`:**

1. `\newtheorem{env}{Name}`: Đánh số độc lập (1, 2, 3...).
    
2. `\newtheorem{env}[other_env]{Name}`: Đánh số nối tiếp theo `other_env`.
    
3. `\newtheorem{env}{Name}[section]`: Đánh số theo section (1.1, 1.2...).