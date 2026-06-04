<h1 align="center">Eric Hiroshi</h1>

<p align="center">
  <strong>Backend Engineer | Java | Spring | Arquitetura Hexagonal | Mensageria | Observabilidade</strong>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/eric-hiroshi">
    <img src="https://img.shields.io/badge/LinkedIn-eric--hiroshi-0A66C2?style=flat-square&logo=linkedin&logoColor=white" />
  </a>
  <a href="mailto:erichiroshi@hotmail.com">
    <img src="https://img.shields.io/badge/Email-erichiroshi%40hotmail.com-D44638?style=flat-square&logo=gmail&logoColor=white" />
  </a>
</p>

---

## Sobre

Desenvolvedor backend com foco em **Java e Spring Boot**, construindo sistemas que vão além do CRUD: autenticação JWT stateless, mensageria assíncrona com RabbitMQ, resiliência com Resilience4j, observabilidade full stack e arquitetura de microsserviços com Spring Cloud.

Formado em **Engenharia de Software** e **Análise e Desenvolvimento de Sistemas** pelo Centro Universitário da Grande Dourados. Construo projetos de portfólio com padrões de produção — com CI/CD, testes de integração, Docker Compose e documentação — porque acredito que código sem contexto operacional não comunica capacidade real.

---

## Stack principal

**Linguagens & Frameworks**

