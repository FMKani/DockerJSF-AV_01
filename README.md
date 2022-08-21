# Atividade-DAC-1-DockerJSF

## Etapa 1/2

### Teste de objetivos de aprendizagem
		1. Qual a diferença entre image e container?
		2. Qual a diferença entre os comandos COPY, EXPOSE e ADD?
		3. Qual a diferença entre os comandos RUN, CMD e ENTRYPOINT?
		4. Qual a diferença entre as estratégias de shell e exec?
		5. Qual a diferença entre os comandos docker stop <container_id> e docker
		kill <container_id>?


## Etapa 2/2

### Atividade prática
Desenvolva uma aplicação que realize as operações de CRUD para a entidade Livro e
Editora. A funcionalidade precisa estar disponível com UI (interface para o usuário) com um
template usável. A aplicação desenvolvida precisa estar disponível em contêiner. As demais
informações de cadastro podem ser inseridas via script sql.
		
    class Livro{
      private int id;
      private String titulo;
      private LocalDate dataDeLancamento;
    }
    class Editora{
      private int codigo;
      private String localDeOrigem;
      private String nomeFantasia;
    }
### Requisitos

● RF01 - Implementar classes de acesso aos dados (em memória e via JDBC);<br>
● RF02 - Criar as páginas para edição e listagem da entidade Livro;<br>
● RF03 - Criar as páginas para edição e listagem da entidade Editora;<br>
● RF04 - Criar uma página para realizar uma busca de Livro por titulo;<br>
● RF05 - Criar uma página para realizar uma busca de Editora por localDeOrigem;<br>
● RF06 - Realizar o deploy da aplicação no Docker usando uma das images do Payara;<br>
● RF07 - Realizar o deploy da aplicação usando o Docker Compose.<br>

### Script do banco

O script para criação do banco.

    CREATE TABLE livro(
        id serial PRIMARY KEY,
        titulo VARCHAR(80),
        dataDeLancamento DATE
    );
    CREATE TABLE editora(
        codigo SERIAL PRIMARY KEY,
        localDeOrigem VARCHAR(100),
        nomeFantasia VARCHAR(100)
    );
