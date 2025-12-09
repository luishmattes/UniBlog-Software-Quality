# 🧪 Plano de Testes de Qualidade – UniBlog

## 1. Objetivo
Garantir que o sistema funcione conforme os requisitos, validando autenticação, segurança e usabilidade.						

---

## 2. Escopo
Os testes cobrem as principais funcionalidades do sistema, incluindo:

✅ Validar limite de caracteres nas Publicações.

✅ Publicação de uma Postagem com anexos.

✅ Visualização de posts em formato de time line.

✅ Login com credenciais válidas.							

✅ Teste de Histório no Perfil.

❌ Testes de performance ou carga	.											

---

## 3. 🗓️ Cronograma

| Atividade | Inicio | Fim | Observação |
|------------|--------------|---------|-----------|
|Preparação de casos| 27/10/2025 |	03/11/2025 |  |
|Execução dos testes | 04/11/2025	| 10/11/2025 |  |
|Relatório final | 12/11/2025 |	12/11/2025 |  |

---

## 4. Critérios de Aceitação
| ID	| Critério	|	Prioridade |
|-----|-----------|------------|
| CA-01	| O sistem não deve permitir uma publicação com mais de 200 caracteres| Alta |
| CA-02	| O sistema deve permitir a publicação de postagens. | Alta |
| CA-03	| O sistema deve permitir a visualização de outras publicações em formato time line. | Alta |
| CA-04	| O sistema deve permitir compartilhar anexos,(fotos, videos), durante a criação da postagem. | Alta |
| CA-05	| O sistema deve exibir os posts realizados no histórico do Perfil | Média |

---

## 5. Estratégia
| Tipo de Teste | Descrição | Responsável |
|----------------|------------|--------------|
| Testes funcionais | Validação de campos, mensagens de erro, fluxo de login.	| QA |
| Testes de segurança | armazenamento de senha criptografada. | QA + Desenvolvedor |
| Testes de usabilidade | Experiência do usuário (UI/UX).	 | QA |

---

## 6. Casos de Teste
|   ID   |       Caso de Teste       |       Pré-condições       |         Passos         |       Dados de Entrada        |     Resultado Esperado     |     Critério de Aceitação     |     Prioridade     |     Status     |     Evidência     |
|--------|---------------------------|---------------------------|------------------------|-------------------------------|----------------------------|-------------------------------|--------------------|----------------|-------------------|
| CT-01 | Validar limite de caracteres nas Publicações | Usuário autenticado. | "1. Acessar a aba de criação de posts. 2. Preencher os campos Titulo e Descrição. 3. Clicar em ""adicionar postagem ao feed""." | "Titulo e descrição" | É exibida mensagem de erro informando o limite de caracteres permitidos | CA-01 | Alta | ✅ Aprovado | [Link] |
| CT-02 | Login com credenciais válidas | Usuário cadastrado: usuario@teste.com, senha: Teste@123 | "1. Acessar página de login. 2. Preencher e-mail e senha. 3. Clicar em ""Entrar""." | "E-mail: usuario@teste.com Senha: Teste@123" | Redireciona para o feed. | CA-02 | Alta | ✅ Aprovado | [Link] |
| CT-03 | Visualizar time line  | Posts existentes | "1. Fazer login na aplicação. 2. Visualizar o feed em formato time line." | Login do usuario | Visualização de postagens em formato time line onde os Comentários aparecem abaixo dos posts. | CA-03 | Alta | ✅ Aprovado | [Link] |
| CT-04 |  Publicar Postagem com anexos | Usuário autenticado. | "1. Acessa a aba de criação de posts. 2. Preenche os campos Titulo e Comentario. 3. Clica no icone de anexos. 4.Adiciona os anexos desejados "fotos ou videos". 5. Clicar em ""adicionar postagem ao feed""." | "Titulo, comentario e anexos" | Postagem com o anexo inserida no feed.  | CA-04 | Alta | ✅ Aprovado | [Link] |
| CT-05 | Teste de Histório no Perfil  | 1. Usuário autenticado. 2. Pelo menos 01 post realizado pelo usuário | "1. Acessa a tela de Perfil 2. Verifica se há o histórico de publicações de acordo com as respectivas postagens do usuário. | "Titulo, comentario e anexos" | Postagem inserida no feed.  | CA-05 | Média | ✅ Aprovado | [Link] |

❌ Não Executado.
⚠️ Falhou.
✅ Aprovado.

---
## 7. RECURSOS		
|	Ferramentas	| Postman |
|-----------|-------------------------|
|	Equipe	| 1 QA e Desenvolvedores para suporte.|
|	Dados de teste	| Usuários fictícios (ex: usuario@teste.com, senha: Teste@123).|							
---
## 8.RISCOS E AÇÕES										

| Risco |Ação Preventiva|
|-------|---------------|
| Ambiente instável. | Validar ambiente antes dos testes.	|
| Dados de teste inconsistentes. | Verificar dados e possivelmente gerar cópia do banco de produção. |

---

## 9. AMBIENTE		
		
|Navegador | Chrome V. 139.0.7258.154/.155|
|------|-------------------------------|
|     SO     | Windows 11|
|    Dispositivo     | Desktop|
|    Ambiente   | Homologação (URL: [link])|	
---
## 10. Evidencias
- Evidências dos testes (prints, logs, vídeos) serão armazenadas na pasta:  [ link do repositório das evidências](https://github.com/luishmattes/UniBlog-Software-Quality/tree/d2c4c5672208665550e140a636446bcbeee5eba2/Arquivos/Evidencias)


