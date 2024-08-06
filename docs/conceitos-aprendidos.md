# Conceitos Aprendidos

## Instalação do MkDocs

MkDocs é uma ferramenta de geração de sites estáticos a partir de arquivos Markdown, ideal para criar documentação de projetos. O processo de instalação envolve a utilização do `pip`, o gerenciador de pacotes do Python, e comandos para criar e configurar um novo projeto MkDocs.

## Instalação do Apache

O Apache é um dos servidores web mais populares do mundo. Ele permite hospedar sites e aplicações web. A instalação do Apache envolve o uso do gerenciador de pacotes do sistema operacional para instalar o software, seguido de configuração para servir o conteúdo da web.

## Instalação do WordPress

WordPress é um sistema de gerenciamento de conteúdo (CMS) amplamente utilizado para criar sites e blogs. A instalação do WordPress inclui a configuração de um servidor web (como Apache), instalação do PHP e MySQL (ou MariaDB), e o download e configuração do WordPress em si. Também pode incluir a instalação de ferramentas adicionais como o PhpMyAdmin para gerenciar o banco de dados.

## Configuração do Apache para Servir o Site MkDocs

Depois de gerar um site estático com MkDocs, você pode usar o Apache para servir o site. Isso envolve copiar os arquivos gerados para o diretório do Apache e configurar o servidor Apache para apontar para esses arquivos.

## Visualização Local de Sites MkDocs

O MkDocs possui um servidor embutido que permite visualizar o site localmente durante o desenvolvimento. Usar `mkdocs serve` inicia um servidor local que serve o site na URL `http://127.0.0.1:8000`, facilitando a visualização e teste das mudanças em tempo real.

## Ferramentas e Comandos Comuns

### Ferramentas:
- **pip**: Gerenciador de pacotes do Python.
- **Apache**: Servidor web.
- **MySQL/MariaDB**: Sistemas de gerenciamento de banco de dados.
- **PhpMyAdmin**: Ferramenta de administração de MySQL/MariaDB via web.

### Comandos:
- **Instalação de Pacotes**: `sudo apt install <pacote>`
- **Gerenciamento de Banco de Dados**: `sudo mysql_secure_installation`
- **Servir Conteúdo Localmente**: `mkdocs serve`
