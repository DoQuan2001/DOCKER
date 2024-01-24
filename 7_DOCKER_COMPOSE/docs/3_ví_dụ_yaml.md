# VÍ DỤ FILE YAML


```
version: "3.8"

service: # NOI DINH NGHIA CAC CONTAINER.
    service name1: # ten cua container 1.
        image: # chỉ ra tên images or dockerfile để build
        build:
            context:
            dockerfile:
        restart: always

        ports: # chỉ ra port của máy host và port của contaier
        environment: # định nghia các biến ví dụ tài khoản, mật khẩu
        
        volumes:
            - type: volume
            source: nginx-data
            target: /usr/share/nginx/html

volumes:
    nginx-data:


```