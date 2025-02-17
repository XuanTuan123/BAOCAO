**Cấu hình SPF và DKIM tăng độ uy tín cho email** (đã edit v1)
-
**1. SPF (Sender Policy Framework)**: là phương thức sử dụng các DNS Record xác định địa chỉ IP để xác thực danh tính của người gửi email.

- Một **record (TXT) SPF** thường sẽ trông như sau:

       v=spf1 a a:spf.vinahost.vn mx +include:sendgrid.net +include:smtpservice.net ~all
        
Trong đó:

   - **'v=spf1'**: là phần khai báo phiên bản spf, cụ thể là v1.
   
   - **'a a:spf.vinahost.vn'**: cho phép các máy chủ có tên miền spf.vinahost.vn gửi email thay cho tên miền của bạn. Nếu trùng khớp địa chỉ IP thì nó sẽ được phép gửi email.
   
   - **'mx +include:sendgrid.net +include:smtpservice.net'**:
   xác định tên miền máy chủ gửi email, cho phép các máy chủ Sendgrid.net và Smtpservice.net được gửi email thay cho tên miền của bạn.
   
   - **'~all'**: chỉ định nếu email không trùng khớp với điều kiện nào ở trong SPF Record thì email đó sẽ bị "Soft Fail". Điều này có nghĩa là email có thể được chấp nhận gửi đi nhưng bị đánh dấu là spam hoặc nghi ngờ. 
   
**2. DKIM (DomainKeys Identified Mail)**: là phương thức dùng để xác thực email dựa trên chữ ký số, kiểm tra nội dung email có bị thay đổi không trong suốt quá trình truyền và đảm bảo tính toàn vẹn của nội dung email.

- Một **record (TXT) DKIM** thường sẽ trông như sau:

       v=DKIM1; k=rsa; p=MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAmwJSivzbdkOQ9yqRaiok0VoNtJcnFJ0D/lqFzb1QxJFVnoViNLfCYHkg0qUfOHk/g/vj+X0zSrS/YGfsKkE+BF0JKeHf905wZL/sW6M6rXkz38Z6zfWY0UtN3Sp9icwxd4TaiIKsQnB8HrngqiRUnvf93i0Y0gHo41NlZrQ56+Fxln85ztNKR36KMEAK5bQbKhc1BZj6YQl4M4Hlw6fD2/W6WfN+s0IUdHDgXINrCMsZPrB/MBuxKbnmpqFrFZT0faYUfkCiTSsZwIT6dT+NiN6P5RTKnSnVI+DuUl+PUKyGUik4Vwoqa30H95Y3LrsXojlChLfeeFFa/DBqh5O+gQIDAQAB;

Trong đó:

   - **'v=DKIM1'**: là phần khai báo phiên bản, cụ thể là v1.
   
   - **'k=rsa'**: là chỉ định một thuật toán mã hóa, cụ thể là thuật toán **RSA**.
   
   - **'p=MIIBIjANBgkqhkiG9w...'**: là khóa công khai được sử dụng xác minh chữ ký DKIM của email gửi đi, trong khi khóa riêng tư được dùng để tạo chữ ký.

 
**Kiểm tra cấu hình SPF và DKIM**
-
- Để kiểm tra cấu hình của SPF Record đã đúng (Pass) sử dụng công cụ trực tuyến bằng cách truy cập  **dkimvalidator.com**:

    - Sử dụng email cần kiểm tra  để gửi đến email như hình:
    
    ![image](https://github.com/user-attachments/assets/acb4f038-e14d-43e1-a41f-190185b65d2f)

    - Kết quả hiển thị như sau:

    ![spf-pass](https://github.com/user-attachments/assets/6d801087-275d-48a7-b1ff-26f80af33f57)

- Tiếp theo để kiểm tra cấu hình của DKIM Record đã đúng (Pass) sử sụng công cụ trực tuyến **dkimvalidator.com**:

    - Sử dụng email cần kiểm tra để gửi đến email như hình:
    
    ![image](https://github.com/user-attachments/assets/ef05c031-d834-4539-944f-b28e92bd1186)

    - Kết quả sau khi gửi và nhấn **View result** sẽ hiển thị như sau:

    ![dkim-pass](https://github.com/user-attachments/assets/b7878607-6c18-43fd-8d9b-8f77bc1f01d0)

    *Đây là hình ảnh cho việc email đã gửi SPF và DKIM: Pass*

Thực hiện thử gửi email từ trong domain đến một email cá nhân, để xem trạng thái SPF và DKIM:

![thu-goc](https://github.com/user-attachments/assets/b883ecfd-f3d8-4218-a121-fd5779bcd1c5)

- Cách xem thư gốc của 1 email:



- Để xem hành trình gửi nhận email trong hệ thống, tại **Dashboard** nhấn chọn **Track Delivery**:

![image](https://github.com/user-attachments/assets/cb0699b6-aa1b-4a5e-8181-1bfeeb00f7d2)
