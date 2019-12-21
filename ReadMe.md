## Docker ftp user password changed..
    docker-compose up -d
- later
  
        docker exec -it ftpd_server /bin/bash
    - set password ftp
  
            pure-pw useradd admin -f /etc/pure-ftpd/passwd/pureftpd.passwd -m -u ftpuser -d /var/www/html
    - then set docker-compose.yml

            environment:
                PUBLICHOST: "localhost"
                FTP_USER_NAME: "admin"
                FTP_USER_PASS: "<your-password>"
                FTP_USER_HOME: "/var/www/html/ftp"
