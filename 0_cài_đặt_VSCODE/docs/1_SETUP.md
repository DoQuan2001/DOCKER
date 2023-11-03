# CÀI ĐẶT VSCODE TRÊN UBUNTU.


1 SỐ LƯU Ý!. KHI CÀI ĐẶT PHẢI ĐỂ Ở QUYỀN ROOT.

VÀ KHI TẠO THƯ MỤC TRONG VSCODE. CẦN CUNG CẤP QUYỀN THỰC THI FULL QUYỀN CHO THƯ MỤC ĐÓ TRƯỚC.

`chmod -R 755 + tênthưmục`: lệnh cung cấp full quyền.

SCRIPT SETUP.

```
#!/bin/bash

# Kiểm tra xem người dùng đang chạy script với quyền root hay không
if [[ $EUID -ne 0 ]]; then
  echo "Script cần chạy với quyền root. Vui lòng chạy lại với lệnh 'sudo'."
  exit 1
fi

# Thêm kho lưu trữ của Microsoft vào danh sách
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
install -o root -g root -m 644 packages.microsoft.gpg /etc/apt/trusted.gpg.d/
rm packages.microsoft.gpg

# Thêm kho lưu trữ VSCode vào danh sách
echo "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list.d/vscode.list

# Cập nhật danh sách kho lưu trữ
apt update

# Cài đặt Visual Studio Code
apt install -y code

# In thông báo cài đặt thành công
echo "Visual Studio Code đã được cài đặt thành công."

# Kết thúc script
exit 0

```