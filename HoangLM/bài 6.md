## Linux Architecture:
![Káº¿t quáº£ hÃ¬nh áº£nh cho Linux architecture](https://cumulusnetworks.com/blog/wp-content/uploads/Screen-Shot-2018-01-04-at-10.43.56-AM.png)
### OS:
OS(Operating System) là gì? Câu trả lời ngắn gọn là một hệ điều hành, là phần mềm mà bạn tải trên phần cứng của mình để làm cho nó hoạt động. Không có hệ điều hành, hầu hết phần cứng đều vô dụng. Ví dụ: bạn có thể có một máy tính Đéll chạy hệ điều hành Ubủntủn 16.04 mà bạn chạy các ứng dụng của mình. Bạn có thể có một chiếc iPhone chạy hệ điều hành Ios và có hẳn cả CỬA HÀNG CỜ HÁT PLAY . Bạn cũng có thể có MacBook của anh bạn hàng xóm Tung Của chạy macOS fake. Tóm quần què các hệ điều hành trên các nền tảng phần cứng này là những gì cho phép chúng chạy các ứng dụng, như được hiển thị ở hình trên.
### Kernel là cái què gì ? 
**What the fcuk is a kernel? and hmm what does it do?**
**Kernel** là phần đặc biệt của hệ điều hành kiểm soát phần cứng CPU, phân bổ bộ nhớ, truy cập dữ liệu, lên lịch xử lý, chạy các ứng dụng và bảo vệ chúng khỏi nhau. Đây là chương trình đầu tiên được tải trên máy tính khi máy tính khởi động. Các đoạn mã quan trọng nhất trong **Kernel** được tải vào các vùng bộ nhớ được bảo vệ để chúng có thể được ghi đè lên bởi các ứng dụng khác đang chạy trong hệ điều hành.
### Các thành phần bao gồm hệ điều hành Linux
Linux là một hệ điều hành nguồn mở có thể được cài đặt trên nhiều loại phần cứng khác nhau để cho phép bạn phát triển phần mềm, chạy các ứng dụng và hơn thế nữa. Trọng tâm của Linux là hạt nhân. Linux được phát triển bằng ngôn ngữ C và hợp ngữ(à sém bờ lý) để chạy trên máy tính cá nhân i386, nhưng nó đã được chuyển sang phần cứng nhiều hơn bất kỳ hệ điều hành nào khác trong lịch sử. Ngày nay, Linux là hệ điều hành được cài đặt nhiều nhất trên toàn cầu.**( cái này chắc báo xàm l @@).**
Linux thường được quản lý từ giao diện dòng lệnh (CLI), còn được gọi là shell. Bên cạnh kernel, quản lý các quy trình phần cứng và phần mềm, các bản phân phối Linux bao gồm một bộ phần mềm Linux, chẳng hạn như trình điều khiển thiết bị để truy cập và kiểm soát phần cứng, thư viện dùng chung, ứng dụng và trình nền hệ thống, chạy nền và đáp ứng các yêu cầu mạng. Đồ họa dưới đây cho thấy một ví dụ về phân phối Linux phổ biến có thể trông như thế nào. Nhiều ngôn ngữ lập trình có sẵn cho Linux, cũng như hơn 70.000 ứng dụng khác nhau. Các ứng dụng được cài đặt từ các gói chứa chính ứng dụng và siêu dữ liệu về ứng dụng.
![Linux architecture](https://cumulusnetworks.com/blog/wp-content/uploads/Screen-Shot-2018-01-04-at-10.44.23-AM.png)
## 2. Shell, Bash,Terminal,SH? 
### 2.1 
**Terminal ** nó là một chương trình phần mềm được cài đặt sẵn trên hệ điều hành Linux cho phép người dùng có thể giao tiếp với máy tính thông qua việc chạy các câu lệnh. Chính vì vậy **Terminal** còn được gọi là một chương trình giao diện cửa sổ dòng lệnh (command line interface).
### 2.2 
**Shell** là chương trình (phần mềm) phát triển dành cho các máy tính chạy hệ điều hành Unix và Linux. Shell cung cấp giao diện cho phép người dùng nhập và chạy các câu lệnh dưới (dạng văn bản) trên máy tính.
Trên các máy tính Mac OS X hay Ubuntu thì chương trình Shell có tên là Terminal. Hoặc khi bạn tạo kết nối SSH tới máy chủ thì bạn cũng đang sử dụng chương trình Shell trên remote server (thường gọi là Console).
### 2.3 
## Bash và SH

**Bash** và **SH** là  _hai ngôn ngữ máy tính_  dùng để biên dịch câu lệnh được nhập trên Shell để máy tính có thể hiểu được.

**SH**  là ngôn ngữ được ra đời đầu tiên dùng cho các chương trình Shell. Sau đó tới lượt  **Bash**  (GNU Bourne-Again SHell) với một số cái tiến hơn so với  **SH**.
#### Tổng kết :
-   **Shell**: Là chương trình phần mềm chạy trên hệ điều hành Unix và Linux.
-   **Bash** và **SH**: Là ngôn ngữ sử dụng bởi Shell để biên dịch câu lệnh người dùng nhập vào sử dụng Terminal (trên máy tính local) hoặc Console (trên remote server).
## 3. Biến  môi trường
### 3.1 Khái niệm :
-Khi làm việc trên máy tính chúng ta cần những thông tin như tên phiên bản hệ điều hành (HĐH) đang chạy, tên thư mục home, thư mục chứa lệnh chương trình …

-Một khái niệm quan trọng trên linux đó là môi trường (_environment_) được định nghĩa qua các biến môi trường. Một số biến được đặt bởi hệ thống, số khác do bạn đặt, hoặc set bởi shell (các lệnh) hay một chương trình nào đó được load.

-Một biến môi trường có tên là một dãy chữ cái và nhận một giá trị nhất định, giá trị này có thể là số, chữ, tên file, thiết bị (_device_) hay một kiểu dữ liệu nào đó.
**Trên Linux**: Bạn có thể set và get ra biến môi trường như sau:

1			`$TEST=”Linux programming”`
2			`$``echo` `$TEST`
3			`Linux programming`
### 3.2 Các biến môi trường quan trọng và cách cài đặt
-Tiếp theo mình trình bày một số khái niệm liên quan đến biến môi trường, ý nghĩa các biến môi trường hay dùng và cách cài đặt chúng.

-Shell  là phần giao diện dịch các lệnh của người dùng gõ vào thành các lệnh cho nhân hệ điều hành thực thi rồi trả lại kết quả. Trong bài đầu về Linux mình có mô tả về shell như là lớp trên của hạt nhân. Khi login vào hệ thống shell sẽ thực thi việc khởi tạo các biến môi trường. Việc này thường là đọc các file cấu hình như sau:
1			`/etc/environment`		`→ lưu các biến môi` `tr``ường mức hệ thống.`
2			`~/.profile`
3			`~/.bashrc hay ~/.bash_profile`
→ lưu các biến môi trường cho người dùng đang login, các file này nằm trong mục home của bạn. Khi đọc file .profile hay .bashrc … hệ thống có thể sẽ load tiếp các file khác được định nghĩa trong đó.

-Các file trên là ví dụ shell bash trên Ubuntu. Cũng tùy loại shell và phiên bản Linux. Và trên CentOS thì các file khởi tạo biến môi trường là  `/etc/profile`, các file trong mục  `/etc/profile.d/`  …  
Muốn xem shell nào được load khi các bạn login thì truy cập file  `/etc/passwd`.
-File  `/etc/environment`  lưu các biến toàn cục (global) quy định:
-   Loại shell bạn sử dụng
-   Các thư mục chứa lệnh commands và các biến quy định cách sử dụng, giao diện cửa sổ lệnh (terminal). Shell có thể là bash, sh hay ksh.
#### Biến $PATH

Biến  `PATH`cho thấy đường dẫn tới các thư mục chứa câu lệnh (_chương trình_) để chạy khi bạn gõ trên terminal, các mục cách nhau dấu “:” ví dụ /usr/local/sbin; /usr/local/bin...

Ví dụ khi bạn cài phần mềm ffmpeg (_thư viện chuyên chỉnh sửa video, audio …_), hay khi các bạn cài phần mềm imagemagick trên Linux thì các chương trình của ffmpeg, imagemagick sẽ được lưu ở mục  `/usr/local/bin`  hoặc là ở  `/sbin`  …

Với biến  `PATH`  như trên thì bạn không cần biết ffmpeg, imagick cài ở đâu, mỗi khi bạn gõ lệnh ffmpeg hay convert (của imagick) trên terminal thì hệ thống tự biết tìm đến mục chứa nó để chạy.
1   `$TEST=”Linux programming”`
2   `$``echo` `$TEST`
3   `Linux programming`
## 4,Tập tin : /etc/profile, /etc/bashrc, ~/.bashrc, ~/ .bash_profile là ?
~ / .bashrc, ~ / .bash_profile, ~ / .profile, / etc / profile, /etc/bash.bashrc và mục đích của nólà gì?  Một số trích đoạn thú vị từ trang bash: Khi bash được gọi dưới dạng shell đăng nhập tương tác hoặc dưới dạng shell không tương tác với tùy chọn --login, trước tiên, nó sẽ đọc và thực thi các lệnh từ tệp / etc / profile, nếu tệp đó tồn tại . Sau khi đọc tệp đó, nó tìm ~ / .bash_profile, ~ / .bash_login và ~ / .profile, theo thứ tự đó, đọc và thực thi các lệnh từ lệnh đầu tiên tồn tại và có thể đọc được. Tùy chọn --noprofile có thể được sử dụng khi shell được bắt đầu để ức chế hành vi này. Khi một vỏ tương tác không phải là vỏ đăng nhập được khởi động, bash sẽ đọc và ```Thực thi các lệnh từ /etc/bash.bashrc và ~ / .bashrc, nếu các tệp này tồn tại. Điều này có thể bị ức chế bằng cách sử dụng tùy chọn --norc. Tùy chọn tệp --rcfile sẽ buộc bash đọc và thực thi các lệnh từ tệp thay vì /etc/bash.bashrc và ~ / .bashrc. Shell đăng nhập có nghĩa là một phiên mà bạn đăng nhập vào hệ thống và trực tiếp kết thúc bằng `Bash, như một phiên ssh từ xa hoặc đăng nhập thông qua một thiết bị đầu cuối văn bản phi đồ họa. Shell không đăng nhập là loại shell bạn mở sau khi đăng nhập: thường là trong phiên đồ họa khi bạn mở cửa sổ terminal mới. Tôi nghĩ mọi thứ sẽ hoạt động như thế nào (đối với một thiết lập điển hình): .profile dành cho những thứ không liên quan cụ thể đến Bash, như biến môi trường PATH và bạn bè, và nên có sẵn bất cứ lúc nào. Ví dụ: .profile cũng nên được tải khi bắt đầu phiên máy tính để bàn đồ họa. .bashrc dành cho việc định cấu hình sử dụng Bash tương tác, như bí danh Bash, đặt trình soạn thảo yêu thích của bạn, đặt dấu nhắc Bash, v.v. Ví dụ: .bash_profile có thể là một cái gì đó đơn giản như. ~ / .profile. ~ / .bashrc Như đã nêu trong đoạn trang man ở trên, nếu bạn bỏ qua .bash_profile, chỉ .profile sẽ được tải.
# 5 Hóng cao nhân giúp :@
