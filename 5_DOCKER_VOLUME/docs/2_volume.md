# GIỚI THIỆU VỀ VOLUME.

DOCKER HOÀN TOÀN QUẢN LÝ VOLUME.


## I. CÁCH LÀM VIỆC.

tức là mount ngược lại dữ liệu từ container sang máy host.


`docker container run -v +thưmụctrênmáyhost:thưmụcchứa data trên cpntainer +images`: tạo volume

trong đó:

- thư mục trên máy host: là thư mục chỉ định ta muốn lưu dữ liệu 

- thư mục chứa data trên container: là thư mục workdir khi khai báo trên dockerfile đó.

- LƯU Ý. TÊN VOLUME CÓ THỂ ĐƯỢC KHAI BÁO TRÊN DOCKER FILE LUÔN NHA.




