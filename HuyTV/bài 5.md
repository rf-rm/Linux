## 1. Các câu lệnh làm việc cơ bản trong Linux:
### 1.1 ls (List):
- lệnh `ls` để liệt kê nội dung file hoặc thư mục trong thư mục hiện hành. thường có các option
  - `-a` : xem tất cả các file và thư mục ẩn
  - `-l` : xem thông tin chi tiết bao gồm ACL (access control list), kích cỡ, ngày tháng cập nhật, chủ sở hữu,..
  - `-p` : thêm slash (`/`) để đánh dấu các thư mục
  - `-R` : xem cả cây thư mục
  ![alt](https://i.imgur.com/yCJTXsN.png)
### 1.2 mkdir (make directory)
- cú pháp `mkdir <tên thư mục mới>` để tạo một thư mục mới.
### 1.3 pwd (print working directory)
- `pwd` dùng để in ra đường dẫn đầy đủ đến thư mục hiện hành
### 1.4 cd (change directory)
- `cd <thư mục>` dùng để chuyển đến một thư mục cho phiên làm việc hiện tại.
### 1.5 rmdir (remove directory)
- `rmdir <thư mục>` để xóa một thư mục
### 1.6 rm (remove)
- `rm <tên file>` để xóa file, có thể dùng option `-r <tên thư mục>` để xóa thư mục và toàn bộ dữ liệu trong thư mục đó.
### 1.7 cp (copy)
- `cp <file nguồn> <file đích>` để sao chép file từ vị trí nguồn đến vị trí đích. có thể sử dụng option `-r` để sao chép thư mục.
### 1.8 mv (move)
- `mv <nguồn> <đích>` để di chuyển một file hoặc thư muc từ vị trí này sang vị trí khác. Lệnh này cũng dùng để đổi tên file hoặc thư mục nếu như `<nguồn>` và `<đích>` là cùng một thư mục.
### 1.9 cat (concatenate and print files)
- `cat <tên file>` để đọc và in nội dung của file ra màn hình.
### 1.10 less (print LESS)
- `less <tên file>` để in ra nội dung của một file theo từng trang trong trường hợp nội dung của file quá lớn và phải đọc theo trang. Bạn có thể dùng `Ctrl F` để chuyển trang tiếp và `Ctrl B` để chuyển về trang trước.
### 1.11 grep
- `grep <chuỗi> <tên file>` để tìm kiếm nội dung của file theo chuỗi cung cấp. Bạn có thể dùng `grep -i <chuỗi> <tên file>` để tìm kiếm không phân biệt hoa thường hoặc `grep -r <chuỗi> <tên thư mục>` để tìm kiếm trong toàn thư mục.
### 1.12 find
- `find <thư mục> -name <tên file>` để tìm kiếm file trong `<thư mục>` theo `<tên file>`.
- Cũng có thể dùng `find <thư mục> -iname <tên file>` để tìm kiếm không phân biệt hoa thường.
### 1.13 help
- `<câu lệnh> --help` để xem thông tin trợ giúp và các tùy chỉnh của câu lệnh.
### 1.14 whatis (what is the command)
- `whatis <tên câu lệnh>` để hiển thị mô tả về câu lệnh.
### 1.15 touch
- `touch <tên file.định dạng>` để tạo file kèm theo định dạng của nó.

## 2. Trình editor VIM
### 2.1 Giới thiệu và cài đặt :
- Vim là một trong những trình bien soạn dòng lệnh mạnh và phổ biến nhất. Nó chỉ sẵn có trên nền của Linux và Unix, nhưng sau đó cũng xuất hiện trên cả Windows.
- Giao diện của nó thì gọn gàng và đơn giản, và bạn có thể kết hợp các phím để thực hiện các công việc như copy-paste, tìm kiếm và thay thế, xóa một số dòng, và nhiều chức năng khác nữa.
- Ưu điểm của VIM là mọi thao tác đều có thể thực hiện thông qua các phím tắt, vì vậy bạn không cần dùng tới con chuột khi dùng VIM nữa.
- để cài đặt ta dùng lệnh `apt-get install vim`
### 2.2 Một số chức năng trong VIM
- Trong Vim chúng ta có thể edit nhiều file cùng 1 lúc bằng cách sử dụng buffers (bộ đệm) : 
  -  Chúng ta mở nhiều file để edit :
    
    ```
        vim test.sh test1.sh test2.sh
    
    ```
    - Chúng ta có thế xem buffers bằng cách : ( Insert Mode)
    
    ```
       :buffers
     1 %a   "test.sh"                      line 1
     2      "test1.sh"                     line 0
     3      "test2.sh"                     line 0
       Press ENTER or type command to continue
    
    ```
    
  - Để chuyển qua file edit tiếp theo trong buffers ta dùng :bn hoặc :b + tên file
    
    ```
    :bn Chuyển tới file edit tiếp theo trong buffers
    :b + tên file : chuyển tới file muốn edit
    
    ```
    
   - Dưới đây là một số câu lệnh để quản lí buffers:
      - : ls - Liệt kê tất cả các file giống lệnh :buffers
      - : bn - Chuyển sang file tiếp theo
      - : bp - Chuyển sang file trước đó
      - : bfirst - Chuyển tới file đầu tiên
      - : blast - Chuyển tới file cuối cùng
      - : bdelete - Xóa file hiện tại
      - : badd - Mở một file với tên file theo sau
      - : e - Chỉnh sửa một file trong một buffers mới và chuyển sang nó.
- Chúng ta có thể edit file dễ dàng hơn bằng cách sử dụng chắc năng windows song song trong vim

```
:sp: Chia 2 file thành 2 cửa sổ theo chiều ngang
:vs: Chia 2 file thành 2 cửa sổ theo chiều dọc 

```

   -  Note: Có thể đánh số trước :sp , :vs để chỉnh kích thước của cửa sổ mới

```
 ctrl-ww: Thay đổi trỏ chuột sang cửa sổ tiếp theo
 ctrl-wc: Đóng cửa sổ hiện tại
 ctrl-w +: Tăng kích thước của cửa sổ hiện tại
 ctrl-w-: Giảm kích thước cửa sổ hiện tại
 ctrl-w =: Đặt tất cả các cửa sổ bằng kích thước
 ctrl-wn: Mở một cửa sổ mới với một bộ đệm mới

```

   - Cũng giống như windows chúng ta có thể mở các tab trong vim một cách dễ dàng bằng cách dùng command

```
 :tabnew

```

- Một số câu lệnh quản lí tab thường dùng :

```
  :tabclose : Đóng tab hiện tại 
  :tabn or (gt) : chuyển tới tab kế tiếp
  :tabp or (gT): chuyển về tab trước
  :tabs: liệt kê các tab hiện có 
```
`
 - Một số lệnh chi tiết khi sử dụng VIM 
   +  Tìm kiếm một từ khóa : (trong normal mode)
   `/tên từ khóa `
   + Hoặc chúng ta có thể tìm kiếm và thay thế theo cách sau :
   `:%/host/testvim/gc`
      - Sau đó hệ thống sẻ hỏi chúng ta :
      `replace with testvim (y/n/a/q/l/^ E/^Y) ?`   `y -> done`
      - Sau khi hoàn tất các việc chỉnh sửa, ta có thể lưu lại hoặc thoát :
      ```
      :q - Thoát khỏi VIM
      :q! - Thoát không cần lưu
      :w - lưu file
      :w! - ghi đè file (bắt buộc)
      :wq - lưu file rồi thoát
      ```
