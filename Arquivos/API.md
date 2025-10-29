# Documentação da API UniBlog

API para gerenciamento de contas, perfis, postagens e interações.

---

## 📌 Índice

* [1. Autenticação](#1-autenticação)
    * [1.1 Registrar conta (POST /account/register)](#11-post-accountregister)
    * [1.2 Login (POST /account/login)](#12-post-accountlogin)
* [2. Perfis](#2-perfis)
    * [2.1 Criar perfil (POST /profile/new)](#21-post-profilenew)
    * [2.2 Consultar perfil (GET /profile/:id)](#22-get-profileid)
* [3. Postagens](#3-postagens)
    * [3.1 Criar postagem (POST /post/new)](#31-post-postnew)
    * [3.2 Consultar postagem (GET /post/:id)](#32-get-postid)
* [4. Interações](#4-interações)
    * [4.1 Curtir postagem (POST /post/:id/like)](#41-post-postidlike)
    * [4.2 Quantidade de likes (GET /post/:id/likes)](#42-get-postidlikes)
* [5. Boas práticas](#5-boas-práticas)
* [6. Links úteis](#6-links-úteis)

---

## 1. Autenticação

### 1.1 POST /account/register

**Descrição:** Cria uma nova conta.

**Requisição:**
```json
{
    "username": "usuario123",
    "email": "email@exemplo.com",
    "password": "senha123"
}
```
***Resposta (201 Created):***
```JSON

{
    "message": "Conta criada com sucesso",
    "userId": "abc123"
}
```

### Exemplo curl:

curl -X POST [https://seusite.com/account/register](https://seusite.com/account/register) \
-H "Content-Type: application/json" \
-d '{"username":"usuario123","email":"email@exemplo.com","password":"senha123"}'

### 1.2 POST /account/login
**Descrição:** Autentica o usuário.

**Requisição:**

```JSON

{
    "email": "email@exemplo.com",
    "password": "senha123"
}
```
***Resposta (200 OK):***
```JSON

{
    "token": "jwt.token.aqui",
    "userId": "abc123"
}
```
### Exemplo curl:

curl -X POST [https://seusite.com/account/login](https://seusite.com/account/login) \
-H "Content-Type: application/json" \
-d '{"email":"email@exemplo.com","password":"senha123"}'


## 2. Perfis
### 2.1 POST /profile/new
**Descrição:** Cria um novo perfil de usuário.

**Requisição:**

```JSON

{
    "userId": "abc123",
    "nome": "João Silva",
    "bio": "Apaixonado por tecnologia"
}
```
***Resposta (201 Created):***
```JSON

{
    "message": "Perfil criado com sucesso",
    "profileId": "prof123"
}
```

### Exemplo curl:
curl -X POST [https://seusite.com/profile/new](https://seusite.com/profile/new) \
-H "Content-Type: application/json" \
-d '{"userId":"abc123","nome":"João Silva","bio":"Apaixonado por tecnologia"}'


### 2.2 GET /profile/:id
Descrição: Retorna as informações de um perfil pelo ID.

**Resposta (200 OK):**

```JSON

{
    "profileId": "prof123",
    "nome": "João Silva",
    "bio": "Apaixonado por tecnologia",
    "createdAt": "2025-10-28T12:34:56Z"
}
```

### Exemplo curl:

curl [https://seusite.com/profile/prof123](https://seusite.com/profile/prof123)


## 3. Postagens
### 3.1 POST /post/new
**Descrição:** Cria uma nova postagem.

**Requisição:**

```JSON

{
    "profileId": "prof123",
    "conteudo": "Meu primeiro post!"
}
```
**Resposta (201 Created):**

```JSON

{
    "message": "Post criado com sucesso",
    "postId": "post123"
}
```
### Exemplo curl:

curl -X POST [https://seusite.com/post/new](https://seusite.com/post/new) \
-H "Content-Type: application/json" \
-d '{"profileId":"prof123","conteudo":"Meu primeiro post!"}'


### 3.2 GET /post/:id
**Descrição:** Retorna uma postagem pelo ID.

**Resposta (200 OK):**

```JSON

{
    "postId": "post123",
    "profileId": "prof123",
    "conteudo": "Meu primeiro post!",
    "createdAt": "2025-10-28T12:40:00Z"
}
```

### Exemplo curl:

curl [https://seusite.com/post/post123](https://seusite.com/post/post123)


## 4. Interações
### 4.1 POST /post/:id/like
**Descrição:** Adiciona um "like" a uma postagem.

**Requisição:**

```JSON

{
    "userId": "abc123"
}
```
**Resposta (200 OK):**

```JSON

{
    "message": "Post curtido",
    "likes": 1
}
```

### Exemplo curl:

curl -X POST [https://seusite.com/post/post123/like](https://seusite.com/post/post123/like) \
-H "Content-Type: application/json" \
-d '{"userId":"abc123"}'


### 4.2 GET /post/:id/likes
**Descrição:** Retorna a quantidade de likes de uma postagem.

**Resposta (200 OK):**

```JSON

{
    "postId": "post123",
    "likes": 1
}
```

### Exemplo curl:

curl [https://seusite.com/post/post123/likes](https://seusite.com/post/post123/likes)

## 5. Boas práticas
- Autenticação: Utilize JWT para autenticação em endpoints protegidos.

- Formato de Resposta: Todos os endpoints retornam JSON.

- Códigos HTTP: Utilize códigos HTTP corretos:

200 → Sucesso

201 → Criado

400 → Requisição inválida

401 → Não autorizado

404 → Não encontrado

500 → Erro do servidor


Você pode copiar o texto acima e salvar em um arquivo, por exemplo, `README.md` (para documentação no Git) ou `api_docs.txt`.

Gostaria de alguma sugestão de nome de arquivo ou de como formatar esse texto como
