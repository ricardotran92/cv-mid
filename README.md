# Computer Vision Midterm Review

Website tĩnh: `index.html` và thư mục `img/` (hình trích từ bài giảng và đề thi). Không cần build, không cần server.

## Xem thử trên máy
Mở thẳng file `index.html` bằng trình duyệt (Chrome, Edge, Firefox, Safari).

## Host trên GitHub Pages

### Cách 1: qua giao diện web (không cần cài gì)
1. Đăng nhập https://github.com, bấm **+** (góc trên phải) → **New repository**.
2. Đặt tên, ví dụ `cv-midterm`, chọn **Public**, bấm **Create repository**.
   (GitHub Pages miễn phí yêu cầu repo Public, trừ khi bạn có gói Pro.)
3. Trong trang repo vừa tạo, bấm **uploading an existing file** (hoặc **Add file → Upload files**).
4. Kéo thả **các file và thư mục bên trong** thư mục này (`index.html`, thư mục `img`, `.nojekyll`, `README.md`) vào. Kéo cả thư mục `img` để giữ nguyên đường dẫn hình. Đừng kéo thư mục ngoài cùng `cv-midterm-site`, vì `index.html` phải nằm ở gốc repo.
   Nếu `.nojekyll` bị ẩn trên máy: macOS bấm `Cmd+Shift+.` trong Finder; Windows bật View → Hidden items. File này không bắt buộc, thiếu cũng chạy.
5. Bấm **Commit changes**.
6. Vào **Settings → Pages** (menu bên trái).
7. Ở **Build and deployment → Source** chọn **Deploy from a branch**; **Branch** chọn `main` và thư mục `/ (root)`; bấm **Save**.
8. Đợi 1–2 phút, tải lại trang Settings → Pages. Link sẽ hiện ở đầu trang:
   `https://<tên-tài-khoản>.github.io/cv-midterm/`

### Cách 2: dùng git (dòng lệnh)
```bash
cd cv-midterm-site
git init
git add .
git commit -m "Add CV midterm study site"
git branch -M main
git remote add origin https://github.com/<tên-tài-khoản>/cv-midterm.git
git push -u origin main
```
Sau đó làm bước 6–8 ở trên.

## Cập nhật nội dung
Sửa `index.html`, rồi upload đè (Add file → Upload files) hoặc `git commit` + `git push`. Trang tự cập nhật sau khoảng 1 phút.

## Lưu ý
- Liên kết thẳng tới từng tab: thêm `#theory`, `#exam-2022`, `#exam-2023`, `#practice`, `#quiz` vào cuối URL.
- Tiến độ làm trắc nghiệm lưu trong trình duyệt của từng người (localStorage), không đồng bộ giữa các máy.
- Font tải từ Google Fonts; nếu không có mạng, trang vẫn hiển thị bằng font hệ thống.
- Lỗi 404 ngay sau khi bật Pages là bình thường; đợi vài phút. Nếu vẫn 404, kiểm tra `index.html` có nằm ở gốc repo không.