![Java](https://img.shields.io/badge/Java_21+-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white)
![Spring Data JPA](https://img.shields.io/badge/Spring_Data_JPA-6DB33F?style=flat-square&logo=spring&logoColor=white)
![Spring Cloud](https://img.shields.io/badge/Spring_Cloud-6DB33F?style=flat-square&logo=spring&logoColor=white)
![Spring AI](https://img.shields.io/badge/Spring_AI-6DB33F?style=flat-square&logo=spring&logoColor=white)

**Mensageria & Integração**

![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=flat-square&logo=rabbitmq&logoColor=white)
![OpenFeign](https://img.shields.io/badge/OpenFeign-000000?style=flat-square)
![RestClient](https://img.shields.io/badge/RestClient-6DB33F?style=flat-square&logo=spring&logoColor=white)

**Persistência**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Flyway](https://img.shields.io/badge/Flyway-CC0200?style=flat-square&logo=flyway&logoColor=white)
![H2](https://img.shields.io/badge/H2-1E90FF?style=flat-square)

**Observabilidade**

![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![Zipkin](https://img.shields.io/badge/Zipkin-FFA500?style=flat-square)
![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-000000?style=flat-square&logo=opentelemetry&logoColor=white)

**Resiliência & Segurança**

![Resilience4j](https://img.shields.io/badge/Resilience4j-2E86AB?style=flat-square)
![JWT](https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white)
![OpenAPI](https://img.shields.io/badge/OpenAPI_3.1-6BA539?style=flat-square&logo=openapiinitiative&logoColor=white)

**Infra & DevOps**

![Docker](https://img.shields.io/badge/Docker_Compose-2496ED?style=flat-square&logo=docker&logoColor=white)
![AWS S3](https://img.shields.io/badge/AWS_S3-FF9900?style=flat-square&logo=amazons3&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

**Testes**

![JUnit 5](https://img.shields.io/badge/JUnit_5-25A162?style=flat-square&logo=junit5&logoColor=white)
![Testcontainers](https://img.shields.io/badge/Testcontainers-000000?style=flat-square&logo=docker&logoColor=white)
![MockWebServer](https://img.shields.io/badge/MockWebServer-000000?style=flat-square)

---

## Projetos em destaque

### 🎙️ [speech-ai-hexagonal](https://github.com/erichiroshi/speech-ai-hexagonal) — Plataforma Backend de Transcrição e Análise de Áudio

API REST de speech-to-text construída com **Arquitetura Hexagonal**, em fases evolutivas com foco em qualidade de produção. Integra Whisper via Speaches, Spring AI + Ollama e notificações multicanal.

| Fase | O que foi construído |
|---|---|
| Fase 1 | Arquitetura Hexagonal desde o início: domínio puro, portas/adapters, RestClient, ProblemDetail RFC 9457, Docker Compose |
| Fase 2 | Qualidade de código: SonarQube + JaCoCo (threshold 60%), Codecov, pipeline CI integrado |
| Fase 3 | Persistência: PostgreSQL + JPA + Flyway, deduplicação por hash SHA-256, portas desacopladas do ORM |
| Fase 4 | Cache Redis com chave SHA-256 do conteúdo binário, TTL configurável, testes com Testcontainers |
| Fase 5 | Resiliência: CircuitBreaker + Retry com backoff exponencial + Bulkhead, testes com WireMock |
| Fase 6 | Observabilidade: Prometheus, Grafana (dashboards provisionados via código), Zipkin/OTel, logs JSON + MDC |
| Fase 7 | Testes arquiteturais com ArchUnit validando regras da Arquitetura Hexagonal no pipeline |
| Fase 8 | Spring AI + OpenAI Whisper como segunda porta de saída, seleção por profile/config |
| Fase 9 | Spring AI + Ollama para resumo de transcrições, novo bounded context `analysis/`, cache Redis para resumos |
| Fase 10 | Mensageria RabbitMQ: EventPublisherPort, consumer de auditoria, DLQ, testes com Testcontainers |
| Fase 11 | Notificações multicanal via eventos RabbitMQ: e-mail, SMS e WhatsApp |

**Destaques técnicos:**
- Domínio 100% livre de Spring — use cases testáveis sem contexto, portas são interfaces Java puras
- Cache SHA-256 do conteúdo binário → mesmo áudio com nomes diferentes acerta o cache · hit em ~15ms vs ~800ms sem cache
- Dois adapters de transcrição intercambiáveis (Speaches local / OpenAI cloud) via `@ConditionalOnProperty` — use case não muda uma linha
- Dois bounded contexts hexagonais independentes: `transcription/` e `analysis/`
- Testes arquiteturais com ArchUnit garantem que nenhuma camada viola as fronteiras hexagonais no CI
- CircuitBreaker + Retry + Bulkhead (Resilience4j) com WireMock simulando falhas reais do Speaches

🔗 [GitHub](https://github.com/erichiroshi/speech-ai-hexagonal) · 🌐 [Documentação](https://erichiroshi.github.io/speech-ai-hexagonal/) · 🗺️ [Roadmap](https://erichiroshi.github.io/speech-ai-hexagonal/roadmap.html)

`Java` `Spring Boot` `Spring AI` `Ollama` `RabbitMQ` `Redis` `Resilience4j` `SonarQube` `ArchUnit` `Prometheus` `Grafana` `Zipkin` `PostgreSQL` `Flyway` `WireMock` `Docker Compose` `Testcontainers` `OpenAPI 3.1`

---

### 📚 [library-api](https://github.com/erichiroshi/library-api) — API de gerenciamento de biblioteca

API REST evoluída do monolito para microsserviços com Spring Cloud, com foco em arquitetura, segurança e observabilidade.

| Fase | O que foi construído |
|---|---|
| Fase 1–2 | Monolito com JWT stateless, upload AWS S3, Redis cache, Resilience4j, Flyway migrations |
| Fase 3 | Microsserviços: Config Server, Eureka, API Gateway com validação JWT centralizada, OpenFeign com Circuit Breaker |
| Fase 4 | Mensageria RabbitMQ, testes de carga com k6/JMeter (monolito vs microsserviços) |

**Destaques técnicos:**
- Gateway como único ponto de entrada: valida JWT e propaga `X-User-Id` / `X-User-Roles` para os serviços internos
- Config Server com Git backend para configuração centralizada e versionada
- Observabilidade full stack: Prometheus · Grafana · logs estruturados
- CI/CD com GitHub Actions: matrix strategy para build paralelo dos serviços, Docker multi-stage

🔗 [GitHub](https://github.com/erichiroshi/library-api)

`Java` `Spring Boot` `Spring Cloud` `Spring Security` `PostgreSQL` `Redis` `RabbitMQ` `Flyway` `AWS S3` `Docker Compose` `GitHub Actions` `Prometheus` `Grafana`

---

### Outros projetos

| Repositório | Descrição | Stack |
|---|---|---|
| [upload-s3](https://github.com/erichiroshi/upload-s3) | Estudo de integração com AWS S3: upload, download e exclusão de arquivos | Java, Spring, AWS SDK |
| [envio-de-email](https://github.com/erichiroshi/EnvioDeEmail) | Estudo de envio de e-mails transacionais com templates HTML | Java, Spring Mail |
| [mapstruct-com-lombok](https://github.com/erichiroshi/mapstruct-com-lombok) | Estudo de mapeamento de DTOs com MapStruct + Lombok | Java, MapStruct |

---

## Formação

**Engenharia de Software** — Centro Universitário da Grande Dourados  
**Tecnologia em Análise e Desenvolvimento de Sistemas** — Centro Universitário da Grande Dourados

---

## Contato

Aberto a oportunidades como **Backend Engineer**, **Java Developer** ou **Spring Boot Developer**.

📧 erichiroshi@hotmail.com · 💼 [linkedin.com/in/eric-hiroshi](https://www.linkedin.com/in/eric-hiroshi)
