# Hướng dẫn cài đặt LaTeX trên VS Code

## 1. Cài đặt trên Windows
### Bước 1: Cài đặt LaTeX
- Tải và cài đặt [MikTeX](https://miktex.org/download) hoặc [TeX Live](https://www.tug.org/texlive/).
- Đảm bảo thêm đường dẫn của LaTeX vào `PATH` trong hệ thống.

### Bước 2: Cài đặt VS Code
- Tải và cài đặt [Visual Studio Code](https://code.visualstudio.com/).

### Bước 3: Cài đặt các tiện ích mở rộng
- Mở VS Code, vào **Extensions** (Ctrl+Shift+X).
- Tìm và cài đặt:
    - **LaTeX Workshop** (James Yu)
    - **LaTeX Utilities** (tecosaur)

### Bước 4: Cấu hình
- Mở file `settings.json` trong VS Code và thêm:
    ```json
    "latex-workshop.latex.tools": [
        {
            "name": "pdflatex",
            "command": "pdflatex",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "%DOC%"
            ]
        }
    ],
    "latex-workshop.latex.recipes": [
        {
            "name": "pdflatex",
            "tools": ["pdflatex"]
        }
    ]
    ```

---

## 2. Cài đặt trên macOS
### Bước 1: Cài đặt LaTeX
- Tải và cài đặt [MacTeX](https://tug.org/mactex/).
- Đảm bảo đường dẫn LaTeX đã được thêm vào `PATH`.

### Bước 2: Cài đặt VS Code
- Tải và cài đặt [Visual Studio Code](https://code.visualstudio.com/).

### Bước 3: Cài đặt các tiện ích mở rộng
- Tương tự như trên Windows.

### Bước 4: Cấu hình
- Tương tự như trên Windows.

---

## 3. Cài đặt trên Ubuntu
### Bước 1: Cài đặt LaTeX
- Mở Terminal và chạy:
    ```bash
    sudo apt update
    sudo apt install texlive-full
    ```

### Bước 2: Cài đặt VS Code
- Tải và cài đặt [Visual Studio Code](https://code.visualstudio.com/).
- Hoặc cài đặt qua Terminal:
    ```bash
    sudo snap install --classic code
    ```

### Bước 3: Cài đặt các tiện ích mở rộng
- Tương tự như trên Windows.

### Bước 4: Cấu hình
- Tương tự như trên Windows.

---

## 4. Kiểm tra hoạt động
- Tạo file `.tex` và sử dụng lệnh `Ctrl+Alt+B` (hoặc `Cmd+Alt+B` trên macOS) để biên dịch.
- Đảm bảo file PDF được tạo thành công.

## 5. Gỡ lỗi
- Nếu gặp lỗi, kiểm tra:
    - Đường dẫn LaTeX trong `PATH`.
    - Cấu hình trong `settings.json`.
    - Log trong **LaTeX Workshop**.
