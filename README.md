# 👋 Olá, eu sou o Andrey Oliveira

**Desenvolvedor Back-end Java | Acadêmico de Análise e Desenvolvimento de Sistemas**

Estou construindo minha base para a primeira vaga em Java aplicando engenharia de software deliberada: TDD do início ao fim, decisões arquiteturais documentadas e explicadas (não só implementadas), e disposição para mostrar bugs reais encontrados e corrigidos — não só código que "já nasceu perfeito".

---

### 🧠 Como eu trabalho

- **TDD (Test-Driven Development):** Red → Green → Refactor. Nenhuma linha de produção sem um teste falhando antes.
- **Decisões documentadas, não só código:** uso ADR (Architecture Decision Record) para registrar o *porquê* de cada escolha técnica não-óbvia — inclusive quando a decisão foi um trade-off consciente, não a solução "ideal" de livro-texto.
- **Bugs reais fazem parte da história:** projetos concluídos têm seção própria documentando bugs de produção encontrados e corrigidos, porque isso prova que a suíte de testes funciona de verdade.

---

### 💎 Projetos em Destaque

#### Library Manager
API REST para gestão de acervo de biblioteca — meu projeto "flagship".

- **Regras de negócio reais:** controle de disponibilidade de cópias, bloqueio de empréstimo duplicado, cálculo automático de multa por atraso, filtros de busca compostos dinamicamente via **JPA Specification**.
- **Autenticação:** Spring Security + **JWT** stateless, com injeção de dependência via construtor (não setter público) — decisão documentada em ADR após identificar risco de mutação indevida da chave de assinatura.
- **Tratamento de erros:** `GlobalExceptionHandler` centralizado distinguindo 404 (recurso inexistente) de 422 (violação de regra de negócio).
- **Stack:** Java 21 · Spring Boot 4 · PostgreSQL · Spring Security + JWT · JPA Specification
- **[🔗 Repositório](https://github.com/Andrey479/librarymanager)**

#### Notification Hub
Serviço satélite do Library Manager — minha resposta à pergunta "e se a API externa cair?".

- **Integração externa resiliente:** consome a API pública da Open Library via **RestClient**, com fallback gracioso em três cenários de falha (404, timeout, JSON malformado) — nunca retorna 500 por causa de uma falha que não é minha.
- **Job agendado:** `@Scheduled` diário para atualizar status de empréstimos vencidos.
- **Testado com WireMock:** testes de integração cobrindo sucesso e todos os cenários de falha da API externa, sem depender de conectividade real.
- **Containerizado:** Docker multi-stage + `docker-compose` orquestrando aplicação e PostgreSQL.
- **Stack:** Java 21 · Spring Boot 4 · RestClient · Docker · WireMock
- **[🔗 Repositório](https://github.com/Andrey479/notification-hub)**

---

### 🛠 Toolbox Técnica

| Categoria | Tecnologias |
| :--- | :--- |
| **Linguagens** | ![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) |
| **Frameworks** | ![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=spring-boot&logoColor=white) |
| **Persistência** | PostgreSQL, JPA/Hibernate, JPA Specification |
| **Segurança** | Spring Security, JWT (JJWT) |
| **Integração** | RestClient, WireMock |
| **Qualidade** | JUnit 5, Mockito, TDD, SOLID, Clean Code |
| **Infra** | Docker, Docker Compose, Git, GitHub Actions |

---

### 📊 Estatísticas e Atividade

<p align="center">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=Andrey479&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true" />
  <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Andrey479&layout=compact&langs_count=7&theme=tokyonight" />
</p>

---

### 📫 Vamos Conversar?

Estou sempre aberto a trocas de conhecimento sobre o ecossistema Java e arquitetura de sistemas.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/andrey-oliveira-software)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:andreyofbbrasil@gmail.com)
