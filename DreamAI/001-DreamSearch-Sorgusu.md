> İnternetten arama yapan bir agent oluşturmak istiyorum. Bunun için google search api vb. internet araması yapmayı sağlayan hizmetler kullanmak istemiyorum. Bütün süreci kendim yapmak istiyorum. Bu sayede chatbotta bir şey arattığımda kendi agentlarım veya mcplerim bu aramayı en yüksek başarıyla nokta atışı cevabını bulabilir.

Evet. Hatta senin tarif ettiğin şey basitçe **“Google Search API'sini kendim yazayım”** değil; doğru tasarlanırsa kendi **Web Search Engine + Research Agent + MCP altyapını** oluşturabilirsin.

Ama burada çok önemli bir ayrım var:

> **İnternette arama yapmak** ile **interneti indekslemek** aynı problem değil.

Google/Bing'in yaptığı şeyin temelini kendin yapabilirsin. Fakat “bütün interneti Google kadar güncel ve kapsamlı şekilde taramak” milyarlarca URL, devasa bandwidth/storage ve crawler altyapısı gerektirir. Common Crawl'ın güncel ölçeği bile petabaytlarca veri ve ayda milyarlarca yeni sayfa seviyesinde. [Common Crawl](https://commoncrawl.org/overview?utm_source=chatgpt.com)

Senin için çok daha ilginç olan ise **küçük ama çok akıllı bir agentic search engine** yapmak.

---

# Ben olsam sistemi böyle kurardım

1

```
                    USER
                      │
                      ▼
             ┌─────────────────┐
             │   Chatbot / UI  │
             └────────┬────────┘
                      │
                      ▼
             ┌─────────────────┐
             │ SEARCH AGENT    │
             │ Query Planner   │
             └────────┬────────┘
                      │
          ┌───────────┼───────────┐
          ▼           ▼           ▼
      Query A      Query B      Query C
          │           │           │
          └───────────┼───────────┘
                      ▼
             ┌─────────────────┐
             │ URL Discovery   │
             └────────┬────────┘
                      ▼
             ┌─────────────────┐
             │ Web Crawler     │
             │ HTTP Fetcher    │
             └────────┬────────┘
                      ▼
             ┌─────────────────┐
             │ Content Parser  │
             │ HTML → Text     │
             └────────┬────────┘
                      ▼
             ┌─────────────────┐
             │ Deduplication   │
             └────────┬────────┘
                      ▼
          ┌───────────┴───────────┐
          ▼                       ▼
    BM25 / Keyword           Embeddings
          │                       │
          └───────────┬───────────┘
                      ▼
             ┌─────────────────┐
             │ Hybrid Retrieval│
             └────────┬────────┘
                      ▼
             ┌─────────────────┐
             │ Reranker        │
             └────────┬────────┘
                      ▼
             ┌─────────────────┐
             │ Evidence Agent  │
             │ Verify claims   │
             └────────┬────────┘
                      ▼
             ┌─────────────────┐
             │ Answer Generator│
             └────────┬────────┘
                      ▼
                    USER
```

Buradaki kritik nokta şu:

**LLM arama motoru değildir.**

LLM:

> “Ne aramalıyım?”

sorusunu çözmeli.

Search engine:

> “Nerede bulabilirim?”

sorusunu çözmeli.

Crawler:

> “Sayfanın içeriğini nasıl elde ederim?”

sorusunu çözmeli.

Reranker:

> “Hangisi gerçekten alakalı?”

sorusunu çözmeli.

Verifier:

> “Bulduğum bilgi gerçekten iddiamı destekliyor mu?”

sorusunu çözmeli.

---

# 1. İlk önce kendi Search Engine'ini yap

Mesela kullanıcı:

> "2026 yılında Türkiye'de yapay zeka girişimleri için verilen devlet destekleri nelerdir?"

dedi.

Agent bunu doğrudan internete göndermemeli.

Önce:

```
USER QUERY

        ↓

Query Understanding

        ↓

Intent:
"Türkiye + AI startups + government support"

        ↓

Query Expansion

Q1:
2026 Türkiye yapay zeka girişim devlet desteği

Q2:
2026 TÜBİTAK yapay zeka girişim desteği

Q3:
2026 KOSGEB yapay zeka girişim desteği

Q4:
site:tubitak.gov.tr yapay zeka destek 2026

Q5:
site:kosgeb.gov.tr yapay zeka girişim 2026
```

Bu noktada **LLM'nin çok ciddi faydası var.**

---

# 2. URL Discovery Engine

Sonra URL bulman gerekiyor.

Burada birkaç yöntem birleştirilebilir.

### A. Kendi crawler'ın

Başlangıç seed'leri:

```
https://www.tubitak.gov.tr
https://www.kosgeb.gov.tr
https://www.sanayi.gov.tr
...
```

Crawler:

```
GET page

     ↓

extract links

     ↓

normalize URLs

     ↓

queue

     ↓

crawl

     ↓

extract new links

     ↓

queue again
```

Böylece:

```
A
├── B
│   ├── D
│   └── E
└── C
    ├── F
    └── G
```

şeklinde interneti keşfetmeye başlarsın.

---

# 3. Ama sadece crawler yeterli değil

Burada çok önemli bir problem var.

Diyelim kullanıcı:

> "NVIDIA'nın 2026 Q2 gelirleri"

dedi.

Senin crawler'ın NVIDIA'nın sitesini henüz keşfetmemiş olabilir.

Bu yüzden **Web Discovery Layer** oluşturmalısın.

Ben bunu üç katman yapardım:

```
                 DISCOVERY
                    │
        ┌───────────┼───────────┐
        │           │           │
     Crawler    Existing     User
                 Corpus      URLs
        │           │           │
        └───────────┼───────────┘
                    │
                    ▼
               URL Frontier
```

Burada **Common Crawl** çok değerli.

Common Crawl açık şekilde kullanılabilen devasa bir web crawl corpus'u sağlıyor; WARC/WET/WAT verileri ve URL index'i mevcut. URL index'i Parquet formatında ve DuckDB, Spark, Pandas, Polars gibi araçlarla sorgulanabiliyor. [Common Crawl](https://commoncrawl.org/get-started?utm_source=chatgpt.com)

Yani:

> Google Search API kullanmıyorum.

ile

> Hazır web verisini hiç kullanmıyorum.

aynı şey değil.

İstersen tamamen kendi crawler'ınla başlayabilirsin.

---

# 4. Web Fetcher

URL buldun:

```
https://example.com/article
```

Şimdi:

```
response = HTTP_GET(url)
```

ile sayfayı çekiyorsun.

Ama burada işler zorlaşıyor.

Çünkü web:

```
<header>
<nav>
ads
cookie banner
sidebar

MAIN ARTICLE

footer
```

şeklinde.

Sen chatbot'a:

> “Cookie settings / navigation / reklam”

göndermek istemiyorsun.

İstediğin:

```
title
author
date
main content
headings
tables
links
metadata
```

Bu nedenle:

```
HTML
 ↓
DOM parser
 ↓
Boilerplate removal
 ↓
Main content extraction
 ↓
Clean document
```

pipeline'ı gerekiyor.

---

# 5. Sonra kendi index'ini oluştur

Burada sistem gerçek bir search engine'e dönüşüyor.

Her sayfa:

```
{
  "url": "...",
  "title": "...",
  "content": "...",
  "domain": "...",
  "published_at": "...",
  "crawled_at": "...",
  "language": "tr",
  "author": "...",
  "links": [],
  "hash": "...",
  "embedding": [...]
}
```

haline gelir.

Sonra index.

Ben başlangıçta **OpenSearch** kullanırdım.

Çünkü:

```
BM25
+
Vector Search
+
Hybrid Search
+
Reranking
```

kombinasyonunu doğrudan destekliyor.

OpenSearch'ün kendi dokümantasyonu da keyword/BM25 ile semantic/vector search'ü hybrid search ile birleştirmenin daha iyi relevance sağlayabildiğini belirtiyor. [OpenSearch Documentation](https://docs.opensearch.org/latest/vector-search/ai-search/hybrid-search/index/?utm_source=chatgpt.com)

---

# 6. Sadece Vector DB kullanma

Bu çok önemli.

Şöyle yapma:

```
query
 ↓
embedding
 ↓
vector search
 ↓
answer
```

Bu sistem genellikle düşündüğünden kötü olur.

Çünkü:

> "GPT-5.6 Luna"

gibi bir query'de exact lexical matching çok değerlidir.

BM25 burada güçlüdür. OpenSearch varsayılan keyword relevance mekanizması olarak BM25 kullanıyor. [OpenSearch Documentation](https://docs.opensearch.org/latest/search-plugins/keyword-search/?utm_source=chatgpt.com)

Dolayısıyla:

```
                 QUERY
                   │
        ┌──────────┴──────────┐
        ▼                     ▼
      BM25                 Vector
        │                     │
      Top 50                Top 50
        │                     │
        └──────────┬──────────┘
                   ▼
                RRF
                   ▼
              Top 30
                   ▼
               Reranker
                   ▼
                Top 10
```

çok daha iyi.

RRF özellikle farklı scoring sistemlerinin sonuçlarını birleştirmek için kullanışlı; OpenSearch bunu doğrudan destekliyor. [OpenSearch Documentation](https://docs.opensearch.org/latest/vector-search/ai-search/hybrid-search/rrf/?utm_source=chatgpt.com)

---

# 7. Asıl "deha" kısmı: Reranker

Bence senin projenin en önemli kısmı burası.

Kullanıcı:

> "2026'da Türkiye'deki yapay zeka startup teşvikleri"

dedi.

Search engine:

```
1. random-ai-blog.com
2. medium.com/article
3. github.com/...
4. kosgeb.gov.tr
5. tubitak.gov.tr
```

getirebilir.

Ama sen:

```
TÜBİTAK
KOSGEB
Sanayi Bakanlığı
Resmi Gazete
```

gibi kaynakları yukarı taşımak istiyorsun.

Dolayısıyla ranking modeline:

```
semantic relevance
+
keyword relevance
+
authority
+
freshness
+
source quality
+
query intent
+
domain authority
+
citation density
+
content quality
```

gibi sinyaller verebilirsin.

Örneğin:

```
FINAL_SCORE =

0.30 semantic relevance
+
0.20 BM25
+
0.15 source authority
+
0.10 freshness
+
0.10 query intent match
+
0.05 content quality
+
0.05 citation/reference quality
+
0.05 domain reputation
```

İlk versiyonda elle ağırlıklandırırsın.

Daha sonra **learning-to-rank** yaparsın.

---

# 8. Sonra Research Agent

İşte burada klasik search engine'den ayrılıyorsun.

Örneğin:

> "OpenAI'nin 2026'da çıkardığı modelleri ve fiyatlarını karşılaştır."

Agent:

```
                    QUERY
                      │
                      ▼
                 PLAN RESEARCH
                      │
        ┌─────────────┼─────────────┐
        ▼             ▼             ▼
     Models        Pricing        Dates
        │             │             │
        ▼             ▼             ▼
     Search         Search         Search
        │             │             │
        └─────────────┼─────────────┘
                      ▼
                  Documents
                      │
                      ▼
                   Verify
                      │
                      ▼
                  Evidence
                      │
                      ▼
                   Answer
```

Bu çok daha güçlü.

---

# 9. "Search until satisfied" mekanizması

Bence senin sisteminin en güçlü özelliği bu olmalı.

Agent ilk aramadan sonra:

```
confidence = 0.62
```

derse:

> Henüz yeterli kanıt yok.

ve tekrar arar.

```
Search
 ↓
Retrieve
 ↓
Read
 ↓
Extract facts
 ↓
Check missing facts
 ↓
Search again
 ↓
Cross-check
 ↓
Confidence
 ↓
Answer
```

Örneğin:

```
Required facts:

[x] revenue
[x] growth
[ ] Q2 margin
[ ] source
[x] date
```

Eksik:

```
Q2 margin
```

Agent yalnızca bunu arar.

Bu, klasik:

> "LLM'ye Google sonuçlarını ver → cevap üret"

yaklaşımından çok daha iyi.

---

# 10. Evidence Graph yap

Ben olsam daha da ileri götürürdüm.

Agent'ın kafasında:

```
CLAIM

"Company X revenue was $10B"

        │
        ├── Source A
        │     └── official filing
        │
        ├── Source B
        │     └── Reuters
        │
        └── Source C
              └── company report
```

tutardım.

Sonra:

```
Claim
 ↓
Evidence
 ↓
Source
 ↓
Timestamp
 ↓
Confidence
```

saklanır.

Böylece chatbot:

> "Bunu nereden çıkardın?"

sorusuna gerçekten cevap verebilir.

---

# 11. MCP burada nereye giriyor?

MCP'yi search engine'in kendisi olarak düşünme.

MCP:

> **Agent ile senin search altyapın arasındaki standart interface**

olabilir.

Örneğin:

```
your-search-mcp

tools:

search_web()
search_news()
search_domain()
fetch_page()
crawl_url()
find_similar()
verify_claim()
research()
```

Agent:

```
{
  "tool": "search_web",
  "query": "2026 AI startup funding Turkey"
}
```

der.

Senin MCP server'ın:

```
Agent
  ↓
MCP
  ↓
Search Engine
  ↓
Crawler
  ↓
Indexer
  ↓
Reranker
  ↓
Evidence
```

şeklinde çalışır.

---

# 12. Hatta birden fazla MCP yapabilirsin

Örneğin:

```
                 MASTER AGENT
                      │
       ┌──────────────┼──────────────┐
       ▼              ▼              ▼
 Web Search MCP   Academic MCP   Company MCP
       │              │              │
       ▼              ▼              ▼
   Your Web       Papers DB       Company DB
    Index
```

Sonra:

```
Research Agent
```

bunların hepsini kullanır.

Örneğin:

> "Tesla'nın yeni bataryasının teknik avantajlarını araştır."

şöyle:

```
Web MCP
     ↓
Tesla announcements

Academic MCP
     ↓
battery papers

Company MCP
     ↓
Tesla financial / corporate docs

Patent MCP
     ↓
patents

       ↓

Evidence Fusion
       ↓

Answer
```

Bu gerçekten güçlü bir architecture olur.

---

# 13. Fakat bir problem var: "bütün internet"

Burada sana biraz acı gerçek söyleyeyim.

Google'ın seviyesinde:

```
crawl entire web
+
continuously recrawl
+
billions of URLs
+
spam detection
+
canonicalization
+
JS rendering
+
distributed crawling
+
ranking
+
freshness
```

yapmaya çalışırsan proje **çok büyük** hale gelir.

Common Crawl'ın güncel corpus'u bile petabayt ölçeğinde; ayrıca aylık milyarlarca yeni sayfa ekleniyor. [Common Crawl](https://commoncrawl.org/overview?utm_source=chatgpt.com)

Dolayısıyla:

### ❌ İlk hedef

> "Google'ı yeniden yapacağım."

### ✅ İlk hedef

> **"Sorulan soruya Google'dan daha iyi araştırma yapan uzman bir agent yapacağım."**

Bu çok daha mantıklı.

---

# 14. Sana önereceğim mimari

Senin mevcut teknik geçmişini de düşünürsek şöyle bir sistem oldukça uygun:

```
                    ┌──────────────┐
                    │   Next.js    │
                    │    Chat UI   │
                    └──────┬───────┘
                           │
                           ▼
                    ┌──────────────┐
                    │ Research API │
                    │   FastAPI    │
                    └──────┬───────┘
                           │
                           ▼
                 ┌───────────────────┐
                 │   Agent Runtime   │
                 └─────────┬─────────┘
                           │
          ┌────────────────┼────────────────┐
          ▼                ▼                ▼
    Query Planner     Search Agent     Verification
          │                │                │
          └────────────────┼────────────────┘
                           ▼
                    ┌──────────────┐
                    │ Search Core  │
                    └──────┬───────┘
                           │
              ┌────────────┼────────────┐
              ▼            ▼            ▼
            BM25        Vector       Metadata
              │            │            │
              └────────────┼────────────┘
                           ▼
                       Reranker
                           │
                           ▼
                    Evidence Store
                           │
                           ▼
                      LLM Answer
```

Altta:

```
Crawler
Fetcher
Parser
Indexer
Scheduler
URL Frontier
Deduplication
```

çalışır.

---

# 15. Teknoloji stack

Ben başlangıç için:

### Frontend

```
Next.js
TypeScript
Tailwind
```

### Agent

```
Python
FastAPI
Pydantic
```

### Crawling

```
httpx
aiohttp
Playwright
```

Playwright'ı **her sayfada değil**, JavaScript gerektiren sayfalarda fallback olarak kullanmak daha mantıklı.

### Parsing

```
BeautifulSoup
trafilatura
readability
```

### Search

```
OpenSearch
```

### Database

```
PostgreSQL
```

### Queue

```
Redis
```

veya ölçek büyüyünce Kafka.

### Object storage

```
S3 / Cloudflare R2
```

### Embeddings

İlk aşamada lokal embedding modeli.

### Reranker

Lokal cross-encoder / modern reranking modeli.

---

# 16. Crawl pipeline

Ben bunu şöyle kurardım:

```
URL
 │
 ▼
Robots Check
 │
 ▼
URL Normalization
 │
 ▼
Duplicate Check
 │
 ▼
Priority Queue
 │
 ▼
HTTP Fetch
 │
 ├── 200
 │
 ├── redirect
 │
 ├── 403
 │
 ├── 404
 │
 └── timeout
 │
 ▼
HTML
 │
 ▼
Content Extraction
 │
 ▼
Language Detection
 │
 ▼
Canonical URL
 │
 ▼
Deduplication
 │
 ▼
Chunking
 │
 ├── BM25 Index
 │
 └── Vector Index
```

---

# 17. Crawler'ın en önemli parçası: URL Frontier

Burası Google'ın yaptığı işin önemli parçalarından biri.

Basit:

```
queue.append(url)
```

değil.

Şöyle:

```
Priority

10 → official government page
9  → major news
8  → high-authority company
7  → academic
...
1  → random blog
```

ve:

```
priority =
authority
+
query relevance
+
freshness
+
historical quality
+
link importance
```

olabilir.

Böylece agent:

> "Bana internetin tamamını getir."

demek yerine:

> **"Bu soruya cevap verebilme ihtimali en yüksek sayfaları önce keşfet."**

der.

Bu **agentic crawling**.

---

# 18. Daha da güzel bir özellik: Adaptive Crawling

Mesela agent şu anda:

```
Query:
"2026 Türkiye AI teşvikleri"
```

araştırıyor.

Crawler:

```
TÜBİTAK
 ↓
AI support page
 ↓
2026 call
 ↓
PDF
 ↓
related regulation
```

keşfeder.

Sonra agent:

> Bu domain/subgraph yüksek değer taşıyor.

der.

Ve:

```
tubitak.gov.tr
```

içindeki ilgili linkleri agresif şekilde crawl eder.

Başka siteleri düşük önceliğe atar.

Bu sayede **arama motorun soruya göre geçici olarak kendini şekillendirir.**

Bence projenin en ilginç taraflarından biri bu.

---

# 19. Ve sonunda "Deep Research Mode"

Chatbot'ta iki mod koyabilirsin:

### ⚡ Fast Search

```
Query
 ↓
Search
 ↓
Rerank
 ↓
Answer
```

2–10 saniye.

### 🧠 Deep Research

```
Understand
 ↓
Plan
 ↓
Search
 ↓
Read
 ↓
Extract
 ↓
Cross-check
 ↓
Search gaps
 ↓
Verify
 ↓
Synthesize
```

30 saniye → birkaç dakika.

Kullanıcı:

> "Deep Research"

dediğinde agent gerçekten araştırma yapar.

---

# 20. Ben olsam projeyi 5 aşamada geliştirirdim

### Phase 1 — Mini Search Engine

```
Crawler
+
Parser
+
OpenSearch
+
BM25
```

Amaç:

> 100K–1M sayfa üzerinde düzgün keyword search.

---

### Phase 2 — Semantic Search

```
BM25
+
Embeddings
+
Vector Search
+
RRF
```

Amaç:

> keyword + semantic hybrid retrieval.

---

### Phase 3 — AI Search Agent

```
Query Planner
+
Query Expansion
+
Search
+
Reranking
+
Answer
```

Amaç:

> Kullanıcının sorusunu anlayıp kendi arama stratejisini oluşturması.

---

### Phase 4 — Research Agent

```
Multi-query
+
Multi-hop search
+
Evidence extraction
+
Claim verification
+
Citation generation
+
Confidence
```

Amaç:

> "Araştır ve bana kanıtlarla cevap ver."

---

### Phase 5 — Adaptive Web Intelligence

Burada işler gerçekten ilginçleşiyor:

```
Agent
 ↓
learns which domains are useful
 ↓
learns which pages are authoritative
 ↓
learns which queries retrieve good evidence
 ↓
learns ranking
 ↓
learns when to stop searching
```

ve sonunda:

> **Kendi kendini geliştiren bir web research engine**

oluşturursun.

---

## Ve sana özellikle bir şey önereceğim

Bu projeyi **"Google alternatifi"** olarak düşünme.

Daha iyi bir hedef var:

> ### **"LLM'ler için yüksek doğruluklu Web Research Infrastructure."**

Yani sen Google'a rakip bir search box yapmak yerine:

```
                 ANY LLM
                    │
                    ▼
             YOUR RESEARCH API
                    │
       ┌────────────┼────────────┐
       ▼            ▼            ▼
    Search        Crawl       Verify
       │            │            │
       └────────────┼────────────┘
                    ▼
             Evidence Graph
                    │
                    ▼
              Grounded Answer
```

yaparsın.

Sonra bunu **MCP olarak expose** edersin.

Böylece ChatGPT benzeri herhangi bir agent:

```
search_web()
research()
crawl()
read_page()
find_evidence()
verify_claim()
```

araçlarını kullanabilir.

**Bu, senin daha önce konuştuğumuz AI Agent / MCP / LLM öğrenme hedeflerinle de çok güzel birleşen gerçek bir mühendislik projesi olur.**

İstersen bir sonraki adımda bunu **gerçekten inşa edilecek seviyeye** indirebiliriz: `monorepo → crawler → URL frontier → parser → OpenSearch → hybrid retrieval → reranker → research agent → MCP` şeklinde, **ilk çalışan MVP'den production mimarisine kadar A'dan Z'ye teknik roadmap** çıkarabiliriz.