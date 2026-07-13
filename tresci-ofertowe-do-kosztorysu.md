# Treści ofertowe — enrichment do Kosztorys.xlsx

---

## 1. Executive Summary (arkusz "Offer Overview")

Bottega proponuje kompleksowe wdrożenie inżynierii oprogramowania wspomaganej
sztuczną inteligencją (AI SDLC) w dwóch obszarach biznesowych: Bankowość Centralna
oraz Capital Markets, wraz z opcjonalną technologiczną restrukturyzacją wybranych
modułów.

Oferta obejmuje budowę baz wiedzy i dokumentacji zoptymalizowanej pod AI,
konfigurację narzędzi i instrukcji dla analityków, developerów i reviewerów,
wdrożenie automatyzacji CI/CD oraz security gates, a także szkolenia i transfer
know-how. Łączna wartość inwestycji została przedstawiona w podziale na sześć
obszarów (TOTAL.01–TOTAL.06).

Efekt: przyspieszenie time-to-market, redukcja długu technicznego, retencja wiedzy
projektowej i skalowanie kompetencji inżynierskich w organizacji.

---

## 2. Podejście i fazy wdrożenia

### Filozofia

Nasze podejście to stopniowa ewolucja, a nie rewolucja. Rozumiemy specyfikę
dojrzałych zespołów deweloperskich, dlatego nie burzymy działających procesów —
integrujemy AI tam, gdzie przynosi wymierny zwrot z inwestycji i odciąża
inżynierów od powtarzalnych zadań. Unikamy pułapek związanych z bezpieczeństwem,
halucynacjami modeli i obniżeniem jakości kodu.

### Faza 1 — Audit i strategia

Analiza obecnego procesu wytwórczego, stosu technologicznego i kultury inżynierskiej.
Identyfikacja obszarów o najwyższym potencjale zwrotu z inwestycji w AI.
Wynik: roadmapa wdrożenia dopasowana do specyfiki organizacji.

### Faza 2 — Proof of Value (pilotaż)

Wdrożenie na wybranym zespole lub module systemu. Dostawa w formie:
- **pracy własnej Bottega** — przygotowanie narzędzi, dokumentacji, instrukcji AI
- **pair programming online** — bezpośredni transfer know-how poprzez wspólną pracę
  z ekspertem Bottega na realnym kodzie i zadaniach

Wynik: działające rozwiązanie na pilocie + udowodniona wartość przed skalowaniem.

### Faza 3 — Skalowanie kompetencji

Systematyczne rozszerzanie praktyk AI SDLC na całą organizację. Przekazanie
licencji i narzędzi z bezterminowym prawem do wewnętrznego użytku i własnego
rozwoju. Szkolenia dla szerszego grona pracowników (analitycy, PM, developerzy).

---

## 3. Zakres wdrożenia — opisy narracyjne (do kolumny Opis w arkuszu Podsumowanie)

### TOTAL.01 — Bankowość Centralna: AI SDLC + Know-How

Dla BU Bankowość Centralna wdrażamy pełen zestaw praktyk AI SDLC:
skonsolidowanie dokumentacji funkcji systemu (IK.1), mapowanie funkcjonalności na
kod i architekturę (IK.2), dokumentację architektury frontendu i backendu
zoptymalizowaną pod AI (IK.4, IK.5), instrukcje AI do analizy regulatorów KNF/UE
(EK.1) oraz narzędzia i instrukcje dla analityków i developerów (TL.1–TL.5).

Efekt: analitycy i developerzy zyskują wspólny język z AI. Skrócenie czasu analizy
impaktu zmian, eliminacja błędów wynikających z nieaktualnej dokumentacji,
przyspieszenie code review i testów. Dostawa: praca własna Bottega + pair
programming online.

### TOTAL.02 — Capital Markets: AI SDLC + Know-How

Analogiczny zakres jak dla Bankowości Centralnej, dostosowany do specyfiki
BU Capital Markets (w tym regulator GPW). Obejmuje budowę baz wiedzy, instrukcji
AI i narzędzi dla wszystkich ról w cyklu wytwórczym.

Dodatkowo zakłada pracę własną Bottega w większym wymiarze, by odciążyć zespół
klienta i ograniczyć zaangażowanie jego inżynierów w fazie budowy.

Efekt: te same korzyści co TOTAL.01 z niższym obciążeniem zespołu wewnętrznego.

