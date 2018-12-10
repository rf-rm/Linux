# Qúa trình boot
## 1. Power On

BIOS là một phần mềm được cài sẵn vào chip ROM nằm trên bo mạch chủ.

Khi nhấn nút khởi động nguồn, chương trình BIOS sẽ chạy đầu tiên. BIOS sẽ thực hiện một công việc gọi là POST nhằm kiểm tra phần cứng.
## 2. Master Boot Record (MBR)

Sector đầu tiên của một thiết bị lưu trữ được gọi là MBR.

BIOS sẽ đọc MRB của thiết bị này để nạp vào bộ nhớ một chương trình rất nhỏ. Chương trình nhỏ này sẽ định vị và khởi động boot loader – đây là chương trình chịu trách nhiệm cho việc tìm và nạp nhân (kernel) của hệ điều hành.

Đến giai đoạn này, máy tính sẽ không truy cập vào bất kì phương tiện lưu trữ nào. Các thông tin về ngày tháng, thời gian và các thiết bị ngoại vi quan trọng nhất được nạp từ CMOS.
## 3. Boot Loader

Boot loader sẽ nằm trong Master Boot Record (MBR). Khi khởi động Linux, boot loader có trách nhiệm nạp kernel và Initial RAM Disk (có chứa một số tệp quan trọng và trình điều khiển thiết bị cần thiết để khởi động hệ thống) vào bộ nhớ.

Bood loader bao gồm hai giai đoạn:

**Giai đoạn thứ nhất:**

Đổi với các hệ thống sử dụng BIOS/MBR, boot loader nằm tại sector đầu tiên của bộ nhớ hay còn gọi là Master Boot Record (MBR). Kích thước của MBR vào khoảng 512 bytes. Trong giai đoạn này boot loader kiểm tra các phân vùng để tìm ra phân vùng chứa hệ điều hành. Khi tìm thấy phân vùng khởi động, nó sẽ tìm một boot loader như là GRUB và tải nó vào RAM.

Đối với các hệ thống sử dụng EFI/UEFI, các firmware UEFI sẽ đọc dữ liệu Boot Manager để tìm các ứng dụng UEFI. Firmware sẽ chạy ứng dụng UEFI

**Giai đoạn thứ hai:**

Boot loader nằm trong thư mục /boot. Một màn hình hiển thị cho phép chúng ta chọn OS để khởi động. Sau đó boot loader sẽ nạp kernel của hệ điều hành đó vào bộ nhớ RAM và chuyển quyền điều khiển máy tính cho kernel này.

## 4. Linux kernel được nạp và khởi chạy


Boot loader sẽ nạp hạt nhân và các file system RAM vào bộ nhớ hệ thống để kernel có thể sử dụng trực tiếp. Khi hạt nhận được nạp vào bộ nhớ RAM, nó ngay lập tức khởi tạo và cấu hình bộ nhớ máy tính hoặc tất cả các phần cứng được gắn vào.

## 5. Inital RAM Disk

Các INITRD cung cấp một giải pháp: một tập các chương trình nhỏ sẽ được thực thi khi kernel vừa mới được khởi chạy. Các chương trình nhỏ này sẽ dò quét phần cứng của hệ thống và xác định xem kernel cần được hỗ trợ thêm những gì để có thể quản lý được các phần cứng đó. Chương trình INITRD có thể nạp thêm vào kernel các module bổ trợ. Khi chương trình INITRD kết thúc thì quá trình khởi động Linux sẽ tiếp diễn.

## 6. Các run level và service

init là tiến trình đầu tiên chạy trong hệ thống Linux: ID của tiến trình này là 1.

File cấu hình runlevel /etc/inittab

