# CentOS và lincense trong Linux.
## 1.Tìm hiểu về Red Hat Enterprise Linux.
### 1.1.Red Hat Enterprise Linux là gì?
- Red Hat Enterprise Linux (RHEL) là một bản phân phối Linux được phát triển bởi Red Hat và mục tiêu hướng tới thị trường thương mại.
- Red Hat Enterprise Linux thường được viết tắt là RHEL, tuy nhiên điều này không phải là chính thức.
- Phiên bản đầu tiên của Red Hat Enterprise Linux phân phối ra thị trường được mang tên "Red Hat Linux Advanced Server". Năm 2003 Red Hat đổi thương hiệu Red Hat Linux Advanced Server thành "Red Hat Enterprise Linux AS", và bổ sung thêm hai biến thể, Red Hat Enterprise Linux ES và Red Hat Enterprise Linux WS.
- Red Hat sử dụng các quy định rất nghiêm ngặt về thương hiệu để hạn chế các bản rebuild của Red Hat Enterprise Linux chính thức. Tuy nhiên, Red Hat lại cung cấp mã nguồn mở của các bản phân phối phần mềm, giấy phép pote about Fedora Cohát hành miễn phí, kết quả là nhiều nhà phân phối đã tạo ra thương hiệu, cộng đồng hỗ trợ tái xây dựng lại RHEL có hiệu lực pháp lý mà không có sự hỗ trợ chính thức của Red Hat
### 1.2. Biến thể.
Cũng có những phiên bản "đào tạo" của các phiên bản máy tính để bàn và máy chủ. Chúng được cung cấp cho các trường học và sinh viên, ít tốn kém, và được cung cấp cùng các hỗ trợ công nghệ từ Red Hat như một tùy chọn mở rộng. Hỗ trợ web dựa trên số lượng khách hàng địa chỉ liên lạc có thể được mua riêng.

Người ta thường cho xây dựng thương hiệu ES và AS tương ứng với "Entry-level Server" và "Advanced Server". Lý do cho điều này là rằng các sản phẩm ES là sản phẩm cơ bản cho các máy chủ của doanh nghiệp, trong khi AS là sản phẩm tiên tiến hơn. Tuy nhiên, không có nơi nào trên trang web hoặc các tài liệu của Red Hat có nói về AS, ES và WS.

Trong Red Hat Enterprise Linux 5 có thêm phiên bản mới bên cạnh các phiên bản cũ Red Hat Enterprise Linux AS/ES/WS/Desktop:
-   Red Hat Enterprise Linux Advanced Platform (bản AS cũ)
-   Red Hat Enterprise Linux (former ES) (giới hạn 2 CPU)
-   Red Hat Enterprise Linux Desktop with Workstation và tùy chọn Multi-OS
-   Red Hat Enterprise Linux Desktop with tùy chọn Workstation (WS cũ)
-   Red Hat Enterprise Linux Desktop with Multi-OS option
-   Red Hat Enterprise Linux Desktop (Desktop cũ)

Red Hat cũng công bố phiên bản Red Hat Global Desktop Linux "cho  thị trường mới nổi

RHEL 4, 3,và bản phát hành trước đó có bốn biến thể:

-   Red Hat Enterprise Linux AS for mission-critical/enterprise  computer system
-   Red Hat Enterprise Linux ES cho các máy chủ mạng hỗ trợ
-   Red Hat Enterprise Linux WS cho máy tính để bàn doanh nghiệp sử dụng sức mạnh kỹ thuật cho điện toán hiệu năng cao
-   Red Hat Desktop cho các triển khai nhiều đơn người dùng máy tính để bàn cho doanh nghiệp
### 1.3.Mối quan hệ với Fedora.
- Ban đầu thì Red Hat tính phí khi hỗ trợ cho các phiên bản Red Hat Linux. Từ bản RHEL 2.1 AS vào năm 2002, Red Hat đã bán bản đầu tiên của RHEL. Sau này Red Hat đã phân phối Fedora - được coi như một bản sao của RHEL nhưng miễn phí và hỗ trợ trực tiếp từ Red Hat.
- Lịch phát hành của Fedora là 6 tháng một lần, của RHEL là 2 năm một lần. Fedora như một upstream của phiên bản RHEL tương lai. Fedora được dùng như một bản thử nghiệm các tính năng mới để sau đó mới phát hành ra một bản RHEL ổn định.
## 2.Tìm hiểu lincense trong Linux


