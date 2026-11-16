# AnhCrisSPORT

Website giới thiệu và trưng bày các sản phẩm thể thao, gồm áo bóng đá, giày, bóng và trang phục thể thao mùa đông. Giao diện được xây dựng dưới dạng website tĩnh, có thể mở trực tiếp bằng trình duyệt hoặc phục vụ bằng máy chủ web.

## Chức năng

- Hiển thị trang chủ với thông điệp giới thiệu cửa hàng.
- Trưng bày sản phẩm kèm hình ảnh và giá tham khảo.
- Điều hướng đến các khu vực Trang chủ, Sản phẩm và Liên hệ.
- Hiển thị địa chỉ, số điện thoại và email liên hệ.
- Cung cấp biểu mẫu nhập thông tin để liên hệ.
- Bố cục tự điều chỉnh theo kích thước màn hình.

> **Lưu ý:** Đây là giao diện minh họa phía trình duyệt. Nút “Thêm vào giỏ” hiện chưa có chức năng giỏ hàng; website chưa có đăng nhập, thanh toán, quản lý sản phẩm hoặc máy chủ xử lý dữ liệu. Biểu mẫu liên hệ dùng `mailto` nên cần có ứng dụng email mặc định và hiện vẫn trỏ đến địa chỉ mẫu `email-cua-ban@gmail.com`.

## Công nghệ

- HTML5
- CSS3
- Hình ảnh sản phẩm định dạng JPG và WebP
- Docker và Nginx (tùy chọn để phục vụ website)

Dự án không cần Node.js, trình biên dịch hay cài đặt thư viện.

## Cấu trúc dự án

```text
.
├── index.html
├── style.css
├── ảnh/
│   └── ... hình ảnh sản phẩm
└── README.md
```

Giữ nguyên tên và vị trí thư mục `ảnh/` cùng các tệp hình ảnh để những đường dẫn ảnh trong trang hoạt động chính xác.

## Yêu cầu môi trường

### Chạy trực tiếp

- Windows, macOS hoặc Linux.
- Trình duyệt hiện đại như Chrome, Edge, Firefox hoặc Safari.
- Không cần cài thêm môi trường phát triển.

### Chạy bằng máy chủ cục bộ

- Python 3 (tùy chọn), hoặc tiện ích Live Server trong Visual Studio Code.

### Chạy bằng Docker

- Docker Desktop trên Windows/macOS hoặc Docker Engine trên Linux.
- Docker CLI hoạt động được trong Terminal, PowerShell hoặc Command Prompt.

## Cài đặt

Tải hoặc sao chép toàn bộ mã nguồn về máy. Nếu dùng Git:

```bash
git clone <URL-kho-ma-nguon>
cd <thu-muc-du-an>
```

Thay `<URL-kho-ma-nguon>` bằng URL kho mã nguồn và `<thu-muc-du-an>` bằng thư mục vừa tải. Nếu đã có thư mục dự án, mở Terminal tại thư mục chứa `index.html`.

### Windows

Mở PowerShell hoặc Command Prompt tại thư mục dự án. Có thể mở `index.html` trực tiếp bằng trình duyệt; hoặc chạy máy chủ cục bộ như hướng dẫn bên dưới.

### macOS

Mở Terminal, dùng `cd` để chuyển đến thư mục dự án, sau đó mở `index.html` bằng trình duyệt hoặc chạy máy chủ cục bộ.

### Linux

Mở Terminal, dùng `cd` để chuyển đến thư mục dự án, sau đó mở `index.html` bằng trình duyệt hoặc chạy máy chủ cục bộ.

## Cấu hình

Không cần tệp cấu hình để xem trang. Có thể tùy chỉnh nội dung như sau:

- **Tên cửa hàng, sản phẩm, giá và thông tin liên hệ:** sửa nội dung trong `index.html`.
- **Màu sắc, bố cục và kiểu chữ:** sửa quy tắc trong `style.css`.
- **Hình ảnh sản phẩm:** thay tệp trong `ảnh/` hoặc cập nhật đường dẫn `src` tương ứng trong `index.html`. Giữ nguyên tên tệp (kể cả dấu tiếng Việt và khoảng trắng) nếu không sửa đường dẫn.
- **Địa chỉ nhận biểu mẫu:** trước khi sử dụng biểu mẫu, thay địa chỉ mẫu trong thuộc tính `action` của thẻ `<form>` trong `index.html` bằng địa chỉ email mong muốn. Cách gửi `mailto` phụ thuộc vào ứng dụng email được cấu hình trên thiết bị và không thay thế dịch vụ xử lý biểu mẫu phía máy chủ.

## Chạy thử

### Mở trực tiếp

Mở tệp `index.html` bằng trình duyệt. Cách này không yêu cầu cài đặt thêm, nhưng dùng máy chủ cục bộ thường thuận tiện hơn khi chỉnh sửa và kiểm tra.

### Dùng Python (Windows, macOS, Linux)

Tại thư mục dự án, chạy:

```bash
python -m http.server 8000
```

Trên một số hệ thống, lệnh có thể là:

```bash
python3 -m http.server 8000
```

Mở <http://localhost:8000> trong trình duyệt. Dừng máy chủ bằng `Ctrl+C`.

### Dùng Visual Studio Code

Mở thư mục dự án trong Visual Studio Code, cài tiện ích **Live Server** nếu chưa có, nhấp chuột phải vào `index.html` và chọn **Open with Live Server**. Mở địa chỉ mà tiện ích hiển thị trong trình duyệt.

## Chạy bằng Docker

Các lệnh sau chạy Nginx trong container và phục vụ trực tiếp các tệp của thư mục dự án. Không cần tạo Dockerfile.

### Windows PowerShell

Mở PowerShell tại thư mục chứa `index.html`, sau đó chạy:

```powershell
docker run --rm --name anhcrissport -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

### macOS hoặc Linux

Mở Terminal tại thư mục chứa `index.html`, sau đó chạy:

```bash
docker run --rm --name anhcrissport -p 8080:80 -v "$PWD:/usr/share/nginx/html:ro" nginx:alpine
```

Sau khi container khởi động, mở <http://localhost:8080>. Dừng container bằng `Ctrl+C`. Nếu cổng `8080` đang được sử dụng, đổi phần `-p 8080:80` thành một cổng khác, ví dụ `-p 8081:80`, rồi mở cổng tương ứng trên trình duyệt.

## Thông tin liên hệ

- **Cửa hàng:** AnhCrisSPORT
- **Địa chỉ:** Xã Tri Lễ - Tỉnh Nghệ An
- **Hotline:** 0388 066 923
- **Email:** ngananh324@gmail.com