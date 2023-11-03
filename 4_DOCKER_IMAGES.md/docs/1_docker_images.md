# DOCKER IMAGES.

## I. GIỚI THIỆU.

- là file app binary + các dependencies( các trương trình con, thư viện...)



![hinh ](../images/1_images.png)

![hinh](../images/2_images.png)

## II. LÀM THẾ NÀO ĐỂ CÓ IMAGES.

- tải trực tiếp images từ docker hub.

- Dùng docker file.

### 2.1. TẢI IMAGES TỪ DOCKER HUB.

`docker images pull +tênimages`: lệnh tải images về.

### 2.1.1. DOCKER_IMAGES_TAG

Là tên images+version.

![hinh](../images/4_tag.png)


![hinh ](../images/3_find_docker_images_docker_hub.png)

### 2.2. DÙNG DOCKER FILE.

Là file chứa các chỉ dẫn cho dockerd.


VÍ DỤ.

![hinh ](../images/6_docker_file.png)

### 2.2.2. BUILD CONTEXT.

![hinh ](../images/9_build_context.png)




## III. CẤU TRÚC DOCKER IMGAES.

Images được tạo bởi 1 chuỗi layer (các layer chỉ read-only)

Mỗi layer chính là 1 sự thay đổi trên filesystem.

các layer xếp chồng lên nhau từ dưới lên trên. bên trên sẽ kế thừa bên dưới. chính vì sự đặc biệt này, có 1 kỹ thuật là kỹ thuật caching layer để tối ưu hóa docker file

![hinh ](../images/7_layer.png)

VÍ DỤ;

![hinh ](../images/8_layer.png)
### 3.1. CACHING LAYER.

là kỹ thuật dùng để tối ưu hóa docker file.

### 3.2. BASE IMGES.