### TOTAL.03 — Capital Markets: Technologiczna restrukturyzacja

Kompleksowa modernizacja wybranych obszarów systemu Capital Markets, obejmująca:
- standaryzację CI/CD na Jenkinsfile i shared library (REF.1)
- migrację builda Ant → Maven/Gradle dla kluczowych modułów (REF.2)
- automatyzację deploy QA z self-service i rollback (REF.3)
- ujednolicenie zarządzania artefaktami release (REF.4)
- automatyzację iOS build/release przez Fastlane (REF.5)
- włączenie Fortify / Dependency-Track z gatingiem w pipeline (REF.6)
- plan migracji technologicznej z wyceną etapową (REF.RE.1)

Efekt: nowoczesny, zautomatyzowany pipeline dostarczania oprogramowania.
Szybsze buildy, eliminacja wąskich gardeł, bezpieczeństwo wbudowane w proces.
Dostawa: praca własna Bottega na pilocie + pair programming przy transferze
know-how + review po stronie klienta.

### TOTAL.04 — Pakiet szkoleń

Szkolenia dla szerszego grona pracowników, jak efektywnie pracować z AI SDLC
wdrożonym do projektów. Szkolenia mogą bazować na realnych zadaniach i kodzie
projektów, jeśli będzie to dopuszczalne.

Obejmuje:
- **Szkolenie AI SDLC dla analityków i PM (2 dni)** — praca z AI w analizie
  biznesowej, generowanie wymagań, review dokumentacji analitycznej z AI
- **Szkolenie AI SDLC dla developerów (3 dni)** — context engineering, testowanie
  z AI, code review z AI, bezpieczna praca z kodem legacy

Efekt: organizacja zyskuje samodzielność w utrzymaniu i rozwijaniu praktyk AI SDLC.

### TOTAL.05 — Gwarancja 1 rok / Bufor dodatkowych godzin

Pakiet dodatkowych godzin prac zarówno nad AI SDLC, jak i technologiczną
restrukturyzacją. Pozwala na:
- bieżące wsparcie w pierwszych miesiącach po wdrożeniu
- dokonanie korekt i dostosowań wynikających z nowych potrzeb
- dodatkowe pary godzin na niespodziewane wyzwania techniczne

Efekt: bezpieczeństwo i elastyczność — organizacja nie zostaje sama z nowym
rozwiązaniem, ma bufor na dopracowanie szczegółów.

### TOTAL.06 — Przekazanie narzędzi AI SDLC i licencji

Przekazanie licencji na narzędzia dla AI SDLC z bezterminowymi prawami do
wewnętrznego użytku i własnego rozwoju. Obejmuje wszystkie narzędzia
skonfigurowane i przetestowane w ramach wdrożenia (szczegóły w arkuszu
"Narzędzia").

Efekt: organizacja staje się samowystarczalna — może samodzielnie utrzymywać,
modyfikować i rozwijać narzędzia bez dalszej zależności od Bottega.

---

## 4. Efekty biznesowe (do arkusza "Offer Overview")

### Przyspieszenie Time-to-Market

Automatyzacja powtarzalnych zadań (generowanie testów, code review, analiza
impaktu) skraca czas dostarczania funkcjonalności. AI przejmuje żmudne czynności,
inżynierowie skupiają się na pracy twórczej i decyzyjnej.

**Powiązane obszary:** TOTAL.01, TOTAL.02, TOTAL.03

### Redukcja długu technicznego

Systematyczna poprawa jakości kodu i architektury poprzez AI Review (bugs,
architektura, complexicity, zgodność ze specyfikacją) oraz refaktoryzację
wspieraną przez AI.

**Powiązane obszary:** TOTAL.03, TOTAL.01, TOTAL.02

### Retencja wiedzy projektowej

AI działa jak "kustosz wiedzy" o projekcie — skonsolidowana dokumentacja, baza
wiedzy mapująca funkcjonalność na kod, instrukcje dla AI. Nowi pracownicy
wdrażają się szybciej, ryzyko utraty wiedzy przy rotacji jest zminimalizowane.

**Powiązane obszary:** TOTAL.01, TOTAL.02, TOTAL.06

### Skalowanie kompetencji inżynierskich

Ujednolicenie standardów pracy w zespołach deweloperskich. Dzięki narzędziom
i instrukcjom AI każdy inżynier pracuje według tych samych wzorców, niezależnie
od doświadczenia. Szkolenia i transfer know-how budują trwałe kompetencje.

