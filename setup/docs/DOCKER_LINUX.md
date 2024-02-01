# CÀI ĐẶT DOCKER TRÊN LINUX.

## I. CÀI ĐẶT DOCKER TRÊN UNBUNTU.

LINK HƯỚNG DẪN CHI TIẾT: https://docs.docker.com/engine/install/ubuntu/


SCRIPT:
```
#!/bin/bash

# Cập nhật hệ thống
sudo apt update

# Cài đặt các gói phụ thuộc để sử dụng repository qua HTTPS
sudo apt install -y apt-transport-https ca-certificates curl software-properties-common

# Thêm GPG key của Docker
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

# Thêm repository của Docker
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

# Cập nhật lại hệ thống để nhận repository mới
sudo apt update

# Cài đặt Docker
sudo apt install -y docker-ce docker-ce-cli containerd.io

sudo curl -L "https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

sudo chmod +x /usr/local/bin/docker-compose


# Kiểm tra phiên bản Docker đã cài đặt
sudo docker version



```




## II. CÀI ĐẶT TRÊN CENTOS 7.




