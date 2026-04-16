<h1 align="center">Eric Hiroshi</h1>

<p align="center">
  <strong>Backend Engineer · Java & Spring Boot</strong>
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

Desenvolvedor backend com foco em **Java e Spring Boot**, construindo APIs REST prontas para produção com observabilidade, resiliência e segurança desde a concepção. Formado em **Engenharia de Software** e **Análise e Desenvolvimento de Sistemas** (Centro Universitário da Grande Dourados).

Interesse em fintech e empresas com cultura de engenharia forte. Gosto de resolver problemas reais de persistência, segurança e infraestrutura — e de documentar bem o que construo.

---

## Stack principal

**Linguagens & Frameworks**

![Java](https://img.shields.io/badge/Java_25-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot_4-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white)
![Spring Data JPA](https://img.shields.io/badge/Spring_Data_JPA-6DB33F?style=flat-square&logo=spring&logoColor=white)

**Persistência**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis_8-DC382D?style=flat-square&logo=redis&logoColor=white)
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
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

---

## Projetos em destaque

### 🎙️ [dio-speech-ai](https://github.com/erichiroshi/dio-speech-ai) — API de transcrição de áudio com Whisper

> Projeto final do bootcamp **DIO × Globant — Java & Spring Boot AI Developer**

API REST de speech-to-text construída em **4 fases evolutivas** com foco em qualidade de produção:

| Fase | O que foi construído |
|---|---|
| Fase 1 | API base, integração Whisper via Speaches, Docker Compose, ProblemDetail (RFC 9457) |
| Fase 2 | Observabilidade completa: Prometheus, Grafana (12 painéis), Zipkin/OTel, logs JSON + MDC |
| Fase 3 | Resiliência: CircuitBreaker + Retry com backoff, JWT stateless, Testcontainers |
| Fase 4 | Documentação: SpringDoc OpenAPI 3.1, Swagger UI interativo |

**Destaques técnicos:**
- Cache inteligente com SHA-256 do conteúdo binário → mesmo áudio com nomes diferentes acerta o cache · hit em ~15ms vs ~800ms sem cache
- CircuitBreaker (Resilience4j) protege contra falhas em cascata do serviço de IA · fallback HTTP 503 imediato
- Logs estruturados JSON com MDC (requestId correlacionado nos erros + nos traces do Zipkin)
- Testes de integração com Redis real (Testcontainers) e Speaches simulado (MockWebServer)
- Provisioning automático do Grafana via arquivos versionados no repositório

🔗 [GitHub](https://github.com/erichiroshi/dio-speech-ai) · 🌐 [Documentação](https://erichiroshi.github.io/dio-speech-ai/) · 🗺️ [Roadmap](https://erichiroshi.github.io/dio-speech-ai/roadmap_dio_speech_ai.html)

`Java 25` `Spring Boot 4` `Redis` `Resilience4j` `Prometheus` `Grafana` `Zipkin` `JWT` `Docker Compose` `Testcontainers` `OpenAPI 3.1`

---

### 📚 [library-api](https://github.com/erichiroshi/library-api) — API de gerenciamento de biblioteca

API REST completa com arquitetura de microservices:

- **Autenticação** JWT stateless com Spring Security
- **Observabilidade** full stack: Prometheus · Grafana · logs estruturados
- **CI/CD** automático com GitHub Actions
- **Microservices**: descoberta de serviços (Eureka), roteamento (API Gateway), configuração centralizada (Config Server)

`Java 25` `Spring Boot` `Spring Cloud` `PostgreSQL` `Flyway` `Docker Compose` `GitHub Actions`

---

### Outros projetos

| Repositório | Descrição | Stack |
|---|---|---|
| [upload-s3](https://github.com/erichiroshi/upload-s3) | Upload de arquivos integrado com AWS S3 | Java, Spring, AWS SDK |
| [envio-de-email](https://github.com/erichiroshi/EnvioDeEmail) | Envio de e-mails transacionais com templates | Java, Spring Mail |
| [mapstruct-com-lombok](https://github.com/erichiroshi/mapstruct-com-lombok) | Mapeamento de DTOs com MapStruct + Lombok | Java, MapStruct |

---

## Formação

**Engenharia de Software** — Centro Universitário da Grande Dourados  
**Tecnologia em Análise e Desenvolvimento de Sistemas** — Centro Universitário da Grande Dourados

---

## Contato

Aberto a oportunidades como **Backend Engineer**, **Java Developer** ou **Spring Boot Developer**.

📧 erichiroshi@hotmail.com · 📱 (67) 99938-4499 · 💼 [linkedin.com/in/eric-hiroshi](https://www.linkedin.com/in/eric-hiroshi)
