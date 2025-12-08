# 📌 Mapeamento de Riscos, Ameaças e Ações de Mitigação
## Risco 1 – Vazamento de senhas e dados pessoais

**Descrição:** Exposição indevida de credenciais e informações sensíveis dos usuários, causada por falhas de autenticação, armazenamento inseguro ou brechas na API.

### Mitigação
**Curto prazo**

- Habilitar hashing de senhas com algoritmos fortes (bcrypt, Argon2).

- Forçar HTTPS em todas as rotas.

**Médio prazo**

- Implementar MFA/2FA.

- Configurar rate limiting e alertas de tentativas de acesso incomuns.

**Longo prazo**

- Realizar auditorias periódicas de segurança e pen tests.

- Implementar rotina automática de detecção de vazamentos de credenciais.

## Risco 2 – Hackeamento de perfil de usuário

Descrição: Atacante obtém controle de contas por força bruta, phishing, sessão mal gerida ou falhas de autorização.

### Mitigação
**Curto prazo**

- Expiração segura de sessões e cookies com flags HttpOnly e Secure.

- Bloqueio temporário após várias tentativas de login.

**Médio prazo**

- Autenticação baseada em tokens com renovação segura (JWT de vida curta).

**Longo prazo**

- Monitoramento de comportamento e detecção de acessos anômalos.

## Risco 3 – Uso indevido de dados para criação de perfis falsos

**Descrição:**Atacantes criam contas falsas usando dados reais de usuários para se passar por eles.

### Mitigação
**Curto prazo**

- Validação de e-mail e uso de CAPTCHA no cadastro.

**Médio prazo**

- Detecção automática de padrões suspeitos (mesmo IP, dispositivo, horário repetitivo).

**Longo prazo**

- Sistema de reputação e verificação adicional para contas novas.

## Risco 4 – Comentários que violem diretrizes do blog

**Descrição:** Comentários contendo discurso de ódio, conteúdo impróprio, spam ou manipulação.

### Mitigação
**Curto prazo**

- Moderação manual ou por lista de palavras proibidas.

**Médio prazo**

- Ferramenta automática de detecção de linguagem tóxica.

**Longo prazo**

- Revisão contínua das diretrizes e sistema de denúncia pelos usuários.

## Risco 5 – Notícias ou publicações falsas (Fake News)

**Descrição:** Publicação de informações falsas ou mal-intencionadas que afetem a credibilidade da plataforma.

### Mitigação
**Curto prazo**

- Sinalização manual ou moderação obrigatória de postagens de alto impacto.

**Médio prazo**

- Ferramenta automática de verificação de conteúdo suspeito.

- Longo prazo

- Parcerias com serviços de fact-checking.
-----
