# Cadastro de Usuários
## Descrição
Aplicação de cadastro de usuários

## Variáveis de ambiente
Os projetos <b>cadastro-usuarios-web</b> e <b>cadastro-usuarios-ws</b> possuem os seus arquivos de configuração de variáveis de ambiente (.env) em seus respectivos diretórios.


### cadastro-usuarios-web (Frontend)
- BASE_URL: URL da aplicação backend.

### cadastro-usuarios-ws (Backend)
- PORT: Porta da aplicação backend;
- HOST: Endereço (HOST) da aplicação backend;
- SECRET: Chave aleatória do algoritmo SHA-256 para criptografia do token JWT;
- POSTGRES_URL: URL do banco de dados;
- POSTGRES_PASSWORD: Senha do banco de dados Postgres.

### db (Banco de Dados)
O banco de dados é construido no docker-compose e linkado ao container da aplicação backend (cadastro-usuarios-ws).

```yml
db:
    image: postgres
    restart: always
    env_file:
      - db.env
    ports:
      - 5432:5432
```

- POSTGRES_PASSWORD: Senha do banco de dados;
- POSTGRES_USER: Usuário do banco de dados;
- POSTGRES_DB: Nome do banco de dados;
- POSTGRES_URL: URL do banco de dados;
- POSTGRES_PASSWORD: Senha do banco de dados Postgres.

## Instruções para execução
- Faça o clone do projeto:
```
git clone https://github.com/feliperibeiroo/cadastro-usuarios.git
```

- Para subir a aplicação, executar o comando:
```
docker-compose up
```
