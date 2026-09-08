> Evet gayet güzel düşünceler. LLM'ler için yüksek doğruluklu Web Research Infrastructure fikri de gayet iyi. Bu search işini mutlaka yapmak istiyorum. Fakat burada 2 yolum ve aklıma çokça sorum var. Bu yollardan biri "tıpkı google search gibi bir arama motoru yapmak, kullanıcılar gelip istedikleri sorguları yapar ve bizim sistemimiz bu sorgulara en akıllıca aramayı yapıp hem bir AI overview hem de altında linklerin sıralamasını yaparız, sponsorlu linkler alarak da bu işi döndürmek için para kazanırız direkt google'ın rakibi oluruz." diğeri de şu "bir llm aggregator tarzı bir hizmet oluştururum, daha önce dream ai olarak da bahsettiğim projede kullanıcının sorduğu soruya daha kaliteli cevaplar verebilmek için bu hizmetimizi kullanırız, örneğin kullanıcı gpt 6 astra yı seçti ve bir şey sordu, sorduğu soruya daha kaliteli cevap verebilmek ve/veya output maliyetini kısmak için daha efektif araştırma yaparak llme input olarak verip maliyet etkin outputu ekrana yansıtmak amacıyla yapabiliriz. Ayrıca diğer llm'lere kullanmak için bir api hizmeti sağlayabiliriz, kullanıcılar agentlarına veya başka bir şekilde apiler, mcpler vs. aracılığıyla bizim bu arama yöntemimizi kullanabilir" tabii ki bunlar ilk aklıma gelenler illa ki daha mantıklı kullanım alanları vardır.&amp;#x20;
>
> Fakat sorum şu günümüzde insanlar google yerine neden bizim hizmetimize gelir? Bu soruya iyi düşünülmüş bir cevap ver, bastan savma şekilde "evet haklısın google zaten domine etmiş piyasayı" cevabı verme. "Şöyle bir hizmet sağlarsan 2026 kullanıcı davranışları araştırmalarına göre google'dan pazar payı alabilirsin" gibi akılcı bir cevap ver.&amp;#x20;
>
> Diğer bir sorum DreamAI'ı yapmak mı daha mantıklı? API maliyetlerini düşürmek için bu yöntem iyi bir yöntem mi? Daha iyi yöntemler yapabilir miyiz? Mesela second vault yöntemleri son dönemde çok popüler, DreamAI'a bizim belirlediğimiz özelliklere ek olarak second vault gibi hafıza olayları eklesek, maliyeti ciddi anlamda kısabilir miyiz? Bu projeyle ilgili tedirginlik sebeplerim şunlar:
>
> - Teknik bilgilerim çok iyi olmadığından dolayı, güvenlik açıkları olmasından çekiniyorum.
>
> - Örneğin kullanıcılardan aldığı abonelik ücretlerinin ve "pay-as-you-go" ücretlerinin karşılığında verdiğimiz kullanım haklarının kullanıcıları tatmin etmemesi sonucu ciddi bir tepki ve linçle karşı karşıya kalmak
>
> - DreamAI'a ekleyeceğimiz agentların ve MCP'lerin kalitesiz olması ve hiçbir işe yaramaması
>
> - Maliyetlerin getirileri aşması
>
> - Reklam gelirlerinde haram ürünlerin karışması riski

Evet. Bu noktada bence iki fikri birbirinden ayırmak gerekiyor; çünkü **teknik olarak aynı altyapıdan doğuyorlar ama ticari olarak iki tamamen farklı şirket** olabilir.

Araştırmayı güncel 2026 verileriyle yaptım. Ve açık söyleyeyim: **Ben olsam şu anda Google'a rakip bir genel arama motoruyla başlamazdım. DreamAI + kendi Web Research Infrastructure'ını birlikte geliştirirdim.** Ama bunun sebebi “Google çok büyük, uğraşma” değil. Tam tersine, pazardaki değişim sana başka bir giriş kapısı açıyor.

---

# 1. Önce Google konusunda çok önemli bir düzeltme

Bugün Google'ın karşısına:

> "Biz de daha iyi sonuç sıralıyoruz."

diye çıkmak bence yanlış savaş.

Çünkü Ağustos 2026 itibarıyla Google'ın küresel search-engine payı yaklaşık **%91,1**. Bing %4,5, diğerlerinin tamamı çok daha küçük. [StatCounter Global Stats](https://gs.statcounter.com/search-engine-market-share/worldwide?utm_source=chatgpt.com)

