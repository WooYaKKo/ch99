# ch99
https://github.com/WooYaKKo/ch99.git

# pip install mysqlclient 설치시 에러
'''bash
yum install mariadb-devel python3-devel
pip install mysqlclient
'''
# MariaDB 외부 연동시 에러
'''sql
mysql -u root -p
'''
- 모든 IP 접근
'''sql
SELECT Host,User,plugin,authentication_string FROM mysql.user;
GRANT ALL PRIVILEGES ON *.* TO '아이디'@'%' IDENTIFIED BY '패스워드';
'''
- 특정 IP
'''sql
GRANT ALL PRIVILEGES ON *.* TO '아이디'@'111.222.%' IDENTIFIED BY '패스워드';
'''
