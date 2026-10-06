# 4. Projeto da Solução

> ⚠️ **Aviso aos Squads (Software House)**
>
> Esta seção **não deve ser preenchida integralmente antes da codificação**.
> Trata-se de um **Documento Vivo**, que deverá ser atualizado **incrementalmente a cada Sprint**, refletindo fielmente o código real implementado.

---

## 4.1 Arquitetura da Solução (Sprint 1 e 2)

Apresente um **diagrama macro** demonstrando como os componentes do sistema se comunicam.

A arquitetura deve refletir o modelo de **fatias verticais**, evidenciando o fluxo:

**Front-end → API (Back-end) → Banco de Dados**

Semelhante à imagem abaixo:

![Exemplo de Arquitetura](https://uds.com.br/blog/wp-content/uploads/2024/09/Imagem-1-Comparativo-ilustrativo-das-diferencas-entre-front-end-e-back-end.jpg)



 **Fonte:** [Guia Completo de Desenvolvimento de Software - UDS](https://uds.com.br/blog/desenvolvimento-de-software-guia-completo/) <br><br>
 
 ### 📎 Inserir o Diagrama de Arquitetura do Projeto do Grupo
🚨 O grupo deverá inserir aqui a imagem


---
🔧**Ferramentas recomendadas:**
- Draw.io
- Lucidchart
- Figma

---

## 4.2 Tecnologias Utilizadas (Sprint 1)

Descreva as tecnologias, linguagens, frameworks, bibliotecas e serviços escolhidos pelo Squad.

| Dimensão | Tecnologia Escolhida |
|----------|----------------------|
| Banco de Dados (SGBD) | PostgreSQL |
| Back-end (API) | Node.js |
| Front-end / Mobile | React Native |
| Hospedagem / Deploy | Ex: Azure, AWS, Render ou Railway |
| Gestão e Versionamento | GitHub e GitHub Projects (Kanban) |

 ⚠️ **Observação:**
 - GitHub Pages não executa back-end.
 - Utilize apenas tecnologias realmente implementadas.

---

##  4.3 Wireframes ou Mockups (A partir da Sprint 2)

Apresente os protótipos das telas (Wireframes/Mockups) apenas das funcionalidades que estão sendo implementadas na Sprint atual.

Cada Wireframe ou Mockups devem estar associados a pelo menos:

- Um Requisito Funcional (RF-XX)
- Uma História de Usuário

## Tela de Login

<img width="330" height="657" alt="WhatsApp Image 2026-09-21 at 21 17 08" src="https://github.com/user-attachments/assets/79b83e18-4656-4b1f-b43c-14357c023123" />

## Tela de Cadastro de cliente cadastraddos

<img width="320" height="667" alt="WhatsApp Image 2026-09-21 at 21 19 19" src="https://github.com/user-attachments/assets/e14e73fc-2518-424f-923a-af72fc0d5298" />


## Tela de Cadastro de Clientes

<img width="332" height="647" alt="WhatsApp Image 2026-09-21 at 21 19 47" src="https://github.com/user-attachments/assets/5b063ead-9e3a-43ff-b8f3-cc51315aca8b" />

## Tela de Dados do cliente

<img width="327" height="657" alt="WhatsApp Image 2026-09-21 at 21 20 20" src="https://github.com/user-attachments/assets/c97e370b-9d2f-448f-b7d3-b6ff2d669685" />


##Tela de nova Aferição de Pressão

<img width="327" height="657" alt="WhatsApp Image 2026-09-21 at 21 20 20" src="https://github.com/user-attachments/assets/735c446c-df87-4389-b828-c9ef56769517" />

## Tela de Exportação dos dados

<img width="332" height="647" alt="WhatsApp Image 2026-09-27 at 19 45 36" src="https://github.com/user-attachments/assets/5928df13-99bc-488e-a151-704d1571dd54" />


---

## 4.4 Modelagem de Dados (Sprint 2 e 3)

O sistema exige persistência de dados.

A documentação do banco seguirá a abordagem de **entrega contínua**, sendo expandida conforme evolução do projeto.

---

### 4.4.1 Script Físico (Entrega na Sprint 2 - MVP)

Para a primeira fatia vertical (MVP), o Squad deverá entregar o **script de criação das tabelas ou coleções utilizadas**.

#### 🔹 Banco Relacional MySQL

* Diagrama Der
  
<img width="791" height="478" alt="image" src="https://github.com/user-attachments/assets/c1bcba0e-26fa-4991-a7b4-67f23aaa775f" />


* Código SQL

```sql

CREATE TABLE FUNCIONARIO (
    id_funcionario INT NOT NULL AUTO_INCREMENT,
    nome VARCHAR(120) NOT NULL,
    email VARCHAR(150) NOT NULL,
    senha VARCHAR(255) NOT NULL,
    cpf VARCHAR(14) NOT NULL,
    telefone VARCHAR(20) NOT NULL,
    data_cadastro DATETIME NOT NULL,
    PRIMARY KEY (id_funcionario),
    UNIQUE (cpf)
);

CREATE TABLE CLIENTE (
    id_cliente INT NOT NULL AUTO_INCREMENT,
    nome VARCHAR(120) NOT NULL,
    cpf VARCHAR(14) NOT NULL,
    telefone VARCHAR(20) NOT NULL,
    data_nascimento DATE NOT NULL,
    data_cadastro DATETIME NOT NULL,
    PRIMARY KEY (id_cliente),
    UNIQUE (cpf)
);

CREATE TABLE MEDICAO_PRESSAO (
    id_medicao INT NOT NULL AUTO_INCREMENT,
    id_cliente INT NOT NULL,
    id_funcionario INT NOT NULL,
    pressao_sistolica DECIMAL(4, 2) NOT NULL,
    pressao_diastolica DECIMAL(4, 2) NOT NULL,
    pulso INT NOT NULL,
    data_hora DATETIME NOT NULL,
    observacoes TEXT,
    PRIMARY KEY (id_medicao),
    FOREIGN KEY (id_cliente) REFERENCES CLIENTE(id_cliente),
    FOREIGN KEY (id_funcionario) REFERENCES FUNCIONARIO(id_funcionario)
);

```

---

### 📁 Obrigatório

O arquivo .sql ou .js deve ser salvo na pasta: src/bd

 - É permitido colar um trecho do script no README apenas para visualização rápida.
 
---
### 4.4.2 Representação do Modelo Físico de Dados (Entrega na Sprint 3 - Core)


> **Fundamentação:** Os modelos de dados físicos fornecem detalhes minuciosos que auxiliam administradores e desenvolvedores na implementação da lógica de negócios em um banco de dados real.
> Eles incluem elementos não especificados no modelo lógico, como:
> - Tipos de dados específicos da plataforma
> - Restrições
> - Índices
> - Triggers (quando aplicável)
> - Procedimentos armazenados (quando aplicável)
>
>Por representarem um banco real, devem respeitar:
> - Convenções de nomenclatura
> - Restrições da plataforma
> - Uso adequado de palavras reservadas <br>


**Exemplo:**

<img src="https://d2908q01vomqb2.cloudfront.net/b6692ea5df920cad691c20319a6fffd7a4a766b8/2021/11/09/BDB-1321-image005.png" width="85%">

**FONTE:** <https://aws.amazon.com/pt/compare/the-difference-between-logical-and-physical-data-model/>

<br>O grupo deverá gerar um diagrama físico do banco de dados (estrutura real das tabelas), evidenciando PKs, FKs e relacionamentos, conforme implementado no código.

Este modelo deve exibir:
- Tabelas ou coleções existentes
- Atributos com seus respectivos tipos de dados
- Chaves Primárias (PK)
- Chaves Estrangeiras (FK)
- Relacionamentos entre tabelas
- Restrições implementadas (quando aplicável)

---

### 📌 Requisitos Obrigatórios

- O diagrama deve representar fielmente o banco já implementado.
- Deve refletir exatamente o que foi criado nas Sprints 2 e 3.
- Não incluir tabelas que não existam no código.
- Deve contemplar o controle de acesso de usuários, quando implementado.
- Deve respeitar as convenções e restrições da plataforma utilizada.

---

### 📎 Representação do Modelo Físico de Dados
🚨 O grupo deverá inserir aqui a imagem do diagrama físico de dados.

---
🔧**Ferramentas Sugeridas**
- MySQL Workbench (engenharia reversa automática)
- DbDesigner
- Lucidchart