## 3.CentOS

### 3.1.CentOS là gì? 
- `CentOS` là viết tắt của `Community Enterprise Operating System`, được phát hành vào tháng 5 năm 2004, là một hệ điều hành miễn phí 100% dựa trên hạt nhân Linux. Nó có nguồn gốc hoàn toàn từ bản phân phối Red Hat Enterprise Linux (RHEL). CentOS tồn tại để cung cấp nền tảng hệ điều hành máy tính cho doanh nghiệp miễn phí và cố gắng duy trì khả năng tương thích nhị phân 100% với nguồn gốc của nó, Red Hat.
### 3.2.Một số thông tin cơ bản về CentOS 
| || 
|------------------|----------------------|
|Trang chủ:|  `https://www.centos.org/ `|
|Nhà phát triển:| `The CentOS Project `|
|Họ HĐH:| `Tương tự Unix (dựa trên RHEL)` |
|Kiểu mã nguồn:| `Phần mềm tự do mã nguồn mở` |
|Hình thức nâng cấp:| ` Yum (PackageKit)`| 
|Quản lý gói cài đặt: |`RPM Package Manager Nền tảng hỗ trợ: i386, x86-64, PowerPC, s390,s390x `|
|Kiểu nhân:| `Monolithic (Linux) `|
|Giao diện người dùng:|` GNOME và KDE (người dùng tự chọn)` |
|Giấy phép: |`GNU GPL & various others.`|
### 3.3.Lịch sử hình thành CentOS
 - Vào tháng 6 năm 2006, David Parsley, nhà phát triển chính của hệ điều hành `“Tao Linux”` (một bản sao của hệ điều hành RHEL), đã tuyên bố nghỉ hưu với dự án “Tao Linux” và sự phát triển `CentOS` (phát triển đồng thời cùng thời điểm đó). Toàn bộ người sử dụng hệ điều hành “Tao Linux” đã chuyển đổi hệ điều hành sang phiên bản CentOS thông qua cập nhật chương trình cập nhật `“yum“`. 
 - Vào tháng 7 năm 2009, một bức thư ngỏ trên trang web của dự án CentOS đã thông báo rằng người sáng lập CentOS, `Lance Davis`, đã mất tích trong năm 2008. Davis đã ngừng đóng góp cho dự án nhưng vẫn giữ đăng ký cho miền CentOS và tài khoản PayPal. Vào tháng 8 năm 2009, nhóm CentOS đã liên lạc với Davis thành công và nhận lại được tên miền `centos.info` và `centos.org`. 
 - Vào tháng 7 năm 2010, CentOS đã vượt qua hệ điều hành Debian để trở thành bản phân phối Linux phổ biến nhất cho các `máy chủ server` như web server, với thị phần gần `30% của tất cả các máy chủ web Linux` đang hoạt động trên thế giới lúc bấy giờ. Nhưng đến tháng 1/2012, thì thị phần đứng đầu đã quay trở lại với gã khổng lồ “Debian“.
 - Vào tháng 1 năm 2014, `Red Hat` tuyên bố sẽ tài trợ cho dự án CentOS với mục tiêu thiết lập một nền tảng phù hợp với nhu cầu của các nhà phát triển mã nguồn mở tích hợp công nghệ vào hệ điều hành. Theo kết quả của những thay đổi này, `quyền sở hữu nhãn hiệu CentOS` đã được chuyển sang `Red Hat`. RedHat hiện vẫn đang tuyển dụng hầu hết các lập trình viên cho dự án phát triển CentOS. Tuy nhiên, nhóm lập trình viên này hoạt động như một phần của nhóm mã nguồn mở và tiêu chuẩn của Red Hat, hoạt động tách biệt với đội ngũ Red Hat Enterprise Linux. Một hội đồng quản trị CentOS mới cũng đã được thành lập.
