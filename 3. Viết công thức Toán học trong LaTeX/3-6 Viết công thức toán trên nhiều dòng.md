Trong thực tế, ta thường gặp các trường hợp phương trình quá dài không hiển thị đủ trên một dòng, hoặc cần trình bày các bước biến đổi toán học liên tiếp. LaTeX cung cấp hai môi trường chính trong gói `amsmath` để xử lý việc này: `multline` và `align`.

### 1. Môi trường `multline`

Môi trường này được sử dụng khi bạn có **một phương trình duy nhất** nhưng quá dài, cần ngắt xuống dòng.

- **Cơ chế hoạt động:**
    
    - Dòng đầu tiên được căn trái.
        
    - Dòng cuối cùng được căn phải.
        
    - Các dòng ở giữa (nếu có) thường được căn giữa.
        
- **Ngắt dòng:** Sử dụng ký hiệu `\\` tại vị trí muốn ngắt.
    

**Mã nguồn ví dụ:**

Đoạn mã

```
\begin{multline}
    x^2 + 3x^3 + 4xy + \dots \text{(phần đầu phương trình)} \\
    + \dots + 5z + 6w \text{(phần cuối phương trình)}
    \label{eq:long_equation}
\end{multline}
```

### 2. Môi trường `align` (Căn chỉnh nhiều phương trình)

Môi trường này hoạt động giống như bảng (table), dùng để căn chỉnh hàng dọc cho nhiều phương trình (ví dụ: hệ phương trình hoặc các bước giải toán).

- **Ký hiệu căn chỉnh:** Sử dụng dấu `&` tại vị trí muốn các dòng thẳng hàng nhau (thường là trước dấu `=`).
    
- **Ngắt dòng:** Sử dụng `\\` để chuyển sang phương trình tiếp theo.
    
- **Nhiều cột:** Bạn có thể dùng nhiều dấu `&` để tạo nhiều cột phương trình trên cùng một dòng.
    

**Ví dụ 1: Hệ phương trình**

Đoạn mã

```
\begin{align}
    2x + 3y + 3z + w &= 2 \\
    3x + 4y + z + 0w &= 4 \\
    x + 4y + 3z + w &= 3
    \label{eq:system}
\end{align}
```

_Kết quả:_ Các dấu bằng `=` của 3 phương trình sẽ nằm thẳng hàng nhau.

**Ví dụ 2: Các bước biến đổi (Rút gọn biểu thức)**

Đoạn mã

```
\begin{align}
    f(x, y) &= 2x + 3y - 2x \\
            &= 3y
\end{align}
```

_Kết quả:_ Dấu `=` của bước rút gọn sẽ thẳng hàng với dấu `=` của biểu thức ban đầu, tạo nên trình bày mạch lạc.

### 3. Quản lý đánh số phương trình (Numbering)

LaTeX mặc định đánh số tất cả các dòng trong các môi trường này.

#### Tắt đánh số toàn bộ (`*`)

Thêm dấu sao `*` vào tên môi trường để tắt đánh số cho tất cả các dòng bên trong.

- `\begin{multline*} ... \end{multline*}`
    
- `\begin{align*} ... \end{align*}`
    

#### Tắt đánh số từng dòng (`\notag`)

Nếu bạn muốn giữ số thứ tự cho một số dòng nhưng tắt ở dòng khác (ví dụ: chỉ đánh số dòng kết quả cuối cùng), hãy dùng lệnh `\notag` trước dấu ngắt dòng `\\`.

Đoạn mã

```
\begin{align}
    2x + 3y + z &= 5 \notag \\ % Dòng này không được đánh số
    3y + z &= 3        % Dòng này được đánh số
\end{align}
```

### 4. Tham chiếu chéo (Cross-referencing)

Quy trình tham chiếu tương tự như phương trình đơn:

1. Gắn nhãn bằng `\label{ten_nhan}` ở dòng cần tham chiếu.
    
2. Gọi lại bằng `\eqref{ten_nhan}` (nếu dùng gói `amsmath`) hoặc `\ref{ten_nhan}`.
    

> **Lưu ý:** Trong môi trường `align`, bạn có thể đặt `\label` ở từng dòng riêng biệt để tham chiếu đến cụ thể dòng đó trong hệ phương trình.

---

**Tóm tắt cú pháp:**

|**Môi trường**|**Mục đích**|**Ký hiệu quan trọng**|
|---|---|---|
|`multline`|1 phương trình dài ngắt thành nhiều dòng|`\\` để ngắt dòng|
|`align`|Nhiều phương trình cần thẳng hàng (dấu =)|`&` để căn chỉnh, `\\` để ngắt dòng|
|`align*`|Giống `align` nhưng không đánh số|`&`, `\\`|
|`\notag`|Tắt đánh số cho 1 dòng cụ thể|Đặt trước `\\`|