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


