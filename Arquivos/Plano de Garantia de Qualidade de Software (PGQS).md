# 📌 ISO/IEC 25010 Aplicado ao Projeto UniBlog

Com base na **ISO/IEC 25010:2011**, foram selecionadas as características de qualidade mais relevantes para o projeto **UniBlog**. Essas características servirão como **requisitos de qualidade** e serão acompanhadas no **Plano de Garantia da Qualidade de Software (PGQS)**.

---

## 🎯 Prioridades de Qualidade no UniBlog

### 1. **Confiabilidade (Confiança)**

* **Maturidade:** O sistema deve apresentar baixa taxa de falhas em produção.
* **Disponibilidade:** O sistema deve estar acessível 99% do tempo em produção.
* **Tolerância a Falhas:** Em caso de falhas parciais (ex.: serviço de eventos), o feed principal deve permanecer acessível.
* **Recuperabilidade:** Backups automáticos diários do banco de dados e plano de recuperação em até 4h.

🔒 **Garantia:**

* Testes de carga e stress.
* Estratégia de rollback em deploys.
* Monitoramento e registro de incidentes.

---

### 2. **Usabilidade**

* **Reconhecimento de Adequação:** Interface intuitiva para estudantes sem necessidade de treinamento.
* **Aprendizibilidade:** Novo usuário deve conseguir realizar seu primeiro post em menos de 5 minutos.
* **Proteção contra Erros:** Mensagens claras de erro e formulários validados antes do envio.
* **Acessibilidade:** Interface compatível com boas práticas de acessibilidade.

🎨 **Garantia:**

* Protótipos no Figma validados com usuários.
* Testes de usabilidade com colegas da comunidade acadêmica.

---

### 3. **Segurança**

* **Confidencialidade:** Dados pessoais dos usuários devem estar protegidos (uso de HTTPS e criptografia).
* **Autenticidade:** Login seguro via JWT.
* **Integridade:** Alterações de conteúdo devem ser registradas e auditáveis.
* **Responsabilização:** Ações críticas associadas a perfis de usuário (ex.: edição de posts).

🔐 **Garantia:**

* Testes de segurança de API (Postman).
* Políticas de senha forte e autenticação segura.

---

### 4. **Eficiência de Desempenho**

* **Comportamento em Tempo:** O feed deve carregar em até **3 segundos** em condições normais.
* **Utilização de Recursos:** Aplicação deve ser otimizada para rodar em hospedagens com recursos limitados.
* **Capacidade:** Deve suportar até **100 usuários simultâneos** no MVP.

⚡ **Garantia:**

* Testes de performance com ferramentas de carga (ex.: JMeter ou k6).
* Monitoramento do consumo de recursos no servidor.

---

### 5. **Manutenibilidade**

* **Modularidade:** Código organizado em módulos reutilizáveis.
* **Analisabilidade:** Padrão de commits e documentação de código para facilitar entendimento.
* **Testabilidade:** Cobertura mínima de 80% do código crítico.

🛠️ **Garantia:**

* Revisões de código no GitHub.
* Linters e formatação padronizada (ESLint)

---

### 6. **Portabilidade**

* **Adaptabilidade:** Sistema responsivo.

🌐 **Garantia:**

* Testes em múltiplos dispositivos e SOs.
* Containerização via Docker para padronizar ambientes.

---

## ✅ Conclusão

No **PGQS do UniBlog**, as características **Confiabilidade, Usabilidade e Segurança** serão as de **maior prioridade**, enquanto **Eficiência, Manutenibilidade e Portabilidade** complementam os requisitos essenciais para garantir que o sistema seja estável, acessível e adequado ao público acadêmico.