**Powiązane obszary:** TOTAL.04, TOTAL.01, TOTAL.02

### Bezpieczeństwo danych i procesu

Pełna kontrola nad tym, gdzie trafia kod źródłowy i dokumentacja. AI działa
w ramach zdefiniowanych instrukcji i narzędzi, z gatingiem bezpieczeństwa
w pipeline. Opcje deploymentu: Cloud Native, Private Cloud (VPC) lub
On-Premise (Air-Gapped) — dopasowane do polityki bezpieczeństwa organizacji.

**Powiązane obszary:** TOTAL.03, TOTAL.06

---

## 5. Model dostawy

### Formy współpracy

| Forma | Opis | Kiedy stosujemy |
|---|---|---|
| **Praca własna Bottega** | Eksperci Bottega realizują zadania samodzielnie, bez angażowania zespołu klienta | Budowa narzędzi, dokumentacji, instrukcji — tam gdzie nie trzeba transferować wiedzy |
| **Pair programming online** | Ekspert Bottega pracuje wspólnie z inżynierem klienta w parach, przekazując know-how w czasie rzeczywistym | Zadania wymagające transferu kompetencji — context engineering, refactoring, konfiguracja pipeline |
| **Review po stronie klienta** | Klient weryfikuje efekty prac Bottega, otrzymuje feedback i możliwość korekty | Każda dostarczona pozycja przed zamknięciem |

### Środowiska docelowe

- **Cloud Native (Enterprise API)** — dla firm akceptujących przetwarzanie w chmurze
  z umowami BAA, stawiających na najwyższą inteligencję modeli
- **Private Cloud (VPC)** — dla organizacji wymagających zgodności z regulacjami
  korporacyjnymi, posiadających infrastrukturę w chmurze publicznej
- **On-Premise (Air-Gapped)** — dla banków i sektora publicznego o najwyższym
  rygorze tajności; obejmuje dobór hardware'u, konfigurację i support

### Harmonogram

Wdrożenie planowane jest w trybie iteracyjnym. Poszczególne obszary (IK, EK, TL,
REF) mogą być realizowane równolegle w miarę dostępności zespołów i środowisk.
Szczegółowy harmonogram ustalany jest w Fazie 1 (Audit i strategia).

---

## 6. Ryzyka i mitigacje

| Ryzyko | Mitigacja |
|---|---|
| **Halucynacje modeli AI** — AI generuje nieprawdziwe lub niepoprawne informacje | Context engineering — budowa precyzyjnego kontekstu dla LLM; instrukcje AI wymuszające weryfikację faktów; rola człowieka w pętli (human-in-the-loop) |
| **Obniżenie jakości kodu** — AI generuje kod niezgodny ze standardami lub wprowadza błędy | AI Review w pipeline (bugs, architektura, complexicity, zgodność ze specyfikacją); gating security (Fortify, Dependency-Track); code review przez doświadczonych inżynierów |
| **Wyciek danych / kodu źródłowego** — wrażliwy kod trafia do publicznych modeli AI | Możliwość deploymentu On-Premise (Air-Gapped); Private Cloud (VPC); polityka danych i instrukcje AI wymuszające lokalne przetwarzanie |
| **Odrzucenie przez zespół** — inżynierowie nie chcą pracować z AI | Stopniowe wprowadzanie (ewolucja, nie rewolucja); pokazanie wartości na pilocie; szkolenia i mentoring; odciążenie od powtarzalnych zadań |
| **Ponoszenie zbędnych kosztów** — niewłaściwe użycie AI przez nieprzeszkolony personel generuje podwyższone koszty bez adekwatnych korzyści | Harness engineering — znacząco podnosi jakość przy wykorzystaniu mniejszych modeli; oszczędności dzięki wycinaniu zbędnego outputu i logów; szkolenia z efektywnego korzystania z AI (TOTAL.04) |
| **Uzależnienie od dostawcy (vendor lock-in)** | Przekazanie narzędzi i licencji na własność; bezterminowe prawa do wewnętrznego użytku i rozwoju; transfer know-how przez pair programming; dokumentacja i instrukcje pozostają w organizacji |

---

## 7. Dlaczego Bottega

- **15 lat doświadczenia** w szkoleniach i doradztwie dla zespołów deweloperskich
- **78 aktywnych trenerów** o modelu kompetencji Π (Pi) — silny filar techniczny
  oraz silny filar wspierający: umiejętności miękkie, talent edukacyjny, myślenie
  strategiczne
