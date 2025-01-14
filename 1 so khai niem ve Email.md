**1. MUA (Mail User Agent)**
-
- Là phần mềm hoặc ứng dụng chạy trên máy tính hoặc thông qua 1 trình duyệt, mà **người dùng tương tác trực tiếp** để thực hiện các thao tác gửi, nhận, đọc và quản lý hộp thư.

 Ví dụ: 
 
    - Gmail, Microsoft OutLook, Mozilla ThunderBird, Webmail,...

- Vai trò chính:

    - Là giao diện chính cho người dùng email.
    - Chịu trách nhiệm tạo email và bắt đầu chuyển tiếp tới MTA để gửi.
    
- Sự khác nhau giữa MUA và MTA:

| MUA (Mail User Agent)                             | MTA (Mail Transfer Agent)                                        |
|---------------------------------------------------|------------------------------------------------------------------|
| Tập trung vào tương tác của người dùng với email. | Chịu trách nhiệm chuyển tin nhắn email thực tế giữa các máy chủ. |

- Các tính năng chính:

    - Soạn email (có tệp đính kèm) -> nhấn nút "**Gửi**".
    - Quản lý hộp thư (inbox, sent, trash,...).
 

**2. MDA (Mail Delivery Agent)**
-
- Là thành phần chịu trách nhiệm **lưu trữ mail** trong hộp thư của người nhận.

Ví dụ: 

    - Dovecot: phổ biến nhất, hỗ trợ cả IMAP và POP3.
    - Procmail: dùng để lọc và phân loại mail.

- Lợi ích của việc sử dụng MDA:

    - Tăng tỷ lệ gửi.
    - Cải thiện hiệu suất email.
    - Tỷ lệ tương tác tốt hơn.
    - Giảm khiếu nại thư rác và nâng cao các tính năng bảo mật.

- Vai trò của MDA:
  
    - Lưu email đúng hộp thư người nhận.
    - Hỗ trợ lấy email qua giao thức IMAP/POP3 cho MUA.
    - Chống spam hoặc gắn cờ các email nghi ngờ.


**3. MTA (Mail Transfer Agent)**
-
- Là thành phần **trung gian** chịu trách nhiệm **gửi email** giữa các máy chủ khác nhau cho đến khi nó đến đúng đích. MTA là "trái tim" của hệ thống email, giúp email được định tuyến qua Internet.
- Hãy coi nó như một dịch vụ bưu chính cho email, đảm bảo tin nhắn đến đúng địa chỉ. MTA rất quan trọng trong hệ sinh thái email, đảm bảo rằng email được gửi chính xác.

Ví dụ về MTA phổ biến:

    - Postfix: phổ biến nhất, mã nguồn mở và mạnh mẽ.
    - Sendmail: cổ điển và lâu đời.
    - Exim: sử dụng rộng rãi trên các máy chủ cPanel.

- Cách hoạt động của MTA thực hiện như sau:

    - Chấp nhận email được gửi từ MUA.
    - Truy vấn bản ghi MX và chọn Mail Server để chuyển email.
    - Gửi tin nhắn trả lời tự động nếu email không đến được đích.
 
- Vai trò chính:

    - Xử lý hậu cần của việc gửi email, bao gồm xếp hàng và thử lại nếu lần thử đầu tiên không thành công.
    - Nhờ đó đảm bảo rằng email được gửi một cách đáng tin cậy.
    
- Chức năng chính: 

    - Chuyển tiếp mail hoặc lưu trữ tạm thời nếu cần.
    - Nhận mail từ nguồn khác và xử lý chúng.
    
**4. Sơ đồ gửi/nhận mail từ các thành phần trên**
-
- Để vẽ sơ đồ gửi nhận mail dựa trên các thành phần trên MUA, MTA và MDA ta có thể hình dung như sau:

    - **MUA (Mail User Agent)**: người dùng soạn và gửi mail.
    - **MTA (Mail Tranfer Agent)**: nhận mail từ MUA, xác định người nhận qua DNS, và chuyển tiếp đến MDA.
    - **MDA (Mail Delivery Agent)**: nhận mail từ MTA và lưu vào hộp thư của người nhận.
    
 - **Quá trình đường đi**:
 
    - Người gửi sử dụng MUA để soạn và gửi mail.
    - Mail đó sẽ được chuyển tới MTA qua giao thức SMTP và chuyển tiếp đến MDA.
    - MDA lưu mail đó vào hộp thư người nhận.
    - Cuối cùng, người nhận sử dụng MUA để lấy mail thông qua giao thức POP3/IMAP.
    
 - **Sơ đồ đường đi**:

   ![Qua trinh MUA MTA MDA drawio (1)](https://github.com/user-attachments/assets/91b2949c-d390-4b4f-b0d2-36cdd3e5d5da)


 
 
 

