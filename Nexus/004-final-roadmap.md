Evet. Bu noktada artık parçalı tavsiyeler vermek yerine, **senin için tek bir sistem** tasarlayabiliriz.

Ve önceki konuşmalarımızdaki fikirleri birleştirince ortaya çıkan şey basit bir “öğrenme roadmap'i” değil:

# **NEXUS — Technical Founder Mastery Roadmap**

### 12 aylık: Computer Engineer → Production Engineer → AI Engineer → Product Builder → Technical Founder

Bu roadmap'in sonunda amaç:

> **Sadece iş bulabilecek bir yazılımcı olmak değil; sıfırdan ciddi bir AI SaaS kurabilen, production'da çalıştırabilen, güvenliğini sağlayabilen, AI ajanlarını yöneten, gerçek kullanıcıdan feedback alabilen, ürününü satabilen ve gerektiğinde bunu bir şirkete dönüştürebilen bir teknik kurucu olmak.**

Ve NEXUS bu eğitimin **laboratuvarı** olacak.

---

# 0. Önce neden bu roadmap'i böyle tasarlıyoruz?

2026'da yazılım öğrenmenin eski modeli:

> HTML → CSS → JS → React → Backend → İş bul

artık yeterli değil.

2025 Stack Overflow araştırmasında profesyonel geliştiricilerin %51'i AI araçlarını günlük kullanıyor; fakat %46'sı AI çıktılarının doğruluğuna aktif olarak güvenmediğini söylüyor. %66'sı da “neredeyse doğru ama tam değil” AI çıktılarından şikâyet ediyor. [Stack Overflow Developer Survey](https://survey.stackoverflow.co/2025/ai?utm_source=chatgpt.com)