- **Ponad 12 000 przeszkolonych uczestników**, **150 dni szkoleń rocznie**
- **43 klientów** z branż: finansowa, medyczna, ubezpieczeniowa, energetyczna,
  zbrojeniowa, e-commerce
- **Doświadczenie w transformacji zespołów** — audyty, refactoring, programy
  rozwoju kompetencji, mentoring techniczny, coaching liderów
- **Eksperci:** Sławomir Sobótka, Jakub Nabrdalik, Łukasz Szydło, Mariusz Gil

### Wybrani klienci

Intel Polska • Orange Polska • Roche Polska • Asseco Polska • Tomtom Polska •
Capgemini • Comarch • Luxoft • Motorola • PZU • Tieto • Atos

---

## 8. Value proposition per item (do arkuszy szczegółowych)

Poniżej opis dla każdej pozycji — co zmienia się dla konkretnych ról w organizacji.

### Obszar IK (Internal Knowledge)

**IK.1 — Skonsolidowana dokumentacja funkcji systemu dla AI**
> Analitycy zyskują pewność, że AI rozumie aktualny stan systemu i impakt na
> istniejącą funkcjonalność — skraca to czas weryfikacji pomysłów i redukuje
> błędy z nieaktualnej wiedzy. Developerzy i agenci wiedzą co jest już
> zaimplementowane. Reviewerzy mają kontekst do oceny impaktu przed
> implementacją. QA rozumie pełny kontekst systemu.

**IK.2 — Baza wiedzy mapująca funkcjonalność na kod/architekturę**
> AI wskazuje potencjalne miejsca zmian w kodzie po opisie zmian — analityk
> robi finalną walidację. Mapowanie PL→EN ogranicza błędy językowe.
> Developerzy wiedzą dokładnie gdzie zmieniać kod. Reviewerzy oceniają pełen
> impact. Testerzy wiedzą co musi być przetestowane.

**IK.3 — Heurystyczne szacowanie pracochłonności**
> Liderzy projektu zyskują estymaty oparte na wartościach eksperckich,
> porównujące artefakty analityczne z realnym stanem systemu.

**IK.4 — Dokumentacja architektury frontendu dla AI**
> Analitycy szybciej oceniają impact na frontend. AI generuje kod zgodny
> z lokalną architekturą i wzorcami (formularze, tabelki, common elements).
> Reviewerzy sprawdzają zgodność z zasadami architektonicznymi.
> UI testy e2e są spójne ze wzorcami.

**IK.5 — Dokumentacja architektury backendu dla AI**
> Analitycy szybciej oceniają impact na backend. AI generuje kod zgodny
> z lokalnymi wzorcami (beany, encje, procedury, exception handling).
> Reviewerzy sprawdzają zgodność architektoniczną. AI pisze testy
> jednostkowe i integracyjne zgodne ze wzorcami.

**IK.7 — Implementacja brakujących scenariuszy e2e**
> Analitycy przygotowują z AI brakujące scenariusze testowe. Developerzy
> dostają scenariusze z przykładowymi danymi. Reviewerzy sprawdzają
> pokrycie wszystkich scenariuszy. QA ma gotowe scenariusze e2e
> w pseudokodzie do automatycznego wykonania.

### Obszar EK (External Knowledge)

**EK.1 — Instrukcje AI dla pracy ze źródłami regulatorów KNF/UE/GPW**
> Analitycy używają AI do rozbudowy wstępnych wymagań (w tym regulacyjnych)
> i generowania pytań doprecyzowujących przed warsztatami z klientem.
> AI weryfikuje analizę vs źródłami regulatorów — przyspiesza pracę,
> nie zwalnia z odpowiedzialności.

### Obszar TL (Tools & Instructions)

**TL.1 — Narzędzia AI dedykowane analitykom**
> Analitycy zyskują dedykowane środowisko AI wspierające rozbudowę
> wymagań, generowanie pytań doprecyzowujących i review dokumentów
> analitycznych.

**TL.2 — Instrukcje AI do Review Analizy**
> AI przeprowadza gap analysis / spike analysis analizy, sprawdza brakujące
> elementy, zasady jakościowe i definition of ready.

