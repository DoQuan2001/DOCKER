# DOCKER FILE.


## I. TỔNG QUAN.

![hinh ](../images/5_docker_file.png)

VÍ DỤ.

![hinh ](../images/6_docker_file.png)

## II. DOCKER FILE.

```

FROM # CHỈ RA IMAGES BASE ĐỂ BUILD RA IMAGES CẦN BUILD.

WORKDIR /app #chỉ ra thư mục làm việc chính của container


RUN  # chỉ ra câu lệnh để build môi trường chạy.

COPY . .

CMD  # các lệnh chạy chương trình sau khi container đã được tạo


```
TỨC RUN ĐỂ CÀI ĐẶT, CÒN CMD ĐỂ CHẠY NHA.

### 2.1. RUN


LÀ CÁI LỆNH CÀI ĐẶT NHA. VÍ DỤ CÂU LỆNH CÀI ĐẶT MYSQL TRÊN UBUNTU, CENTOS THẾ NÀO THÌ LỆNH RUN NÓ COPY LẠI RỒI THÊM CHỮ RUN VÀO TRƯỚC THÔI.

để cho đẹp họ thường gộp câu lệnh lại nha.

ví dụ: NÓ CŨNG TỰA TỰA NHAU CẢ THÔI.

lệnh cài nginx trên ubuntu:

```
sudo apt update
sudo apt install nginx

```

lệnh cài ngin trên RUN của dockerfile


```
RUN apt-get -y update && apt-get -y install nginx

```

### 2.2. CMD

CMD NÀY LÀ LỆNH KHỞI ĐÔNHJ CHƯƠNG TRÌNH NHA.  


`CMD ["executable","param1","param2"]`: CÚ PHÁP CMD

LƯU Ý, TA CŨNG CÓ THỂ COPY NGUYÊN CÂU LỆNH START CHƯƠNG TRÌNH CỦA CENTOS, UBUNTU NẾU HỆ ĐIỀU HÀNH TA ĐẶT Ở FROM LÀ UBUNTU, CETNOTS
trong đó:

- executable: Là tên của chương trình hoặc lệnh mà bạn muốn container thực thi.
- param1, param2: Là các tham số cho lệnh được chỉ định.


VÍ DỤ: 

lệnh khởi động nginx trên unbuntu;

```
sudo systemctl start nginx

```

lệnh khởi động nginx trên docker file.