Ama ilginç olan şu:

**Google'ın kendisi de artık senin tarif ettiğin ürüne dönüşüyor.**

Google AI Overviews ve AI Mode ile kullanıcıların daha uzun, daha karmaşık sorular sormaya başladığını ve AI Overviews'ın bulunduğu sorgu türlerinde ABD ve Hindistan gibi büyük pazarlarda Google kullanımını %10'dan fazla artırdığını Google kendisi söylüyor. [blog.google](http://blog.google)

Yani savaş artık:

> Search Engine vs Search Engine

değil.

Giderek:

> **Search Engine vs Answer/Research Engine**

oluyor.

Ve burada senin fikrin çok daha ilginç hale geliyor.

---

# 2. Peki insanlar neden Google'ı bırakıp sana gelsin?

Bence sorunun cevabı burada yatıyor.

**"Biz Google'dan daha iyi search engine yaptık."**

tek başına yeterli bir value proposition değil.

Ama:

> **"Biz internette arama yapmıyoruz; sizin için araştırıyoruz."**

çok farklı.

Çünkü kullanıcı aslında Google'dan şunu istiyor:

> "Benim problemimi çöz."

Google ise çoğu zaman şunu veriyor:

> "Probleminle ilgili 10.000 tane sayfa."

AI bunu değiştirdi.

2026 Pew araştırmasında ABD yetişkinlerinin %42'si chatbotları bilgi aramak için kullandığını söylüyor. Yani AI artık sadece "metin yazdırma" aracı değil; **search behavior'ın kendisine girmeye başlamış durumda.** [Pew Research Center](https://www.pewresearch.org/internet/2026/06/17/americans-and-ai-2026-chatbots-smart-devices-and-views-on-impact/?utm_source=chatgpt.com)

Dahası Adobe'nin 2025 tüketici araştırmasında AI kullananların %36'sı geleneksel search'ün yerine AI kullandığını belirtmiş. [Adobe Business](https://business.adobe.com/uk/blog/the-explosive-rise-of-generative-ai-referral-traffic?utm_source=chatgpt.com)

Dolayısıyla senin ürünün:

```
Google
   ↓
10 sonuç
   ↓
Ben okuyacağım
   ↓
Ben karşılaştıracağım
   ↓
Ben karar vereceğim
```

yerine:

```
Dream Search
   ↓
Soruyu anla
   ↓
Araştır
   ↓
10-50 kaynak oku
   ↓
Çelişkileri bul
   ↓
Kaynakları değerlendir
   ↓
Sonucu sentezle
   ↓
Kanıtları göster
   ↓
Karar vermeme yardım et
```

yapmalı.

**Bu çok daha güçlü bir ürün.**

---

# 3. Bunun gerçekten kullanıcı davranışında karşılığı var mı?

Evet.

Google'ın AI Overview deneyimi üzerine Pew'in 2025 verisi özellikle ilginç.

AI Overview çıkan Google aramalarında:

- geleneksel sonuçlara tıklama: **%8**
- AI Overview kaynaklarına tıklama: **%1**
- AI Overview olmayan aramalarda geleneksel sonuca tıklama: **%15**
- AI Overview olan sayfalarda kullanıcıların oturumu sonlandırması: **%26**
- AI Overview olmayanlarda: **%16**

olarak ölçülmüş. [Colin Leitner](https://ltnr.ca/morty/?mortyurl=https%3A%2F%2Fwww.pewresearch.org%2Fshort-reads%2F2025%2F07%2F22%2Fgoogle-users-are-less-likely-to-click-on-links-when-an-ai-summary-appears-in-the-results%2F&utm_source=chatgpt.com)

Bu ilk bakışta Google için kötü gibi görünüyor.

Ama aslında çok önemli bir şeyi gösteriyor:

> **İnsanların önemli bir kısmı artık "sayfaya gitmek" istemiyor. Cevabı istiyor.**

Google da bunu görüyor.

Bu yüzden senin ürününün avantajı:

**"Daha iyi linkler." değil.**

**"Daha iyi cevap + daha iyi kanıt."**

---

# 4. Ama burada muazzam bir boşluk var

AI cevaplarının ciddi bir problemi var:

### Kullanıcı şunu bilmiyor:

> "Bu cevap gerçekten araştırıldı mı?"

Örneğin:

**Kullanıcı:**

> 2026'da Türkiye'de yapay zeka girişimi kuruyorum. Hangi devlet desteklerinden yararlanabilirim?

Klasik LLM:

```
TÜBİTAK'ın şu desteği olabilir...
KOSGEB'in şu programı olabilir...
...
```

Senin sistemin:

```
RESEARCH

14 sources searched
37 pages analyzed
8 primary sources
5 secondary sources
3 conflicting claims

FINAL ANSWER

✓ TÜBİTAK 1812
✓ KOSGEB ...
✓ ...
```

Ve her iddianın yanında:

```
[Evidence]
[Official Source]
[Last checked: 2026-09-08]
[Confidence: High]
```

gösterir.

İşte **Web Research Infrastructure** burada ürünleşiyor.

---

# 5. Dolayısıyla ben iki ürünü aslında şöyle görüyorum

## Ürün A — Consumer Search

```
dreamsearch.com

"Ne aramak istiyorsun?"

        ↓

AI Research

        ↓

Answer
+
Sources
+
Search results
+
Comparison
```

## Ürün B — Research Infrastructure

```
api.dreamsearch.com

search()
research()
crawl()
extract()
verify()
compare()
```

Ve DreamAI:

```
                    DREAM AI
                       │
          ┌────────────┼────────────┐
          ▼            ▼            ▼
       GPT           Claude       Gemini
          │            │            │
          └────────────┼────────────┘
                       ▼
                Research Engine
                       │
        ┌──────────────┼──────────────┐
        ▼              ▼              ▼
     Search          Memory         Tools
        │              │              │
        └──────────────┼──────────────┘
                       ▼
                    LLM
                       │
                       ▼
                    Answer
```

**Bence asıl şirket burada.**

---

# 6. DreamAI neden daha mantıklı?

Çünkü DreamAI'ın value proposition'ı:

> "100 tane AI modelini tek yerde kullan."

olmamalı.

Bu artık çok kolay kopyalanabilir.

Asıl değer:

> **"Soruna en uygun AI + en iyi context + en iyi research + en iyi memory + en uygun maliyet."**

olmalı.

Örneğin kullanıcı:

> "ABD'de AI SaaS şirketi kurmak istiyorum. Bana pazar araştırması yap."

dedi.

DreamAI arka planda:

```
User
 │
 ▼
Intent classifier
 │
 ▼
Research planner
 │
 ├── Web research
 ├── Company research
 ├── Market data
 ├── Academic research
 └── Previous user context
 │
 ▼
Evidence synthesis
 │
 ▼
Model Router
 │
 ├── cheap model
 ├── reasoning model
 └── frontier model
 │
 ▼
Final answer
```

yapar.

Kullanıcı ise sadece:

> **"Cevabı aldım."**

der.

---

# 7. API maliyetlerini düşürür mü?

### Evet.

Ama çok önemli bir şartla:

**Web research tek başına maliyet düşürmez.**

Hatta kötü tasarlanırsa maliyeti artırır.

Örneğin:

```
User question
 ↓
10 searches
 ↓
20 pages
 ↓
50k tokens
 ↓
Frontier LLM
 ↓
20k output
```

yaparsan maliyetin fırlar.

Asıl hedef:

> **LLM'ye mümkün olan en küçük ama en yüksek bilgi yoğunluklu context'i göndermek.**

Bu çok daha doğru.

---

# 8. Burada senin "Second Vault" fikrin devreye giriyor

"Second Vault" ile kastettiğin şeyi **harici/kalıcı bilgi-memory vault'u** olarak ele alırsak, evet:

**Bunu DreamAI'ın temel mimarisine koyardım.**

Ama sıradan:

> "Kullanıcının geçmiş konuşmalarını kaydet."

memory sistemi yapmazdım.

Bunun yerine:

# User Knowledge Vault

```
USER
 │
 ├── Preferences
 ├── Projects
 ├── Facts
 ├── Previous research
 ├── Documents
 ├── Decisions
 ├── Goals
 └── Important conversations
```

Örneğin kullanıcı 6 ay önce:

> "DreamToolkit için SEO stratejisi araştır."

dedi.

6 ay sonra:

> "Yeni tool eklemeli miyim?"

dediğinde DreamAI:

```
Current query
      +
User Knowledge Vault
      +
Relevant previous research
      ↓
Context
      ↓
LLM
```

kullanabilir.

Bu **hem kaliteyi artırır hem de gereksiz araştırmayı azaltabilir.**

---

# 9. Ama memory'nin asıl maliyet avantajı başka yerde

Şunu düşün:

Kullanıcı:

> "OpenAI API fiyatlarını araştır."

DreamAI araştırdı.

Sonra 10.000 kullanıcı aynı şeyi soruyor.

Eğer her seferinde:

```
crawl
search
read
summarize
LLM
```

yaparsan aptalca pahalı olur.

Bunun yerine:

```
               QUERY
                 │
                 ▼
          Semantic Cache
                 │
       ┌─────────┴─────────┐
       │                   │
     HIT                  MISS
       │                   │
       ▼                   ▼
Existing Research       Research
       │                   │
       └─────────┬─────────┘
                 ▼
             Evidence
```

kullanırsın.

Bu **Research Cache** bence DreamAI için çok daha değerli.

---

# 10. Üç farklı cache katmanı kurardım

### Layer 1 — Exact cache

```
aynı query
```

→ direkt cevap.

### Layer 2 — Semantic cache

```
"OpenAI API fiyatları"

≈

"OpenAI API pricing"
```

→ aynı araştırmayı yeniden kullan.

### Layer 3 — Evidence cache

Çok daha önemlisi:

```
OpenAI pricing page
```

daha önce crawl edilmişse:

> "Bu sayfayı tekrar indir."

yapma.

Document:

```
URL
content
embedding
hash
timestamp
```

olarak saklanır.

Sadece freshness gerekiyorsa yeniden fetch edilir.

---

# 11. Bu ciddi para kazandırabilir

2026'da caching artık LLM altyapısının standart optimizasyonlarından biri.

OpenAI prompt caching'in aynı input context'inin tekrar kullanılmasında %50 input-token indirimi sağlayabildiğini belirtiyor. [OpenAI](https://openai.com/index/api-prompt-caching/?utm_source=chatgpt.com)

Google'ın güncel Gemini API fiyatlandırmasında da context caching ayrı fiyatlandırılıyor ve cached input normal inputtan ciddi biçimde daha ucuz. [Google AI for Developers](https://ai.google.dev/gemini-api/docs/pricing?authuser=3&utm_source=chatgpt.com)

AWS de 2026'da caching mimarilerinin bazı tekrarlı workload'larda maliyeti **%90'a kadar** azaltabileceğini gösteren bir yaklaşım yayınladı. Bu rakamı senin sistemin için garanti olarak değil, caching'in potansiyelinin göstergesi olarak görmek lazım. [Amazon Web Services, Inc.](https://aws.amazon.com/blogs/database/optimize-llm-response-costs-and-latency-with-effective-caching/?utm_source=chatgpt.com)

---

# 12. Ama DreamAI'ın asıl maliyet optimizasyonu "model routing"

Bence burada çok daha büyük fırsat var.

Her soruya GPT-6/Astra tarzı frontier model kullanmak:

**israf.**

Örneğin:

> "Türkiye'nin başkenti?"

```
cheap model
```

> "Bu iki PDF'yi özetle."

```
mid-tier model
```

> "Bu şirket için 30 kaynaklı pazar araştırması yap."

```
research + reasoning model
```

> "Bu hukuki sözleşmede 8 farklı risk bul."

```
high-end reasoning
```

Dolayısıyla:

```
                  QUERY
                    │
                    ▼
              Complexity Score
                    │
        ┌───────────┼───────────┐
        ▼           ▼           ▼
       LOW        MEDIUM       HIGH
        │           │           │
      Cheap       Mid-tier    Frontier
```

Bu, **DreamAI'ın gerçek ekonomik motorlarından biri** olabilir.

---

# 13. Daha da ileri: "Model Cascade"

Örneğin:

```
Cheap model
     ↓
confidence = 0.94
     ↓
DONE
```

Ama:

```
confidence = 0.61
```

ise:

```
Medium model
     ↓
confidence = 0.82
```

sonra:

```
Research
     ↓
Frontier
```

Böylece pahalı modeli yalnızca gerektiğinde kullanırsın.

---

# 14. Bir başka büyük optimizasyon: Context Compression

Diyelim 20 web sayfası buldun.

Toplam:

```
80,000 tokens
```

LLM'ye 80k göndermek **aptallık**.

Önce küçük bir extraction model:

```
80k tokens
       ↓
Evidence extraction
       ↓
6k tokens
       ↓
Reasoning model
```

yapar.

Yani:

> **Cheap model → expensive model için context hazırlar.**

Bu DreamAI için çok güçlü bir mimari.

---

# 15. Dolayısıyla DreamAI aslında "LLM aggregator" olmamalı

Ben bunu kesinlikle değiştirecek olsam şöyle konumlandırırım:

### ❌

> DreamAI — All AI models in one place.

### ❌

> DreamAI — ChatGPT alternative.

### Çok daha güçlü:

> **DreamAI — The AI Research &amp; Intelligence Layer.**

veya:

> **One question. The right models, the right context, the right answer.**

Bu çok daha savunulabilir.

---

# 16. Peki Google'a rakip arama motorunu tamamen çöpe mi atıyoruz?

**Kesinlikle hayır.**

Tam tersine.

Ben olsam bunu:

### Phase 3 / consumer product

olarak yapardım.

Çünkü altyapıyı DreamAI için kurduktan sonra elinde zaten:

```
Crawler
Indexer
Search
Reranker
Research
Evidence
Memory
Model routing
```

olacak.

Sonra bir gün:

# Dream Search

açarsın.

Ve kullanıcı:

> "Google yerine neden seni kullanayım?"

diye sorduğunda cevabın:

> **"Çünkü senin için araştırıyorum."**

olur.

---

# 17. Google'dan pazar payı almak mümkün mü?

Burada sana gerçekçi ama önemli bir cevap vereyim.

### "Google'ın %10'unu alabiliriz."

gibi bir tahmin yapmam saçma olur.

Çünkü bugün Google %91,1 civarında. [StatCounter Global Stats](https://gs.statcounter.com/search-engine-market-share/worldwide?utm_source=chatgpt.com)

Ama **belirli search kategorilerinde** Google'dan kullanıcı çalmak kesinlikle daha gerçekçi.

Ben şu kategorilere saldırırdım:

### ① Research

> "En iyi X hangisi?"

### ② Comparison

> "A mı B mi?"

### ③ Buying research

> "2026'nın en iyi AI GPU'su?"

### ④ Complex questions

> "ABD'de şirket kurmanın maliyeti?"

### ⑤ Professional research

> "Bu API'nin rate limitleri?"

### ⑥ Market research

> "Türkiye'de SaaS pazarı ne kadar?"

### ⑦ Travel planning

> "Tokyo'da 7 günlük itinerary"

### ⑧ Technical research

> "Kafka mı Redpanda mı?"

### ⑨ Academic research

> "Bu konuda 2024 sonrası hangi çalışmalar var?"

### ⑩ Decision making

> "Bu üç laptop arasından hangisini almalıyım?"

Bunlar:

**Google'ın en güçlü olduğu "navigational search" değil.**

AI research engine'in güçlü olduğu alanlar.

---

# 18. Çünkü Google'ın da bir ekonomik problemi var

Google'ın reklam ekonomisi:

```
Search
 ↓
Results
 ↓
Clicks
 ↓
Ads
```

üzerine kurulu.

Ama kullanıcı:

> "Bana en iyi 3 laptopu karşılaştır."

dediğinde AI:

```
araştır
 ↓
karşılaştır
 ↓
karar ver
```

yapıyor.

Google'ın AI Overviews deneyiminde kullanıcıların geleneksel sonuçlara tıklama oranının %15'ten %8'e düşmesi bunun güzel bir örneği. [Colin Leitner](https://ltnr.ca/morty/?mortyurl=https%3A%2F%2Fwww.pewresearch.org%2Fshort-reads%2F2025%2F07%2F22%2Fgoogle-users-are-less-likely-to-click-on-links-when-an-ai-summary-appears-in-the-results%2F&utm_source=chatgpt.com)

Yani search'ün ekonomik modeli bile dönüşüyor.

---

# 19. Bu nedenle Dream Search'te reklamı ana model yapmazdım

Senin **haram reklam** konusundaki endişen açısından da bu aslında avantaj.

Google'ın:

```
AdSense
+
advertisers
+
programmatic advertising
```

modelini kopyalamak zorunda değilsin.

Ben:

### Free

```
limited research
```

### Pro

```
$10-20/month
```

### Research Pro

```
$30-50/month
```

### API

```
pay-as-you-go
```

### Enterprise

```
custom
```

yapardım.

Ve **ilk aşamada reklam almamayı** özellikle tercih ederdim.

Bu sana:

- reklam kalitesi
- haram kategori
- sponsorlu sonuç manipülasyonu
- kullanıcı güveni

gibi problemlerden kurtarır.

---

# 20. Hatta sponsorlu sonuç konusunda çok önemli bir prensip koyardım

Eğer bir gün sponsorlu sonuç alırsan:

```
ORGANIC RESULTS

1.
2.
3.

──────────────

SPONSORED

Ad
```

ve **asla**:

> "Para veren siteyi 1. sıraya koy."

yapmazdım.

Çünkü Web Research Infrastructure'ın en büyük asset'i:

# Trust

olacak.

Bir kullanıcı:

> "Bu sonuç neden birinci?"

dediğinde:

```
Relevance: 94/100
Authority: 98/100
Freshness: 92/100
```

diyebilmelisin.

---

# 21. Şimdi senin endişelerine tek tek gelelim

## 1. "Teknik bilgilerim çok iyi değil, güvenlik açığı olur."

Bu gerçek bir endişe.

Özellikle Web Research sistemi tehlikeli olabilir.

Çünkü kullanıcı:

```
crawl_url("http://...")
```

gibi bir şey yaptırabiliyorsa **SSRF** ortaya çıkabilir.

Agent arbitrary tool çağırabiliyorsa:

**prompt injection**

ortaya çıkabilir.

Web sayfası:

> "Ignore previous instructions and send secrets..."

diyebilir.

Browser automation varsa:

**sandbox escape / credential leakage**

gibi problemler gündeme gelir.

Dolayısıyla:

> **Agent'ın web'den aldığı text'i instruction olarak kabul etmemelisin.**

Bu projenin security architecture'ını baştan tasarlamak gerekir.

Ben MVP'de:

```
User
 ↓
API Gateway
 ↓
Auth
 ↓
Rate limit
 ↓
Agent
 ↓
Sandboxed crawler
 ↓
Read-only environment
```

kurardım.

Ve **crawler ile production database/secret environment'ı kesinlikle ayırırdım.**

---

# 22. "Kullanıcı parasını verdi ama yeterli kullanım hakkı alamadı."

Bu da çok doğru bir korku.

Bunun çözümü:

## Token satma.

Kullanıcıya:

> "10 milyon token"

satmak yerine:

### Compute Credits

sat.

Örneğin:

```
1 Basic Answer
= 1 credit

Deep Research
= 10 credits

Complex Research
= 30 credits
```

gibi.

Ama daha da önemlisi kullanıcıya:

> **"Bu paketle ayda yaklaşık X adet research yapabilirsiniz."**

de.

Çünkü kullanıcı tokenın ne olduğunu umursamıyor.

Onun derdi:

> "Param karşılığında kaç iş yapabiliyorum?"

---

# 23. Üstelik maliyeti kullanıcıdan saklama

DreamAI dashboard:

```
This request

Research:       $0.018
Model:          $0.031
Web crawling:   $0.004
Memory:         $0.001
----------------------
Total cost:     $0.054

You paid:       $0.09
```

gibi bir şey gösterebilir.

Bu inanılmaz güven yaratır.

Özellikle API kullanıcıları için.

---

# 24. "Agent/MCP kalitesiz olur."

Bu da bence **DreamAI'ın en büyük risklerinden biri.**

50 tane MCP yapmak yerine:

### İlk etapta 5 tane mükemmel tool:

```
web_search
web_research
fetch_page
extract_evidence
verify_claim
```

yeter.

Sonra:

```
GitHub
Academic
Finance
News
Company
Maps
Shopping
```

gibi vertical research MCP'leri eklenir.

**Tool count değil task success rate** KPI olmalı.

---

# 25. Hatta kendi benchmark'ını oluştur

Bu bence projenin çok önemli bir parçası.

Örneğin:

```
1000 real-world questions
```

oluştur.

Her biri:

```
Question
Expected facts
Required sources
Freshness requirement
Difficulty
```

ile etiketlenir.

Sonra:

```
Google
Perplexity
ChatGPT
Gemini
DreamAI
```

karşılaştırılır.

Metrikler:

```
Answer correctness
Source correctness
Citation correctness
Freshness
Hallucination
Latency
Cost
```

olur.

O zaman:

> "Biz daha iyiyiz."

demek yerine:

> **"DreamAI 1,000 araştırma testinde %X factual accuracy, %Y citation accuracy ve $Z/query maliyet elde etti."**

diyebilirsin.

Bu **startup açısından çok daha güçlü**.

---

# 26. "Maliyetler getiriyi aşar."

Bence bu riskin çözümü architecture'da.

DreamAI'ın her request'i:

```
Expensive LLM
+
web search
+
20 pages
```

olursa batarsın.

Ama:

```
Semantic cache
       ↓
Exact cache
       ↓
Existing evidence
       ↓
Cheap classifier
       ↓
Cheap model
       ↓
Research only if needed
       ↓
Model cascade
       ↓
Context compression
       ↓
Expensive model only when needed
```

yaparsan unit economics kontrol edilebilir hale gelir.

---

# 27. Ben DreamAI için şu "Cost Engine"i kurardım

```
                    USER QUERY
                        │
                        ▼
                Query Classifier
                        │
              ┌─────────┴─────────┐
              ▼                   ▼
          Cache Hit            Cache Miss
              │                   │
              ▼                   ▼
            Answer            Complexity
                                  │
                       ┌──────────┼──────────┐
                       ▼          ▼          ▼
                       S          M          L
                       │          │          │
                     Cheap      Mid        Research
                       │          │          │
                       └──────────┼──────────┘
                                  ▼
                           Context Builder
                                  │
                                  ▼
                            Model Router
                                  │
                       ┌──────────┼──────────┐
                       ▼          ▼          ▼
                    Cheap       Mid      Frontier
                                  │
                                  ▼
                              Validator
                                  │
                                  ▼
                                USER
```

Bu sistemin **asıl ürünü LLM değildir.**

Asıl ürün:

# Orchestration Layer

---

# 28. Ve burada çok önemli bir stratejik avantajın var

Sen aslında:

```
OpenAI
Anthropic
Google
xAI
...
```

ile yarışmak zorunda değilsin.

Tam tersine onların üzerine çıkabilirsin.

```
             USER
               │
               ▼
           DREAM AI
               │
      ┌────────┼────────┐
      ▼        ▼        ▼
    OpenAI   Gemini   Claude
      │        │        │
      └────────┼────────┘
               ▼
        Dream Research
               │
      ┌────────┼─────────┐
      ▼        ▼         ▼
    Web      Memory     Tools
```

Bu model seni **model bağımlılığından** kurtarır.

---

# 29. Ve bence en büyük fırsat burada

DreamAI'ın uzun vadeli ürünü:

> **"AI Aggregator"**

değil.

### "AI Operating Layer"

olabilir.

Bir kullanıcı:

> "Şunu araştır."

der.

DreamAI karar verir:

```
Which model?
Which search?
How many searches?
Which sources?
Need memory?
Need tools?
Need reasoning?
Need verification?
Need another model?
```

Ve kullanıcı hiçbirini düşünmez.

Bu aslında:

# **AI Decision &amp; Research Orchestrator**

olur.

---

# 30. İki proje arasında benim kararım


|                        | Dream Search | DreamAI        |
| ---------------------- | ------------ | -------------- |
| Google ile rekabet     | 🔴 Çok zor   | —              |
| İlk kullanıcı edinme   | 🔴           | 🟢             |
| Teknik MVP             | 🟠           | 🟢             |
| Gelir modeli           | 🟠           | 🟢             |
| API geliri             | 🟢           | 🟢🟢           |
| Enterprise potansiyeli | 🟢           | 🟢🟢           |
| Network effect         | 🟢🟢         | 🟢             |
| Web research altyapısı | 🟢🟢         | 🟢🟢           |
| Model bağımsızlığı     | —            | 🟢🟢           |
| Güvenlik riski         | 🔴           | 🔴             |
| Reklam ihtiyacı        | Yüksek       | Düşük          |
| Haram reklam riski     | Daha yüksek  | Çok daha düşük |
| Başlangıç maliyeti     | 🔴           | 🟠             |
| Stratejik değer        | 🟢🟢         | 🟢🟢🟢         |


---

# 31. Ben olsam nihai stratejiyi şöyle kurardım

### Aşama 1

**Dream Research Engine**

Sadece backend.

```
/search
/research
/fetch
/evidence
/verify
```

---

### Aşama 2

**DreamAI**

```
Multi-model
+
Research
+
Memory
+
Routing
+
Caching
```

---

### Aşama 3

**DreamAI API**

```
POST /research

POST /search

POST /verify

POST /extract
```

---

### Aşama 4

**DreamAI MCP**

```
search_web()
research_web()
verify_claim()
find_sources()
```

---

### Aşama 5

Diğer agentların DreamAI'ı kullanması:

```
Claude Agent
      │
      ▼
DreamAI MCP
      │
      ▼
Dream Research Engine
```

---

### Aşama 6

Sonunda:

# Dream Search

```
Google-like UI
+
AI Research
+
Evidence
+
Sources
+
Personalized search
```

---

# 32. Böylece çok güzel bir flywheel oluşuyor

```
                  USERS
                    │
                    ▼
                DreamAI
                    │
                    ▼
              More Queries
                    │
                    ▼
             Better Research
                    │
                    ▼
             Better Ranking
                    │
                    ▼
            Better Evidence
                    │
                    ▼
            Better Answers
                    │
                    ▼
              More Users
```

API tarafı:

```
AI Agents
    │
    ▼
DreamAI API
    │
    ▼
More queries
    │
    ▼
More data
    │
    ▼
Better infrastructure
```

Consumer tarafı:

```
Dream Search
    │
    ▼
More searches
    │
    ▼
Better ranking
    │
    ▼
More users
```

**Aynı altyapı üç ayrı gelir kanalı yaratıyor.**

---

# 33. Ve senin korkularına karşı en önemli prensip

Ben bu projeyi **"büyük launch"** şeklinde yapmazdım.

İlk ürün:

> "Dünyanın en iyi AI platformu."

olmayacak.

İlk ürün:

> **"100 gerçek araştırma sorusunda gerçekten çok iyi cevap veren küçük bir research engine."**

olacak.

Örneğin kendine:

```
Benchmark v0.1

100 questions
10 categories

accuracy
citation accuracy
cost
latency
```

koy.

Sonra:

```
v0.2 → 500 questions
v0.3 → 2,000 questions
v1.0 → public API
```

Bu şekilde ilerlersen **linç edilme riskini de ciddi biçimde azaltırsın**, çünkü kullanıcıya ne sattığını ölçebiliyorsun.

---

# 34. Sonuç: Ben olsam ne yapardım?

Çok net:

## **Google'a rakip arama motoruyla başlamazdım.**

Ama Google rakibi olma fikrini **öldürmezdim**.

Onu uzun vadeli hedef olarak tutardım.

### İlk ürün:

# **DreamAI Research Infrastructure**

Bunun kalbi:

```
                    DREAM RESEARCH CORE

          ┌───────────┼────────────┐
          ▼           ▼            ▼
       SEARCH       MEMORY       TOOLS
          │           │            │
          └───────────┼────────────┘
                      ▼
                 EVIDENCE
                      │
                      ▼
                 VERIFICATION
                      │
                      ▼
                MODEL ROUTING
                      │
                      ▼
                CONTEXT ENGINE
                      │
                      ▼
                  LLMs
```

Ve bence **DreamAI'ın gerçek moat'i LLM'ler değil**.

### Moat:

**Search + Research + Evidence + Memory + Routing + Cost Optimization + User Context**

kombinasyonu.

Bu çok daha zor kopyalanır.

---

## Bir de özellikle şunu söyleyeyim

Senin mevcut durumda **"benim teknik bilgilerim yeterli mi?"** diye endişelenmen bence projenin önündeki en büyük problem değil.

Asıl tehlike:

> **6 ay boyunca sistem kurup hiçbir zaman gerçek kullanıcı üzerinde benchmark yapmamak.**

Teknik eksiklikler öğrenilir.

Ama **hangi research workflow'un gerçekten kullanıcıya para ettirdiğini** ancak gerçek kullanıcıdan öğrenebilirsin.

Bu nedenle ben olsam ilk hedefi:

> **"DreamAI'ı yapmak"**

değil,

> **"100 zor gerçek soruda mevcut AI search ürünlerini ölçülebilir şekilde geçebilen bir Research Engine yapmak."**

olarak koyardım.

Bunu başarırsan DreamAI, API, MCP ve en sonunda Dream Search zaten **aynı çekirdeğin farklı ürün yüzleri** haline gelir.

Ve bence bu fikir, daha önce konuştuğumuz DreamAI fikrinin şimdiye kadarki en güçlü versiyonu.