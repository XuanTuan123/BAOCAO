

**Các chức năng về Email trên cPanel**
-
**1. Email Accounts**

**Chức năng**:

- **Tạo tài khoản email**: Bạn có thể tạo nhiều tài khoản email với tên miền của mình (ví dụ: example@domain.com).
Quản lý mật khẩu: Thay đổi mật khẩu cho các tài khoản email để bảo mật.

- **Quản lý dung lượng lưu trữ**: Thiết lập hạn mức dung lượng cho từng tài khoản, giúp quản lý tài nguyên hiệu quả.

**Cách sử dụng**:

- Nhấn vào Email Accounts, sau đó chọn Create để tạo tài khoản mới. Điền thông tin cần thiết như tên người dùng, mật khẩu và dung lượng lưu trữ.

![image](https://github.com/user-attachments/assets/516a409f-6882-4a85-8d0e-0c654cff9bbb)


**2. Forwarders**

**Chức năng**:

- **Chuyển tiếp email**: Cho phép bạn chuyển tiếp email từ một địa chỉ đến một địa chỉ khác. Ví dụ, bạn có thể chuyển tiếp tất cả email gửi đến sales@yourdomain.com đến một tài khoản cá nhân.

**Cách sử dụng**:

- Truy cập Forwarders, chọn Add Forwarder, nhập địa chỉ email cần chuyển tiếp và địa chỉ đích.

![image](https://github.com/user-attachments/assets/3b2340eb-af70-4d21-bb12-78d458978b7e)

![image](https://github.com/user-attachments/assets/4fdac71e-c31d-4d5e-bbaf-e53d1a69a9ac)

**3. Autoresponders**

**Chức năng**:

- **Trả lời tự động**: Thiết lập thông điệp tự động gửi đến người gửi khi bạn không có mặt hoặc đang nghỉ phép. Điều này rất hữu ích để thông báo cho khách hàng hoặc đối tác.

**Cách sử dụng**:

- Vào mục Autoresponders, nhấn vào Add Autoresponder, điền thông tin như địa chỉ email, tiêu đề và nội dung thông điệp tự động.

**4. Track Delivery**

**Chức năng**:

- **Theo dõi quá trình gửi email**: Giúp bạn kiểm tra xem email đã được gửi đi thành công hay không, và nếu không thì lý do là gì.

**Cách sử dụng**:

- Chọn Track Delivery, bạn sẽ thấy danh sách các email đã gửi, cùng với trạng thái của chúng (đã gửi, bị lỗi, v.v.).

**5. Global Filters**

**Chức năng**:

- **Thiết lập bộ lọc toàn cầu**: Giúp bạn quản lý và tổ chức email hiệu quả hơn bằng cách tạo các quy tắc tự động cho việc xử lý email đến.

**Cách sử dụng**:

- Truy cập vào Global Filters, chọn Add Filter, sau đó định nghĩa các điều kiện và hành động mà bạn muốn áp dụng cho các email đến.

**6. Email Routing**

**Chức năng**:

- **Quản lý cách xử lý email đến**: Bạn có thể chọn cách mà email đến sẽ được xử lý, như sử dụng máy chủ email nội bộ (Local Mail Exchanger) hoặc máy chủ từ xa (Remote Mail Exchanger).

**Các tùy chọn**:
- **Automatically Detect Configuration**: Tự động phát hiện cấu hình dựa trên MX Records.
- **Local Mail Exchanger**: Nhận email trực tiếp trên máy chủ của bạn.
- **Backup Mail Exchanger**: Giữ email khi máy chủ chính không hoạt động.
- **Remote Mail Exchanger**: Gửi tất cả email đến máy chủ khác.

**8. Mailing Lists**

**Chức năng**:

- **Tạo danh sách gửi thư**: Cho phép bạn tạo danh sách người nhận để gửi thông báo hoặc bản tin đến nhiều người cùng lúc. Điều này hữu ích cho việc quảng cáo hoặc thông báo sự kiện.

**Cách sử dụng**:

- Vào mục Mailing Lists, chọn Add Mailing List, sau đó điền thông tin cần thiết như tên danh sách và địa chỉ email quản lý.

**9. Email Deliverability**

**Chức năng**:

- Cải thiện khả năng gửi email: Đảm bảo rằng email của bạn không bị đánh dấu là spam và đến được hộp thư đến của người nhận. Điều này thường bao gồm việc cấu hình SPF, DKIM và DMARC.

**Cách sử dụng**:
- Kiểm tra và cấu hình các bản ghi DNS liên quan đến SPF, DKIM và DMARC trong phần DNS Zone Editor của cPanel để tối ưu hóa khả năng gửi email.

**10. Spam Filters**

**Chức năng**:

- **Lọc spam**: Sử dụng Apache SpamAssassin để tự động xác định và xử lý email không mong muốn.

- **Cấu hình linh hoạt**: Bạn có thể điều chỉnh mức độ nhạy của bộ lọc bằng cách thay đổi Spam Threshold Score (điểm ngưỡng spam), từ 1 (nhạy nhất) đến 10 (ít nhạy hơn) 13.

- **Tùy chọn xử lý**: Có thể chọn tự động xóa hoặc chuyển email vào thư mục spam 67.

**Cách sử dụng**:

- Truy cập vào mục Spam Filters, bật tùy chọn "Process New Emails and Mark them as Spam", và điều chỉnh các tùy chọn theo nhu cầu.

**11. BoxTrapper**

**Chức năng**:

- **Xác thực người gửi**: BoxTrapper yêu cầu người gửi xác nhận email trước khi nó được gửi đến hộp thư của bạn, giúp giảm thiểu spam.

- **Quản lý danh sách gửi thư**: Bạn có thể thêm hoặc xóa người gửi từ danh sách cho phép để kiểm soát ai có thể gửi email đến bạn.

**Cách sử dụng**:

- Vào mục BoxTrapper, thiết lập các tùy chọn xác thực và quản lý danh sách người gửi.

**12. Email Disk Usage**

**Chức năng**:

- **Theo dõi dung lượng lưu trữ email**: Cho phép bạn xem dung lượng mà các tài khoản email đang sử dụng, giúp quản lý tài nguyên hiệu quả.

- **Xóa email không cần thiết**: Bạn có thể dễ dàng xác định và xóa những email chiếm nhiều dung lượng để giải phóng không gian.

**Cách sử dụng**:

- Truy cập vào mục Email Disk Usage, xem thông tin chi tiết về dung lượng và thực hiện các hành động cần thiết để tối ưu hóa lưu trữ.

**Cách tạo Account Email**
-
**Bước 1**:

- Đăng nhập tài khoản được cấp, ví dụ như hình:

![Screenshot 2025-01-01 184613](https://github.com/user-attachments/assets/67fc745d-8e26-492e-afd6-8cdaa0ec71b8)


- Đăng nhập thành công, dashboard của cPanel hiện ra:

![Screenshot 2025-01-01 184857](https://github.com/user-attachments/assets/6276e37c-fe3f-405b-a365-2198868be10b)


**Bước 2**:

- Để tạo tài khoản email, ta tìm đến **Email** -> **Email Accounts**. Sau đó, sẽ hiển thị giao diện như sau:

![Screenshot 2025-01-01 185323](https://github.com/user-attachments/assets/c15fed6c-3142-4567-9ca3-0ef61396ee24)


**Bước 3**:

- Nhấn vào nút **Create** màu xanh ở góc phải màn hình.

![Screenshot 2025-01-01 185602](https://github.com/user-attachments/assets/1098d3d1-cd12-44b7-af5b-707c0f383c17)


**Bước 4**:

- Tại giao diện này, chúng ta điền vào ô **Username** và **Password** rồi nhấn chọn **Create**. Sau khi tạo tài khoản xong, sẽ hiển thị các tài khoản như sau:

![Screenshot 2025-01-01 185911](https://github.com/user-attachments/assets/6e5d9155-53d9-49d5-a468-6bee081c5624)


- Lưu ý: Nếu muốn giới hạn dung lượng sử dụng email, chúng ta có thể chọn **Edit Settings** tại mục **Optional Settings**:

![Screenshot 2025-01-01 190202](https://github.com/user-attachments/assets/9154ccbd-8ef0-4473-abe6-d50508c838a4)


    Tại Storage Space có 2 tùy chọn 1024 MB hoặc Unlimited.
    
**Bước 5**:

- Nhấn vào biểu tượng có hình cây bút đầu tiên góc trái để soạn email với email nhận là **user2@tuanhhx.io.vn** với nội dung như hình:

![Screenshot 2025-01-01 191450](https://github.com/user-attachments/assets/27f7a188-6f83-4001-a99d-569aacb63430)


- Tiếp đó, bấm vào nút **Gửi**, để kiểm tra thư đã gửi đi nhấn chọn **Đã gửi** như hình:

![Screenshot 2025-01-01 191901](https://github.com/user-attachments/assets/89707536-a473-4ba2-ba4c-c6499a7cf793)

![Screenshot 2025-01-01 192049](https://github.com/user-attachments/assets/25002ee1-a581-4c2d-9100-b41e072aa33b)


- Đăng nhập vào **user2@tuanhhx.io.vn** để kiểm tra email đã được gửi từ **user1@tuanhhx.io.vn**

![Screenshot 2025-01-01 192145](https://github.com/user-attachments/assets/1090bd6c-de53-482b-a1b5-cf1333d3e516)

![Screenshot 2025-01-01 192323](https://github.com/user-attachments/assets/13d2a335-5a82-4f81-aba6-c9568c3ffc95)


**Bước 6**:

Cấu hình Mail Client trên OutLook như sau:

- Nhấn chọn tab **File** -> **Info** -> **Add Account**.

![Screenshot 2025-01-01 192529](https://github.com/user-attachments/assets/22b0b3dc-f59b-4324-9bf3-3323e6c74e68)

![Screenshot 2025-01-01 192650](https://github.com/user-attachments/assets/e13358dd-22b8-4299-9808-5ec086b2b82e)

- Giao diện đăng nhập ban đầu. Nhập thông tin tài khoản email **user1@tuanhhx.io.vn**, nhấn **Connect**.

![Screenshot 2025-01-01 192749](https://github.com/user-attachments/assets/2e2b5876-7e85-4513-b907-2c0cb90dd3c1)

- Tại **Choose account type** chọn **IMAP** để tài khoản có thể gửi/nhận và lưu trữ email.

![Screenshot 2025-01-01 193002](https://github.com/user-attachments/assets/50afdcb4-a298-42de-847b-acbc7e0c80ca)


- Nhập thông tin như hình bên dưới kèm theo **Password** của **user1@tuanhhx.io.vn** và bấm **Connect**.

![Screenshot 2025-01-01 193251](https://github.com/user-attachments/assets/16d2c154-4773-4032-b6ee-ca57115d8f01)

![Screenshot 2025-01-01 193422](https://github.com/user-attachments/assets/e4036536-116a-4afc-8775-9ec5b8cc31ba)

- Cuối cùng, hoàn tất đăng nhập.

![Screenshot 2025-01-01 193748](https://github.com/user-attachments/assets/b89935f3-c3c3-4564-a6a9-91264fb0c0e3)

    Việc đăng nhập user2@tuanhhx.io.vn cũng làm tương tự như vậy.
    
- Kết quả gửi nhận ở **bước 5**, chúng ta sẽ thấy khi đăng nhập trên OutLook như hình:

![Screenshot 2025-01-01 194040](https://github.com/user-attachments/assets/7a3246de-dec2-44e5-addb-7b44d1b0752b)

![Screenshot 2025-01-01 194109](https://github.com/user-attachments/assets/db4a0076-500c-4292-b0a0-6dea781cd4e9)








    
 


