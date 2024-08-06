# Comandos Utilizados

```bash
sudo apt install python3-pip
sudo pip3 install mkdocs
mkdocs new my-docs
cd my-docs
mkdocs build
mkdocs serve
# Acesse http://127.0.0.1:8000 no navegador
# Copiar os arquivos da pasta site gerada para o diretório do Apache
# Configurar o Apache para servir o conteúdo
```

```bash
sudo apt update
sudo apt upgrade
sudo apt install apache2
systemctl status apache2
systemctl is-enabled apache2
ip addr | grep inet
sudo apt install mariadb-server mariadb-client
systemctl status mariadb.service
sudo mysql_secure_installation
sudo apt install php libapache2-mod-php php-mysql
sudo systemctl restart apache2
sudo apt install phpmyadmin
sudo systemctl reload apache2.service
wget -c http://wordpress.org/latest.tar.gz
tar -xzvf latest.tar.gz
sudo cp -R wordpress /var/www/html/{nome do seu projeto}
sudo chmod -R 775 /var/www/html/{nome do seu projeto}/
sudo mysql -u root -p
CREATE DATABASE {nome do seu projeto};
sudo apt install nautilus-admin
sudo reboot
cd wordpress/
sudo mv wp-config-sample.php wp-config.php
sudo vim /etc/apache2/sites-available/{nome do seu projeto}.conf
# Adicionar no arquivo:
# <VirtualHost *:80>
# ServerName jurandajob
# ServerAdmin root@localhost
# DocumentRoot /var/www/html/jurandajob
# ErrorLog ${APACHE_LOG_DIR}/error.log
# CustomLog ${APACHE_LOG_DIR}/access.log combined
# </VirtualHost>
apachectl -t
# Adicionar no arquivo /etc/apache2/apache2.conf:
# ServerName localhost
sudo a2ensite {nome do seu projeto}.conf
systemctl reload apache2
sudo a2dissite 000-default.conf
# Acessar no navegador:
# http://{seu_ip}/wp-admin/install.php

```
