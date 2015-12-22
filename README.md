# apache24-vhost
<VirtualHost *:80>
    ServerName www.example1.com
    ServerAdmin root@www.example1.com
    DocumentRoot /home/sites/projects/www.example1.com/htdocs
 
    ErrorLog  /var/log/httpd/www.example1.com-error_log
    CustomLog /var/log/httpd/www.example1.com-access_log combined env=!no_log
    <Directory "/home/sites/projects/www.example1.com/htdocs/>
        Options Includes ExecCGI FollowSymLinks
        AllowOverride All
        Require all granted
    </Directory>
</VirtualHost>
