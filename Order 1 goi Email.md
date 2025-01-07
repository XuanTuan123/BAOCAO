

**Các chức năng về Email trên cPanel**
-
**1. Email Accounts**

**Chức năng**:

- **Tạo tài khoản email**: Bạn có thể tạo nhiều tài khoản email với tên miền của mình (ví dụ: user1@tuanhhx.io.vn).
Quản lý mật khẩu: Thay đổi mật khẩu cho các tài khoản email để bảo mật.

- **Quản lý dung lượng lưu trữ**: Thiết lập hạn mức dung lượng cho từng tài khoản, giúp quản lý tài nguyên hiệu quả.

**Cách sử dụng**:

- Nhấn vào **Email Accounts**, sau đó chọn **Create** để tạo tài khoản mới. Điền thông tin cần thiết như tên người dùng, mật khẩu và dung lượng lưu trữ.

![image](https://github.com/user-attachments/assets/0cc8d5a6-392c-47d2-9e96-d20fee70dd9a)

**2. Forwarders**

**Chức năng**:

- **Chuyển tiếp email**: Cho phép bạn chuyển tiếp email từ một địa chỉ đến một địa chỉ khác. Ví dụ, bạn có thể chuyển tiếp tất cả email gửi đến sales@yourdomain.com đến một tài khoản cá nhân.

**Cách sử dụng**:

- Truy cập **Forwarders**, chọn **Add Forwarder**, nhập địa chỉ email cần chuyển tiếp và địa chỉ đích.

![image](https://github.com/user-attachments/assets/3b2340eb-af70-4d21-bb12-78d458978b7e)

![image](https://github.com/user-attachments/assets/c4be8104-913e-4b7f-9d19-74786e860233)

**3. Autoresponders**

**Chức năng**:

- **Trả lời tự động**: Thiết lập thông điệp tự động gửi đến người gửi khi bạn không có mặt hoặc đang nghỉ phép. Điều này rất hữu ích để thông báo cho khách hàng hoặc đối tác.

**Cách sử dụng**:

- Vào mục **Autoresponders**, nhấn vào **Add Autoresponder**, điền thông tin như địa chỉ email, tiêu đề và nội dung thông điệp tự động.

![image](https://github.com/user-attachments/assets/61df693c-91ae-44c6-ae6e-ae617a627e43)

![image](https://github.com/user-attachments/assets/fef67446-9a5e-41c6-8e26-3c1a5b168f8e)

**4. Track Delivery**

**Chức năng**:

- **Theo dõi quá trình gửi email**: Giúp bạn kiểm tra xem email đã được gửi đi thành công hay không, và nếu không thì lý do là gì.

**Cách sử dụng**:

- Chọn **Track Delivery**, bạn sẽ thấy danh sách các email đã gửi, cùng với trạng thái của chúng (đã gửi, bị lỗi, v.v.).

![image](https://github.com/user-attachments/assets/228750e6-05a4-4e06-8398-c82b122876b0)

**5. Global Filters**

**Chức năng**:

- **Thiết lập bộ lọc toàn cầu**: Giúp bạn quản lý và tổ chức email hiệu quả hơn bằng cách tạo các quy tắc tự động cho việc xử lý email đến.

**Cách sử dụng**:

- Truy cập vào **Global Filters**, chọn **Add Filter**, sau đó định nghĩa các điều kiện và hành động mà bạn muốn áp dụng cho các email đến.

![image](https://github.com/user-attachments/assets/e655782b-a022-4265-974a-6b318e53fa6b)

**6. Email Routing**

**Chức năng**:

- **Quản lý cách xử lý email đến**: Bạn có thể chọn cách mà email đến sẽ được xử lý, như sử dụng máy chủ email nội bộ (Local Mail Exchanger) hoặc máy chủ từ xa (Remote Mail Exchanger).

**Các tùy chọn** (tùy theo mục đích sử dụng của mình):
- **Automatically Detect Configuration**: Tự động phát hiện cấu hình dựa trên MX Records.
- **Local Mail Exchanger**: Nhận email trực tiếp trên máy chủ của bạn.
- **Backup Mail Exchanger**: Giữ email khi máy chủ chính không hoạt động.
- **Remote Mail Exchanger**: Gửi tất cả email đến máy chủ khác.

![image](https://github.com/user-attachments/assets/7b0567a9-229b-4191-bf29-da0c00a6f282)

**8. Mailing Lists**

**Chức năng**:

- **Tạo danh sách gửi thư**: Cho phép bạn tạo danh sách người nhận để gửi thông báo hoặc bản tin đến nhiều người cùng lúc. Điều này hữu ích cho việc quảng cáo hoặc thông báo sự kiện.

**Cách sử dụng**:

- Vào mục **Mailing Lists**, chọn **Add Mailing List**, sau đó điền thông tin cần thiết như tên danh sách và địa chỉ email quản lý.

![image](https://github.com/user-attachments/assets/50d8d4de-91f2-485f-a9d7-4fcb59aec3a0)

**9. Email Deliverability**

**Chức năng**:

- Cải thiện khả năng gửi email: Đảm bảo rằng email của bạn không bị đánh dấu là spam và đến được hộp thư đến của người nhận. Điều này thường bao gồm việc cấu hình SPF, DKIM và DMARC.

**Cách sử dụng**:
- Kiểm tra và cấu hình các bản ghi DNS liên quan đến SPF, DKIM và DMARC trong phần DNS **Zone Editor** của cPanel để tối ưu hóa khả năng gửi email.

![image](https://github.com/user-attachments/assets/77343a87-60c6-4847-b842-52a85138116a)

**10. Spam Filters**

**Chức năng**:

- **Lọc spam**: Sử dụng Apache SpamAssassin để tự động xác định và xử lý email không mong muốn.

- **Cấu hình linh hoạt**: Bạn có thể điều chỉnh mức độ nhạy của bộ lọc bằng cách thay đổi Spam Threshold Score (điểm ngưỡng spam), từ 1 (nhạy nhất) đến 10 (ít nhạy hơn) 13.

- **Tùy chọn xử lý**: Có thể chọn tự động xóa hoặc chuyển email vào thư mục spam 67.

**Cách sử dụng**:

- Truy cập vào mục **Spam Filters**, bật tùy chọn "**Process New Emails and Mark them as Spam**", và điều chỉnh các tùy chọn theo nhu cầu.

![image](https://github.com/user-attachments/assets/9323a48c-c12a-4364-a878-203095ebc115)

**11. BoxTrapper**

**Chức năng**:

- **Xác thực người gửi**: BoxTrapper yêu cầu người gửi xác nhận email trước khi nó được gửi đến hộp thư của bạn, giúp giảm thiểu spam.

- **Quản lý danh sách gửi thư**: Bạn có thể thêm hoặc xóa người gửi từ danh sách cho phép để kiểm soát ai có thể gửi email đến bạn.

**Cách sử dụng**:

- Vào mục **BoxTrapper**, thiết lập các tùy chọn xác thực và quản lý danh sách người gửi.

![image](https://github.com/user-attachments/assets/eb14b66a-d64f-4660-9eb4-bbc0186e8a36)

**12. Email Disk Usage**

**Chức năng**:

- **Theo dõi dung lượng lưu trữ email**: Cho phép bạn xem dung lượng mà các tài khoản email đang sử dụng, giúp quản lý tài nguyên hiệu quả.

- **Xóa email không cần thiết**: Bạn có thể dễ dàng xác định và xóa những email chiếm nhiều dung lượng để giải phóng không gian.

**Cách sử dụng**:

- Truy cập vào mục **Email Disk Usage**, xem thông tin chi tiết về dung lượng và thực hiện các hành động cần thiết để tối ưu hóa lưu trữ.

![image](https://github.com/user-attachments/assets/f0923b5d-a651-413e-a3d7-8c31b5d88ef3)

<có 2 tính năng mới, nghiên cứu cập nhật>

**Cách tạo Account Email**
-
**Bước 1**:

- Đăng nhập tài khoản được cấp, ví dụ như hình:

![Screenshot 2025-01-01 184613](https://github.com/user-attachments/assets/67fc745d-8e26-492e-afd6-8cdaa0ec71b8)


- Đăng nhập thành công, dashboard của cPanel hiện ra:

![image](https://github.com/user-attachments/assets/7126395f-c826-4d5e-ae6b-26df35c0e7f4)


**Bước 2**:

- Để tạo tài khoản email, ta tìm đến **Email** -> **Email Accounts**. Sau đó, sẽ hiển thị giao diện như sau:

![Screenshot 2025-01-01 185323](https://github.com/user-attachments/assets/c15fed6c-3142-4567-9ca3-0ef61396ee24)


**Bước 3**:

- Nhấn vào nút **Create** màu xanh ở góc phải màn hình.

![image](https://github.com/user-attachments/assets/264db2f7-6cb9-4476-b86c-eea2af57c98a)


**Bước 4**:

- Tại giao diện này, chúng ta điền vào ô **Username** và **Password** rồi nhấn chọn **Create**. Sau khi tạo tài khoản xong, sẽ hiển thị các tài khoản như sau:

![image](https://github.com/user-attachments/assets/3a3c3076-211c-48cb-ad11-0d63c4bf784e)

- Lưu ý: Nếu muốn giới hạn dung lượng sử dụng email, chúng ta có thể chọn **Edit Settings** tại mục **Optional Settings**:

![Screenshot 2025-01-01 190202](https://github.com/user-attachments/assets/9154ccbd-8ef0-4473-abe6-d50508c838a4)


    Tại Storage Space có 2 tùy chọn 1024 MB hoặc Unlimited.
    
**Bước 5**:

- Nhấn vào biểu tượng có hình cây bút đầu tiên góc trái để soạn email với email nhận là **user2@tuanhhxtts.freehost.vn** với nội dung như hình:
![image](https://github.com/user-attachments/assets/25ac8422-0b5a-46d7-917a-9616272550b5)

![image](https://github.com/user-attachments/assets/b8d72f4c-1e18-41bf-8adf-252d82a0072c)

- Tiếp đó, bấm vào nút **Gửi**, để kiểm tra thư đã gửi đi nhấn chọn **Đã gửi** như hình:

![image](https://github.com/user-attachments/assets/888b7091-7168-41ca-8006-e0df067da9f6)

![image](https://github.com/user-attachments/assets/226782ec-e31e-4fae-bcc6-9c9b8290bea1)

- Đăng nhập vào **user2@tuanhhxtts.freehost.vn** để kiểm tra email đã được gửi từ **user1@tuanhhxtts.freehost.vn**

![image](https://github.com/user-attachments/assets/b6081ee1-8b4e-4035-8885-924a3c8d85ca)


**Bước 6**:

Cấu hình Mail Client trên OutLook như sau:

- Nhấn chọn tab **File** -> **Info** -> **Add Account**.

![Screenshot 2025-01-01 192529](https://github.com/user-attachments/assets/22b0b3dc-f59b-4324-9bf3-3323e6c74e68)

![Screenshot 2025-01-01 192650](https://github.com/user-attachments/assets/e13358dd-22b8-4299-9808-5ec086b2b82e)

- Giao diện đăng nhập ban đầu. Nhập thông tin tài khoản email **user1@tuanhhxtts.freehost.vn**, nhấn **Connect**.

![image](https://github.com/user-attachments/assets/56186ec3-b883-4b49-aa4d-6c4614be3db4)

- Cuối cùng, hoàn tất đăng nhập.

![image](https://github.com/user-attachments/assets/24f518ae-ff9d-4b8a-ac94-b793cbad78bd)

    Việc đăng nhập user2@tuanhhxtts.freehost.vn cũng làm tương tự như vậy.
    
- Kết quả gửi nhận ở **bước 5**, chúng ta sẽ thấy khi đăng nhập trên OutLook như hình:

![image](https://github.com/user-attachments/assets/b3506bda-82df-4748-bb8b-0cc0ee3f6827)









    
 


