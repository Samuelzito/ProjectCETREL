# 🌍 ProjectCETREL – API REST com Spring Boot

O ProjectCETREL é uma API REST desenvolvida em Java com Spring Boot, utilizando arquitetura em camadas. A aplicação permite realizar operações CRUD para entidades de cidades e estados, além de realizar uma simulação de consumo de API externa por meio de um cliente HTTP.

O projeto está pronto para ser executado com Docker e testado via Postman.

---

## 🚀 Funcionalidades

- ✅ CRUD completo de **Cidades**
- ✅ CRUD completo de **Estados**
- 🌐 Simulação de consumo de API externa com `PhotoClient`
- ❌ Tratamento global de exceções com `GlobalExceptionHandler`
- ✅ Teste automatizado da aplicação com JUnit
- 🐳 Executável com Docker + Docker Compose

---

## 🧰 Tecnologias utilizadas

- Java 17  
- Spring Boot  
- Spring Data JPA  
- Maven  
- Docker & Docker Compose  
- JUnit 5  
- Postman (para testes)

---

## 🗂️ Estrutura do Projeto

src/ ├── main/java/br/com/terceiroperiodo/ │ ├── controller/ # Endpoints REST │ ├── service/ # Regras de negócio │ ├── repository/ # Acesso ao banco de dados │ ├── model/ # Entidades JPA │ ├── dto/ # Transferência de dados │ ├── exception/ # Manipulação de erros │ ├── client/ # Cliente para API externa │ └── TerceiroPeriodoApplication.java ├── test/java/br/com/terceiroperiodo/ │ └── TerceiroPeriodoApplicationTest.java ├── Dockerfile ├── docker-compose.yml ├── pom.xml

yaml
Copiar
Editar

---

## ▶️ Como executar

1. Clone o projeto:
```bash
git clone https://github.com/Samuelzito/ProjectCETREL.git
cd ProjectCETREL
Execute com Docker:

bash
Copiar
Editar
docker-compose up --build
Isso iniciará o banco de dados e a aplicação.

📬 Endpoints
📍 Cidade
Método	Endpoint	Descrição
POST	/cidade	Cadastrar nova cidade
GET	/cidade/all	Listar todas as cidades
GET	/cidade/pageable/all	Listar cidades com paginação
🗺️ Estado
Método	Endpoint	Descrição
POST	/estado	Cadastrar novo estado
GET	/estado/all	Listar todos os estados
GET	/estado/{id}	Buscar estado por ID
GET	/estado/nome/{nome}	Buscar estado por nome
PUT	/estado	Atualizar estado
DELETE	/estado/{id}	Deletar estado
🖼️ Photo
Método	Endpoint	Descrição
GET	/photos/{id}	Buscar foto por ID (simulação)
🧪 Testes
Teste básico com JUnit:

bash
Copiar
Editar
./mvnw test
Testes manuais via Postman:

Requisições CRUD para /estado e /cidade

Requisição de simulação externa via /photos/{id}

📌 Observações
O projeto utiliza CORS liberado (@CrossOrigin(origins = "*")) para facilitar testes locais

Exceções personalizadas são lançadas com mensagens amigáveis ao consumidor da API

O controller de Photo simula uma chamada externa e demonstra controle de falha com try/catch

✍️ Autor
Feito com 💻 por Samuel Leite de Moraes
