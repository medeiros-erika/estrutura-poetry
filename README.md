Estou aprendendo a utilizar o Poetry como ferramenta de gerenciamento de dependências e empacotamento.


Alguns comandos básicos:

- Instalar o poetry
- Ver versão do poetry instalado
- Criar novo projeto - gera o arquivo pyproject.toml

      poetry new <nome_project>: cria um novo projeto poetry
      


- Criar a virtualenv
  
O  comando abaixo:
     
     python3 -m venv venv
     
Pode ser substituído por (já ativa a venv):
     
     poetry shell

- Criar a virtualenv dentro do projeto/pasta: 
  
    poetry config virtualenvs.in-project true



## O que consta no arquivo pyproject.toml


[tool.poetry] #setup.py
name = "projeto-python"
version = "0.1.0"
description = ""
authors = ["medeiros-erika <ems.erikamedeiros@gmail.com>"]

[tool.poetry.dependencies] #requeriments.txt
python = "^3.9.9"

[tool.poetry.dev-dependencies] #requeriments-dev.txt
pytest = "^5.2"

[build-system]
requires = ["poetry-core>=1.0.0"] #setuptools
build-backend = "poetry.core.masonry.api"

## O que consta no arquivo poetry.lock

Comando que instala os pacotes determinados no pyproject.toml:

     poetry install

O comando acima cria o arquivo com as dependências: poetry.lock

Ver as dependências instaladas:

    poetry show


## Como instalar pacotes e dependências no poetry

    
     poetry add <pandas>

Instalando pacotes com poetry, não precisamos sempre atualizar o requeriments.txt (que foi gerado com o 'pip install -r requirements.txt') como acontece quando é feito o 'pip freeze > requirements.txt'

## Como instalar pacotes e dependências somente no ambiente de desenvolvimento

     poetry add --dev pytest-asyncio

     poetry remove --dev pytest-asyncio # deletar o pacote


## Criando um CLI

#identificar o script no pyproject.toml, após isso rodar o script

     [tool.poetry.scripts]
     meu-script = 'projeto.cli:cli'


### Rodar meu-script
     poetry run meu-script # nome do script setado no arquivo pyproject.toml

## Como buildar o código?

Comando para criar deliverable package.

     poetry build


