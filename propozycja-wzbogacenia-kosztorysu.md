# Propozycja wzbogacenia Kosztorys.xlsx o warstwę opisową

## Cel

Dodać narrację biznesową do szczegółowego arkusza kalkulacyjnego, aby Middle Management
i Board of Directors mogli szybko zrozumieć *czego* dotyczy inwestycja, *dlaczego* jest potrzebna
i *jakie przyniesie efekty* — bez zagłębiania się 94+ pozycji kosztowych.

---

## Proponowane zmiany

### 1. Nowy arkusz: "Offer Overview"

Strona tytułowa oferty zawierająca sekcje:

| Sekcja | Opis | Dla kogo |
|---|---|---|
| **Exec Summary** | 3–4 zdania: czym jest AI SDLC, zakres (Banking + Capital Markets + refactor), łączna wartość | Board |
| **Podejście i fazy** | Audit & Strategy → Proof of Value → Skalowanie. Wyjaśnienie filozofii delivery (ewolucja, nie rewolucja; pair programming; knowledge transfer) | Middle Management |
| **Zakres per domena** | Dla każdego TOTAL.x — co obejmuje, *dlaczego* to potrzebne, *co zmienia* dla zespołów | Middle Management |
| **Efekty biznesowe** | Time-to-market, redukcja długu technicznego, retencja wiedzy, skalowanie kompetencji, bezpieczeństwo. Mapowanie na konkretne TOTAL items | Board |
| **Model dostawy** | Cloud / Private Cloud / On-Premise, podział pair programming vs praca własna, harmonogram | Middle Management |
| **Ryzyka i mitigacje** | Jak unikamy halucynacji, obniżenia jakości, wycieków danych (context engineering, gating, air-gapped options) | Obie grupy |
| **Dlaczego Bottega** | 15 lat, 78 trenerów, kluczowi klienci (Intel, Orange, Roche, PZU), model kompetencji PI | Board |

### 2. Nowa kolumna w "Podsumowanie": Opis oferty / Opis

Dodać do arkusza podsumowującego kolumnę (np. **G: "Opis ofertowy"**), która dla każdego TOTAL.x
zawiera rozszerzony opis narracyjny.

**Przykład dla TOTAL.01** (obecnie: *"Wdrożenie AI SDLC z przekazaniem Know-How dla BU Bankowość"*):

> Dla BU Bankowość wdrażamy kompleksowe wsparcie AI SDLC:
> skonsolidowanie dokumentacji systemu (IK.1–IK.5), mapowanie
> funkcji na kod i architekturę (IK.2), instrukcje AI do analizy
> regulacyjnej KNF/UE (EK.1) oraz narzędzia AI dla analityków
> i developerów (TL.1–TL.5). Efekt: analitycy i developerzy
> zyskują wspólny język z AI, skracając czas analizy impaktu
> o ~40% i eliminując błędy z nieaktualnej dokumentacji.
> Dostawa: pair programming online + praca własna Bottega.

### 3. Nowa kolumna w arkuszach szczegółowych: "Value proposition"

Dodać do arkuszy (Central Banking, Capital Markets, Refactor Capital Markets, Narzędzia)
kolumnę opisującą *dla każdej pozycji* — co zmienia się dla konkretnej roli (Analityk,
Developer, Reviewer, QA).

**Przykład dla IK.1** (obecnie tylko suchy opis):

> **Dla Analityka**: pewność, że AI rozumie aktualny stan systemu → szybsza weryfikacja pomysłów.
> **Dla Developera**: AI i agenci wiedzą co jest już zaimplementowane.
> **Dla Reviewera**: kontekst do oceny impaktu przed implementacją.
> **Dla QA**: pełny kontekst systemu → wie co testować po zmianach.

---

## Sugerowany układ arkusza "Offer Overview"

| Wiersz | Zawartość |
|---|---|
| 1 | **AI SDLC — Oferta wdrożenia** |
| 3 | **Executive Summary** |
| 4 | (3–4 zdania podsumowania) |
| 6 | **Podejście** |
| 7 | Faza 1: Audit & Strategy — opis |
| 8 | Faza 2: Proof of Value — opis |
| 9 | Faza 3: Skalowanie — opis |
| 11 | **Zakres wdrożenia** |
| 12 | TOTAL.01 — Bankowość: opis narracyjny + wartość |
| 13 | TOTAL.02 — Capital Markets: opis narracyjny + wartość |
| 14 | TOTAL.03 — Refaktoryzacja: opis narracyjny + wartość |
| 15 | TOTAL.04 — Szkolenia: opis narracyjny + wartość |
| 16 | TOTAL.05 — Gwarancja/Bufor: opis narracyjny + wartość |
| 17 | TOTAL.06 — Narzędzia/Licencje: opis narracyjny + wartość |
| 19 | **Efekty biznesowe** |
| 20 | Przyspieszenie Time-to-Market: ... |
| 21 | Redukcja długu technicznego: ... |
| 22 | Retencja wiedzy: ... |
| 23 | Skalowanie kompetencji: ... |
| 24 | Bezpieczeństwo danych: ... |
| 26 | **Model dostawy** |
| 27 | Cloud Native / Private Cloud / On-Premise opcje |
| 28 | Pair programming vs praca własna — podział |
| 30 | **Bottega — competence** |
| 31 | 15 lat, 78 trenerów, lista kluczowych klientów |

---

## Status quo — co już jest w Kosztorys.xlsx

| Mocne strony | Braki |
|---|---|
| Szczegółowy podział na BU | Brak executive summary |
| Konkretne pozycje kosztowe z kodami | Brak narracji biznesowej |
| Podział na obszary (IK, EK, TL, REF) | Brak powiązania pozycji z efektami |
| Ceny netto + sumy | Brak opisu podejścia/metodologii |
| Oddzielne arkusze per obszar | Brak sekcji o Bottega jako firmie |
| Opisy zadań w komórkach C | Brak wytłumaczenia "co to zmieni dla nas" |

---

## Kolejne kroki (do uzgodnienia)

1. Zaakceptować zakres zmian (arkusz + kolumny)
2. Przygotować treści opisowe dla każdej sekcji
3. Wdrożyć do pliku XLSX (Python + openpyxl)
4. Review treści z zespołem ofertowym
