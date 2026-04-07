# 🎓 Aluno Online - API RESTful

Uma API robusta desenvolvida em Java com Spring Boot para o gerenciamento acadêmico. Este projeto foi construído para facilitar o controle de alunos e professores, servindo como núcleo backend para aplicações educacionais.

---

## 📖 Explicação do Projeto

O sistema **Aluno Online** é uma aplicação backend focada em operações de CRUD (Create, Read, Update, Delete). O objetivo principal é garantir o armazenamento seguro, a validação estruturada e a manipulação eficiente dos dados do corpo acadêmico (alunos e professores) de uma instituição de ensino.

O projeto foi desenvolvido focando nas boas práticas de desenvolvimento backend, garantindo que o código seja limpo, escalável e de fácil manutenção.

---

## ⚙️ Descrição da Arquitetura Utilizada

A aplicação foi estruturada seguindo o padrão de **Arquitetura em Camadas** (Layered Architecture), o que garante um excelente nível de desacoplamento. As camadas se dividem da seguinte forma:

1. **Model (Entidades):** Representação das tabelas no banco de dados. É aqui que definimos as colunas e os relacionamentos.
2. **Repository (Persistência):** Interfaces que herdam do Spring Data JPA, responsáveis por realizar toda a comunicação direta com o banco de dados PostgreSQL sem a necessidade de escrever SQL manualmente.
3. **Service (Regra de Negócio):** Camada central onde toda a lógica da aplicação acontece. Ela atua como uma ponte entre o banco de dados e os controladores, realizando validações e processamentos.
4. **Controller (Endpoints):** A porta de entrada da API. Responsável por receber as requisições HTTP (GET, POST, PUT, DELETE), encaminhar para os Services e devolver as respostas adequadas ao usuário.

---

## 📂 Detalhamento do Código

A organização dos pacotes da aplicação reflete diretamente a arquitetura escolhida, separando as responsabilidades de forma clara:

```text
src/main/java/br/com/alunoonline/api/
 ├── controller/    # Contém as classes AlunoController e ProfessorController (Rotas REST)
 ├── service/       # Contém as classes AlunoService e ProfessorService (Regras de negócio)
 ├── repository/    # Interfaces AlunoRepository e ProfessorRepository (Acesso aos dados)
 └── model/         # Entidades JPA (Aluno e Professor) que mapeiam o banco
Principais Rotas Implementadas:
POST /alunos e POST /professores: Criação de novos registros.

GET /alunos e GET /professores: Listagem de todos os cadastros.

GET /{id}: Busca de um registro específico pelo ID.

PUT /{id}: Atualização completa de um cadastro existente.

DELETE /{id}: Remoção de um registro do banco de dados.
```

## 🛠️ Tecnologias Utilizadas
Java

Spring Boot (Web, Data JPA)

PostgreSQL (Banco de dados relacional)

Maven (Gerenciamento de dependências)

## 📸 Testes e Demonstração

### 1. Requisições no Insomnia
**Criando um Aluno (POST):**
<img width="1919" height="1029" alt="CriarAlunoDepois" src="https://github.com/user-attachments/assets/138d70b5-b1f9-43be-a29d-bc9ce0af3d89" />

**Listando Professores (GET):**
<img width="1919" height="1034" alt="ListarTodosProfessores" src="https://github.com/user-attachments/assets/6a18a6d1-0d03-49d7-9497-156db2bc7ede" />


**Atualizando um Aluno (PUT):**
<img width="1919" height="1030" alt="AtualizarAlunoPorIdDepois" src="https://github.com/user-attachments/assets/ad224da1-fed1-4aad-b08a-e68ad85df42f" />


**Deletando um Professor (DELETE):**
<img width="1919" height="1027" alt="DeletarProfessorPorIdDepois" src="https://github.com/user-attachments/assets/a202f652-77a5-44b0-a7b5-0116fea0e4b2" />


### 2. Persistência no DBeaver (PostgreSQL)
**Tabela de Alunos Atualizada Depois De Testes:**
<img width="1919" height="1031" alt="TabelaBdAlunoAtualizada" src="https://github.com/user-attachments/assets/d37ea042-2fa5-4c85-b510-ea7f40a948c2" />


**Tabela de Professores Atualizada Depois De Testes:**
<img width="1919" height="1034" alt="TabelaBdProfessorAtualizada" src="https://github.com/user-attachments/assets/b3101420-c27d-47ca-9e05-a190dd795425" />

## 👨‍💻 Autor
Rodolfo Santiago Romero  Garcia
Ciência da Computação - UNIESP