DORA'nın 2025 araştırması da AI'ın sihirli bir verimlilik katmanı olmadığını, mevcut mühendislik sisteminin güçlü ve zayıf yönlerini **büyüttüğünü** söylüyor. [Dora](https://dora.dev/research/2025/dora-report/?utm_source=chatgpt.com)

Dolayısıyla senin hedefin:

> **AI'ın yapabildiği şeyleri ezberlemek değil.**

Şunları öğrenmek:

```
Problem
  ↓
System
  ↓
Architecture
  ↓
Implementation
  ↓
AI assistance
  ↓
Verification
  ↓
Testing
  ↓
Deployment
  ↓
Observation
  ↓
Iteration
  ↓
Business outcome
```

Bu yüzden NEXUS'u özellikle böyle tasarlıyoruz.

---

# 1. NEXUS'un nihai vizyonu

NEXUS'u ilk günden devasa yapmayacağız.

Ama **mimari vizyonu** şu:

```
                         NEXUS
              AI Operating System
                for Organizations
                         │
       ┌─────────────────┼─────────────────┐
       │                 │                 │
    PEOPLE             DATA             AGENTS
       │                 │                 │
       ↓                 ↓                 ↓
    Teams            Knowledge        Research Agent
    Roles             Documents       Sales Agent
    Permissions       CRM             Support Agent
    Approvals         DB              Finance Agent
                       │               Analyst Agent
                       ↓
                COMPANY CONTEXT
                       │
                Knowledge Graph
                       │
                Agent Runtime
                       │
       ┌───────────────┼────────────────┐
       ↓               ↓                ↓
    Reason          Execute           Learn
       │               │                │
       └───────────────┼────────────────┘
                       ↓
                HUMAN APPROVAL
                       ↓
                    ACTION
                       ↓
                   OUTCOME
                       ↓
                    EVALS
                       ↓
                   MEMORY
```

Bu vizyonu destekleyen pazar sinyali de güçlü: Microsoft, insan + AI ajanlarından oluşan “hybrid teams” ve AI-operated/human-led şirketleri geleceğin organizasyon modeli olarak tanımlıyor; araştırmasında liderlerin %81'i ajanların 12–18 ay içinde AI stratejilerine orta veya yoğun şekilde entegre olmasını beklediğini bildiriyor. [Microsoft](https://www.microsoft.com/en-us/worklab/work-trend-index/2025-the-year-the-frontier-firm-is-born?utm_source=chatgpt.com)

YC de 2025 RFS'inde **multiplayer AI** fikrini özellikle öne çıkarıyor: ajanların tek kişinin kullandığı chatbotlar olmaktan çıkıp ekiplerin birlikte izlediği, yönlendirdiği ve devrettiği ortak çalışma alanlarına dönüşmesi. [Y Combinator](https://www.ycombinator.com/rfs/?utm_source=chatgpt.com)

Ama:

## NEXUS V1 bunun tamamı olmayacak.

İlk ürün:

# **AI Revenue Operations Team**

Yani:

```
Leads
CRM
Email
Calendar
Documents
Customer data
Analytics
       ↓
NEXUS
       ↓
Research Agent
Sales Agent
Analytics Agent
Customer Success Agent
       ↓
Human approval
       ↓
Actions
```

Bu **wedge** olacak.

---

# 2. Yol haritasının temel çalışma prensibi

Her konu için şu döngüyü kullanacaksın:

```
LEARN
  ↓
UNDERSTAND
  ↓
BUILD
  ↓
BREAK
  ↓
DEBUG
  ↓
TEST
  ↓
DEPLOY
  ↓
MEASURE
  ↓
IMPROVE
```

Ve AI kullanımında:

```
YOU THINK
    ↓
AI ASSISTS
    ↓
YOU VERIFY
    ↓
YOU TEST
    ↓
YOU OWN THE RESULT
```

**AI senin yerine öğrenmeyecek.**

---

# 3. Teknoloji yığını

Roadmap boyunca stack'i mümkün olduğunca sabit tutacağız.

### Frontend

- TypeScript
- React
- Next.js
- Tailwind
- shadcn/ui

### Backend

- TypeScript
- Fastify

### AI backend

- Python
- FastAPI

### Database

- PostgreSQL
- pgvector

### State / infrastructure

- Redis
- background workers
- queues

### DevOps

- Docker
- GitHub Actions
- Cloudflare
- AWS gerektiğinde

### Testing

- Vitest
- Playwright

### Observability

- Sentry
- OpenTelemetry
- Prometheus/Grafana gerektiğinde

### AI

- OpenAI
- Anthropic
- Google
- open-source models
- model gateway

### Architecture

**Modular monolith first.**

Microservices **sonradan**.

Bu karar özellikle önemli.

---

# 4. 12 aylık harita

Genel resim:

```
MONTH 1
Software foundations
       ↓
MONTH 2
Backend + Database
       ↓
MONTH 3
Frontend + Full Stack
       ↓
MONTH 4
Testing + Security + Architecture
       ↓
MONTH 5
Docker + CI/CD + Cloud
       ↓
MONTH 6
Redis + Queues + Workers + Observability
       ↓
MONTH 7
LLM Engineering
       ↓
MONTH 8
RAG + Company Context
       ↓
MONTH 9
Agent Runtime + Tools
       ↓
MONTH 10
Evals + AI Security + Reliability
       ↓
MONTH 11
Product + Users + Sales
       ↓
MONTH 12
Billing + Growth + Scale + Founder Mode
```

Şimdi bunu gerçekten ayrıntılandıralım.

---

# PHASE I — FOUNDATION

# Ay 1 — Engineering Fundamentals

## Hedef

Kod yazmayı değil:

> **mühendislik yapmayı**

öğrenmek.

---

## Hafta 1 — Git + GitHub + CLI

### Öğren

- Git internals
- working tree
- staging
- commit
- branch
- merge
- rebase
- cherry-pick
- revert
- reset
- stash
- tags
- GitHub
- PR
- issue
- release

### Neden?

Çünkü gerçek mühendislik:

> dosyayı kaydet → çalıştır

değil.

Takım içinde değişiklik yönetmektir.

### NEXUS

Repository oluştur:

```
nexus/
├── apps/
├── packages/
├── docs/
├── .github/
└── README.md
```

Henüz büyük kod yazma.

---

# Hafta 2 — Linux + CLI + Networking Fundamentals

### Öğren

- filesystem
- processes
- permissions
- environment variables
- pipes
- grep
- curl
- SSH
- ports
- localhost
- DNS
- TCP/IP temel mantığı

### Neden?

Çünkü production'da terminalden kaçamayacaksın.

### NEXUS

Local development environment'ını CLI üzerinden yönet.

---

# Hafta 3 — HTTP

Şunları gerçekten anlamalısın:

```
Browser
 ↓
DNS
 ↓
TCP
 ↓
TLS
 ↓
HTTP
 ↓
Server
```

Öğren:

- GET
- POST
- PUT
- PATCH
- DELETE
- headers
- cookies
- sessions
- status codes
- CORS
- caching
- idempotency

### Mini proje

Fastify ile:

```
GET /health
GET /users
POST /users
PATCH /users/:id
DELETE /users/:id
```

---

# Hafta 4 — TypeScript Deep Dive

Sen zaten JS/TS biliyorsun; şimdi bunu profesyonel seviyeye çekiyoruz.

Öğren:

- type system
- generics
- unions
- intersections
- narrowing
- utility types
- interfaces
- type guards
- async
- promises
- error handling
- modules
- runtime vs compile-time

### Çıkış sınavı

AI'a sormadan:

> “Neden TypeScript type safety runtime'da seni korumaz?”

açıklayabilmelisin.

---

# Ay 1 sonunda

NEXUS:

```
Next.js
+
Fastify
+
TypeScript
```

ile ayağa kalkmış olacak.

Henüz ürün yok.

**Temel var.**

---

# PHASE II — BACKEND ENGINEERING

# Ay 2 — Database + API + Multi-tenancy

Burada NEXUS gerçek bir SaaS olmaya başlıyor.

---

# Hafta 5 — PostgreSQL

Öğren:

- tables
- primary keys
- foreign keys
- constraints
- joins
- indexes
- normalization
- transactions

Schema:

```
users
organizations
memberships
```

---

# Hafta 6 — Advanced SQL

Öğren:

- CTE
- window functions
- subqueries
- EXPLAIN
- query planning
- composite indexes
- partial indexes

### Neden?

Çünkü:

> “SQL biliyorum.”

ile:

> “Database neden yavaş?”

arasında büyük fark var.

---

# Hafta 7 — API Design

NEXUS API:

```
/auth
/users
/organizations
/memberships
/agents
/tasks
```

Öğren:

- validation
- pagination
- filtering
- sorting
- error schemas
- API versioning
- idempotency

---

# Hafta 8 — Multi-tenancy

Bu NEXUS için kritik.

Bir şirket:

```
Organization A
```

diğer şirket:

```
Organization B
```

verisini asla görememeli.

Öğren:

- tenant isolation
- RBAC
- permissions
- ownership
- authorization boundaries

---

# Ay 2 sonunda

NEXUS:

> Multi-tenant SaaS backend

olacak.

---

# PHASE III — FULL STACK

# Ay 3 — Frontend Engineering

---

# Hafta 9 — React Architecture

Öğren:

- component design
- composition
- hooks
- state
- server state
- forms
- validation

---

# Hafta 10 — Next.js

Öğren:

- App Router
- Server Components
- Client Components
- server actions
- caching
- loading
- error boundaries
- metadata

---

# Hafta 11 — Product UI

NEXUS:

```
Login
Dashboard
Organization
Members
Projects
Settings
```

---

# Hafta 12 — UX

Öğren:

- information architecture
- empty states
- loading states
- error states
- responsive design
- accessibility
- onboarding

Burada önemli:

**UI sadece güzel görünmek değildir.**

Kullanıcıya:

> “Şimdi ne yapmalıyım?”

sorusunun cevabını vermektir.

---

# Ay 3 sonunda

İlk gerçek NEXUS:

```
Frontend
    ↓
API
    ↓
PostgreSQL
```

çalışacak.

---

# PHASE IV — PROFESSIONAL ENGINEERING

# Ay 4 — Testing + Security + Architecture

Burada “kod yazan adam” ile “mühendis” arasındaki fark açılmaya başlıyor.

---

# Hafta 13 — Testing

Öğren:

### Unit

Fonksiyon.

### Integration

Modüller.

### E2E

Gerçek kullanıcı akışı.

NEXUS testleri:

```
register
login
create organization
invite user
create task
authorization
```

---

# Hafta 14 — Security

Öğren:

- OWASP Top 10
- SQL injection
- XSS
- CSRF
- SSRF
- authentication
- authorization
- password hashing
- secrets
- encryption
- rate limiting

---

# Hafta 15 — Architecture

Öğren:

- separation of concerns
- modular monolith
- dependency inversion
- domain boundaries
- service layer
- repositories
- event boundaries

---

# Hafta 16 — Refactoring

NEXUS koduna geri dön.

Şunları bul:

> Neresi coupling?

> Neresi duplication?

> Neresi yanlış abstraction?

> Neresi gereksiz abstraction?

---

# Ay 4 sonunda

NEXUS:

**test edilmiş + güvenli + modüler**

olacak.

---

# PHASE V — PRODUCTION

# Ay 5 — Docker + CI/CD + Cloud

---

# Hafta 17 — Docker

Öğren:

- image
- container
- volume
- network
- Dockerfile
- Compose
- multi-stage builds

NEXUS:

```
frontend
backend
postgres
redis
```

containerized.

---

# Hafta 18 — CI

GitHub Actions:

```
push
 ↓
lint
 ↓
typecheck
 ↓
test
 ↓
build
```

---

# Hafta 19 — CD

```
main
 ↓
CI
 ↓
build
 ↓
deploy
 ↓
production
```

---

# Hafta 20 — Cloud

Öğren:

- DNS
- HTTPS
- reverse proxy
- secrets
- environment separation
- staging
- production
- backups

---

# Ay 5 sonunda

NEXUS internette gerçek bir production deployment'a sahip olacak.

---

# PHASE VI — DISTRIBUTED BACKEND

# Ay 6 — Redis + Workers + Observability

Bu ay çok önemli.

---

# Hafta 21 — Redis

Öğren:

- caching
- TTL
- sessions
- rate limiting
- distributed locks

---

# Hafta 22 — Queues

Öğren:

- jobs
- retries
- dead-letter queues
- backoff
- idempotency

NEXUS:

```
API
 ↓
Queue
 ↓
Worker
 ↓
Task
```

---

# Hafta 23 — Observability

Öğren:

### Logs

Ne oldu?

### Metrics

Ne kadar oldu?

### Traces

Nerede oldu?

---

# Hafta 24 — Reliability

Öğren:

- timeout
- retry
- exponential backoff
- circuit breaker
- graceful degradation
- health checks
- backups

---

# Ay 6 sonunda

NEXUS artık:

> **gerçek bir production backend**

olacak.

---

# 🧠 Bu noktada ilk büyük sınav

Kendine şu görevi ver:

> **NEXUS'a aynı anda 10.000 kullanıcı task gönderirse ne olur?**

Araştır.

Test et.

Kır.

Optimize et.

İşte burada system design öğrenmeye başlıyorsun.

---

# PHASE VII — AI ENGINEERING

# Ay 7 — LLM Fundamentals + AI Gateway

Şimdi AI'ı sisteme ekliyoruz.

---

# Hafta 25 — LLM internals

Öğren:

- tokenization
- embeddings
- transformers
- attention
- positional information
- context window
- inference
- sampling

Amaç:

> Transformer'ı sıfırdan üretmek değil.

**LLM'nin neden nasıl davrandığını anlayabilmek.**

---

# Hafta 26 — Model APIs

OpenAI / Anthropic / Google.

Öğren:

- streaming
- structured output
- tool calling
- function calling
- retries
- fallbacks

---

# Hafta 27 — AI Gateway

NEXUS:

```
Application
     ↓
AI Gateway
     ↓
Model Router
 ┌───┼────┐
 ↓   ↓    ↓
GPT Claude Gemini
```

Tek sağlayıcıya kilitlenme.

---

# Hafta 28 — AI Cost + Latency

Ölç:

```
tokens
latency
cost
success rate
```

Routing:

```
simple → cheap
complex → expensive
```

---

# Ay 7 sonunda

NEXUS'un ilk AI yeteneği:

> **AI task execution**

çalışacak.

---

# PHASE VIII — COMPANY CONTEXT

# Ay 8 — RAG + Knowledge + Context Engineering

Burası NEXUS'un en önemli katmanlarından biri.

---

# Hafta 29 — Embeddings

Öğren:

- semantic similarity
- embedding spaces
- cosine similarity
- vector search

---

# Hafta 30 — RAG

```
Document
 ↓
Parser
 ↓
Chunk
 ↓
Embedding
 ↓
Vector DB
 ↓
Retrieve
 ↓
Context
 ↓
LLM
```

---

# Hafta 31 — Advanced Retrieval

Öğren:

- hybrid search
- BM25
- reranking
- metadata filtering
- query rewriting
- retrieval evaluation

---

# Hafta 32 — Company Knowledge

NEXUS'a:

```
PDF
Docs
Website
CSV
```

yükle.

Agent bunlardan cevap üretsin.

---

# Sonra:

## Knowledge Graph

```
Alice
 ↓ works_on
Project X
 ↓ belongs_to
Customer Y
 ↓ bought
Product Z
```

Öğren:

- entities
- relationships
- graph traversal
- graph-based context

---

# Ay 8 sonunda

NEXUS:

> **şirketin bilgisini anlayan AI platformu**

olacak.

---

# PHASE IX — AGENT ENGINEERING

# Ay 9 — Agent Runtime

Şimdi projenin kalbine geliyoruz.

---

# Hafta 33 — Tools

Agent:

```
search_web()
query_database()
send_email()
create_crm_task()
create_calendar_event()
```

kullanabilecek.

---

# Hafta 34 — Agent Loop

```
Observe
 ↓
Reason
 ↓
Plan
 ↓
Tool
 ↓
Observe
 ↓
Reason
 ↓
...
 ↓
Complete
```

---

# Hafta 35 — State + Memory

Öğren:

- short-term state
- long-term memory
- execution state
- task history
- context management

---

# Hafta 36 — Multi-agent

NEXUS:

```
Research Agent
       ↓
Analysis Agent
       ↓
Strategy Agent
       ↓
Execution Agent
```

Ama kritik:

**Multi-agent kullanmak zorunda değilsin.**

Tek agent daha basitse tek agent.

---

# Ay 9 sonunda

NEXUS:

> **gerçek iş yapabilen AI agent runtime**

olacak.

---

# PHASE X — TRUST

# Ay 10 — Evals + AI Security + Governance

Bence NEXUS'u sıradan AI wrapper'lardan ayıracak ay burası.

Stack Overflow'un 2025 verisinde AI agent kullanan geliştiricilerin %87'si doğruluk, %81'i güvenlik/gizlilik konusunda endişe bildiriyor. [Stack Overflow Developer Survey](https://survey.stackoverflow.co/2025/ai?utm_source=chatgpt.com)

Dolayısıyla:

> Agent yapabiliyorum.

yeterli değil.

**Güvenilir agent yapabilmelisin.**

---

# Hafta 37 — Evals

Ölç:

```
accuracy
tool selection
hallucination
policy compliance
completion rate
```

---

# Hafta 38 — Agent Observability

Her execution:

```
user
prompt
model
tools
context
latency
tokens
cost
result
error
```

olarak kayıtlı.

---

# Hafta 39 — AI Security

Öğren:

- prompt injection
- indirect prompt injection
- data exfiltration
- tool abuse
- excessive agency
- insecure output handling
- privilege escalation

---

# Hafta 40 — Human-in-the-loop

Risk seviyeleri:

```
LOW
   ↓
automatic

MEDIUM
   ↓
notify

HIGH
   ↓
human approval
```

Örneğin:

### Araştırma

Automatic.

### CRM update

Automatic/low risk.

### Email gönderme

Approval.

### Para transferi

**Mandatory approval.**

### Data deletion

**Mandatory approval.**

---

# Ay 10 sonunda

NEXUS:

> **AI-powered**

değil sadece.

> **AI-trustworthy**

hale gelecek.

---

# PHASE XI — PRODUCT

# Ay 11 — Gerçek kullanıcı

Burada çok önemli bir kural:

## Kod yazmayı azalt.

Artık kullanıcılarla konuş.

---

# Hafta 41 — ICP

İlk hedef:

> SMB / startup Revenue Teams

Örneğin:

```
5–50 employee
B2B SaaS
US market
Sales-driven
CRM kullanıyor
AI adoption'a açık
```

---

# Hafta 42 — Customer Interviews

En az:

**20 potansiyel müşteriyle konuş.**

Ama:

> “NEXUS'u beğenir misiniz?”

deme.

Sor:

> “Son 30 günde bu işi nasıl yaptınız?”

> “Nerede zaman kaybettiniz?”

> “Bunun size maliyeti ne?”

> “Şu anda hangi araçları kullanıyorsunuz?”

> “Bunu çözmek için daha önce para ödediniz mi?”

---

# Hafta 43 — MVP

NEXUS V1:

### Tek workflow.

Örneğin:

> **Lead Research + Qualification + CRM Update**

---

# Hafta 44 — Real Users

Hedef:

**5–10 gerçek kullanıcı.**

Ücretsiz olabilir.

Ama:

> gerçek problem + gerçek kullanım.

---

# PHASE XII — FOUNDER

# Ay 12 — Revenue + Growth + Scale

Artık mühendislikten founder moduna geçiyorsun.

---

# Hafta 45 — Billing

Öğren:

- subscriptions
- usage billing
- invoices
- webhooks
- failed payments
- entitlement

---

# Hafta 46 — Pricing

Test et:

```
Free
Pro
Team
Business
```

veya:

```
Platform
+
Usage
```

AI ürünlerinde usage-based veya hibrit model özellikle mantıklı olabilir.

---

# Hafta 47 — Analytics

Öl:

```
Visitors
 ↓
Signup
 ↓
Activation
 ↓
First successful task
 ↓
Weekly usage
 ↓
Paid
 ↓
Retention
```

---

# Hafta 48 — Founder Review

Şu metriklere bak:

### Product

- activation
- retention
- task success
- intervention rate

### AI

- accuracy
- cost/task
- latency
- failure rate

### Business

- conversion
- revenue
- churn
- CAC
- LTV

### Engineering

- uptime
- deployment frequency
- lead time
- failure rate
- recovery time

---

# 5. Bu 12 ay boyunca LeetCode ne olacak?

LeetCode'u **roadmap'in efendisi değil, destekleyicisi** yapıyoruz.

## Ay 1–3

Haftada:

**4–5 problem**

Pattern:

```
Arrays
Hash Map
Two Pointers
Sliding Window
Stack
Binary Search
Linked List
Trees
```

---

## Ay 4–6

Haftada:

**4 problem**

Ek:

```
Heap
Intervals
BFS
DFS
Greedy
Backtracking
```

---

## Ay 7–10

Haftada:

**3 problem**

Ek olarak:

> system design

---

## Ay 11–12

İş görüşmesi hedefliyorsan:

**5–8**

değilse:

**2–3**

yeter.

---

# 6. LeetCode + AI protokolün

Her problem:

### Aşama 1

**15–20 dakika AI yok.**

---

### Aşama 2

Tıkandıysan:

> “Give me one hint. Don't give me the solution.”

---

### Aşama 3

Kodu kendin yaz.

---

### Aşama 4

AI:

> “Review my solution.”

---

### Aşama 5

Optimal solution.

---

### Aşama 6

Kapat.

---

### Aşama 7

Ertesi gün:

**sıfırdan çöz.**

---

# 7. AI'ı roadmap'in tamamında nasıl kullanacaksın?

Burada sana çok net bir kural veriyorum.

## AI'ın yapmasına izin ver:

- documentation search
- boilerplate
- test generation
- refactoring suggestions
- code review
- debugging hypotheses
- SQL optimization suggestions
- architecture alternatives
- learning explanations
- test data
- repetitive code
- documentation

## AI'a bırakma:

- architecture'ın nihai kararı
- security assumptions
- database design'ın tamamı
- production debugging'in tamamı
- testlerin gerçekten neyi test ettiğine karar verme
- AI output'un doğruluğunu kabul etme

Çünkü profesyonel geliştiricilerin AI kullanım oranı çok yüksek olsa da güven problemi hâlâ ciddi; Stack Overflow verisinde geliştiricilerin %46'sı AI çıktılarının doğruluğuna güvenmediğini belirtiyor. [Stack Overflow Developer Survey](https://survey.stackoverflow.co/2025/ai?utm_source=chatgpt.com)

---

# 8. Her ayın sonunda “Gate Exam”

Roadmap'i kurs gibi tüketmeni istemiyorum.

Her ay:

## **NO AI EXAM**

yap.

---

### Ay 1

Sıfırdan REST API.

---

### Ay 2

Database + auth + multi-tenancy.

---

### Ay 3

Full-stack feature.

---

### Ay 4

Test + security audit.

---

### Ay 5

Docker + CI/CD deployment.

---

### Ay 6

Queue + worker + observability.

---

### Ay 7

Multi-model AI gateway.

---

### Ay 8

RAG system.

---

### Ay 9

Agent + tools.

---

### Ay 10

Agent eval + security.

---

### Ay 11

MVP + 5 gerçek kullanıcı.

---

### Ay 12

Paid product.

---

# 9. “Ustalaştım” ölçütümüz

Her teknoloji için:


| Level | Ne yapabiliyorsun?                    |
| ----- | ------------------------------------- |
| 0     | Duymadım                              |
| 1     | Açıklayabiliyorum                     |
| 2     | Tutorial takip ediyorum               |
| 3     | Dokümantasyonla yapıyorum             |
| 4     | Bağımsız çözebiliyorum                |
| **5** | **Production kararını verebiliyorum** |


Senin hedefin:

### Core

**Level 4–5**

- TypeScript
- React/Next
- Backend
- PostgreSQL
- APIs
- Git
- Testing
- Docker
- Cloud
- Security
- System design
- AI engineering

### Secondary

**Level 3–4**

- Redis
- queues
- observability
- distributed systems
- Kubernetes
- Terraform
- Kafka

### Specialized

**Level 4–5**

- LLM applications
- RAG
- agents
- evals
- context engineering
- AI security

---

# 10. System Design'ı ne zaman öğreniyorsun?

**Ay 4'te başlıyor.**

Ama Ay 6'dan itibaren ciddi hale geliyor.

Öğreneceğin konular:

```
Load balancing
Caching
Database scaling
Replication
Sharding
Queues
Event-driven architecture
Consistency
Availability
CAP
Distributed systems
Rate limiting
Idempotency
Fault tolerance
```

Ve NEXUS üzerinden çalış:

> “100K şirket olursa?”

> “1M agent execution/minute olursa?”

> “PostgreSQL çökerse?”

> “Redis çökerse?”

> “LLM provider down olursa?”

> “Bir agent sonsuz loop'a girerse?”

> “Bir tenant 10 milyon request atarsa?”

İşte **system design böyle öğrenilir.**

---

# 11. Business tarafını ne zaman öğreniyorsun?

Başlangıçtan itibaren ama düşük dozda.

Ay 1–6:

**%10**

Ay 7–10:

**%15**

Ay 11–12:

**%40–50**

Çünkü ilk önce bir şey yapabilmen gerekiyor.

Sonra insanların onu isteyip istemediğini anlamalısın.

Sonra satmalısın.

---

# 12. Haftalık çalışma sistemi

Senin mevcut hedeflerin ve öğrenme yaklaşımın için ben bunu şöyle kurardım:

## Haftada 6 gün

### Pazartesi–Cuma

```
2 saat
Deep technical learning

3 saat
NEXUS implementation

1 saat
LeetCode / CS

30 dk
Documentation / notes
```

Yaklaşık:

**6.5 saat/gün**

---

### Cumartesi

```
3 saat
NEXUS

2 saat
System design / architecture

2 saat
Research / product
```

---

### Pazar

**Half-day review**

```
What did I build?
What broke?
What did I misunderstand?
What should I improve?
```

Sonrası dinlenme.

---

# 13. Fakat “6.5 saat” kutsal değil

Önemli olan:

> **Saat doldurmak değil, output üretmek.**

Bir gün:

> 6 saat çalışıp hiçbir şey üretmediysen

başarısız.

Bir gün:

> 3 saat çalışıp production bug çözdüysen

çok değerli.

---

# 14. Her gün sonunda şu 5 soruyu cevapla

```
1. What did I learn?

2. What did I build?

3. What did I break?

4. What did I fix?

5. What did I understand deeply today?
```

Özellikle:

### “What did I break?”

çok önemli.

Çünkü gerçek mühendislik:

> her şeyin çalıştığı tutorial ortamında değil,

**çalışmayan sistemin karşısında** öğreniliyor.

---

# 15. NEXUS GitHub'ı da profesyonel olacak

Repository:

```
nexus/
│
├── apps/
│   ├── web/
│   ├── api/
│   └── worker/
│
├── packages/
│   ├── ui/
│   ├── config/
│   ├── database/
│   ├── auth/
│   ├── ai/
│   └── observability/
│
├── docs/
│   ├── architecture/
│   ├── decisions/
│   ├── api/
│   └── security/
│
├── tests/
│
├── infrastructure/
│
└── .github/
```

---

# 16. ADR kullan

Her önemli mimari kararı yaz:

```
ADR-001
Why PostgreSQL?

ADR-002
Why modular monolith?

ADR-003
Why Redis?

ADR-004
Why queue?

ADR-005
Why multi-model?

ADR-006
Why human approval?

ADR-007
Why RAG?

ADR-008
Why not microservices?
```

Bu seni inanılmaz geliştirir.

Çünkü senior mühendislik:

> “Ne kullandın?”

değil.

> **“Neden onu seçtin?”**

sorusudur.

---

# 17. NEXUS'u aşamalı olarak şu hale getireceğiz

## Version 0.1

```
Auth
Organizations
Users
Dashboard
```

---

## Version 0.2

```
Tasks
Workflows
Background jobs
```

---

## Version 0.3

```
AI Gateway
Model routing
Usage tracking
```

---

## Version 0.4

```
Documents
RAG
Company knowledge
```

---

## Version 0.5

```
Tools
Agents
Executions
```

---

## Version 0.6

```
Permissions
Approvals
Audit logs
```

---

## Version 0.7

```
Evals
Observability
Cost analytics
```

---

## Version 0.8

```
CRM
Email
Calendar
```

---

## Version 0.9

```
Revenue Agent
Sales Agent
Research Agent
```

---

# Version 1.0

## **AI Revenue Operations Team**

Gerçek müşteriye aç.

---

# 18. Sonrasında vizyon

```
V1
Revenue

 ↓

V2
Customer Success

 ↓

V3
Marketing

 ↓

V4
Finance

 ↓

V5
Operations

 ↓

V6
Engineering

 ↓

V7
Company OS
```

Bu noktada NEXUS:

> **AI Agent Platform**

değil,

# **AI Business Operating System**

olur.

---

# 19. Ve burada çok önemli bir “moat” stratejisi var

Model senin moat'in olmayacak.

Çünkü modeller commoditize olabilir.

Agent framework de moat değil.

UI de değil.

Asıl savunulabilir katman:

```
Company Context
       +
Knowledge Graph
       +
Permissions
       +
Execution History
       +
Human Corrections
       +
Evals
       +
Workflow Intelligence
```

Yani:

> **NEXUS şirketin nasıl çalıştığını öğrenir.**

Zamanla:

```
Intent
 ↓
Context
 ↓
Plan
 ↓
Action
 ↓
Human correction
 ↓
Outcome
 ↓
Learning
```

döngüsü oluşur.

Bu çok daha güçlü bir ürün tezidir.

---

# 20. Ve burada senin eski hedefin de birleşiyor

Hatırlarsan daha önce:

> **LLM'lerin nasıl çalıştığını öğrenmek**

istiyordun.

Sonra:

> **AI Context Engineer**

olmak istiyordun.

Sonra:

> kendi AI ürünlerini yapmak

istiyordun.

Şimdi bunların hepsi tek yerde birleşiyor:

```
LLM Fundamentals
        ↓
Context Engineering
        ↓
RAG
        ↓
Knowledge Graph
        ↓
Agent Runtime
        ↓
AI Systems
        ↓
AI Product
        ↓
AI Company
```

Bu yüzden bu proje senin için rastgele seçilmiş bir SaaS değil.

**Öğrenmek istediğin şeylerin doğal birleşim noktası.**

---

# 21. 12 ayın sonunda senden beklediğim profil

Şunu söyleyebiliyor olmalısın:

> “Bir fikrim var.”

Ve:

```
Idea
 ↓
Market research
 ↓
Architecture
 ↓
Database
 ↓
API
 ↓
Frontend
 ↓
Authentication
 ↓
AI
 ↓
RAG
 ↓
Agents
 ↓
Testing
 ↓
Security
 ↓
Docker
 ↓
CI/CD
 ↓
Cloud
 ↓
Observability
 ↓
Analytics
 ↓
Billing
 ↓
Users
 ↓
Revenue
```

zincirini **tek başına yönetebilecek** durumda olmalısın.

Her konuda dünyanın en iyi uzmanı olmayacaksın.

Ama:

> **“Bunu nasıl yapacağımı bilmiyorum.”**

dediğinde araştırıp çözebileceksin.

Bence gerçek mühendislik özgüveni tam olarak buradan geliyor.

---

# 22. Kariyer tarafında da inanılmaz güçlü bir sonuç çıkar

Bir şirket seni mülakata çağırdığında artık:

> “React biliyorum.”

demek yerine:

> **“Multi-tenant, AI-native, production SaaS geliştirdim.”**

diyebilirsin.

Ve sorarlarsa:

### “Database?”

> PostgreSQL, indexing, query optimization, transactions, multi-tenancy.

### “Backend?”

> TypeScript/Fastify, API design, authentication, authorization, queues.

### “DevOps?”

> Docker, CI/CD, cloud deployment.

### “AI?”

> Multi-model gateway, RAG, agent runtime, tools, evals.

### “Production?”

> Logging, metrics, tracing, retries, rate limiting, monitoring.

### “Security?”

> RBAC, tenant isolation, secrets, prompt injection, tool permissions.

### “System design?”

> “İşte NEXUS'un architecture'ı.”

Ve GitHub'a yönlendirebilirsin.

**Bu, CV'deki 20 tane tutorial projesinden çok daha güçlü bir hikâye.**

---

# 23. Fakat en önemli hedefimiz “NEXUS yapmak” değil

Bunu özellikle ayırıyorum.

## NEXUS araç.

## Sen asıl ürünsün.

NEXUS sayesinde:

```
Software Engineering
       +
AI Engineering
       +
System Design
       +
Product
       +
Business
       +
Sales
       +
Founder Thinking
```

birleşecek.

12 ay sonra NEXUS başarısız olsa bile:

**sen kazanmış olacaksın.**

Çünkü elinde:

> ciddi production mühendisliği deneyimi

olacak.

Ama NEXUS başarılı olursa:

> **öğrenme projen şirketin olabilir.**

İşte flagship project'in gücü burada.

---

# 24. Sana tek cümlelik çalışma manifestosu

Bunu bir yere yaz:

> **“Tutorial tüketmeyeceğim; sistem inşa edeceğim. AI'dan yardım alacağım ama anlamadığım kodu sahiplenmeyeceğim. Her öğrendiğimi NEXUS'ta uygulayacağım, sistemi bilerek kıracağım, production'a çıkaracağım, ölçeceğim ve gerçek kullanıcılarla doğrulayacağım.”**

Ve yol haritasının omurgası:

```
        LEARN
          ↓
        BUILD
          ↓
        BREAK
          ↓
        DEBUG
          ↓
        TEST
          ↓
       DEPLOY
          ↓
       OBSERVE
          ↓
       MEASURE
          ↓
        SELL
          ↓
        LEARN
          ↺
```

**Bu döngüyü 12 ay boyunca gerçekten uygularsan, bence asıl dönüşüm “NEXUS'u yapmayı öğrenmek” değil; NEXUS'u yaparken kendi başına teknoloji şirketi kurabilecek bir mühendis haline gelmek olacak.**

Ve özellikle AI çağında bu yaklaşımın mantığı güçlü: AI kullanımı artık profesyonel geliştirmede norm haline geliyor, fakat doğruluk, güvenlik, privacy ve karmaşık görevlerde doğrulama hâlâ ciddi sorunlar. Dolayısıyla **AI kullanan ama AI çıktısının üzerinde mühendislik kontrolü kurabilen kişi** olmak çok daha değerli. [Stack Overflow Developer Survey](https://survey.stackoverflow.co/2025/ai?utm_source=chatgpt.com)

### Bundan sonraki en doğru aşama

Bu roadmap artık **“ne öğreneceğini”** belirliyor. Bir sonraki katmanda bunu daha da operasyonel hale getirmek gerekir:

**48 haftanın her birini tek tek açıp**, her hafta için:

- 📚 tam öğrenilecek konular
- 🎓 en iyi ücretsiz kaynaklar
- 📖 okunacak dokümantasyon
- 🧠 öğrenme hedefleri
- 💻 NEXUS'ta yazılacak kod
- 🏗️ mimari milestone
- 🧪 test görevi
- 🔥 bilerek kırılacak sistem
- 🤖 AI'ı nasıl kullanacağın
- 🧩 LeetCode patternleri
- 📝 haftalık sınav
- 🚪 haftayı geçme kriteri
- 📊 ölçülecek metrikler
- 💼 CV/GitHub çıktısı

şeklinde **48 haftalık gerçek bir müfredat** haline getirmek.

Bence artık tam olarak bunu yapmak gerekiyor; çünkü o noktada elinde bir “roadmap” değil, **uygulanabilir bir 1 yıllık Technical Founder eğitim programı** olur.
[[001-learn-logic]]