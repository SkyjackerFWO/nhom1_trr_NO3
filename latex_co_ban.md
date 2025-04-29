# Hướng dẫn cú pháp LaTeX cơ bản
## 1. Giới thiệu về LaTeX
LaTeX là một hệ thống soạn thảo văn bản mạnh mẽ, đặc biệt hữu ích cho việc tạo các tài liệu khoa học, kỹ thuật và toán học. Nó sử dụng cú pháp dựa trên mã lệnh để định dạng văn bản, cho phép tạo ra các tài liệu chuyên nghiệp với độ chính xác cao.

Một file LaTeX cơ bản thường bao gồm các phần sau:
- **Phần khai báo**: Bắt đầu bằng `\documentclass{}` để xác định kiểu tài liệu.
- **Phần tiền tố**: Chứa các gói lệnh bổ sung (`\usepackage{}`) và các thiết lập.
- **Phần nội dung**: Được đặt giữa `\begin{document}` và `\end{document}`.

Ví dụ về cấu trúc cơ bản của một file LaTeX:
```latex
\documentclass{article} % Khai báo kiểu tài liệu
\usepackage[utf8]{inputenc} % Hỗ trợ mã hóa UTF-8

\title{Tài liệu LaTeX cơ bản} % Tiêu đề
\author{Nhóm 1} % Tác giả
\date{\today} % Ngày tháng

\begin{document}
\maketitle % Tạo tiêu đề

\section{Giới thiệu}
Đây là một tài liệu LaTeX cơ bản.

\end{document}
```

## 2. Cách viết công thức toán học
Trong LaTeX, công thức toán học được viết trong môi trường `$...$` (inline) hoặc `\[...\]` (block). Ví dụ:

- Inline: `$a^2 + b^2 = c^2$` → \(a^2 + b^2 = c^2\)
- Block:
    ```latex
    \[
    a^2 + b^2 = c^2
    \]
    ```

Ngoài ra, bạn có thể sử dụng môi trường `equation` để đánh số công thức:
```latex
\begin{equation}
E = mc^2
\end{equation}
```

Kết quả:
\[
E = mc^2
\]

## 3. Các ký hiệu cơ bản trong toán rời rạc

### 3.1 Tập hợp
- Tập rỗng: `\emptyset` → \(\emptyset\)
- Tập hợp: `\{a, b, c\}` → \(\{a, b, c\}\)
- Tập con: `\subseteq` → \(\subseteq\), `\subset` → \(\subset\)
- Không là tập con: `\nsubseteq` → \(\nsubseteq\)

### 3.2 Logic
- Và: `\land` → \(\land\)
- Hoặc: `\lor` → \(\lor\)
- Phủ định: `\neg` → \(\neg\)
- Kéo theo: `\implies` → \(\implies\)
- Tương đương: `\iff` → \(\iff\)

### 3.3 Quan hệ
- Bằng: `=` → \(=\)
- Không bằng: `\neq` → \(\neq\)
- Nhỏ hơn: `<` → \(<\), Lớn hơn: `>` → \(>\)
- Nhỏ hơn hoặc bằng: `\leq` → \(\leq\), Lớn hơn hoặc bằng: `\geq` → \(\geq\)

### 3.4 Phép đếm
- Giai thừa: `n!` → \(n!\)
- Tổ hợp: `\binom{n}{k}` → \(\binom{n}{k}\)
- Hoán vị: `P(n, k)` → \(P(n, k)\)

### 3.5 Hàm số
- Hàm số: `f(x) = x^2` → \(f(x) = x^2\)
- Tổng: `\sum_{i=1}^n i` → \(\sum_{i=1}^n i\)
- Tích: `\prod_{i=1}^n i` → \(\prod_{i=1}^n i\)

