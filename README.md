Estou aprendendo a utilizar o Poetry como ferramenta de gerenciamento de dependências e empacotamento.


Alguns comandos básicos:

- Instalar o poetry
- Ver versão do poetry instalado
- Criar novo projeto - gera o arquivo pyproject.toml

      poetry new <nome_project>: cria um novo projeto poetry
      


- Criar a virtualenv
O  comando abaixo:
     
     python3 -m venv venv
     
Pode ser substituído por:
     
     poetry shell

- Criar a virtualenv dentro do projeto/pasta: 
  
    poetry config virtualenvs.in-project true

- Adicionar/instalar bibliotecas e dependências no projeto:
    
     poetry add <pandas>

