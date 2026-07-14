# RevOps: Content-to-Pipeline Map — AWSM

*Założenia: sales-led B2B, ACV ~€50–200k (zespół outsourcingowy), cykl 2–6 miesięcy, ICP = niemieckie ubezpieczenia/finanse.*

---

## 1. Touchpointy — gdzie klient styka się z treścią

| Touchpoint | Kanał | Content | Intencja czytelnika | Co mierzymy |
|------------|-------|---------|---------------------|-------------|
| T1 | LinkedIn organic | Post o problemie hiringowym | Skanowanie, ciekawość | Impressions, clicks, profile visits |
| T2 | LinkedIn DM | Odpowiedź na komentarz / InMail | Chce wiedzieć więcej | Reply rate, rozmowa |
| T3 | Email (lista ICP) | Newsletter / powiadomienie o wpisie | Otwiera, czyta | Open rate, CTR do bloga |
| T4 | Blog organic (SEO) | Artykuł o Polish nearshore | Szuka rozwiązania | Time on page, scroll depth |
| T5 | Blog — lead magnet | CTA → formularz po case study | Chce dowodu | Conversion rate (email capture) |
| T6 | Blog — discovery call | CTA → formularz na rozmowę | Gotów do rozmowy | Conversion rate (form) |
| T7 | Case study (PDF) | Po pobraniu — email follow-up | Analizuje, porównuje | Open rate, reply, meeting booked |

**Luka #1:** Brak middle-of-funnel contentu między "pobieram case study" a "umawiam rozmowę" — np. checklista compliance VAIT, webinar, porównanie kosztów.

**Luka #2:** Brak UTM parameterów na wszystkich linkach — nie wiesz, który touchpoint przyprowadził leada.

---

## 2. Lead scoring — jakie zachowania kwalifikują

### Explicit (fit) — kto to jest

| Atrybut | Punkty | Źródło |
|---------|--------|--------|
| Branża: insurance / finance | +30 | Email domain, formularz |
| Branża: ERP / regulated | +20 | Email domain, formularz |
| Stanowisko: CTO / VP Eng / IT Director | +25 | LinkedIn, formularz |
| Stanowisko: Team Lead / PM | +15 | LinkedIn, formularz |
| Firma: >200 employees | +20 | Enrichment (Clearbit/Apollo) |
| Domena: .de / .at / .ch | +10 | Email domain |
| Email osobisty (gmail, etc.) | -20 | Regex na domenie |

### Implicit (engagement) — co robi

| Zachowanie | Punkty | Uwagi |
|------------|--------|-------|
| Pobrał case study msg Life | +15 | Research phase |
| Kliknął CTA "Umów rozmowę" | +25 | Wysoka intencja |
| Odwiedził /pricing | +20 | Porównanie ofert |
| Odwiedził blog >2 razy w miesiącu | +10 | Budowanie zaufania |
| Otworzył email >3 razy w miesiącu | +5 | Stałe zainteresowanie |
| Odszedł z formularza (za wysokie friction) | -5 | Obniż friction lub follow-up |

### MQL threshold: 50 punktów

Przykład MQL: CTO z ubezpieczeń (+30) z domeny .de (+10), który pobrał case study (+15) = 55 pkt → MQL.

**Luka #3:** Brak narzędzia do scoringu (brak CRM / brak automatyzacji). Jeśli nie masz HubSpota lub Salesforce, scoring jest ręczny i nie skaluje się.

---

## 3. Handoff — jak lead trafia od marketingu do sprzedaży

```
Lead (pobiera case study / wypełnia formularz)
  │
  ▼
CRM: automatyczne utworzenie kontaktu (lub manualny import z arkusza)
  │
  ▼
Marketing: lead jest w stanie "Subscriber"
  │ Jeśli scoring >= 50:
  ▼
MQL alert → e-mail do Sales / SDR (lub Slack)
  │ SLA: kontakt < 4h robocze
  ▼
SDR: outreach (telefon + email) — próba disco calla
  │ Jeśli lead odbiera i zgadza się na rozmowę:
  ▼
SQL → przekazany do AE (Account Executive)
  │ Jeśli lead nie odbiera / nie odpowiada:
  ▼
Nurture: automatyczna sekwencja emaili (case study → webinar → checklista)
```

### SLA

| Krok | Czas | Odpowiedzialny |
|------|------|----------------|
| MQL → alert | Natychmiast | System (CRM) |
| Alert → pierwszy kontakt | < 4h robocze | SDR |
| Kontakt → kwalifikacja | < 48h | SDR |
| Kwalifikacja → przekazanie AE | < 24h | SDR |
| AE → pierwsze demo | < 5 dni roboczych | AE |

**Luka #4:** Jeśli nie ma CRM-a, ten handoff istnieje tylko w teorii. W praktyce lead ląduje w skrzynce mailowej i jest obsługiwany ad hoc. Przy skali >10 leadzi/miesiąc to się nie skaluje.

