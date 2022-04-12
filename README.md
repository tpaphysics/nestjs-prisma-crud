<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="200" alt="Nest Logo" /></a>
</p>

[circleci-image]: https://img.shields.io/circleci/build/github/nestjs/nest/master?token=abc123def456
[circleci-url]: https://circleci.com/gh/nestjs/nest

  <p align="center">A progressive <a href="http://nodejs.org" target="_blank">Node.js</a> framework for building efficient and scalable server-side applications.</p>
    <p align="center">
<img src="https://img.shields.io/badge/yarn-%232C8EBB.svg?style=for-the-badge&logo=yarn&logoColor=white" alt="yarn" />

<img src="https://img.shields.io/badge/nestjs-%23E0234E.svg?style=for-the-badge&logo=nestjs&logoColor=white" alt="NestJs" />

<img src="https://img.shields.io/badge/Prisma-3982CE?style=for-the-badge&logo=Prisma&logoColor=white" alt="Prisma.io" />

<img src="https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />

<img src="https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white" alt="Prisma" />

## Descrição

Nessa postagem criamos um CRUD utilizando o framework [Nest](https://nestjs.com/) para criar, deletar, pesquisar e atualizar uma tabela de usuários em um banco de dados. O Nest tem se mostrado um framework poderoso para criação de APIs, neste post usamos também o [Prisma](https://www.prisma.io/) como ORM.

Criamos um schema bem simples no arquivo <strong>schema.prisma</strong> para criação de um usuário no banco de dados:

```prisma
model User {
  id    String @id @default(uuid())
  email String @unique
  name  String
}

```

## Rotas

```
Mapped {/users, POST} route
Mapped {/users, GET} route +0ms
Mapped {/users/:id, GET} route +1ms
Mapped {/users/:id, PATCH} route +1ms
Mapped {/users/:id, DELETE} route +1ms
```

## Instalação

```bash
# Instalação das dependências
$ yarn

# Iniciar container com banco de dados postgress:
$ yarn dev:db

# Migração dos models definidos no schema.prisma para o banco de dados
$ yarn prisma migrate dev
```

## Iniciando o servidor

```bash
# development
$ yarn start

# watch mode
$ startc start:dev

# production mode
$ yarn start:prod
```
## Observação

```bash
# Para remover o container criado: 
$ yarn dev:rm
```  

## **👨‍🚀 Autor**

<a href="https://github.com/tpaphysics">
<img alt="Thiago Pacheco" src="https://images.weserv.nl/?url=avatars.githubusercontent.com/u/46402647?v=4?v=4&h=300&w=300&fit=cover&mask=circle&maxage=7d" width="100px"/>
  <br />
  <sub>
    <b>Thiago Pacheco de Andrade</b>
  </sub>
</a>
<br />

👋 Meus contatos!

[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=for-the-badge&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/thiago-pacheco-200a1a86/)](https://www.linkedin.com/in/thiago-pacheco-200a1a86/)
[![Gmail Badge](https://img.shields.io/badge/-Gmail-c14438?style=for-the-badge&logo=Gmail&logoColor=white&link=mailto:physics.posgrad.@gmail.com)](mailto:physics.posgrad.@gmail.com)

## Licença

Veja o arquivo [MIT license](LICENSE).
