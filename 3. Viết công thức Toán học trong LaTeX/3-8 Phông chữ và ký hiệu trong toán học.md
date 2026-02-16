### 1. Yêu cầu gói (Packages)
```
\usepackage{amsfonts}
\usepackage{amsmath}
```

### 2. Các kiểu Font chữ đặc biệt

LaTeX cung cấp các lệnh để thay đổi kiểu chữ trong môi trường toán học (`$...$`).

#### A. Chữ in đậm (Bold Face)

- **Mục đích**: Thường dùng để biểu diễn vector hoặc ma trận.
    
- **Lệnh**: `\mathbf{...}`
    
- **Ví dụ**:
    
    Đoạn mã
    
    ```
    \mathbf{A}
    ```
    
    $\rightarrow$ Kết quả: $\mathbf{A}$
    

#### B. Chữ hoa mỹ (Calligraphy Font)

- **Mục đích**: Dùng cho các không gian topo, tập hợp hoặc họ các tập hợp.
    
- **Lệnh**: `\mathcal{...}`
    
- **Lưu ý**: Chỉ hoạt động tốt với **chữ cái in hoa**. Nếu dùng chữ thường sẽ ra các ký hiệu lạ (như ký hiệu logic).
    
- **Ví dụ**:
    
    Đoạn mã
    
    ```
    \mathcal{T} % Cho Topology
    \mathcal{C} % Cho Collection
    ```
    
    $\rightarrow$ Kết quả: $\mathcal{T}, \mathcal{C}$
    

#### C. Chữ nét đôi / Bảng đen (Blackboard Bold)

- **Mục đích**: Dùng để ký hiệu các tập hợp số chuẩn ($\mathbb{R}$ - số thực, $\mathbb{N}$ - số tự nhiên, $\mathbb{Z}$ - số nguyên).
    
- **Lệnh**: `\mathbb{...}`
    
- **Lưu ý**: Chỉ hoạt động với **chữ cái in hoa**. Nếu dùng chữ thường (ví dụ `\mathbb{a}`), LaTeX sẽ hiển thị các ký tự lỗi hoặc không mong muốn.
    
- **Ví dụ**:
    
    Đoạn mã
    
    ```
    \mathbb{R}
    ```
    
    $\rightarrow$ Kết quả: $\mathbb{R}$
    

### 3. Ký hiệu trên ký tự (Accents & Bars)

Cách thêm các dấu gạch ngang, dấu chấm hoặc dấu phẩy trên đầu ký tự.

#### A. Dấu gạch ngang (Bar & Overline)

Có hai lệnh để tạo dấu gạch ngang trên đầu, cần phân biệt rõ ngữ cảnh sử dụng:

|**Lệnh**|**Phạm vi sử dụng**|**Ví dụ**|**Kết quả**|
|---|---|---|---|
|`\bar{...}`|Dùng cho **một ký tự duy nhất**.|`\bar{a}`|$\bar{a}$|
|`\overline{...}`|Dùng cho **nhiều ký tự** (chuỗi).|`\overline{AB}`|$\overline{AB}$|

> **⚠️ Lưu ý:** Không nên dùng `\bar{AB}` cho nhiều ký tự vì dấu gạch sẽ chỉ nằm nhỏ ở giữa, không bao phủ hết các chữ cái.

#### B. Đạo hàm (Derivatives)

Có hai cách ký hiệu đạo hàm phổ biến:

1. **Đạo hàm theo thời gian (Time derivative):** Dùng dấu chấm trên đầu.
    
    - Lệnh: `\dot{f}`
        
    - Kết quả: $\dot{f}$
        
2. **Đạo hàm thông thường (Spatial/General derivative):** Dùng dấu phẩy (prime).
    
    - Lệnh: `f'` hoặc `f''` (đạo hàm cấp 2).
        
    - Kết quả: $f', f''$
        

---

### Tóm tắt lệnh

|**Kiểu hiển thị**|**Lệnh LaTeX**|**Ví dụ hiển thị**|
|---|---|---|
|**In đậm**|`\mathbf{A}`|$\mathbf{A}$|
|**Hoa mỹ**|`\mathcal{A}`|$\mathcal{A}$|
|**Nét đôi**|`\mathbb{R}`|$\mathbb{R}$|
|**Gạch đơn**|`\bar{x}`|$\bar{x}$|
|**Gạch dài**|`\overline{xy}`|$\overline{xy}$|
|**Đạo hàm (chấm)**|`\dot{x}`|$\dot{x}$|