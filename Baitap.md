

## Giải bài tập

## 1. Cấu hình cho card mạng mới

- Kiểm tra card vừa mới được thêm vào - Ví dụ card ens224
![](https://i.imgur.com/BSyPRby.png)

- Khởi tạo tập tin cấu hình cho device enss224 trong `/etc/syconfig/network-scripts`
- Đây là các tùy chọn tối thiểu để cấu hình IP static , có thể cấu hình nhiều tùy chọn thêm
```
DEVICE=ens224
NAME=ens224
TYPE=Ethernet
IPADDR=192.168.69.131
PREFIX=24
GATEWAY=192.168.69.1
ONBOOT=yes
BOOTPROTO=static
```

- Sau đó restart dịch vụ 
```bash
systemctl restart network
```


