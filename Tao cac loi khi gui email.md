**EMAIL FILTERS**
-
**1. Cấu hình Email Filter**

**Bước 1**: 

- Truy cập vào cPanel: **mail.tuanhhxtts.freehost.vn:2083**

- Đăng nhập tài khoản được cấp như hình và nhấn **Log in**:

![Screenshot 2025-01-01 184613](https://github.com/user-attachments/assets/67fc745d-8e26-492e-afd6-8cdaa0ec71b8)


- Đăng nhập thành công, dashboard của **cPanel** hiện ra:

![image](https://github.com/user-attachments/assets/7126395f-c826-4d5e-ae6b-26df35c0e7f4)

**Bước 2**:

- Truy cập vào phần **"Email Filters"**:

- Nhấp vào **"Email Filters"**.
Chọn tài khoản email: **tuanhhx@tuanhhxtts.freehost.vn** (hoặc tại mục **"Filters by Users"** nhập email cần cấu hình, nhấn **Go**):

![image](https://github.com/user-attachments/assets/deb0073c-9662-47c1-831b-24a3b8373f57)

- Chọn **"Manage Filters"**.
Tạo bộ lọc mới:

- Nhấp vào **"Create a New Filter"** để tạo bộ lọc mới cho tài khoản **tuanhhx@tuanhhxtts.freehost.vn**.

**Bước 3**: Cấu hình bộ lọc:

- **Filter Name (Tên bộ lọc)**: "Chặn Spam".

- **Rules (Các điều kiện)**:

     - **Subject**: Trong phần này, bạn nhập từ khóa bạn muốn lọc: "Congratulations! You've won $1000, click now to claim your prize!"".
     
     - **Equals**: Tùy chọn này yêu cầu trường thông tin phải hoàn toàn khớp chính xác với giá trị bạn chỉ định.

- **Actions (Hành động)**:

     - **Deliver to folder**: Chọn "Spam" trong danh sách thư mục để chuyển các email có chứa **Subject** như trên vào thư mục Spam.
     
     - **Stop Processing Rules**: Nếu bạn muốn dừng các bộ lọc khác áp dụng cho email này, hãy chọn tùy chọn này.
     
- Lưu bộ lọc, xem hình sau:

![image](https://github.com/user-attachments/assets/e04d6085-4476-4142-b1ff-333ffb9572f5)

**2. Cách tạo Email Spam**

Để tạo một email có điểm spam cao (khoảng 5 điểm hoặc hơn), bạn có thể sử dụng một số kỹ thuật sau:

- Sử dụng các từ khóa spammy như "Free", "Winner", "Congratulations", "Claim your prize", "Earn money", "No cost", v.v., sẽ làm tăng điểm spam.

- Thêm các liên kết không đáng tin cậy, chẳng hạn như liên kết tới các trang web lạ hoặc liên kết giảm giá từ các nguồn không uy tín.

- Nếu email thiếu các yếu tố bảo mật như SPF và DKIM, khả năng bị đánh giá là spam cũng tăng lên.

- Tiêu đề gây hiểu nhầm hoặc chứa từ khóa spam như "URGENT!", "Limited Offer!", hoặc "Immediate Action Required!" có thể làm tăng khả năng email bị xem là spam.

- Các email sử dụng quá nhiều hình ảnh và ít nội dung văn bản có thể bị đánh giá là spam.

- Sử dụng từ viết hoa (ALL CAPS) trong tiêu đề hoặc nội dung của email có thể làm email bị đánh giá là spam.

Ví dụ: 

Tạo một email có thể có điểm spam cao từ một email cá nhân với nội dung như sau:

  - Người nhận: tuanhhx@tuanhhxtts.freehost.vn
  
  - Tiêu đề: Congratulations, You have WON a prize!
  
  - Nội dung email:
  
        Dear user,
        You have WON a FREE prize worth $1000! Click the link below to claim your reward NOW:
        [Link] www.freesomething.com
        Don't miss this LIMITED TIME offer!
        Best regards,
        [Fake Company Name]


![image](https://github.com/user-attachments/assets/5af9c591-cfe3-4c22-8354-cdc790393097)

 - Email được gửi đi, được chuyển vào thư mục **Thư rác**:

![image](https://github.com/user-attachments/assets/f5ffc39b-eb65-40cf-a5f7-8b3fed393a9c)

 - Có thể kiểm tra Email được gửi đi, được chuyển vào thư mục **Thư rác (Spam)** bằng cách xem **Track Delivery**:
 
 ![image](https://github.com/user-attachments/assets/74d0f536-ddcf-4105-a0b9-135affb930c1)
 
 ![image](https://github.com/user-attachments/assets/31c6064f-e4f4-4fc5-ac9d-6208fa6b3e26)
 
 *Delivered To: "tuanhhx+spam"@tuanhhxtts.freehost.vn* tức là email đã được chuyển vào thư mục **Thư rác** 
 
 **SPAM FILTERS**
 -
 