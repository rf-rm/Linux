
# Bài 8
## 1. Link
### 1.1 Hard link.
- cùng số inode với file gốc
- chỉ tạo link được từ một file
- chỉ tạo được link trong cùng phân vùng với file gốc.
- khi xóa file gốc thì hard link không bị ảnh hưởng
- các tạo hard link : **ln  <path/tên file> <tên hard link>**
### 1.2. Soft Link.
- khác số inode với file gốc.
- tạo được link với file, folder cùng hoặc khác phân vùng.
- khi xóa file, folder gốc thì soft link mất hiệu lực.
- các tạo soft link: **ln -s <path/tên file> <tên soft link>**
- Ví dụ : 
    - tạo soft link đến file cấu hình card mạng trên thư mục /root:
    ![](http://i.imgur.com/2VCkGzh.png)
## 2. Thêm card mạng mới.
- sau khi thêm card mạng mới (*ens37*), card ens37 sẽ báo đang kết nối:
![](http://i.imgur.com/VuxdD7J.png)
- Hiện chưa có file cấu hình cho card mạng này, ta tiến hành tạo file cấu hình:
`touch /etc/sysconfig/network-scripts/ifcfg-ens37`
- Để cấu hình ta sẽ sửa file cấu hình, lệnh
`vi /etc/sysconfig/network-scripts/ifcfg-ens37`
sửa file cấu hình như sau:
![](http://i.imgur.com/Rxprh0q.png)
lưu lại.
- Khởi động lại dịch vụ network để áp dụng cấu hình cho card ens37, lệnh:
`systemctl restart network`.
![](http://i.imgur.com/71QIhO8.png)
ok hihihi
## 3. Thêm ổ đĩa.
- B1 Thêm ổ cứng trên Vmware. Restart lại máy ảo.
- B2: dùng `fdisk -l` để kiểm tra ổ cứng và các phân vùng.
    - Ổ mới có đường dẫn: `/dev/sdb/`
![](http://i.imgur.com/rxOiVkF.png)
- B3: Sử dụng fdisk để phân vùng cho ổ cứng mới.
`fdisk /dev/sdb`
nhập **m** để xem hướng dẫn:
![](http://i.imgur.com/CSHYKgd.png)
- tạo 2 phân vùng 2GB và 8G:
 bấm n để tạo phân vùng mới
 ![](http://i.imgur.com/5evsT7p.png)
 `w` để lưu cấu hình phân vùng.
 - B4: Định dạng phân vùng vừa tạo:
 Định dạng /dev/sdb1 là swap, lệnh:
  ```
 mkswap /dev/sdb1/

 ```
 
 Định dạng /dev/sdb2 là ext4, lệnh: `mkfs.ext4 /dev/sdb2/`
 
 
