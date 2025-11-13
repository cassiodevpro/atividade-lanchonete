# 🍔 **API de Cardápio — Lanchonete**

Bem-vindo(a) à API da lanchonete **🍟 Lanchonete!**  
Este projeto foi desenvolvido para modernizar o cardápio da lanchonete, permitindo o gerenciamento digital dos produtos: lanches, bebidas, acompanhamentos e sobremesas.  

---

## 🧾 **Objetivo da Atividade**

A ideia é criar uma **API RESTful** em **Java** que permita:
- 📋 Listar todos os produtos do cardápio  
- 🔍 Consultar detalhes de um produto específico  
- 🧃 Buscar produtos por categoria  
- ➕ Adicionar novos produtos  
- ✏️ Atualizar informações de produtos existentes  
- ❌ Deletar produtos do cardápio  

---

## 🧩 **Estrutura dos Produtos**

Cada produto do cardápio contém as seguintes informações:

| Campo | Tipo | Descrição |
|-------|------|------------|
| 🆔 **id** | `Long` | Identificador único do produto |
| 🍔 **nome** | `String` | Nome do produto |
| 📝 **descricao** | `String` | Detalhes do produto |
| 💰 **preco** | `Double` | Valor em reais |
| 🗂️ **categoria** | `String` | Tipo do produto (Lanche, Bebida, Acompanhamento, Sobremesa) |
| ✅ **disponivel** | `Boolean` | Indica se o produto está disponível |
| ⏱️ **tempoPreparo** | `Integer` | Tempo estimado de preparo (em minutos) |

---

## 🍴 **Categorias Disponíveis**

1. 🥪 **Lanches** — Sanduíches diversos  
2. 🧃 **Bebidas** — Refrigerantes, sucos e bebidas quentes  
3. 🍟 **Acompanhamentos** — Porções e acompanhamentos  
4. 🍰 **Sobremesas** — Doces e sobremesas deliciosas  

---

## 🚀 **Endpoints da API**

| Método | Endpoint | Descrição |
|--------|-----------|-----------|
| **GET** | `/produtos` | 📋 Lista todos os produtos disponíveis |
| **GET** | `/produtos/{id}` | 🔍 Busca um produto específico pelo ID |
| **GET** | `/produtos/categoria/{categoria}` | 🗂️ Lista produtos de uma categoria |
| **POST** | `/produtos` | ➕ Adiciona um novo produto |
| **PUT** | `/produtos/{id}` | ✏️ Atualiza um produto existente |
| **DELETE** | `/produtos/{id}` | ❌ Remove um produto do cardápio |

---

## ⚙️ **Regras de Negócio**

🔸 Todo produto deve ter um **nome único**  
🔸 O **preço** nunca pode ser **zero ou negativo**  
🔸 Somente produtos com `disponivel = true` aparecem nas listagens  
🔸 Tempo de preparo padrão por categoria:
   - 🥪 Lanches → 10–15 min  
   - 🧃 Bebidas → 2–5 min  
   - 🍟 Acompanhamentos → 8–10 min  
   - 🍰 Sobremesas → 5 min  
🔸 Produtos adicionados começam **disponíveis por padrão**

---

## 🛠️ **Tecnologias Utilizadas**

- ☕ **Java 17+**  
- 🌱 **Spring Boot**  
- 🧰 **Maven** (gerenciador de dependências)  
- 🗄️ **Banco de dados H2** (ou outro de sua escolha)  
- 📫 **Postman / Insomnia** (para testes da API)

---

## 🧑‍💻 **Como Executar o Projeto**

## 1. Clone este repositório:
   ```bash
   - git clone https://github.com/seuusuario/atividade-lanchonete.gii


## 2. Acesse a pasta do projeto:**

- cd api-lanchonete

## 3.  Execute o projeto:

- mvn spring-boot:run


## 4.  Acesse no navegador ou Postman:

- http://localhost:8080/produtos

🧁 Exemplo de Produto (JSON)
{
  "id": 1,
  "nome": "X-Bacon",
  "descricao": "Pão, hambúrguer, bacon crocante, queijo",
  "preco": 25.0,
  "categoria": "Lanche",
  "disponivel": true,
  "tempoPreparo": 12
}
