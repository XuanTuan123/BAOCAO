**Tổng hợp các dịch vụ Email**
-
**1. Email Hosting**: Là dịch vụ phù hợp với doanh nghiệp vừa và nhỏ, không có đội ngũ IT chuyên sâu để quản lý.

Nhược điểm: 

    - Phụ thuộc vào nhà cung cấp dịch vụ (nhà cung cấp dịch vụ chỉ cung cấp user đăng nhập mail).
    - Nếu 1 người sử dụng chung nguồn IP đó bị đánh dấu spam, thì sẽ ảnh hưởng đến uy tín và khả năng gửi email. Tuy nhiên, điều này có thể giải quyết bằng việc sử dụng thêm dịch vụ Email Relay để bị đưa vào danh sách spam.
    
 Ưu điểm: 
 
    - Dễ triển khai, không cần quản lý quá nhiều về mặt kỹ thuật.
    - Giảm thiểu tình trạng email bị đánh dấu spam, bị đưa vào blacklist IP.
    - Tăng độ uy tín của thương hiệu doanh nghiệp.
    - Việc bảo trì đều được đội ngũ kỹ thuật hỗ trợ 24/7.
    
Một số nhà cung cấp dịch vụ email hosting uy tín như là Vinahost,...

**2. Email Relay**: là dịch vụ email chuyển tiếp, là quá trình sử dụng một máy chủ trung gian có độ uy tín IP cao để gửi mail đến địa chỉ được chỉ định.

 Nhược điểm:
 
    - Chi phí bảo trì rất tốn kém, cần đầu tư vào hạ tầng, nhân lực chuyên môn.
    - Cần kiến thức chuyên môn hiểu các tiêu chuẩn xác thực như SPF, DKIM, DMARC để tối ưu hóa cho chiến dịch email marketing của mình.
    - Phụ thuộc vào nhà cung cấp dịch vụ relay.
    
 Ưu điểm:
 
    - Cải thiện độ tin cậy và khả năng gửi mail, giảm tỉ lệ bị đánh dấu spam.
    - Bảo mật và kiểm soát đường đi của các email được chuyển tiếp, ẩn thông tin máy chủ nội bộ gửi đi.
    - Giúp quản lý lưu lượng phân phối email hiệu quả, tránh việc máy chủ nội bộ bị quá tải.
    - Đảm bảo các email từ máy chủ gửi đi đều tuân thủ các tiêu chuẩn xác thực như SPF, DKIM, DMARC, giúp email không bị từ chối bởi người nhận.

**3. Email Marketing**: là dịch vụ phù hợp cho doanh nghiệp cần triển khai chiến dịch quảng bá, bán hàng và thiếp thị sản phẩm với số lượng lớn đến tệp khách hàng mục tiêu.

 Nhược điểm:
 
    - Email marketing dễ bị đánh dấu spam.
    - Đối mặt với sự thờ ơ của khách hàng đới với email quảng cáo.
    - Phụ thuộc vào khả năng kết nối Internet của khách hàng.
    
 Ưu điểm:
 
    - Doanh nghiệp dễ dàng truyền tải thông tin chiến dịch đến với khách hàng mục tiêu.
    - Nâng cao giá trị thương hiệu của doanh nghiệp. 
    - Giúp doanh nghiệp có thể theo dõi chỉ số (tỉ lệ mở mail, tỉ lệ nhấp chuột) để tìm ra cách xây dựng email marketing tốt nhất nhờ công cụ Google Analytics.
    - Chi phí thấp so với việc quảng bá truyền thống.

Tuy nhiên, việc triển khai Email Marketing cần tuân thủ quy định như Luật chống Spam CAN-SPAM ở Mỹ, GDPR ở Châu Âu.

**4. Các phương thức xác thực email phổ biến**

**SPF (Sender Policy Framework)**: là phương thức xác thực địa chỉ người dùng.

**DKIM (DomainKeys Identified Mail)**: là phương pháp xác thực mail dựa trên chữ ký số, kiểm tra nội dung email có bị thay đổi không nhờ cặp khóa công khai và riêng tư.

    - Khóa công khai được lưu trên DNS server.
    - Khóa riêng tư được lưu trên Email Server để tạo chữ ký số.

**DMARC (Domain-based Message Authentication, Reporting, and Conformance)**: là phương pháp giải quyết hạn chế các giao thức xác thực email.

    - Hoạt động dựa trên hai phương thức phổ biến là SPF và DKIM.
     
Cả ba phương thức trên đều lưu trữ ở DNS server.

**Giải pháp cho những vấn đề trên**
-
**1. Email filter**: là giải pháp chặn các email không mong muốn và có khả năng gây nguy hiểm như thư rác, mạo danh lừa đảo, virus và các dạng phần mềm độc hại khi sử dụng Email Hosting, Email Server. Chức năng chính của Email filter:

- Phân loại email.
- Loại bỏ thư rác.
- Chặn email (blacklist).
- Cho phép mail (whitelist).
- Bảo mật mail.
- Quản lý dung lượng hộp thư.

**2. Email server**: là hệ thống hỗ trợ việc gửi/ nhận email và lưu trữ mail.

Có hai loại chính: 

    - Incoming Mail Server (xử lý mail đến, sử dụng giao thức SMTP/POP3).
    - Outgoing Mail Server (xử lý mail gửi đi, sử dụng giao thức IMAP).

Các chức năng chính: 
- Cho phép gửi/nhận thông qua giao thức SMTP
cổng 25 mặc định thường bị chặn do spam, cổng 465/587 kết nối bảo mật SSL/TSL; POP3 (cổng 110 không mã hóa, cổng 995 kết nối bảo mật SSL/TLS).
- Quản lý hộp thư (hộp thư, thư nháp, đã gửi, thư rác, thùng rác, lưu trữ).
- Lọc spam.
- Xác thực email thông qua SPF, DKIM, DMARC.
- Quản lý nhóm.

**3. Email hybrid**: là giải pháp kết hợp Email hosting với các dịch vụ Email Google Workspace, Email Microsoft 365. Cho phép các thao tác thực hiện gửi và nhận cơ bản trên cả hai nền tảng cPanel và Email Google Workspace, Email Microsoft 365.

    - Hoạt động dựa trên mô hình song song 
    - Các email gửi từ môi trường Internet đến máy chủ Email Google Workspace, Email Microsoft 365 sẽ được xử lý trước, nếu như địa chỉ không tồn tại thì email được chuyển tiếp về Email Hosting.
    
 Ưu điểm:
 
    - Tối ưu chi phí quản lý cho doanh nghiệp.
    - Sử dụng nhiều tính năng kết hợp trên cả 2 nền tảng.
    - Hỗ trợ cộng tác mạnh mẽ trong công việc khi mọi người đều có thể kết hợp với nhau trên nền tảng Email hybrid.

