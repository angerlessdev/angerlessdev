# Angel Cancho

**Practicante de Desarrollo de Software en Lima Expresa (VINCI Highways)** · Ingeniería de Software en la UPC (9.º ciclo) · Lima, Perú

Construyo software que funciona en producción: backends en Python/FastAPI con arquitectura hexagonal, frontends en Angular, apps en Flutter y SQL Server, siempre con pruebas automatizadas.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-angel--cancho-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/angel-cancho/)

## En producción

> Estos proyectos son privados. Aquí cuento qué hacen y qué resultados tienen.

### PEX Monitoreo · monitoreo operacional de la red de peajes

Diseñé y construí de punta a punta la plataforma que vigila en tiempo real más de 500 equipos de 9 tipos (barreras, antenas RFID, cámaras IP, UPS y PCs), integrados por ingeniería inversa de protocolos propietarios.

- **Arquitectura:** FastAPI con arquitectura hexagonal y DDD, frontend en Angular 21, Event Bus y WebSocket para el tiempo real, alertas por WhatsApp.
- **Migración:** pasé la base de producción de MySQL a SQL Server con un traductor de dialecto en un solo adaptador, sin modificar ningún repositorio.
- **Rendimiento:** endpoint crítico de 953 ms a 16 ms; 5,071 deadlocks contenidos con reintentos y backoff; pool de conexiones de 32/32 a cero agotamientos.
- **Vida útil:** relojes de desgaste en competencia (Palmgren-Miner en barreras); 278 de 547 equipos ya superan su vida de diseño.
- **Calidad:** más de 3,200 pruebas con pytest, BDD con behave, mutation testing (mutmut, Stryker) y gates de cobertura en CI.

### AVIX · registro de incidencias por voz

Los operadores de peaje dictan la incidencia y siguen trabajando, incluso sin señal; los supervisores la revisan en un panel web. Del pedido a producción en una semana, con 294 pruebas automatizadas y login con Active Directory.

`Flutter` `FastAPI` `SQL Server`

### Reporte de Caudales · alertas de crecida por WhatsApp

Reporte horario de 4 estaciones hidrológicas y alertas de umbral. La regla de confirmación (4 de las últimas 5 lecturas) descarta los 19 picos falsos del historial del sensor y confirma una crecida en 2.5 minutos (mediana).

`Python` `Microsoft Graph API` `WhatsApp`

### Tesis · riesgo crediticio para MyPEs (en curso, en coautoría)

Plataforma web predictiva: comparamos 11 algoritmos de machine learning, las predicciones se explican con SHAP y un LLM (Gemini) redacta las recomendaciones.

`Python` `scikit-learn` `FastAPI` `React`

## Código público: Nexus Finance

Plataforma de microcréditos en microservicios: un núcleo bancario en Java decide los préstamos apoyado en un motor de riesgo con machine learning en Python.

| Repositorio | Qué hace | Stack |
|---|---|---|
| [nexus-backend-core](https://github.com/nexus-fintech/nexus-backend-core) | Clientes y préstamos con DDD, CQRS y puertos y adaptadores | Java 21 · Spring Boot · MySQL |
| [nexus-risk-engine](https://github.com/nexus-fintech/nexus-risk-engine) | Evaluación de riesgo crediticio con machine learning, expuesta como API | Python · FastAPI · scikit-learn · Docker |
| [nexus-frontend-web](https://github.com/nexus-fintech/nexus-frontend-web) | Portal web administrativo | Angular 19 · Signals |
| [nexus-finance-platform](https://github.com/nexus-fintech/nexus-finance-platform) | Orquestación de los servicios y documentación de la arquitectura | Docker Compose |

También: [springboot-testing-practice](https://github.com/angerlessdev/springboot-testing-practice), pruebas unitarias y de integración con JUnit 5 y Mockito (Java 21).

## Stack

| Área | Tecnologías |
|---|---|
| Backend | Python, FastAPI, Java, Spring Boot · arquitectura hexagonal, DDD, REST, WebSockets |
| Frontend y móvil | Angular, TypeScript, RxJS, Tailwind CSS, Flutter |
| Datos | SQL Server (T-SQL), MySQL, PostgreSQL |
| Calidad y DevOps | pytest, behave (BDD), Playwright, mutmut, Stryker, Docker, GitHub Actions |
| IA aplicada | scikit-learn, SHAP, LLM (Gemini), desarrollo con agentes (Claude Code) |
