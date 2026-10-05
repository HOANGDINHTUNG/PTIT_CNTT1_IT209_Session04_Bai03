# Bài 3: Cấu hình xác thực SSH và Đẩy dự án lên GitHub

## Các bước thực hiện cấu hình SSH Ed25519
1. **Sinh khóa SSH:** (Ghi lại lệnh bạn dùng để tạo khóa)
   `ssh-keygen -t ed25519 -C "email_cua_ban@example.com"`

2. **Khởi động SSH Agent và thêm khóa:**
   `eval $(ssh-agent -s)`
   `ssh-add ~/.ssh/id_ed25519`

3. **Cấu hình trên GitHub:** 
   - Lấy nội dung khóa public (`cat ~/.ssh/id_ed25519.pub`).
   - Vào GitHub > Settings > SSH and GPG keys > New SSH key, và dán nội dung vào.

4. **Đổi remote URL sang SSH:**
   `git remote set-url origin git@github.com:HOANGDINHTUNG/PTIT_CNTT1_IT209_Session04_Bai03.git`

5. **Đẩy mã nguồn lên:**
   `git push -u origin main`

## Kết quả kiểm tra
- **Kiểm tra kết nối SSH (`ssh -T git@github.com`):**
*(Bạn dán kết quả lệnh kiểm tra vào đây)*

- **Kiểm tra cấu hình remote (`git remote -v`):**
*(Bạn dán kết quả lệnh kiểm tra vào đây)*

- **Đường dẫn URL của kho lưu trữ GitHub:**
[https://github.com/HOANGDINHTUNG/PTIT_CNTT1_IT209_Session04_Bai03](https://github.com/HOANGDINHTUNG/PTIT_CNTT1_IT209_Session04_Bai03)
