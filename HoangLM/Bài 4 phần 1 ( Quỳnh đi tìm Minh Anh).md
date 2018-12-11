## 1.Cấu trúc cây thư mục

-   /Root:root là nơi bắt đầu của tất cả các file và thư mục. Chỉ có root user mới có quyền ghi trong thư mục này. Chú ý rằng /root là thư mục home của root user chứ không phải là /.
-   /bin : Thư mục này chứa các chương trình thực thi. Các chương trình chung của Linux được sử dụng bởi tất cả người dùng được lưu ở đây. Ví dụ như: ps, ls, ping...
-   /sbin :/sbinn là nơi chứa các chương trình thực thi, nhưng chúng là những chương trình của admin, dành cho việc bảo trì hệ thống. Ví dụ như:fdisk, iptables...
-   /etc : Thư mục này chứa các file cấu hình của các chương trình, đồng thời nó còn chứa các shell script dùng để khởi động hoặc tắt các chương trình khác. Ví dụ: /etc/resolv.conf,and more
-   /dev: Các phân vùng ổ cứng, thiết bị ngoại vi như USB, ổ đĩa cắm ngoài, hay bất cứ thiết bị nào gắn kèm vào hệ thống đều được lưu ở đây. Ví dụ: /dev/sdb1 là tên của USB bạn vừa cắm vào máy, để mở được USB này bạn cần sử dụng lệnh mount với quyền root: # mount /dev/sdb1 /tmp
-   /tmp : Thư mục này chứa các file tạm thời được tạo bởi hệ thống và các người dùng. Các file lưu trong thư mục này sẽ bị xóa khi hệ thống khởi động lại.
-   /proc (Thông tin về các tiến trình): Thông tin về các tiến trình đang chạy sẽ được lưu trong /proc dưới dạng một hệ thống file thư mục mô phỏng. Ví dụ thư mục con /proc/{pid} chứa các thông tin về tiến trình có ID là pid (pid ~ process ID). Ngoài ra đây cũng là nơi lưu thông tin về về các tài nguyên đang sử dụng của hệ thống như: /proc/version, /proc/uptime...
-   /var (File về biến của chương trình): Thông tin về các biến của hệ thống được lưu trong thư mục này. Như thông tin về log file: /var/log, các gói và cơ sở dữ liệu /var/lib...
-   /usr (Chương trình của người dùng): Chứa các thư viện, file thực thi, tài liệu hướng dẫn và mã nguồn cho chương trình chạy ở level 2 của hệ thống. Trong đó
    -   /usr/bin chứa các file thực thi của người dùng như: at, awk, cc, less... Nếu bạn không tìm thấy chúng trong /bin hãy tìm trong /usr/bin
    -   /usr/sbin chứa các file thực thi của hệ thống dưới quyền của admin như: atd, cron, sshd... Nếu bạn không tìm thấy chúng trong /sbin thì hãy tìm trong thư mục này.
    -   /usr/lib chứa các thư viện cho các chương trình trong /usr/bin và /usr/sbin
    -   /usr/local chứa các chương tình của người dùng được cài từ mã nguồn. Ví dụ như bạn cài apache từ mã nguồn, nó sẽ được lưu dưới /usr/local/apache2
-   /home : Thư mục này chứa tất cả các file cá nhân của từng người dùng. Ví dụ: /home/john, /home/marie
-   /boot : Tất cả các file yêu cầu khi khởi động như initrd, vmlinux. grub được lưu tại đây. Ví dụ vmlixuz-2.6.32-24-generic
-   /lib: Chứa cá thư viện hỗ trợ cho các file thực thi trong /bin và /sbin. Các thư viện này thường có tên bắt đầu bằng ld* hoặc lib*.so.*. Ví dụ như ld-2.11.1.so hay libncurses.so.5.7
-   /opt: Tên thư mục này nghĩa là optional (tùy chọn), nó chứa các ứng dụng thêm vào từ các nhà cung cấp độc lập khác. Các ứng dụng này có thể được cài ở /opt hoặc một thư mục con của /opt
-   /mnt: Đây là thư mục tạm để mount các file hệ thống. Ví dụ như # mount /dev/sda2 /mnt
-   /media: Thư mục tạm này chứa các thiết bị như CdRom /media/cdrom. floppy /media/floopy hay các phân vùng đĩa cứng /media/Data (hiểu như là ổ D:/Data trong Windows)
-   /srv ): Chứa dữ liệu liên quan đến các dịch vụ máy chủ như /srv/svs, chứa các dữ liệu liên quan đến CVS.

## 2.SeLinux

-   SELinux là một từ viết tắt của Security-enhanced Linux (Linux tăng cường bảo mật). Nó là một tính năng bảo mật của Linux kernel, được thiết kế để bảo vệ máy chủ chống lại cấu hình sai và/hoặc các compromised daemons. Nó đặt các giới hạn và chỉ thị cho server và các chương trình: những file nào user có thể truy cập và những hành động nào user có thể thực hiện bằng cách đưa ra một chính sách bảo mật.
-   SELinux là một thực thi của cơ chế bảo mật MAC. Nó được xây dựng trong Linux kernel và được kích hoạt mặc định trên Fedora, CentOS, RHEL và một vài bản phân phối Linux khác. SELinux cho phép quản trị viên máy chủ xác định các quyền khác nhau cho tất cả quy trình. Nó xác định cách tất cả các tiến trình có thể tương tác với các phần khác của máy chủ.
-   SELinux đặt các hạn chế đối với từng đối tượng trên theo chính sách. Ví dụ, một người dùng apache với sự cho phép đầy đủ chỉ có thể truy cập thư mục /var/www/html, nhưng không thể chạm vào các phần khác của hệ thống như thư mục /etc. Nếu có thể chiếm quyền truy cập vào sendmail mail hoặc bind dns hoặc apache web server, thì kẻ tấn công này cũng chỉ có quyền truy cập vào máy chủ bị khai thác đó và các tệp trong máy chủ này. Kẻ tấn công không thể truy cập vào các phần khác của hệ thống hoặc mạng nội bộ. Nói cách khác, thiệt hại sẽ được hạn chế đối trong phạm vi máy chủ và các files cụ thể. Các cracker cài cắm được shell lên trên máy chủ của bạn thông qua daemon phổ biến như Apache/BIND/Sendmail khi SELinux cung cấp các tính năng bảo mật sau đây:
    -   Bảo vệ dữ liệu của người dùng khỏi bị truy cập trái phép.
    -   Bảo vệ ports/ sockets/ files khỏi truy cập trái phép.
    -   Bảo vệ máy chủ chống lại việc khai thác.
    -   Tránh leo thang đặc quyền.
-   Việc bảo mật trên Linux là rất cần thiết, tuy nhiên có những trường hợp nó lại gây ra sự phiền phức khi bạn muốn cài một phần mềm mà phần mềm đó lại cần can thiệp sâu vào hệ thống Linux và người dùng thông thường không cần sự rườm rà sẽ tốn rất nhiều thời gian để tìm hiểu và xử lý vấn đề, gián đoạn các dịch vụ khác.
