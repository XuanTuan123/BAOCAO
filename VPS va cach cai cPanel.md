
**Chuẩn bị hệ thống**
-
**1. Cập nhật các gói**

Sử dụng 2 lệnh sau:

     apt update -y
     apt upgrade -y

**2. Tải cPanel**

     cd /home && curl -o latest -L https://securedownloads.cpanel.net/latest && sh latest

**3. Tạo file cpanel.config**

     mkdir /root/cpanel_profile
     touch /root/cpanel_profile/cpanel.config

**4. Kiểm tra phiên bản MySQL**

     mysql -V

![image](https://github.com/user-attachments/assets/f437ba21-6a38-4eb5-b645-6e844eb7b076)

Ví dụ: mysql mariadb = 10.6 thì 

     echo "mysql-version=10.6" > /root/cpanel_profile/cpanel.config

**5. Xem tiến trình cài đặt**

     tail -f /var/log/cpanel-install.log

![image](https://github.com/user-attachments/assets/6d31e619-4b45-47e2-a649-9b3b9658c095)

**6. Xem trạng thái dịch vụ**

     service cpanel status
     service cpanel restart

![image](https://github.com/user-attachments/assets/d34cf930-9587-48d4-8b7c-36bb14567e4d)

*Nâng cấp phiên bản Ubuntu*

     do-release-upgrade 

**Thông tin đăng nhập WHM**
-
https://ip-server-vps:2087 hoặc https://ten-vps.cprapid.com:2087

User: root

Passwd: passwd root server

**Thông tin đăng nhập cPanel**
-
https://ip-server-vps:2083 hoặc https://ten-vp.cprapid.com:2083

User: user được tạo trong WHM 

Passwd: passwd được tạo cho user

=================================================

**Lệnh xem thông tin disk free**:

     free -m

![image](https://github.com/user-attachments/assets/c2f03521-009c-49e8-853f-1e57d00e96f9)

**Lệnh xem thông tin đăng nhập**:

     cat /usr/local/cpanel/logs/login_log

![image](https://github.com/user-attachments/assets/a863dcdc-54e4-4e1d-93e7-7bb7a10c6f11)

=================================================


**Kiểm tra dịch vụ exim (quá trình MTA)**:

    systemctl status exim
    cat /var/log/exim_mainlog
    grep 'dia-chi-email-gui' /var/log/exim_mainlog

*Xem log theo ID của email*

    grep 'id-email' /var/log/exim_mainlog

=================================================

**Kiểm tra dịch vụ dovecot (quá trình MDA)**:

    systemctl status dovecot
    cat /var/log/mail.log 
    tail -f /var/log/mail.log 

*Xem log theo địa chỉ của email*

    grep 'dia-chi-email-nhan' /var/log/mail.log
