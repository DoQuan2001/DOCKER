# PERSISTENT DATA.

## I. PERSISTENT DATA LÀ GÌ?

Khi tạo, thay thế container hay contianer bị đột tử thì dữ liệu sẽ bị mất.

=> cần tạo ra 1 không gian tách biệt với container để lưu trữ data ra khỏi container.

CÁCH TẠO PERSISTIENT DATA: 

- DÙNG BINDMOUNT.
- DÙNG VOLUME.

![hinh ](../images/4_persitent_data.png)


## II. BIND MOUND.

### 2.1. KHÁI NIỆM.

Là tạo ra kết nối giữa thư mục trong container và thư mục trên host

Là kỹ thuật dựa trên kỹ thuật mounting: khi gắn 1 máy A vào filesystem của máy B thì máy B có thể nhìn thấy data của máy A.

Là tạo ra kết nối giữa thư mục trong container và thư mục trên host


VÍ DỤ:

![hinh ](../images/2_bindmount.png)

### 2.2. CÁCH TẠO BIND MOUNT.


` docker container run -v +thưmụctrênmáyhost:thưmụctrêncontainer +images`: mounte data từ thư mục trên máy host vào thư mnục trên conatiner. 

`docker container --name +têncontainer -`

![hinh ](../images/1_bindmount.png).

## III. VOLUME.

### 3.1. KHÁI NIỆM

Mục đích thì giônngs với bindmoubt. tuy nhiên, docker hoàn toàn quản lý volume(khác với bindmount thì dữ liệu nằm trên máy host và do mình quản lý)

Cách làm: mount ngược lại thư mục từ container về máy host.

![hinh ](../images/5_volume.png)



### 3.2. CÁCH TẠO VOLUME.

`docker container run -v +TÊNCỦAVOLUME: thưmụctrêncontaienercần mounte + images`: tạo volume

![hinh ](../images/6_volume.png)









