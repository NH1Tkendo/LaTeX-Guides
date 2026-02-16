Bài học này tập trung vào cách hiển thị các toán tử toán học phức tạp bằng gói `amsmath`. Điểm quan trọng cần lưu ý là sự khác biệt về cách hiển thị giữa **chế độ cùng dòng** (Inline math) và **chế độ hiển thị** (Display math).

### 1. Tổng chuỗi 

Lệnh cơ bản để tạo dấu tổng là `\sum`.

#### Cú pháp và hiển thị

- **Cận dưới:** Dùng dấu gạch dưới `_`.
    
- **Cận trên:** Dùng dấu mũ `^`.
    
- **Vô cực:** Dùng lệnh `\infty`.
    

#### Sự khác biệt giữa Inline và Display

- **Inline Math (`$...$`):** Các cận (trên và dưới) sẽ nằm **bên cạnh** dấu tổng để tiết kiệm không gian dòng, tránh làm giãn dòng văn bản.
    
- **Display Math (`\[...\]`):** Các cận sẽ nằm **trực tiếp bên trên và bên dưới** dấu tổng, giúp công thức rõ ràng hơn.
    

**Mã nguồn ví dụ:**

Đoạn mã

```
% Inline math (Cận nằm ngang hàng)
The sum is $\sum_{n=0}^{\infty} \frac{1}{n^2+1}$.

% Display math (Cận nằm trên/dưới)
\[
    \sum_{n=0}^{\infty} \frac{1}{n^2+1}
\]
```

### 2. Tích phân 

Lệnh cơ bản để tạo dấu tích phân là `\int`. Cú pháp cận trên/dưới tương tự như lệnh `\sum`.

#### Các loại tích phân

- **Tích phân đơn:** `\int`
    
- **Tích phân đôi:** `\iint`
    
- **Tích phân ba:** `\iiint`
    

**Mã nguồn ví dụ:**

Đoạn mã

```
% Tích phân đơn
\int_{0}^{1} x^2 dx

% Tích phân đôi
\iint (x + y) dy dx

% Tích phân ba
\iiint f(x,y,z) dx dy dz
```

> **Lưu ý:** Trong chế độ _Display math_, các dấu tích phân sẽ lớn hơn và thoáng hơn so với chế độ _Inline_.

### 3. Giới hạn (Limits)

Lệnh cơ bản là `\lim`. Thường đi kèm với ký hiệu mũi tên "tiến tới".

- **Mũi tên:** Dùng lệnh `\to` (ví dụ: $x \to 1$).
    
- **Vị trí điều kiện:**
    
    - _Inline:_ Điều kiện $x \to 1$ nằm bên cạnh chữ `lim`.
        
    - _Display:_ Điều kiện nằm ngay bên dưới chữ `lim`.
        

**Mã nguồn ví dụ:**

Đoạn mã

```
% Giới hạn cơ bản
\lim_{x \to 1} x

% Giới hạn trong Display math
\[
    \lim_{x \to \infty} \frac{1}{x} = 0
\]
```

### 4. Các toán tử khác (Other Operators)

LaTeX cung cấp nhiều lệnh toán tử hoạt động tương tự như `\lim` (cho phép đặt chỉ số bên dưới trong chế độ Display).

|**Lệnh**|**Ý nghĩa**|**Ví dụ mã**|
|---|---|---|
|`\max`|Giá trị lớn nhất|`\max_{n}`|
|`\min`|Giá trị nhỏ nhất|`\min_{x}`|
|`\sup`|Cận trên đúng (Supremum)|`\sup`|
|`\inf`|Cận dưới đúng (Infimum)|`\inf`|
|`\limsup`|Giới hạn trên|`\limsup`|
|`\liminf`|Giới hạn dưới|`\liminf`|

#### Lưu ý về dấu ngoặc nhọn `{ }`

Dấu ngoặc nhọn `{}` là ký tự đặc biệt trong LaTeX (dùng để nhóm lệnh). Để hiển thị dấu ngoặc nhọn trong công thức (ví dụ: tập hợp), bạn cần thêm dấu gạch chéo ngược `\` phía trước.

**Ví dụ:** Tìm max trong tập hợp $\{1, 2, 3\}$:

Đoạn mã

```
% Chú ý dấu \{ và \}
\max_{n \in \{1, 2, 3\}} n
```