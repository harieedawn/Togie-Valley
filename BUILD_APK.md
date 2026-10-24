# Tạo file APK Togie Valley (không cần Android Studio)

1. Đăng ký tài khoản GitHub, bấm **New repository**, đặt tên (ví dụ `togie-valley`), chọn Private hoặc Public rồi tạo.
2. Tải TOÀN BỘ nội dung thư mục dự án lên nhánh `main` (bấm **uploading an existing file**). Nhớ cả thư mục ẩn `.github`; nếu kéo thả trên web không thấy, hãy dùng GitHub Desktop.
3. Mở tab **Actions** của repo. Nếu được hỏi, bấm nút xanh để bật workflow.
4. Chọn **Build APK** ở cột bên trái, bấm **Run workflow** (nhánh `main`). Đợi khoảng 5-10 phút đến khi có dấu tích xanh.
5. Bấm vào lần chạy đó, kéo xuống mục **Artifacts**, tải **Togie_Valley_apk** (file .zip) rồi giải nén ra `app-debug.apk`.
6. Chép `app-debug.apk` sang điện thoại, mở file. Nếu máy hỏi, cho phép **Cài đặt ứng dụng không rõ nguồn**, rồi bấm Cài đặt.

## Cập nhật game
- Sửa file trong repo (hoặc tải file mới đè lên), commit vào `main`: máy chủ tự build lại. Hoặc bấm **Run workflow** để build tay.
- Tải APK mới và cài đè lên bản cũ; dữ liệu lưu game vẫn còn.
- Nếu báo "ứng dụng chưa được cài", hãy gỡ bản cũ rồi cài lại (lưu ý: sẽ mất dữ liệu).

## Ghi chú
- Nhạc: bỏ các file `01.mp3`, `02.mp3`... vào thư mục `music/` TRƯỚC khi tải lên; APK sẽ nặng thêm đúng bằng dung lượng MP3.
- Bản tạo ra là APK **debug**, chỉ để chơi cá nhân, không đưa lên Google Play.
- Lỗi build: mở lần chạy bị dấu đỏ trong Actions, xem dòng đỏ trong log, bấm **Re-run jobs** nếu là lỗi mạng.
