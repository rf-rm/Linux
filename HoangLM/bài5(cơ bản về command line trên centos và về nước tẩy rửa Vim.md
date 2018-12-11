# Cơ bản làm việc với Linux

### 1.1.Các lệnh điều hướng và thăm dò

### Xác định vị trí với  _pwd_

Lệnh  `pwd`  ( print working directory) sẽ in ra vị trí làm việc hiện tại. để sử dụng lệnh này chỉ cần gõ :`pwd` .
![Káº¿t quáº£ hÃ¬nh áº£nh cho pwd ubuntu](http://goctinhoc.top/wp-content/uploads/2016/07/ubuntu-pwd.jpg)
### Xác định các thư mục và file với  _ls_

`ls`  là một trong các câu lệnh được dùng phổ biến nhất và dùng để liệt kê các tập tin và thư mục trên Linux.  )  Có thể dùng  `ls`  để liệt kê ở thư mục hiện tại hoặc dùng  `ls <đường dẫn thư mục>`  để liệt kê file, thư mục trong thư mục sau  **ls**  trong câu lệnh. Lệnh  `ls`  có thể có các tùy chọn sau:![Káº¿t quáº£ hÃ¬nh áº£nh cho ls ubuntu](https://i.stack.imgur.com/Npv5b.png)

-   `-a`: xem cả các file và thư mục ẩn
-   `-p`: thêm slash (`/`) để đánh dấu các thư mục
-   `-R`: xem cả cây thư mục

### Chuyển thư mục với  _cd_

Lệnh  `cd`- Change Directory, đúng như cái tên, lệnh này được dùng để chuyển thư mục làm việc.  [1.2 Xem nội dung của file
![Káº¿t quáº£ hÃ¬nh áº£nh cho cd ubuntu](https://i.ytimg.com/vi/8l52Pc3DUZ8/hqdefault.jpg)
### Hiển thị nội dung toàn bộ file với  _cat_

 `cat [filename]`, và sau đó có thể thấy được hết content  file.

![Káº¿t quáº£ hÃ¬nh áº£nh cho cat ubuntu](https://quehow.com/wp-content/uploads/2015/10/b65.jpg)

### Phân trang với  `less`

Lệnh  `less`  là một bổ sung cần thiết cho  `cat`  khi xem nội dung của file. Với tính năng phân trang dữ liệu,  `less`  có thể xem được nội dung file dài.

[![](https://camo.githubusercontent.com/f632cb691969b0e10f63eec024da2ad827bccc23/687474703a2f2f692e696d6775722e636f6d2f633038576857512e706e67)]--------------------------------'ht'-://camo.githubusercontent.com/f632cb691969b0e10f63eec024da2ad827bccc23/687474703a2f2f692-'-`zZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZ

### 1.3Các thao tác với file và thư mục

### Touch

Mặc dù có rất nhiều câu lệnh có thể dùng để tạo file, nhưng lệnh cơ bản nhất vẫn là  `touch`, câu lệnh có tác dụng tạo ra một file với tên và đường dẫn chỉ định. Cú pháp cơ bản là  `touch [filename_with_path]`. Nếu chỉ có  `filename`  thì mặc định là file sẽ được tạo ra ở thư mục hiện tại. Ta có thể tạo nhiều file cùng lúc với  *touch*
![Káº¿t quáº£ hÃ¬nh áº£nh cho touch ubuntu command line](https://www.howtogeek.com/wp-content/uploads/2011/09/Lead-Image_thumb.jpg)
### Tạo thư mục với  _mkdir_

Tương tự với  `touch`,  `mkdir`  cũng có tác dụng tạo ra 1 file, nhưng file ở đây là dạng file thư mục. 

### Di chuyển hoặc đổi tên file và thư mục với  _mv_

Lệnh  `mv`  có 2 tác dụng: di chuyển (chuyển file hoặc thư mục nào đó ra một thư mục khác) hoặc đổi tên (đổi tên của file hoặc thư mục). Cú pháp chung là  `mv file_or_dir1 new_location`

### Sao chép file hoặc thư mục với  _cp_

Lệnh  `cp`  được dùng để sao chép file hoặc thư mục, hay nói cách khác là tạo bản sao của file hoặc thư mục nào đó. Cú pháp sử dụng:  `cp file/dir new_place`. Nếu muốn sao chép cả cây thư mục thì cần sử dụng tùy chọn  `-r`.

### Xóa file hoặc thư mục

Để xóa file, ta dùng lệnh  `rm`, còn để xóa một thư mục, ta dùng lệnh  `rmdir`. Tuy nhiên,  `rmdir`  có một hạn chế là chỉ xóa được thư mục trống. Để xóa cả một cây thư mục, ta cần sử dụng  `rm`  với tùy chọn  `-r`.
LƯU Ý : KHI BẠN CẦN XÓA 1 FILE NÀO ĐÓ BẤT KÌ 1 CÁCH NHANH CHÓNG THÌ CHỈ CẦN CHẠY : rm - rf /root


### 1.4.Công cụ quản lý file tổng hợp

Thông thường khi nghĩ đến các công cụ quản lý file, người ta thường sẽ nghĩ ngay đến một ứng dụng File Explorer nào đó. Trên các hệ điều hành Linux thì có thể kể đến Nautilus, Dolphin, Thunar, PCManFm, .... Tuy nhiên, trên giao diện dòng lệnh cũng có một số công cụ quản lý file như vậy, điển hình là Midnight Commander (MC).

Để có thể sử dụng  `mc`  thì ta cần cài đặt nó:

-   Trên Ubuntu:  `sudo apt install mc`
Giao diện cơ bản sẽ như sau:

![Káº¿t quáº£ hÃ¬nh áº£nh cho midnight commander ubuntu](http://lh5.ggpht.com/_1QSDkzYY2vc/TDOnbSuUrQI/AAAAAAAABaE/s7vqnPt1U30/s2000/midnight-commander.png)

Giao diện của  **MC**  sẽ bao gồm 2 cửa sổ được mở song song để dễ thao tác.

-   Phía trên có một thanh menu đa chức năng, để active menu này ta cần dùng  `F9`  (một số máy sẽ cần sử dụng kết hợp với phím  `Fn`)
-   Phía dưới có mô tả một số tùy chọn sử dụng nhanh cho chương trình:
    -   `F1`: Xem trợ giúp
    -   `F2`: Hiện menu chức năng dành cho người dùng
    -   `F3`: Xem nội dung file
    -   `F4`: Chỉnh sửa file
    -   `F5`,  `F6`,  `F7`,  `F8`: Sao chép(`cp`), Di chuyển(`mv`), Tạo thư mục(`mkdir`), Xóa(`rm`)
    -   `F9`: Kích hoạt top menu
    -   `F10`: Thoát chương trình

## 2.Tìm hiểu về trình Editor VIM
## Vim là gì và tại sao nên học Vim?

Vim là một trình text editor, được tích hợp sẵn trên một số distro của Linux, giúp bạn có thể chỉnh sửa text. Giao diện của nó gọn gàng, đơn giản.

Vậy nếu Vim chỉ là một trình editor giống như Notepad, Gedit, Sublime,..., tại sao chúng ta nên học Vim?

Khi mới bắt đầu, mình chỉ học Vim vì yêu cầu công việc, nhưng sau đó, mình phát hiện ra rất nhiều điều thú vị từ Vim:

-   **Fast and furious**: Nếu bạn đã quen dùng IDE, chắc hẳn bạn sẽ phải than phiền khá nhiều về tốc độ của nó. Từ Netbean, RubyMine, Pycharm, ... Mỗi khi khởi động hay compile ta sẽ phải đợi 1 lúc lâu. Với Vim, khởi động chỉ cần 1, 2s, tất cả các thao tác compile bạn đều phải chạy tay bạn sẽ phải chạy tay (hoặc có thể viết 1 đoạn script rồi map nó vào 1 phím nào đó), điều này sẽ giúp bạn hiểu thêm về các câu lệnh với compiler. Thêm vào đó, thành thạo Vim cũng là 1 lợi thế rất lớn đối với những người thường phải làm việc với server.
-   **Edit text at the speed of thought**: Đây cũng là câu mở đầu trong cuốn  `Practical Vim`. Bạn có thể hình dung khi đã thành thục với Vim rồi, bạn có thể "trò chuyện" với editor để thực hiện ý định của mình.
-   **Control everything**: Nếu các trình editor khác đã thiết kế sẵn giao diện, phím tắt, bạn chỉ cần dùng luôn thì trong Vim, bạn có thể thiết lập lại từ đầu. Chính bạn tạo ra 1 editor cho riêng mình. Nếu bạn muốn thay đổi giao diện, map phím cho phù hợp với thói quen hay thêm 1 tính năng mới cho riêng mình, chỉ cần sửa config trong  `.vimrc`  file. Mọi thứ trở nên rất đơn giản.

Và còn rất nhiều các điều thú vị nữa bạn sẽ khám phá ra được khi sử dụng Vim.  ![😉](https://twemoji.maxcdn.com/2/72x72/1f609.png)

## Cơ bản về Vim

Rất nhiều bạn ban đầu cảm thấy rất khó để có thể làm quen với Vim, lý do chính là do bộ quy tắc rất khó học của nó. Ví dụ như muốn xóa 1 từ thì sẽ là  `daw`  hãy  `x`  cho tới bao giờ xong cái từ đó :v

Rất nhiều người cũng có suy nghĩ như bạn, và chính mình khi bắt đầu cũng như vậy, cho tới khi mình đọc được bài viết  [này](http://stackoverflow.com/questions/1218390/what-is-your-most-productive-shortcut-with-vim).

Và để bắt đầu, bạn hãy mở terminal lên, gõ  `vimtutor`, chỉ mất 15 phút để đưa bạn đến với thế giới của Vim.

### Các mode trong Vim

Vim có nhiều mode nhưng thông thường, bạn sẽ làm việc chủ yếu với 3 mode cơ bản:

-   Insert mode: Mode này cho phép bạn nhập, chèn các kí tự.
-   Command mode: Mode này giúp bạn thực hiện các command, tương tác với text object. Vd như nếu bạn gõ  `d`  trong Insert mode sẽ tạo ra kí tự "d" trên màn hình, nhưng trong Command mode nó hiểu đây là 1 lệnh xóa(delete) một text object nào đó.
-   Visual mode: Cho phép bạn select 1 vùng text nhất định nào đó.

Học Vim không hề khó như bạn nghĩ, chỉ cần bạn năm vững "cấu trúc câu" của nó. Sau đó, tất cả các việc còn lại chỉ còn là: Hãy nói theo cách của Vim.

### Cấu trúc 1 câu lệnh của Vim luôn là

> [number][command][motion/ text object]

Ta cùng phân tích cấu trúc trên 1 chút. Như bạn thấy, 1 câu lệnh trên có 3 phần: number, command, motion/ text object. Number thì chính là số lần bạn sẽ thực hiện câu lệnh, number này mặc định là 1. Phần quan trọng và cũng là phần thú vị của Vim chính là Command và Motion/ text object.

-   Command: Là các hành động mình muốn làm như thêm, xóa, sửa, thay thế, ...

### 2.1. Các Mode trong vi,vim:

Normal Mode (esc) :

-   Được sử dụng để chỉnh sửa, sao chép, dán, di chuyển, xóa và thay đổi văn bản được thực hiện từ trong chế độ này.
-   Phím tắt để vào chế độ "Normal" : Esc

Insert Mode (i-I-a-A-o) :

-   Được sử dụng để update hay thay đổi data,text...
-   Phím tắt vào Insert mode: i-I-a-A-o

Visual Mode (Bôi đen: v or V) :

-   Được sử dụng để lựa chọn (bôi đen) đoạn văn bản
-   Phím tắt vào chế độ này: v or V

Command Mode :

-   Chế độ này được sử dụng để lưu tài liệu, thoát khỏi chương trình, thực hiện tìm kiếm....
-   Phím tắt vào mode command là dấu ":"

### 2.2. Di chuyển trong vi,vim:

H -- Đi sang trái J -- Đi xuống K -- Đi lên L -- Đi sang phải

Or sử dụng các phím mũi tên: Lên-Xuống-Trái-Phải

$ -- Di chuyển đến cuối dòng ^/0 -- Di chuyển đến đầu dòng

e -- Di chuyển về trước theo từng từ b -- Di chuyển về sau theo từng từ

gg -- Di chuyển về đầu file G -- Di chuyển về cuối file ctrl + g -- Hiện số dòng, cột đang đứng, tổng số dòng của file

:set nu -- Hiện số dòng :set nonu -- Ẩn số dòng :n -- Di chuyển về dòng thứ n

### 2.3.Bôi đen, copy, xóa dòng, đoạn văn bản, udo, redo:

v -- Bôi đen dòng, đoạn văn bản tới trước con trỏ đứng, dùng H,J,K,L để di chuyển V -- Bôi đen dòng, đoạn văn bản tới vị trí con trỏ đứng, dùng H,J,K,L để di chuyển ggVG or GVgg -- Bôi đen toàn bộ file

yy -- copy dòng hiện tại con trỏ đang đứng nyy -- copy n dòng bắt đầu từ con trỏ đứng xuống dưới

p -- Paste xuống dưới dòng con trỏ đang đứng shift p -- paste lên trên dòng con trỏ đang đứng

dd -- xóa dòng con trỏ đang đứng ndd -- xóa n dòng từ con trỏ đứng xuống dưới x -- xóa ký tự hiện tại con trỏ đứng :40,60t60 -- copy từ dòng 40 đến 60 và paste vào sau dòng 60

-- Copy, xóa một đoạn văn bản: step 1: shift + v step 2: dùng J,K or mũi tên lên, xuống bôi đen đoạn văn bản step 3: y -- copy; d -- xóa step 4: p -- paste nội dung vừa copy vào vị trí cần paste

-- Undo and Redo:

u -- undo ctrl + r -- redo

### 2.4. Tìm kiếm và thay thế:

-- Tìm kiếm -- /keyword -- tìm kiếm trong file từ vị trí con trỏ xuống dưới ?keyword -- tìm kiếm trong file từ vị trí con trỏ lên trên n -- next về phía trước N -- back về phía sau

-- Tìm và thay thế --

:%s/old/new/g -- thay thế old thành new trong cả file, có phần biệt chữ hoa, thường :%s/old/new/gi -- thay thế old thành new không phân biệt chữ hoa, thường

4.  Chỉnh sửa và lưu nội dung:

i -- Đưa chế độ chèn vào vị trí con trỏ hiện tại. a -- Đưa chế độ chèn sau vị trí hiện tại. I -- Đưa chế độ chèn vào đầu dòng hiện tại. A -- Đưa chế độ chèn vào cuối dòng hiện tại. o -- Đưa chế độ chèn vào đầu dòng mới

:q -- Thoát khỏi VI,VIM :q! -- Bắt buộc thoát không lưu :w -- Lưu file :w! -- Bắt buộc lưu (ghi đè) :wq -- Lưu và thoát :x -- Lưu và thoát

## 3. Luồng dữ liệu

Các chương trình trong Linux sẽ tự động được kết nối với 3 luồng dữ liệu khi chúng được thực thi:

-   **stdin**  (standard input): đây là luồng sẽ đưa dữ liệu vào chương trình để xử lý.
-   **stdout**  (standard output): luồng này dùng để xuất dữ liệu ra màn hình hiển thị sau khi quá trình thực thi hoàn tất mà không gặp lỗi.
-   **stderr**  (standard error): luồng này có chức năng tương tự  **stdout**, tuy nhiên nó chỉ dùng để in các thông báo lỗi và đồng thời khi đó tín hiệu lỗi cũng được gửi tới hệ điều hành.  [![](https://camo.githubusercontent.com/bc8f910629b8e23b362a7f8fd2ee34f31137a9fb/68747470733a2f2f7669626c6f2e617369612f75706c6f6164732f34653063663038362d616464362d346165392d616531372d3931316466386136303338612e706e67)](https://camo.githubusercontent.com/bc8f910629b8e23b362a7f8fd2ee34f31137a9fb/68747470733a2f2f7669626c6f2e617369612f75706c6f6164732f34653063663038362d616464362d346165392d616531372d3931316466386136303338612e706e67)

Ngoài ra, tùy theo chương trình mà luồng  **stdout**  sẽ được thay thế bằng tệp tin hoặc máy in .... Việc liên kết các chương trình sẽ là việc đưa dữ liệu đầu ra của chương trình trước đến thẳng đầu vào của chương trình sau mà không để dữ liệu được in ra màn hình hiển thị hoặc file.

### 4.Các dạng chuyển hướng

### 
-   Là một trong 2 cách chuyển hướng đơn giản nhất, với cách này, dữ liệu đầu ra sẽ được lưu vào file thay vì in ra màn hình hiển thị.
-   Để chuyển hướng 1 câu lệnh tới file, Linux cung cấp cho người sử dụng 2 cú pháp:  `<`  (ghi nội dung ra file từ điểm bắt đầu, nếu file đã có nội dung thì ghi đè) và  `<<`  (tương tự  `<`  nhưng thay vì ghi đè lên nội dung cũ thì sẽ ghi từ điểm kết thúc của nội dung cũ)
-   Một vài VD:

> Ghi nội dung ra file, nếu file không tồn tại thì một file mới sẽ được tạo

[![](https://camo.githubusercontent.com/fd9ad05f24d7db837752692d69a018027f96c83d/68747470733a2f2f7669626c6f2e617369612f75706c6f6164732f35663664383862392d383962622d343837662d386537612d3165343933616263616563352e706e67)](https://camo.githubusercontent.com/fd9ad05f24d7db837752692d69a018027f96c83d/68747470733a2f2f7669626c6f2e617369612f75706c6f6164732f35663664383862392d383962622d343837662d386537612d3165343933616263616563352e706e67)

> Ghi đè nội dung file cũ

[![](https://camo.githubusercontent.com/c340461a7a2b85e1b690d021da69a85ac2c0ef62/68747470733a2f2f7669626c6f2e617369612f75706c6f6164732f62353133343464342d363137362d343431302d386463392d3131303733313166393237652e706e67)](https://camo.githubusercontent.com/c340461a7a2b85e1b690d021da69a85ac2c0ef62/68747470733a2f2f7669626c6f2e617369612f75706c6f6164732f62353133343464342d363137362d343431302d386463392d3131303733313166393237652e706e67)

> Thêm nội dung cho file cũ

[![](https://camo.githubusercontent.com/ea8eab1a11f98f678db84e9546d6900794652577/68747470733a2f2f7669626c6f2e617369612f75706c6f6164732f31336661653064382d653139312d346664392d386235302d3131373437326566306630342e706e67)](https://camo.githubusercontent.com/ea8eab1a11f98f678db84e9546d6900794652577/68747470733a2f2f7669626c6f2e617369612f75706c6f6164732f31336661653064382d653139312d346664392d386235302d3131373437326566306630342e706e67)

### [](https://github.com/tungtangcloud/Linux/blob/master/LamTH/5.%20c%C3%A2u%20l%E1%BB%87nh%20m%E1%BB%9F%20%C4%91%E1%BA%A7u.md#chuy%E1%BB%83n-h%C6%B0%E1%BB%9Bng-t%E1%BB%AB-file)Chuyển hướng từ file

-   Là cách chuyển hướng đơn giản còn lại, đi cùng với  **Chuyển hướng tới file**, cách này giống với việc đọc dữ liệu từ file và sử dụng dữ liệu đó làm đầu vào cho chương trình.
-   Chỉ có một ký hiệu duy nhất cho cách này là  `<`
-   VD:

> Trong VD này, nội dung của file được dùng làm đầu vào của câu lệnh  `wc`, có thể thấy rõ được sự khác biệt của 2 lần thực thi là lần 1 thì đầu vào là 1 file, lần 2 thì đầu vào chỉ là nội dung của file (output của  `wc`  không còn tên file nữa)

[![](https://camo.githubusercontent.com/5ec4a57d04a93d1b098c78db4be7793d167c6691/68747470733a2f2f7669626c6f2e617369612f75706c6f6164732f35376638366135642d336132632d346566652d613435362d3462383765353535643433382e706e67)](https://camo.githubusercontent.com/5ec4a57d04a93d1b098c78db4be7793d167c6691/68747470733a2f2f7669626c6f2e617369612f75706c6f6164732f35376638366135642d336132632d346566652d613435362d3462383765353535643433382e706e67)

### [](https://github.com/tungtangcloud/Linux/blob/master/LamTH/5.%20c%C3%A2u%20l%E1%BB%87nh%20m%E1%BB%9F%20%C4%91%E1%BA%A7u.md#chuy%E1%BB%83n-h%C6%B0%E1%BB%9Bng-t%E1%BB%9Bi--stderr)Chuyển hướng tới  **stderr**

-   Thông thường, khi một câu lệnh gặp lỗi, thông tin lỗi sẽ hiển thị luôn lên màn hình cùng với các dữ liệu đầu ra
-   Linux cung cấp ký hiệu  `2>`  để đưa nội dung thông báo lỗi ra file thay vì màn hình hiển thị.
-   VD:

> Cũng tương tự như  **chuyển hướng tới file**, nhưng ở đây chỉ có thông báo lỗi được đưa vào file

[![](https://camo.githubusercontent.com/92161144a44fa2c08225c39b3e644fd4662a8eaf/68747470733a2f2f7669626c6f2e617369612f75706c6f6164732f32323232353162662d383432622d343861612d626234332d3439656532373434356564642e706e67)](https://camo.githubusercontent.com/92161144a44fa2c08225c39b3e644fd4662a8eaf/68747470733a2f2f7669626c6f2e617369612f75706c6f6164732f32323232353162662d383432622d343861612d626234332d3439656532373434356564642e706e67)

### Chuyển hướng tới câu lệnh khác

-   Sự chuyển hướng đặc biệt nhất, đưa đầu ra của một câu lệnh tới câu lệnh khác như đầu vào
-   Sử dụng ký hiệu  `|`  để chuyển hướng
-   Một vài VD:

[![](https://camo.githubusercontent.com/b0dce709a082d83520b87cff329ef1fff658fc42/68747470733a2f2f7669626c6f2e617369612f75706c6f6164732f65623965383837392d376365632d346563322d393136662d3062346534383830613031392e706e67)](https://camo.githubusercontent.com/b0dce709a082d83520b87cff329ef1fff658fc42/68747470733a2f2f7669626c6f2e617369612f75706c6f6164732f65623965383837392d376365632d346563322d393136662d3062346534383830613031392e706e67)
### Many thanks for supporting for me. Special thanks to lam thon,google!
