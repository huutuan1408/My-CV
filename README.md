# Nguyễn Hữu Tuấn — Portfolio CV

Trang portfolio/CV cá nhân giới thiệu Nguyễn Hữu Tuấn, định hướng Frontend Developer. Dự án được xây dựng dưới dạng website tĩnh bằng HTML và CSS, có thể mở trực tiếp trên trình duyệt hoặc phục vụ bằng máy chủ web.

## Chức năng

- Giới thiệu cá nhân và định hướng nghề nghiệp.
- Hiển thị các mục kỹ năng và dự án tiêu biểu.
- Điều hướng nhanh đến phần Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Cung cấp liên kết email, GitHub và LinkedIn.
- Bố cục responsive cho điện thoại, máy tính bảng và máy tính.
- Không cần tài khoản, cơ sở dữ liệu hay dịch vụ backend.

> Đây là website giới thiệu tĩnh. Các thẻ dự án hiện là nội dung minh họa; liên kết “Xem chi tiết” chưa trỏ đến trang dự án cụ thể.

## Công nghệ

- HTML5: cấu trúc và nội dung trang.
- CSS3: giao diện, Flexbox, CSS Grid và thiết kế responsive.
- Không sử dụng framework, thư viện JavaScript hay quy trình build.

## Cấu trúc dự án

```text
.
├── index.html
├── README.md
└── assets/
    ├── css/
    │   └── styles.css
    └── img/
        └── avatar.jpg
```

## Yêu cầu môi trường

- Trình duyệt hiện đại như Chrome, Firefox, Edge hoặc Safari.
- Để mở trực tiếp: không cần cài thêm phần mềm.
- Để chạy máy chủ cục bộ: Python 3 (hoặc dùng Docker thay thế).
- Để chạy bằng container: Docker Engine và Docker CLI; trên Windows/macOS có thể dùng Docker Desktop.
- Git chỉ cần thiết nếu muốn tải mã nguồn bằng lệnh `git clone`.

## Cài đặt

### Tải mã nguồn bằng Git

```bash
git clone https://github.com/huutuan1408/My-CV.git
cd My-CV
```

Hoặc tải mã nguồn dưới dạng ZIP từ GitHub, giải nén rồi mở thư mục dự án.

### Windows

Mở PowerShell hoặc Windows Terminal:

```powershell
git clone https://github.com/huutuan1408/My-CV.git
Set-Location My-CV
```

### macOS

Mở Terminal:

```bash
git clone https://github.com/huutuan1408/My-CV.git
cd My-CV
```

### Linux

Mở Terminal:

```bash
git clone https://github.com/huutuan1408/My-CV.git
cd My-CV
```

## Cấu hình và tùy chỉnh

Không có tệp cấu hình môi trường hay biến `.env`. Chỉnh sửa trực tiếp nội dung trong `index.html`:

- Thay tên, phần giới thiệu, kỹ năng và nội dung các thẻ dự án.
- Cập nhật email, GitHub và LinkedIn tại phần Liên hệ.
- Sửa tiêu đề trang, mô tả và thông tin tác giả trong phần `<head>`.
- Thay ảnh bằng tệp được lưu trong thư mục dự án và dùng đường dẫn tương đối, ví dụ `./assets/img/avatar.jpg`.

**Lưu ý về ảnh:** một số thẻ `<img>` hiện đang tham chiếu đến các đường dẫn tuyệt đối trên máy Windows cá nhân (ví dụ `C:\Users\...`). Các ảnh đó không được đóng gói trong dự án nên có thể không hiển thị trên máy khác hoặc khi chạy Docker. Hãy thay những đường dẫn này bằng ảnh đã thêm vào `assets/img/` và đường dẫn tương đối. Tệp `assets/img/avatar.jpg` hiện có sẵn trong dự án.

Để thay đổi giao diện, chỉnh sửa các quy tắc và biến màu trong `assets/css/styles.css`.

## Chạy thử

### Mở trực tiếp

Mở tệp `index.html` bằng trình duyệt. Cách này phù hợp để xem nhanh giao diện; một số tính năng hoặc đường dẫn ảnh có thể khác khi triển khai trên máy chủ.

### Chạy máy chủ cục bộ bằng Python

Chạy lệnh tại thư mục chứa `index.html`, sau đó truy cập <http://localhost:8000>.

**Windows (PowerShell):**

```powershell
py -m http.server 8000
```

Nếu lệnh `py` không có sẵn nhưng Python đã được cài đặt:

```powershell
python -m http.server 8000
```

**macOS:**

```bash
python3 -m http.server 8000
```

**Linux:**

```bash
python3 -m http.server 8000
```

Dừng máy chủ bằng `Ctrl+C`.

## Chạy bằng Docker

Không cần tạo Dockerfile hoặc cài dependency của dự án. Các lệnh dưới đây dùng Nginx để phục vụ thư mục hiện tại dưới dạng website tĩnh. Đảm bảo Docker Engine đang chạy và thực hiện lệnh tại thư mục có `index.html`.

**Windows (PowerShell):**

```powershell
docker run --rm -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

**macOS và Linux:**

```bash
docker run --rm -p 8080:80 -v "$PWD:/usr/share/nginx/html:ro" nginx:alpine
```

Mở <http://localhost:8080> trong trình duyệt. Dừng container bằng `Ctrl+C`. Tùy chọn `:ro` gắn thư mục ở chế độ chỉ đọc bên trong container.

## Thông tin liên hệ

- **Tác giả:** Nguyễn Hữu Tuấn
- **Email:** [td945852@gmail.com](mailto:td945852@gmail.com)
- **GitHub:** [github.com/huutuan1408](https://github.com/huutuan1408)
- **LinkedIn:** [linkedin.com/in/nguyenhuutuan](https://linkedin.com/in/nguyenhuutuan)