**Luka #5:** Brak SLA i brak accountability — jeśli SDR nie odezwie się w 48h, nikt o tym nie wie. Potrzebne jest narzędzie do eskalacji (np. Slack bot, automatyczne przypomnienie).

---

## 4. Feedback loop — jak sprzedaż informuje marketing, co działa

### Closed-won: co wpisać w CRM

| Pole | Przykład | Dla kogo |
|------|----------|----------|
| Lead source (kampania UTM) | `linkedin-organic-jul2026` | Marketing attribution |
| Content, który wpłynął | Case study msg Life, Blog article | Który content działa |
| Competitor beaten | Sii, Luxoft, niemiecki hiring | Kogo atakować w treściach |
| Key buying reason | German fluency, speed, domain expertise | Co podbijać w copy |
| Sales cycle length | 73 dni | Prognoza pipeline'u |
| Deal value (TCV) | €120,000/rok | Które segmenty są najbardziej wartościowe |

### Closed-lost: co wpisać (najważniejsze)

| Pole | Przykład | Działanie |
|------|----------|-----------|
| Loss reason | "Wybrali konkurenta" → jaki? | Content o przewadze nad tym konkurentem |
| Loss reason | "Za drogo" vs "Nie mamy budżetu" | Pricing page test |
| Loss reason | "Nie teraz, ale za 6 miesięcy" | Nurture sequence + przypomnienie |
| Content gaps | "Chcieli zobaczyć case study z msg nexinsure" | Brief dla copywritera |

### Cotygodniowy rytuał (30 min, poniedziałek)

| Agenda | Kto prowadzi | Czas |
|--------|-------------|------|
| 1. Closed-won last week — co zadziałało? | AE | 5 min |
| 2. Closed-lost last week — dlaczego? | AE | 10 min |
| 3. Nowe MQL — które odrzucamy i dlaczego? | SDR | 5 min |
| 4. Content performance — co generuje leady? | Marketing | 5 min |
| 5. Akcje na ten tydzień | Wszyscy | 5 min |

**Luka #6:** Jeśli nie ma CRM-a, ten feedback loop jest niemożliwy. Nawet przy arkuszu Google z biegiem czasu powstają niespójności.

---

## 5. Luki — podsumowanie

| # | Luka | Priorytet | Koszt naprawy | Co zrobić |
|---|------|-----------|---------------|-----------|
| 1 | Brak middle-of-funnel contentu | Medium | Niski (1 dzień copywritingu) | Stworzyć checklistę VAIT compliance |
| 2 | Brak UTM na linkach | Wysoki | Niski (30 min w GA4) | Dodać UTM do wszystkich linków w treściach i emailach |
| 3 | Brak automatyzacji scoringu | Wysoki | Średni (CRM setup) | Wdrożyć HubSpot (darmowy tier na start) lub przynajmniej spreadsheet z manualnym scoringiem |
| 4 | Brak CRM = brak handoffu | Krytyczny | Średni (CRM setup) | HubSpot / Salesforce / Pipedrive — bez tego pipeline nie istnieje |
| 5 | Brak SLA i eskalacji | Średni | Niski (Proces) | Ustalić SLA w dokumentacji + Slack przypomnienia |
| 6 | Brak feedback loop | Średni | Niski (Rytuał) | Wpisać cotygodniowe spotkanie MQL review do kalendarza |

---

## 6. Pipeline — pełna ścieżka (od contentu do deala)

```
LinkedIn post → kliknięcie → blog → time-on-page > 60s → lead magnet (case study PDF)
  │
  ▼
Formularz (email) → Subscriber
  │ scoring >= 50? + domain .de + CTO title
  ▼
MQL → alert do SDR (< 4h)
  │
  ├── SDR: disco call → potrzeba + budżet + timeline OK
  │   ▼
  │   SQL → demo z AE → proposal → negocjacja → Closed-won
  │
  └── SDR: brak odpowiedzi → nurture (3-email sequence)
      │
      ├── Reaktywacja (otworzył maila po 30 dniach) → powrót do SDR
      │
      └── Brak aktywności 90 dni → Archive
```

### Wąskie gardła (najczęstsze miejsca utraty)

| Stage | Conversion (benchmark) | AWSM risk | Przyczyna |
|-------|----------------------|-----------|-----------|
| Blog → Formularz | 3–5% | ✅ OK jeśli lead magnet | Bez lead magnetu: <1% |
| Formularz → MQL | 50–70% | ⚠️ Bez CRM nie wiesz | Automatyzacja scoringu |
| MQL → pierwszy kontakt | 80% (jeśli < 4h) | 🔴 Bez alertu: 0% | Slack / email notification |
| MQL → SQL | 30–50% | ⚠️ Zależy od jakości leada | Jakość ICP match |
| SQL → Opportunity | 50–70% | ✅ Długi cykl, ale wysokie ACV | Wytrzymałość procesu |
| Opportunity → Won | 20–30% | ⚠️ Zależy od przewagi nad konkurencją | Sales enablement |
