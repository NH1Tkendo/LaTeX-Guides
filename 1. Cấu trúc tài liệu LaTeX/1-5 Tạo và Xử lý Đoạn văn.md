### Nguyên tắc xuống dòng trong LaTeX

- **Phím Enter đơn:** Trong trình soạn thảo code, việc nhấn Enter một lần (xuống dòng đơn) sẽ bị LaTeX bỏ qua và coi như một dấu cách thông thường.
    
- **Tạo đoạn văn mới:** Để thực sự tạo một đoạn văn mới, bạn cần nhấn Enter hai lần để tạo ra một **dòng trống** (blank line) giữa các khối văn bản.
    
    - Kết quả: Văn bản sẽ xuống dòng và có phần thụt đầu dòng (indentation) đặc trưng của đoạn văn mới.
        

### Các lệnh điều khiển đoạn văn

Ngoài việc dùng phím Enter, bạn có thể sử dụng các lệnh sau:

1. **Lệnh `\par`**:
    
    - Chức năng: Tương đương với việc để lại một dòng trống. Nó báo hiệu kết thúc đoạn văn hiện tại và bắt đầu đoạn mới.
        
    - Đặc điểm: Có thụt đầu dòng.
        
    - _Gợi ý:_ Nên kết hợp `\par` với việc xuống dòng trong code để dễ nhìn hơn.
        
2. **Lệnh `\newline`**:
    
    - Chức năng: Ngắt dòng ngay lập tức tại vị trí đặt lệnh.
        
    - Đặc điểm: **Không** thụt đầu dòng ở dòng mới.
        
    - Sử dụng khi: Bạn muốn xuống dòng nhưng vẫn muốn giữ nội dung thuộc cùng một đoạn văn (về mặt ngữ nghĩa hoặc trình bày).
        

---

## Định dạng Văn bản (Text Formatting)

### Các lệnh định dạng cơ bản

Để nhấn mạnh từ ngữ hoặc thay đổi kiểu chữ, sử dụng các lệnh sau bao quanh văn bản cần định dạng:

- **In đậm (Bold): `\textbf{nội dung in đậm}`
- **In nghiêng (Italic): `\textit{nội dung in nghiêng}`
- **Gạch chân**(Underline): `\underline{nội dung gạch chân}`