### 3.4.Các phiên bản của CentOS
 - Số phiên bản của CentOS có hai phần, `một phiên bản chính` và `một phiên bản nhỏ`, tương ứng với phiên bản chính và cập nhật của Red Hat Enterprise Linux được sử dụng để xây dựng là phiên bản của CentOS. Ví dụ, CentOS 4.4 được xây dựng từ các gói nguồn từ Red Hat Enterprise Linux 4 cập nhật 4. Từ giữa 2006, bắt đầu với phiên bản 4.4 (chính thức được gọi là Red Hat Enterprise Linux 4.0 cập nhật 4), Red Hat đã thông qua một quy ước phiên bản giống hệt của CentOS, ví dụ như, Red Hat Enterprise Linux 4.5.
 - Bắt đầu với phiên bản 7.0 trở đi, các số phiên bản CentOS sẽ bao gồm thêm một phần số cho biết tháng năm của mã nguồn hệ điều hành CentOS phát hành. Ví dụ phiên bản 7.0-1406, cho biết bản cập nhật thứ 0 đầu tiên của CentOS 7, trong khi “1406” chỉ ra rằng bản phát hành này từ tháng 6 năm 2014.  
 - Tính tới thời điểm viết bài này thì hiện tại Hệ Điều Hành CentOS đã phát hành `5 phiên bản` CentOS (từ CentOS 3 -> CentOS 7). Dưới đây là bảng thông tin phát hành các phiên bản CentOS.
     ![](http://i.imgur.com/JomXbKJ.png)

## 4. Cài CentOS trên Vmware 14
### 4.1. Tạo môi trường trên Vmware để cài đặt Centos.
- Mở Vmware , Chọn `File`-->`New Virtual Machine...`
- Chọn kiểu config là Typical và chọn `Next`:
![](http://i.imgur.com/6pMBuXJ.png)
- Chọn cài đặt bằng file ISO --> browse đến file iso của CentOS -- Next
![](http://i.imgur.com/CbeYAlS.png)
- Chọn hệ điều hành là Linux, Version là Centos 7 --> Next 
![](http://i.imgur.com/8iwoThz.png)
- Đặt tên và chọn vị trí lưu máy ảo--> Next
![](http://i.imgur.com/NVcZURX.png)
- Cấu hình dung lượng ổ đĩa cho máy ảo -->Next 
![](http://i.imgur.com/bK8ULTE.png)
- Thay đổi cấu hình máy ảo--> tích chọn tự khởi động sau khi tạo--> chọn Finish để hoàn tất quá trình tạo máy ảo.
![](http://i.imgur.com/sqN4HRr.png)
### 4.2. Cài đặt CentOS.
- Khi máy ảo khởi động, chọn install CentOS 7 --> Enter
![](http://i.imgur.com/g1lqQMt.png)
- Giao diện cài đặt centos 7 hiện lên, để ngôn ngữ và bàn phím mặc định và chọn Continue
![](http://i.imgur.com/UaNZ5xz.png)
- Chon Installation Destination, chọn ổ đĩa để cài CentOS --> Done,
![](http://i.imgur.com/78U9cF9.png)
![](http://i.imgur.com/ukmS0OK.png)
- Chọn `Begin Installation`  để bắt đầu quá trình cài đặt.
![](http://i.imgur.com/MkLeIn1.png)
- Chọn `Root Password ` để cài đặt mật khẩu cho tài khoản root.
![](http://i.imgur.com/catEHCJ.png)
- Nhập mật khẩu và chọn Done,
![](http://i.imgur.com/fYzA7QR.png)
- Khi cài đặt xong sẽ có yêu cầu reboot lại, chọn Reboot để khởi động lại.
![](http://i.imgur.com/477WWkc.pngrô)
- Sau khi khởi động lại --> nhập tài khoản đăng nhập là `root` --> Enter --> Nhập password vừa đặt . 
Hoàn tất quá trình cài đặt CentOS.
![](http://i.imgur.com/uIu7ZqI.png)
### 4.3.Tạo Snapshot
- Chọn `Vm`-->`Snapshot`-->`Take Snapshot...`  hoặc chọn biểu tượng Take Snapshot trên thanh công cụ -> nhập tên begin và chọn `ok` để tạo snapshot. ![](http://i.imgur.com/mnMJc2h.png)



mệt vl
nguồn: https://cuongquach.com/he-dieu-hanh-centos-la-gi.html
            wikipedia
