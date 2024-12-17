# 📦 Projeto CRUD de Produtos com Spring Boot

Este projeto é um sistema **CRUD (Create, Read, Update, Delete)** de gerenciamento de produtos desenvolvido utilizando **Spring Boot** e **Thymeleaf** para a camada de apresentação. É uma aplicação simples que permite cadastrar, listar, editar e excluir produtos.

---

## 🛠️ Tecnologias Utilizadas
As principais tecnologias e ferramentas utilizadas no projeto incluem:

- **Java**: Linguagem principal de programação.
- **Spring Boot**: Framework que agiliza o desenvolvimento de aplicações Java.
- **Thymeleaf**: Motor de templates utilizado na renderização do HTML.
- **Bootstrap**: Framework CSS para estilização e responsividade da interface.
- **Banco H2**: Banco de dados em memória para teste e desenvolvimento.
- **HTML/CSS**: Estrutura e estilo das páginas.
- **Maven**: Gerenciador de dependências do projeto.

---

## 🚀 Funcionalidades

- **Listar produtos**: Exibe todos os produtos cadastrados em uma tabela.
- **Cadastrar um novo produto**: Inclui produtos com informações como nome, preço e descrição.
- **Atualizar produto**: Permite editar as informações de um produto já existente.
- **Excluir produto**: Remove o produto selecionado.
- **Banco em memória**: Utiliza o banco **H2**, que facilita o desenvolvimento rápido, sem configuração externa.
- **Importação inicial de dados**: O arquivo `import.sql` insere dados iniciais automaticamente.

---

## 📂 Estrutura do Projeto
Abaixo está uma descrição simplificada da estrutura de pastas do projeto:

```
crud-produto/
|
├── src/
|   ├── main/
|   │   ├── java/com/exemplo/crudproduto/
|   │   │   ├── controller/         # Controladores responsáveis (ProdutoController)
|   │   │   ├── entidades/          # Classe de entidade Produto
|   |   |   ├── servicos/           # Servicos 
|   │   │   └── repository/         # Interfaces de acesso aos dados (Spring Data JPA)
|   │   │
|   │   ├── resources/
|   │   │   ├── templates/
|   │   │   │   ├── produtos/       # Templates Thymeleaf
|   │   │   │   │   ├── listar.html # Tela de listagem de produtos
|   │   │   │   │   └── formulario.html # Tela de cadastro/edição de produtos
|   │   │   │
|   │   │   ├── application.properties # Configurações do Spring Boot e banco H2
|   │   │   └── import.sql         # Dados iniciais para o banco H2
|   │
|   └── pom.xml                   # Gerenciamento de dependências Maven
|
├── target/                       # Arquivos gerados após compilação (ignorar)
|
└── README.md                     # Documentação do projeto
```

---

## 🔏 Configuração do Banco H2

O projeto utiliza o **banco de dados em memória H2** configurado no arquivo `application.properties`.

**Propriedades principais**:
```properties
spring.h2.console.enabled=true
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=
spring.jpa.hibernate.ddl-auto=update
```

**Acesso ao console do banco H2**:
- URL: `http://localhost:8080/h2-console`
- JDBC URL: `jdbc:h2:mem:testdb`
- Username: `sa`
- Password: (deixe vazio)

O arquivo `import.sql` adiciona dados iniciais automaticamente ao banco.

---

## 💼 Como Rodar o Projeto

1. **Pré-requisitos**:
   - Java 17 (ou superior)
   - Maven instalado

2. **Passos**:
   - Clone o repositório:
     ```bash
     git clone https://github.com/FelipeTiLustosa/CrudProducts-SpringBoot.git
     ```
   - Acesse o diretório:
     ```bash
     cd CrudProducts-SpringBoot
     ```
   - Execute o projeto com Maven:
     ```bash
     mvn spring-boot:run
     ```
   - Acesse a aplicação no navegador:
     - Listagem de Produtos: `http://localhost:8080/produtos`
     - Console H2: `http://localhost:8080/h2-console`

---

## 🔊 Exemplo das Páginas

- **Listar Produtos**:
   - Exibe todos os produtos cadastrados em uma tabela.
   - Botões para **Editar** e **Excluir**.
- **Formulario de Cadastro/Atualização**:
   - Formulário com campos: **Nome**, **Preço**, **Descrição**.

---

## ✨ Contribuição

1. Fork o projeto
2. Crie uma branch:
   ```bash
   git checkout -b minha-nova-feature
   ```
3. Adicione suas modificações e faça commit:
   ```bash
   git commit -m "Adicionei nova feature"
   ```
4. Suba as alterações:
   ```bash
   git push origin minha-nova-feature
   ```
5. Abra um Pull Request

---

## 💼 Contato

- **Nome**: Felipe Lustosa Carvalho
- **E-mail**: felipelustosa915@gmail.com
- **LinkedIn**: https://www.linkedin.com/in/felipe-lustosa-carvalho-6a3581276/

---

## 🌎 Licença

Este projeto está licenciado sob a licença MIT - veja o arquivo [LICENSE](LICENSE) para mais detalhes.