**TL.3 — Generowanie diagramów BPMN/UML**
> Analitycy generują wstępne diagramy edytowalne bez konieczności
> integracji z Enterprise Architect.

**TL.4 — Generowanie UI/UX low fidelity**
> Szybkie prototypowanie interfejsów z AI, bez Enterprise Architect.

**TL.5 — Proponowanie scenariuszy testowych z analizy**
> AI generuje scenariusze na podstawie analizy (UI, walidacje, reguły,
> przykłady danych).

**TL.6 — Reverse Engineering mapowania funkcjonalność → kod**
> Automatyczne odtworzenie mapowania funkcji na kod i architekturę.

**TL.9 — Integracja AI z bazą Oracle (readonly)**
> AI analizuje model danych i odpyta o przykładowe dane na środowisku
> testowym.

**TL.10 — Reverse Engineering zasad architektonicznych**
> Automatyczne wydobycie i sformalizowanie reguł architektonicznych
> z istniejącego kodu.

**TL.13 — AI hot swap / redeploy + logi**
> AI może podmienić kod, uruchomić redeploy i podejrzeć logi — jak
> developer.

**TL.14 — AI uruchamia pipeline Jenkins**
> AI może wywołać pipeline i podejrzeć logi z Jenkins.

**TL.31 — AI lokalny troubleshooting**
> AI podpowiada co sprawdzać po kolei — wgląd w logi, bazę, instrukcje.

**TL.32 — Tool dla AI do interakcji z remote beans**
> AI wywołuje requesty na środowisku dev dla smoke test / troubleshooting.

**TL.11 — AI Review zbiorcze w pipeline**
> Wszystkie review (bugs, architektura, complexicity, specyfikacja)
> uruchamiane automatycznie w pipeline + publikacja do review tool.

**TL.15 — AI Review potential bugs**
> Przyrostowe wykrywanie potencjalnych błędów w nowym kodzie.

**TL.16 — AI Review architektury**
> Przyrostowe sprawdzenie zgodności z architekturą w nowym kodzie.

**TL.17 — AI Review complexity check**
> Przyrostowa kontrola złożoności kodu.

**TL.18 — AI Review implementacja vs specyfikacja**
> Sprawdzenie czy kod realizuje postawione wymagania.

### Obszar REF (Refaktoryzacja)

**REF.RE.1 — Plan migracji + wycena etapowa**
> Klient dostaje realny plan migracji z etapami, ryzykami, zależnościami
> i estymacją — zamiast szacowania w ciemno.

**REF.1 — Standaryzacja CI/CD na Jenkinsfile**
> Jeden wzorcowy Jenkinsfile + shared library dla wszystkich repozytoriów.
> Zespoły i agenty AI mają jeden znajomy flow.

**REF.2 — Migracja builda Ant → Maven/Gradle**
> Szybsze buildy, łatwiejsze utrzymanie, dependency management
> i security scanning out-of-the-box.

**REF.3 — Automatyzacja deploy QA**
> Self-service deploy z pipeline (klik + API dla agenta), rollback, runbook.
> Eliminacja wąskiego gardła "tylko X potrafi wgrać release".

**REF.4 — Ujednolicenie zarządzania artefaktami**
> Nexus/Artifactory — w każdej chwili wiadomo co i kiedy trafiło
> na środowisko.

**REF.5 — Automatyzacja iOS build/release**
> Mac worker + Fastlane w pipeline. Koniec ręcznych obejść z kontami
> i uprawnieniami.

**REF.6 — Fortify + Dependency-Track z gatingiem**
> Stałe skany SAST/SCA jako warunki blokujące w pipeline. Jednolity
> raport. Jasna odpowiedzialność za naprawy.

---

## 9. Podsumowanie — mapowanie TOTAL.x na arkusze szczegółowe

| Kod | Arkusz źródłowy | Opis wysoki |
|---|---|---|
| TOTAL.01 | Central Banking | AI SDLC + Know-How dla Bankowości Centralnej |
| TOTAL.02 | Capital Markets | AI SDLC + Know-How dla Capital Markets |
| TOTAL.03 | Refactor Capital Markets | Technologiczna restrukturyzacja Capital Markets |
| TOTAL.04 | (osobna sekcja) | Pakiet szkoleń AI SDLC |
| TOTAL.05 | (osobna sekcja) | Gwarancja 1 rok / bufor godzin |
| TOTAL.06 | Narzędzia | Przekazanie narzędzi i licencji AI SDLC |
