    docker exec -it ftpd_server /bin/bash
        pure-pw useradd admin -f /etc/pure-ftpd/passwd/pureftpd.passwd -m -u ftpuser -d /var/www/html