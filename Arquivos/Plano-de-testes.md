# 🧪 Plano de Testes de Qualidade – UniBlog

## 1. Objetivo
Garantir a qualidade, confiabilidade e estabilidade do sistema **UniBlog**, verificando se todas as funcionalidades atendem aos requisitos definidos e oferecem uma boa experiência ao usuário.

---

## 2. Escopo
Os testes cobrem as principais funcionalidades do sistema, incluindo:
- Cadastro e login de usuários  
- Criação e publicação de postagens  
- Interações (curtidas, comentários e compartilhamentos)  
- Gerenciamento de perfil e configurações  
- Painel administrativo e controle de usuários  

---
## 🗓️ CRONOGRAMA DE TESTES

### 🗓️ Acompanhamento de Testes

| Atividade | Data proposta da entrega | Status | Data da conclusão   | Observação |
|------------|--------------------------|---------|-----------------------------|---|
| Perfil -  Criar página de perfil do usuário/comunidade |-|🔄 Em andamento| - | ||
| Perfil - (RNF01) Interface responsiva - Estilizar layout do perfil | - |🔄 Em andamento | - | ||
| Perfil - Adicionar paginação ou scroll infinito para a timeline | - |🔄 Em andamento | - | ||
| Perfil - Criar componente para listar postagens do usuário no perfil | - |🔄 Em andamento | - | ||
| Perfil - Criar componente para listar postagens do usuário no perfil | - |🔄 Em andamento | - | ||
| Perfil - Criar componente para edição do perfil (Altera foto e descrição) | - |🔄 Em andamento | - | ||
| Project - Configurando Workflow | - |🔄 Em andamento | - | ||
| Desenvolver a tela do feed onde as publicações ficarão visiveis| - |🔄 Em andamento | - | ||
| (RF02) Publicações - Criar tela de formulário para nova publicação (Título, conteúdo, upload de imagens ou anexos). | - |🔄 Em andamento | - | ||
| Integrar frontend com a API de criação de post | - |🔄 Em andamento | - | ||
| Exibir pré-visualização da publicação antes de postar | - |🔄 Em andamento | - | ||
| Adicionar validações e feedbacks visuais (Mensagens de erro/sucesso) | - |🔄 Em andamento | - | ||
| Implementar tratamento de erros (imagem muito grande, formato inválido) | - |🔄 Em andamento | - | ||
| Testes do fluxo de postagens simulando postagens reais. | - |🔄 Em andamento | - | ||
| (RNF01) Interface responsiva - Estilizar layout de publicações e feed. | - |🔄 Em andamento | - | ||
| NavBar para Busca | - |🔄 Em andamento | - | ||
| NavBar para Notificações | - |🔄 Em andamento | - | ||
| Nav Bar para Profile | - |🔄 Em andamento | - | ||
| NavBar Styleshet | - |🔄 Em andamento | - | ||
| Aparecer todas as publicações em ordem de postagem mais recente | - |🔄 Em andamento | - | ||
| respeitar layout de cores e fontes do figma | - |🔄 Em andamento | - | ||
| Perfil - Realizar testes dos fluxos > Criar post > aparece no histórico de perfil e Compartilhar posts > aparece no histórico de perfil. | - |🔄 Em andamento | - | ||
| Perfil - Adicionar validações (descrição com limite de caracteres, formato da imagem). | - |🔄 Em andamento | - | |
| Perfil - Exibir estatísticas simples (Número de posts, curtidas recebidas). | - |🔄 Em andamento | - | |
| Backlog - Envio de notificações | - |🔄 Em andamento | - | |
| Backlog - Gerenciamento de eventos/grupos | - |🔄 Em andamento | - | |
| Backlog - Criar layout para o painel (sidebar). | - |🔄 Em andamento | - | | 
| Backlog - Configuração do ambiente de produção | - |🔄 Em andamento | - | |
| Backlog - Documentação de uso | - |🔄 Em andamento | - | |
| Backlog - Fazer Pagina de Busca | - |🔄 Em andamento | - | |
| Backlog - Comunicação com Backend | - |🔄 Em andamento | - | |
| Backlog - Buscar por nome de perfil | - |🔄 Em andamento | - | |
| Backlog - Buscar por tags de posts | - |🔄 Em andamento | - | |
| Backlog - Perfil - Foto de Perfil | - |🔄 Em andamento | - | |
| Backlog - Publicação da aplicação | - |🔄 Em andamento | - | |


---

📘 **Legenda de Status:**
- ✅ **Concluído**
- 🔄 **Em andamento**
- ⏳ **Pendente**


---

## 3. Tipos de Testes
| Tipo de Teste | Descrição | Responsável |
|----------------|------------|--------------|
| **Teste Funcional** | Verifica se cada funcionalidade atende aos requisitos definidos. | QA |
| **Teste de Integração** | Valida a comunicação entre frontend (React) e backend. | QA + Desenvolvedor |
| **Teste de Interface (UI/UX)** | Avalia a usabilidade, layout e responsividade. | QA |
| **Teste de Regressão** | Garante que novas alterações não afetem funcionalidades anteriores. | QA |
| **Teste de Desempenho** | Mede tempo de resposta e desempenho da aplicação. | QA |

---

## 4. Ferramentas Utilizadas
- **Jest** – Testes unitários em React  
- **Postman / Insomnia** – Testes de integração com API  
- **GitHub Actions** – Execução automática de pipeline em cada push   
---

## 5. Casos de Teste
| ID | Funcionalidade | Pré-condição | Ação | Resultado Esperado | Status |
|----|----------------|---------------|-------|--------------------|---------|
| CT01 | Login de Usuário | Usuário cadastrado | Inserir e-mail e senha válidos | Sistema redireciona para o feed | ✅ |
| CT02 | Publicar Postagem | Usuário autenticado | Criar postagem com título e imagem | Post é exibido no feed | 🔄 |
| CT03 | Comentar Postagem | Post existente | Inserir comentário e enviar | Comentário aparece abaixo do post | ⏳ |
| CT04 | Curtir Postagem | Post existente | Clicar em "Curtir" | Ícone muda e contador incrementa | ⏳ |
| CT05 | Editar Perfil | Usuário autenticado | Alterar nome e salvar | Dados atualizados no perfil | ⏳ |

---

## 6. Critérios de Aceitação
- 100% dos testes críticos devem ser aprovados.  
- Nenhum erro de alta gravidade deve permanecer pendente.  
- As funcionalidades devem atender aos requisitos funcionais e não funcionais.  

---

## 7. Registro e Evidências
- Evidências dos testes (prints, logs, vídeos) serão armazenadas na pasta:  *Inserir o link do repo*


