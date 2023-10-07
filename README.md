# phpiggy

 A PHP application for tracking expenses.

## How to build at first

1. Need XAMPP, Composer
2. xampp\apache\conf\extra\httpd-vhosts.conf
   > <VirtualHost *:80>
    DocumentRoot "G:/xampp/htdocs/phpiggy/public"  # 指定文件根目錄
    ServerName phpiggy.local # 自訂伺服器名稱
    <Directory "G:/xampp/htdocs/phpiggy/public">
    RewriteEngine On # 能在不同 Routes 中切換
    RewriteCond %{REQUEST_FILENAME} !-d
    RewriteCond %{REQUEST_FILENAME} !-f
    RewriteRule ^ /index.php [L]
    </Directory>

3. C:\Windows\System32\drivers\etc\hosts
   > #XAMPP Virtual Hosts
    127.0.0.1 phpiggy.local # 設定虛擬主機
4. 產生 vendor (composer.json)
   > composer dump-autoload

## Build this project

Terminal
> composer install