-   Runlevel 0: tắt hệ thống
-   Runlevel 1: chế độ đơn người sử dụng
-   Runlevel 2: chế độ multi user
-   Runlevel 3: chế độ đa người dùng không có giao diện đồ họa
-   Runlevel 4: không sử dụng
-   Runlevel 5: chế độ đa người dùng có giao diện đồ họa
-   Runlevel 6: reboot hệ thống
# Cấu hình ổ đĩa:
Trong mục other storage options có thể chọn auto configure hoặc i will configure. Nếu chọn auto => system sẽ tự phân vùng ổ đĩa còn khi chọn mục còn lại bạn sẽ phải tự phân vùng. Ở đây trong mục tự phân vùng sẽ chia ra làm 4 mục chính bao gồm : /,var,boot,swap. trong đó :
**/boot** – các tập tin cấu hình cho quá trình khởi động hệ thống (boot configuration files)
**/var** – thư mục này lưu lại tập tin ghi các số liệu biến đổi (variable files) như các tập tin dữ liệu và tập tin bản ghi (logs and databases). 
**swap **- đây còn gọi là ram ảo thường nên set nó = 1 hay 1,5 ram vật lý.
# Nơi lưu trữ các Package trong Centos:
CentOS là các bản phân phối liên quan chặt chẽ, là upstream và downstream (tương ứng) của Red Hat Enterprise Linux. Sự khác biệt của chúng xuất phát từ cách gói được chọn để đưa vào kho.  
  
Cả hai hệ thống sử dụng yum để tương tác với kho hệ thống và cài đặt phụ thuộc, và cũng bao gồm một công cụ cấp thấp hơn được gọi là rpm, cho phép bạn tương tác với từng gói.  
  
**Yellow Dog Updater, Modified (YUM)**  
Công cụ YUM được phát triển cho hệ thống Yellow Dog Linux như là một thay thế cho Yellow Dog Updater (yup). RedHat tìm thấy công cụ YUM là một bổ sung có giá trị cho hệ thống của họ. Ngày nay, YUM là gói mặc định và kho lưu trữ công cụ quản lý cho một số hệ điều hành.  
  
Bạn có thể sử dụng các lệnh sau để tương tác với YUM:  

-   **yum install package-name(s)**  - Cài đặt các gói cùng với bất kỳ phụ thuộc yêu cầu
-   **yum remove package-name(s)** - Loại bỏ các gói cụ thể từ hệ thống của bạn
-   **yum search search-pattern** - Tìm kiếm danh sách các tên gói và mô tả cho các gói phù hợp với mô hình tìm kiếm và cung cấp một danh sách các tên gói, với kiến trúc và mô tả ngắn gọn về các nội dung gói.
-   **yum deplist package-name(s)**  - Danh sách tất cả các thư viện và các module mà gói có tên phụ thuộc vào, cùng với tên của các gói (bao gồm cả các phiên bản) cung cấp phụ thuộc.
-   **yum check-update**  - làm mới bộ nhớ cache cục bộ của cơ sở dữ liệu yum vì vậy thông tin phụ thuộc và các gói mới nhất luôn được cập nhật.
-   **yum info package-name(s)**  - Kết quả của lệnh info cung cấp tên, mô tả của gói, cũng như liên kết tới trang chủ cho phần mềm, phiên bản phát hành và kích thước cài đặt của phần mềm.
-   **yum reinstall package-name(s)**  - Xóa và sau đó tải về một bản sao mới của tập tin gói và cài lại đặt các phần mềm trên hệ thống của bạn
-   **yum localinstall local-rpm-file** - Kiểm tra sự phụ thuộc của một file .rpm địa phương và sau đó cài đặt nó
-   **yum update optional-package-name(s)**  - Tải xuống và cài đặt tất cả các bản cập nhật bao gồm các bản vá lỗi, phiên bản bảo mật và nâng cấp, được cung cấp bởi các nhà phân phối của hệ thống điều hành của bạn.
-   **yum upgrade**  - Nâng cấp tất cả các gói được cài đặt trong hệ thống của bạn lên phiên bản mới nhất.
**Nơi lưu trữ**: -Mặc định khi dùng yum các package sẽ được lưu ở /home.
