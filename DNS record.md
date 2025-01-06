**DNS Records là gì?**
-
- **DNS Records (Domain Name Server Records)** là một bản ghi có chứa thông tin về tên miền, bao gồm địa chỉ IP tương ứng với tên miền đó.

- Khi gõ tên miền vào trình duyệt web, trình duyệt sẽ gửi yêu cầu đến máy chủ DNS để xác định địa chỉ IP tương ứng với tên miền đó.

**Các loại DNS record phổ biến**
-
- **Record A**: là loại record phổ biến nhất, nó là bản ghi chứa địa chỉ tên miền.

      - Ví dụ: freehost.vn IN A 125.212.217.216

- **Record MX**: là loại record đặc biệt, được sử dụng để chuyển hướng thư đến máy chủ email của tên miền đó. Khi tạo bản ghi MX, Data sẽ chứa hai trường: Priority và Exchange.

      - Ví dụ: IN MX 10  freehost.vn. 
      - Trong trường hợp trên Priority là 10 có nghĩa là mức độ ưu tiên thấp (số càng thấp mức ưu tiên càng cao).

- **Record TXT**: là một loại record cho phép lưu trữ các thông tin không phải là tên miền hoặc địa chỉ IP. 

       - Ví dụ như một khóa xác thực SPF được sử dụng để xác minh tính xác thực của email gửi từ tên miền.
       
- **CNAME Record**: là loại record tạo ra một bản ghi tên miền kết nối với một tên miền khác. Nó thường được sử dụng để thiết lập tên miền phụ.

       - Ví dụ: mail.freehost.vn IN CNAME freehost.vn 
       
- **NS Record**: là một loại record giúp xác định thông tin của một tên miền cụ thể được khai báo và quản lý trên máy chủ nào.

       - Ví dụ: IN  NS  ns1.freehost.vn.
      
**Tại sao lại cần cấu hình SPF và DKIM trong việc bảo vệ email**
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
   
**Vậy thuật toán mã hóa RSA là gì?**

- **RSA (Rivest-Shamir-Adleman)**: là thuật toán mã hóa bất đối xứng nổi tiếng và phổ biến nhất hiện nay, được sử dụng rộng rãi trong các ứng dụng bảo mật như mã hóa email, chứng chỉ SSL/TLS và chữ ký số.

*Thuật toán RSA được phát triển vào năm 1977 bởi Ron Rivest, Adi Shamir, và Leonard Adleman tại Viện Công nghệ Massachusetts (MIT).*

- **Ưu điểm của RSA**: 

    - Bảo mật mạnh mẽ.
    
    - Khả năng tương thích cao.

- **Nhược điểm của RSA**: 

    - Hiệu suất chậm.
    
    - Yêu cầu nhiều tài nguyên tính toán và bộ nhớ.

**3. Kiểm tra cấu hình SPF và DKIM**

- Để kiểm tra cấu hình của SPF Record đã đúng (Pass) sử sụng công cụ trực tuyến **MXToolBox SPF Check**:

    - Nhập tên miền cần kiểm tra vào ô **Domain Name** và nhấn **SPF Record Lookup**:
    
    ![image](https://github.com/user-attachments/assets/6cd888a2-b62c-4a78-9ae3-76158f6580cb)

    - Kết quả hiển thị như sau:
    
    ![image](https://github.com/user-attachments/assets/be0e19da-384f-4abd-8079-7e351072ab24)

    ![image](https://github.com/user-attachments/assets/486bf741-7e1e-4f81-85d9-d2db180ae5ad)

    
- Tiếp theo để kiểm tra cấu hình của DKIM Record đã đúng (Pass) sử sụng công cụ trực tuyến **dkimvalidator.com**:

    - Sử dụng email cần kiểm tra để gửi đến email như hình:
    
    ![image](https://github.com/user-attachments/assets/ef05c031-d834-4539-944f-b28e92bd1186)

    - Kết quả sau khi nhấn **View result** sẽ hiển thị như sau:

  Ví dụ:

   ![image](https://github.com/user-attachments/assets/38469c75-9dd1-4b5c-80e0-c8fa2e1303b0)

   ![image](https://github.com/user-attachments/assets/1ca9e025-ef65-49eb-9e3b-46b62427124a)

   ![image](https://github.com/user-attachments/assets/f72f2d31-4946-4c61-9697-533c6b0af80e)


    
    
