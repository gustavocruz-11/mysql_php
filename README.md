# 🛒 Sistema de Cadastro de Produtos

> **Aplicação Web Back-End** desenvolvida para cadastro e inserção de produtos em banco de dados MySQL utilizando **PHP** e **HTML5**.

---

## 📌 Sobre o Projeto

Este projeto consiste em um formulário web dinâmico que permite ao usuário registrar novos produtos informando o **nome** e o **preço**. O código realiza a validação dos dados no servidor (Back-End) e faz a inserção segura das informações no banco de dados relational MySQL.

---

## 🛠️ Tecnologias Utilizadas

- 🐘 **PHP:** Processamento do formulário, validação de regras de negócio e conexão com o banco de dados via MySQLi.
- 🗄️ **MySQL:** Banco de dados relacional para persistência dos dados cadastrados.
- 🌐 **HTML5:** Estruturação do formulário de entrada.

---

## ⚡ Funcionalidades

- 📝 **Formulário de Entrada:** Campos para nome e valor do produto.
- 🔄 **Tratamento de Dados:** Conversão automática de vírgula para ponto no preço (ex: `10,50` para `10.50`).
- ✅ **Validação Back-End:**
  - Impede o envio de campos vazios.
  - Valida se o preço é um valor numérico e positivo.
- 💾 **Persistência no Banco:** Conexão nativa PHP + MySQL para salvar o produto na tabela `produtos`.
- 💬 **Feedback ao Usuário:** Mensagens estilizadas de sucesso ou de erro na validação/conexão.

---

## 📂 Estrutura do Banco de Dados

Para rodar a aplicação, o banco de dados MySQL deve conter a seguinte estrutura base:

```sql
CREATE DATABASE exercicio;

USE exercicio;

CREATE TABLE produtos (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL,
    preco DECIMAL(10,2) NOT NULL
);
