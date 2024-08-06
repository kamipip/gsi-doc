# Configuração do WordPress

## Introdução

O WordPress é um sistema de gerenciamento de conteúdo que facilita a criação e gestão de sites. Abaixo estão os passos para configurar o WordPress em um servidor.

## Passos para Configuração

### Instalação do Apache e PHP

   Primeiro, instale o Apache e PHP:

   ```bash
   sudo apt install apache2
   sudo apt install php libapache2-mod-php php-mysql

### Instalação do MariaDB

Instale o MariaDB:

```bash
sudo apt install mariadb-server mariadb-client

   Configure o MariaDB com o comando:

```bash
sudo mysql_secure_installation

### Criação do Banco de Dados para o Wordpress

Acesse o MariaDB como root:

``` bash
sudo mysql -u root -p

```

No prompt do MariaDB, crie um banco de dados e um usuário para o Wordpress:

```bash 
CREATE DATABASE wordpress;
GRANT ALL PRIVILEGES ON wordpress.* TO 'wpuser'@'localhost' IDENTIFIED BY 'senha_forte';
FLUSH PRIVILEGES;
EXIT;
```

### Download e Configuração do WordPress

    Faça o download do WordPress:

```bash

cd /tmp
wget https://wordpress.org/latest.tar.gz
tar -xvzf latest.tar.gz
```
    Mova os arquivos do WordPress para o diretório raiz do Apache:

```bash
sudo mv wordpress/* /var/www/html/
```

### Configuração do WordPress

    Altere as permissões dos arquivos do WordPress:

```bash
sudo chown -R www-data:www-data /var/www/html/
sudo chmod -R 755 /var/www/html/
```
    Renomeie o arquivo wp-config-sample.php para wp-config.php:

```bash
cd /var/www/html/
sudo mv wp-config-sample.php wp-config.php
```
    Edite o arquivo wp-config.php para adicionar as informações do banco de dados:

```bash
sudo nano wp-config.php
```
    No arquivo wp-config.php, atualize as seguintes linhas com as informações do banco de dados:

```bash
define('DB_NAME', 'wordpress');
define('DB_USER', 'wpuser');
define('DB_PASSWORD', 'senha_forte');
define('DB_HOST', 'localhost');

###  Conclusão da Instalação

Abra o navegador e acesse o endereço do seu servidor para concluir a instalação do WordPress:

```bash

http://seu_servidor_ip
``
