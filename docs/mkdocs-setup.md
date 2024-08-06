# Configuração do MkDocs

## Introdução

MkDocs é uma ferramenta para criar documentação estática a partir de arquivos Markdown. É fácil de configurar e oferece uma maneira prática de gerar sites de documentação.

## Passos para Configuração

### Instalação do MkDocs

   Para instalar o MkDocs, use o pip:

   ```bash
   sudo apt install python3-pip
   sudo pip3 install mkdocs
```
###  Criação de um novo projeto
   Crie um novo projeto MkDocs:
	```bash 
   mkdocs new my-docs
   cd my-docs```

### Adicionando Conteúdo

No diretório `docs/`, adicione arquivos Markdown para criar suas páginas. Edite o arquivo `mkdocs.yml` para configurar o menu de navegação e as páginas.

### Construindo o Site

Gere o site estático com o comando:

```bash
mkdocs build
```

### Visualizando Localmente

Para visualizar o site localmente:

```bash
mkdocs serve
```
Acesse http:127.0.0.1:8000 no seu navegador.

### Configuração do Apache

Para servir o site com Apache, copie os arquivos da pasta site gerada para o diretório do Apache e configure o Apache para servir o conteúdo.


