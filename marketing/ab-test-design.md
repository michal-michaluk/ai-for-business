# A/B Test Design — Blog Article (AWSM)

*Źródło: Rekomendacje z marketing-council (Hopkins, Sharp, Handley)*

---

## Założenia wspólne

| Parametr | Wartość |
|----------|---------|
| Kanał dystrybucji | Email (do ICP) + LinkedIn organic + blog |
| Szacowany ruch/miesiąc | ~500 unikalnych odwiedzin |
| Bazowy CVR (klik w CTA) | ~3% |
| MDE | 50% (wzrost z 3% → 4.5%) |
| Poziom ufności | 95% |
| Power | 80% |
| Wymagana próba | ~5 200 na wariant (~10 400 total) |
| Przewidywany czas | 6–8 tygodni na test (sequential testing dopuszczalny) |
| Narzędzie | PostHog / GA4 + własny CRM do lead attribution |

**Uwaga:** Dla B2B z niskim wolumenem ruchu testy są długie. Rekomendacja: jeśli email lista >= 1 500 kontaktów w ICP, zacznij od testu #2 (CTA) na emailu — tam masz kontrolowaną wielkość próby i szybszy wynik.

---

## Test #1: Hook (headline + lead)

**Council source:** Ann Handley — "Hook jest za długi, pierwsze 3 słowa nie zatrzymują."

### Hipoteza

```
Because obecny hook ("You have a BaFin deadline coming…") jest zbyt ogólny
i nie odróżnia się od setek innych artykułów B2B,
we believe zastąpienie go konkretnym, zaskakującym stwierdzeniem
zwiększy CTR (z wyników wyszukiwania / email subject line → przeczytanie artykułu)
dla decydentów IT w niemieckich ubezpieczeniach.
We'll know this is true when CTR wzrośnie o >=50% (z 3% do 4.5%+).
```

### Zmienna

| Element | Control (A) | Variant (B) |
|---------|-------------|-------------|
| Headline | "Why German insurance CTOs are choosing Polish teams over local hiring" | "137,000 job vacancies — and your board still expects Q4 delivery" |
| Lead (first 100 słów) | "You have a BaFin deadline coming. Your backlog is growing. And you cannot find a single Java developer in Germany." | "Every German insurance CTO has the same secret: they're 2–3 developers short and hoping nobody notices. The BaFin deadline will tell." |
| Meta description | Current: "German insurance CTOs are turning to Polish nearshore teams…" | "137k unfilled IT roles. 6-month hiring cycles. Your board doesn't know you're understaffed. Here's what the market leaders are doing." |

Reszta artykułu bez zmian.

### Metryka sukcesu

- **Primary:** Click-through rate (email → article open / LinkedIn → article read) — % osób, które kliknęły i spędziły >30s na stronie
- **Secondary:** Time on page, scroll depth (>75%), social shares
- **Guardrail:** Bounce rate (nie powinien wzrosnąć)

### Czas trwania

6 tygodni (przy ~500 visitor/mc) lub 2 wysyłki emailowe.

### Minimalna próba

~5 200 visitorów na wariant (łącznie ~10 400). Przy ruchu organicznym ~500/mc = ~6.5 tygodnia.

---

## Test #2: CTA — lead magnet vs. discovery call

**Council source:** Claude Hopkins — "Nie ma mierzalnej odpowiedzi. 'Book a discovery call' to nie jest testowalne."

### Hipoteza

```
Because obecne CTA prosi o zobowiązanie (rozmowa) bez wcześniejszej dostarczonej wartości,
a Hopkins od 1923 roku dowodzi, że konkretna oferta (case study, próbka) konwertuje lepiej
niż ogólne "skontaktuj się",
we believe zastąpienie CTA lead magnetem (case study do pobrania)
zwiększy współczynnik konwersji (kliknięcie w CTA / wypełnienie formularza)
dla czytelników w fazie researchu (nie gotowych do rozmowy).
We'll know this is true when konwersja na lead (email capture) wzrośnie o >=50%.
```

### Zmienna

| Element | Control (A) | Variant (B) |
|---------|-------------|-------------|
| CTA button | "Book a discovery call →" | "Download the case study →" |
| Za CTA | Formularz: "Umów rozmowę" (imię, email, firma, tel) | Formularz: "Pobierz case study" (tylko email — niskie friction) |
| Value prop | "We will assess your current team…" | "See how msg Life built a stable 4-person team in 3 weeks — with 7 years of zero turnover." |
| Link | /contact | /case-studies/msg-life (dedykowany landing page) |

