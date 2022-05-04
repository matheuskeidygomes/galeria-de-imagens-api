# Galeria de Imagens

Galeria de imagens feita com NodeJS, ExpressJS e MySQL. Para listar, armazenar e excluir imagens no banco de dados.

![Node](https://img.shields.io/badge/Node-v16.14%20(LTS)-brightgreen)
![Npm](https://img.shields.io/badge/Npm-v8.3.1-blue) 
![License](https://img.shields.io/badge/License-MIT-red)

-------------------------------------------------------------------------------

<h2 align="center">
 <a href="#Status">Status</a> •
 <a href="#Features">Features</a> •
 <a href="#Pré-requisitos">Pré-requisitos</a> • 
 <a href="#Rodando-a-aplicação">Rodando a aplicação</a> • 
 <a href="#Testes">Testes</a> • 
 <a href="#Rotas">Rotas</a> • 
 <a href="#Tecnologias">Tecnologias</a> • 
 <a href="#Autor">Autor </a>
</h2>

--------------------------------------------------------------------------------

# Status

:heavy_check_mark: Finalizado

--------------------------------------------------------------------------------

# Features

- [x] Listar imagens armazenadas no banco de dados.
- [x] Cadastrar novas imagens no banco de dados.
- [x] Excluir imagens do banco de dados.
- [x] Visualizar imagem específica.

--------------------------------------------------------------------------------

# Pré-requisitos

Será necessário ter instalado em sua máquina as seguintes ferramentas:
[Git](https://git-scm.com), [Node.js](https://nodejs.org/en/). Também é 
aconselhável ter um editor para trabalhar com o código, como o [VSCode](https://code.visualstudio.com/).
O banco de dados desta aplicação se encontra na nuvem, porém se desejar roda-lo em sua máquina local, é aconselhável instalar o [MySQL](https://dev.mysql.com/downloads/mysql/) e um Gerenciador de banco de dados, como o [DBeaver](https://dbeaver.io/download/).

```bash

# Versão Node utilizada nesta aplicação: v16.14 (LTS)

```

--------------------------------------------------------------------------------

# Rodando a aplicação

```bash

# Clone este repositório
$ git clone <https://github.com/matheuskeidygomes/galeria-de-imagens-back-end-api.git>

# Acesse a pasta do projeto no terminal/cmd
$ cd galeria-de-imagens-back-end-api

# O banco de dados desta aplicação se encontra na nuvem, caso deseje rodar com banco local,  
# crie um arquivo ".env" na raiz do projeto, e insira as variáveis de ambiente responsáveis 
# pela conexão com o banco de dados local: MYSQL_HOST, MYSQL_USER, MYSQL_PASSWORD e MYSQL_PORT.

# Instale as dependências
$ npm install

# Antes de executar a aplicação, caso esteja rodando com banco local, verifique se o serviço do MySQL se encontra
# ativo, e certifique-se de realizar o backup do arquivo sql presente na raiz do projeto, pois o mesmo é responsável 
# pela criação do banco de dados utilizado na aplicação.  

# Execute a aplicação 
$ npm start

# O servidor iniciará na porta:3333 - acesse <http://localhost:3333>

```

------------------------------------------------------------------------------

# Rotas

## (Público) GET /images

Este endpoint é utilizado para visualizar a lista de imagens cadastradas.

### RESPOSTAS

#### OK! 

Caso essa seja a resposta, você vai receber uma lista com os dados das imagens cadastradas no banco de dados.

Exemplo de resposta:

```bash

[

    {
        "id": 1,
        "image": "716f590dc928edf80a62161c32cc932d.jpg",
        "imageTitle": "titulo da imagem",
        "path": "files/716f590dc928edf80a62161c32cc932d.jpg"
    },
    {
        "id": 2,
        "image": "716f590dc928edf80adasdadas32cc932d.jpg",
        "imageTitle": "titulo da imagem 2",
        "path": "files/716f590dc928edf80a621dsadasadd.jpg"
    }

]

```


----------------------------------------------------------------------------------------------

## (Público) GET /images/:id

Este endpoint é utilizado para visualizar uma imagem em específico no banco de dados.

### PARÂMETROS

É necessário passar o id da imagem desejada na url.

Exemplo:

```bash

http://localhost:3333/images/10

```

### RESPOSTAS

#### OK! 

Caso essa seja a resposta, você vai visualizar os dados da imagem desejada.

Exemplo de resposta:

```bash

{
    "id": 1,
    "image": "716f590dc928edf80a62161c32cc932d.jpg",
    "imageTitle": "titulo da imagem",
    "path": "files/716f590dc928edf80a62161c32cc932d.jpg"
}

```

-------------------------------------------------------------------------------------------


## (Público) DELETE /images/:id

Este endpoint é utilizado para deletar uma imagem específica no banco de dados.

### PARÂMETROS

É necessário passar o id da imagem a ser deletada na url.

Exemplo:

```bash

http://localhost:3333/images/10

```

### RESPOSTAS

#### OK! 

Caso essa seja a resposta, a imagem será deletada com sucesso.


-------------------------------------------------------------------------------------------


## (Público) POST /upload

Este endpoint é utilizado para inserir uma nova imagem no banco de dados.

### PARÂMETROS

Devem ser enviados o título da imagem e o arquivo da imagem (via form data).

Exemplo:

```bash

{
    "imageTitle": "titulo da imagem",
    "file": "716f590dc928edf80a62161c32cc932d.jpg"
}

```

### RESPOSTAS

#### OK! 

Caso essa seja a resposta, você vai receber de volta o filename da imagem inserida.

Exemplo de resposta:

```bash

{
    "image": "716f590dc928edf80a62161c32cc932d.jpg"
}

```

-------------------------------------------------------------------------------------------------------

# Tecnologias 

![Javascript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![NodeJS](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express.js-404D59?style=for-the-badge)
![MySQL](https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white)

-------------------------------------------------------------------------------------------------------

# Autor

Desenvolvido por <a href="https://github.com/matheuskeidygomes"> Matheus Keidy </a>. Entre em contato!  
  
[![Linkedin](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/matheus-keidy-7b9886190/)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:matheuskeidygomes@gmail.com)











