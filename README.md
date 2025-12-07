# 🏆 spring-boot-jpa-security-web: Sistema Web Integrado (Java 17)

## Gerenciador de Processos com Segurança, Persistência e Emissão de Documentos

Este é o meu projeto Full-Stack Básico que demonstra o ciclo de desenvolvimento completo. Utilizei **Spring Boot** para o Backend robusto, **Spring Security** para controle de acesso, **JPA** para persistência e **Thymeleaf** para a interface web dinâmica. É uma versão demo de um sistema já em produção, com foco total na aplicação da arquitetura e boas práticas.

---

## 🛠️ Tecnologias e Arquitetura

Este projeto comprova o domínio de uma stack moderna e completa de Backend Java:

| Categoria | Tecnologia | Habilidade Demonstrada |
| :--- | :--- | :--- |
| **Framework** | **Spring Boot 3.4.0** | Construção rápida de APIs e serviços. |
| **Segurança** | **Spring Security** | Controle de acesso e proteção de rotas (Login, Logout). |
| **Persistência** | **Spring Data JPA** (Hibernate) & **MySQL** | Modelagem de dados e transações eficientes. |
| **Interface** | **Thymeleaf** (Template Engine) & Spring Web | Renderização de páginas dinâmicas e MVC. |
| **Desenvolvimento** | Java 17, Lombok | Código moderno e limpo. |

---

## 📸 Demonstração Visual do Sistema

Aqui estão as telas que validam as funcionalidades Back-end, focando nas habilidades de **Segurança**, **Persistência com CRUD** e **Geração de Documentos**.

### 1. Segurança e Acesso (Spring Security)

* **Tela de Login:** Demonstra a configuração do filtro de segurança, exigindo autenticação para acessar as rotas protegidas.
    ![Página de Login do Sistema](https://raw.githubusercontent.com/JVFrancaLisboa/spring-boot-jpa-security-web/main/assets/login.png)

### 2. Gerenciamento de Movimentações (Persistência Avançada)

* **Registro de Gastos:** Formulário complexo para entradas de despesas, incluindo a funcionalidade de **upload de comprovante (anexo)**, que demonstra persistência de arquivos e dados.
    ![Formulário de Registro de Gastos e Upload de Comprovante](https://raw.githubusercontent.com/JVFrancaLisboa/spring-boot-jpa-security-web/main/assets/gastos.png)

* **Relatório Geral:** Tabela complexa que utiliza consultas otimizadas no MySQL para gerar um relatório financeiro de entradas e saídas.
    ![Tabela de Relatório Geral de Movimentações](https://raw.githubusercontent.com/JVFrancaLisboa/spring-boot-jpa-security-web/main/assets/relatorio-geral.png)

### 3. Gerenciamento de Membros (CRUD)

* **Cadastro e Listagem:** Demonstração do ciclo completo de CRUD (Cadastrar, Listar, Atualizar, Excluir) de membros.
    ![Lista de Membros Cadastrados com CRUD](https://raw.githubusercontent.com/JVFrancaLisboa/spring-boot-jpa-security-web/main/assets/lista-membros-cadastrados.png)
* **Formulário de Entrada:** Exemplo de formulário para inserção e validação de dados.
    ![Formulário de Cadastro de Membro](https://raw.githubusercontent.com/JVFrancaLisboa/spring-boot-jpa-security-web/main/assets/cadastro-membros.png)

### 4. Emissão de Documentos (Geração de Conteúdo)

* **Carteirinhas com Regra de Negócio Visual:** O sistema gera o documento PDF aplicando estilos diferentes automaticamente com base no cargo do membro (Enum). Isso demonstra domínio de lógica condicional no Thymeleaf.

| Membro (Padrão) | Ministro (Liderança) | Missionário (Campo) |
| :---: | :---: | :---: |
| ![Carteirinha Membro](https://raw.githubusercontent.com/JVFrancaLisboa/spring-boot-jpa-security-web/main/assets/emissao-carteirinha-membro.png) | ![Carteirinha Ministro](https://raw.githubusercontent.com/JVFrancaLisboa/spring-boot-jpa-security-web/main/assets/emissao-carteirinha-ministro.png) | ![Carteirinha Missionário](https://raw.githubusercontent.com/JVFrancaLisboa/spring-boot-jpa-security-web/main/assets/emissao-carteirinha-missionario.png) |
  
* **Geração de Contrato:** Demonstra a capacidade do sistema de gerar documentos dinâmicos (como um Contrato de Locação) com base em dados do banco.
    ![Contrato de Locação de Imóvel gerado pelo sistema](https://raw.githubusercontent.com/JVFrancaLisboa/spring-boot-jpa-security-web/main/assets/contrato-aluguel.png)

---

Este é um projeto Spring Boot desenvolvido com o objetivo de automatizar processos feitos por igrejas, com validação de dados e uma interface web com Thymeleaf.

## 🛠 Tecnologias Utilizadas

Este projeto foi desenvolvido com as seguintes tecnologias:

- **Spring Boot 3.4.0**
- **Java 17**
- **Spring Data JPA** (com Hibernate)
- **Spring Web**
- **Spring Security**
- **MySQL Driver**
- **Thymeleaf** (Template Engine)
- **Lombok**
- **Bootstrap** (+ js e ajax)

---

## 🚀 Funcionalidades

- Cadastro e validação de dados do usuário.
- Tesouraria e geração de relatórios.
- Emissão de carteirinhas e contrato de aluguel.
- Persistência de dados utilizando MySQL e Spring Data JPA.
- Renderização de páginas dinâmicas com Thymeleaf.
- Integração com banco de dados para gerenciamento de informações.

---

## ⚙️ Pré-requisitos

Antes de começar, você precisará ter as seguintes ferramentas instaladas no seu ambiente de desenvolvimento:

- **Java 17** ou superior
- **Maven 3.8+**
- **MySQL** (ou outro banco compatível)
- **Git** (para controle de versão)

---

## 🚧 Como Executar o Projeto

1. **Clone este repositório**:
   ```bash
   git clone https://github.com/seu-usuario/iadsn.git
   Acesse o diretório do projeto:

   bash
   Copiar código
   cd iadsn
   Configure o banco de dados:
  
   Crie um banco de dados no MySQL com o nome, por exemplo, iadsn_db.
   Execute o arquivo .sql (insert-login.sql) para ter acesso ao sistema com Login: admin, senha: 123
   Atualize o arquivo application.properties localizado em src/main/resources com as configurações do banco de dados:
   properties
   Copiar código
   spring.datasource.url=jdbc:mysql://localhost:3306/iadsn_db
   spring.datasource.username=SEU_USUARIO
   spring.datasource.password=SUA_SENHA
   spring.jpa.hibernate.ddl-auto=update
   Instale as dependências do projeto: Use o Maven para baixar e configurar as dependências necessárias:
  
   bash
   Copiar código
   mvn clean install
   Inicie a aplicação: Execute o servidor Spring Boot:
  
   bash
   Copiar código
   mvn spring-boot:run
   Acesse a aplicação: Abra o navegador e vá para o endereço: http://localhost:8080
   ```
## 💻 Autor

Desenvolvido por **Josué Vítor** 🚀

- [LinkedIn](https://www.linkedin.com/in/jvfrancalisboa/)
- [GitHub](https://github.com/JVFrancaLisboa)
- Email: josuevitorfrancalisboa@gmail.com
