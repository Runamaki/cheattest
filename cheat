Commands วันที่ 14/10
1. yum install httpd php ติดตั้ง HTTP และ PHP  
   systemctl restart httpd / systemctl enable httpd  
   แก้ไขไฟล์ vi /etc/httpd/conf/httpd.conf  
   DirectoryIndex index.html index.php Index.html แก้ลำดับอินเด็กซ์  

2. useradd -d /var/www/html/test -s /bin/bash test  
   Passwd ตั้ง Password ของ User  

3. chmod ตั้งสิทธิ์ 777 ตามผู้ใช้งาน  
   chmod 775 /var/www/html/test  

Commands วันที่ 25/10
1. yum install -y vsftpd  
   แก้ไขไฟล์ vi /etc/vsftpd/vsftpd.conf  
   - anonymous_enable = NO  
   - ascii_upload_enable = YES  
   - ascii_download_enable = YES  
   - ls_recurse_enable = YES  
   - chroot_local_user = YES  
   - chroot_list_enable = YES  
   - chroot_list_file = /etc/vsftpd/chroot_list  

   เพิ่มแก้ไขไฟล์:
   1. local_root = public_html  
   2. use_localtime = YES

4. vi /etc/vsftpd/chroot_list เพิ่มชื่อ User  
5. systemctl enable --now vsftpd  
6. vi /etc/sysconfig/selinux แก้ SELINUX เป็น disable  

7. setsebool -P ftpd_full_access on  
   firewall-cmd --add-service=ftp --runtime-to-permanent  
   firewall-cmd --reload  

8. httpd  
   systemctl enable --now httpd  
   firewall-cmd --add-service=http --add-service=https --runtime-to-permanent  

9. vi /var/www/html/สร้างไฟล์ชื่อ index.html

Commands วันที่ 8/11
1. yum install mariadb-server  
   systemctl enable --now mariadb  

2. firewall-cmd --add-service=mysql --runtime-to-permanent  

3. mysql_secure_installation  
   1. Enter  
   2. N  
   3. Enter  
   4. Y  
   5. Y  
   6. Y  
   7. Y  

4. mysql -u root -p  
   1. show databases;  
   2. use ชื่อDB;  
   3. show tables;  
   4. exit;  

5. yum install epel-release -y  
/ dnf —enable repo=epel -y  
yum install phpMyAdmin php-mysqlnd  

Vi /etc/httpd/conf.d/phpMyAdmin.conf
แก้ require all granted
systectl reload httpd
