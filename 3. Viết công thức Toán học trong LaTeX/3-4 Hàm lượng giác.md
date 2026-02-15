### Cú pháp cơ bản

Trong chế độ toán học (Math mode), không nên viết tên hàm như văn bản thường (ví dụ: viết `sin` hay `cos` trực tiếp). LaTeX sẽ hiểu đó là tích của các biến số $s, i, n$ và in nghiêng chúng ($sin$).

Để hiển thị đúng định dạng hàm (chữ đứng), cần sử dụng dấu gạch chéo ngược `\` trước tên hàm.

- **Sai:** `sin(x)` $\rightarrow$ hiển thị là $sin(x)$ (chữ nghiêng, sai quy chuẩn).
    
- **Đúng:** `\sin(x)` $\rightarrow$ hiển thị là $\sin(x)$ (chữ đứng, đúng quy chuẩn).
    

**Ví dụ mã nguồn:**
```
% Inline math
\sin(2)
\sin{2} 
% Cả hai cách viết ngoặc đơn () hay ngoặc nhọn {} đều chấp nhận được
```

### Hằng đẳng thức lượng giác và Trình bày mã nguồn

Khi viết các công thức dài trong môi trường **Toán khối (Display Math)**, bạn có thể ngắt dòng trong trình soạn thảo code để dễ đọc. Việc xuống dòng trong code không ảnh hưởng đến hiển thị kết quả cuối cùng.

**Ví dụ:** Hằng đẳng thức $\cos^2(x) + \sin^2(x) = 1$

**Mã nguồn:**

Đoạn mã

```
\[
    \cos^{2}(x) 
    + 
    \sin^{2}(x) 
    = 1.
\]
```

_Lưu ý: Việc dùng ngoặc nhọn `{}` bao quanh số mũ `^{2}` là thói quen tốt (good practice), dù không bắt buộc với một ký tự số._

---

## Quy tắc dấu câu trong môi trường Toán (Punctuation)

Khi kết thúc một công thức toán khối (Display Math) bằng dấu chấm câu (như dấu chấm hoặc phẩy):

- **Quy tắc:** Đặt dấu câu ở **bên trong** môi trường toán học (trước dấu đóng `\]`).
    
- **Lý do:** Nếu đặt bên ngoài, dấu câu sẽ bị rớt xuống dòng mới hoặc nằm sai vị trí lề, gây mất thẩm mỹ.
    

**So sánh:**

- _Đúng:_ `... = 1.]` $\rightarrow$ Dấu chấm nằm cùng dòng với công thức.
    
- _Sai:_ `... = 1].` $\rightarrow$ Dấu chấm bị đẩy ra ngoài, có thể rớt dòng.
    

---

## Công cụ tra cứu ký hiệu: Detexify

Vì LaTeX có quá nhiều ký hiệu và lệnh khó nhớ hết, công cụ **Detexify** giúp tìm lệnh bằng cách vẽ tay.

### Cách sử dụng

1. Truy cập công cụ Detexify (có thể tìm trên Google).
    
2. Vẽ phác thảo ký hiệu muốn tìm vào khung vẽ bằng chuột.
    
3. Công cụ sẽ gợi ý các lệnh tương ứng.
    

### Ví dụ thực tế: Ký hiệu tập con

Giả sử cần tìm ký hiệu "tập con hoặc bằng" ($\subseteq$).

- Vẽ ký hiệu tập con lên Detexify.
    
- Kết quả gợi ý: `\subseteq` (viết tắt của _subset equation_).
    

**Mã nguồn:**

Đoạn mã

```
A \subseteq B
```

---