Reszta artykułu bez zmian.

### Metryka sukcesu

- **Primary:** Conversion rate (osoby, które kliknęły CTA i zostawiły email / total unique visitors)
- **Secondary:** Jakość leadów (% leadów z domeny .de/.at/.ch, % C-level), czas do pierwszej kwalifikacji
- **Guardrail:** Spam complaints, unsubscribe rate (jeśli email)

### Czas trwania

4 tygodnie (lead magnet z niskim friction powinien konwertować szybciej). Można testować równolegle z Testem #1 na osobnych segmentach ruchu.

### Minimalna próba

~5 200 visitorów na wariant. Jeśli test idzie przez email do listy 2 000 ICP, wystarczy jedna wysyłka z splitem 50/50.

---

## Test #3: Format — long-form article vs. story-first case study

**Council source:** Byron Sharp (więcej CEP-ów) + Ann Handley (brak konkretnej osoby/historii) + Hopkins (case study = "let the product prove itself")

### Hipoteza

```
Because obecny artykuł adresuje tylko jeden category entry point (ostry kryzys kadrowy),
a sekcja "Seven years with the same team" ma najwyższe zaangażowanie (Handley),
we believe zmiana formatu na narrację case study (konkretny klient, konkretny problem,
konkretny wynik) zwiększy czas na stronie i współczynnik konwersji
dla czytelników, którzy nie są w kryzysie, ale rozważają opcje.
We'll know this is true when średni time-on-page wzrośnie o >=30%
a CVR o >=40%.
```

### Zmienna

| Element | Control (A) — obecny artykuł | Variant (B) — case study format |
|---------|------------------------------|---------------------------------|
| Struktura | Problem → rozwiązanie → dowód → CTA | Story: bohater (CTO) → problem → zwrot → rozwiązanie → wynik → CTA |
| Otwarcie | "You have a BaFin deadline coming…" | "Falko's team was stuck. Four Java developers short, a msg Life platform to maintain, and the board asking why Q4 milestones were slipping. Then he tried something none of his peers had." |
| Dowód | Wbudowany w sekcje | Osobna sekcja "The numbers" z timeline: Day 1 → Week 3 → Year 7 |
| Głos | Ekspercki, "my" (AWSM) | Narracyjny, "he" (klient) — AWSM pojawia się w połowie |
| CTA | "Book a discovery call →" | "Want the same result? Here's how we can do it for your team →" (ten sam lead magnet co Test #2) |

### Metryka sukcesu

- **Primary:** Time on page (avg) + Conversion rate
- **Secondary:** Scroll depth, return visits, link clicks (social shares), bounce rate
- **Guardrail:** Współczynnik odrzuceń (bounce) — narracja nie może być dłuższa kosztem utrzymania uwagi

### Czas trwania

8 tygodni (format to większa zmiana — wymaga więcej danych). Alternatywnie: test na emailu z podziałem na dwie wysyłki.

### Minimalna próba

~5 200 visitorów na wariant. Najlepiej testować po zakończeniu Testów #1 i #2, żeby nie krzyżować zmiennych.

---

## Plan wykonania

| Kolejność | Test | Kanał | Czas | Uwagi |
|-----------|------|-------|------|-------|
| 1 | #2 CTA | Email (split 50/50) | 2 tyg (jedna wysyłka + 2 tyg follow-up) | Najszybszy wynik — lead magnet vs. call |
| 2 | #1 Hook | LinkedIn organic + blog | 6 tyg | Testuj zwycięskie CTA z Testu #2 |
| 3 | #3 Format | Blog + email | 8 tyg | Największa zmiana — najpierw potwierdź, że CTA i hook działają |

## Kryteria sukcesu (decision framework)

| Wynik | Decyzja |
|-------|---------|
| 1+ test wygrywa z p < 0.05 | Wdrożyć zwycięski wariant, resztę artykułu dostosować |
| Wszystkie nieistotne statystycznie | Wykonać test jakościowy (wywiady z 5 CTO: która wersja bardziej przekonuje?) |
| Sprzeczne wyniki (np. format wygrywa na czasie, przegrywa na CVR) | Zastosować format case study, ale z lead magnetem CTA z Testu #2 |
