# Ideal Customer Profile — AWSM

*Last updated: 2026-07-14*

---

## Verticals Overview

| Wymiar | 🏛️ Ubezpieczenia | 🚀 Fintech / Insurtech | 💳 Usługi Finansowe | ⚙️ ERP / SAP |
|--------|------------------|----------------------|-------------------|-------------|
| **Regulacje** | VAIT (BaFin), Solvency II | BaFin, BSI, GDPR (lżejsze) | MaRisk (BaFin), KWG, GDPR | ISO, branżowe (brak BaFin) |
| **Core system** | msg nexinsure, msg life | Własne platformy cloud | Core banking (SAP, własne) | SAP ECC / S/4HANA |
| **Stack dominujący** | Java, Angular, Oracle | Node.js, Python, AWS/Azure | Java, .NET, mainframe COBOL | ABAP, SAPUI5, Fiori, Java |
| **Decyzja** | 3-6 mies., konserwatywna | 1-3 mies., agile | 3-6 mies., formalna | 2-4 mies., techniczna |
| **Główny trigger** | Compliance + nie mogę zatrudnić | Skalowanie produktu, time-to-market | Digital transformation, cost cutting | SAP S/4HANA migration |
| **Klienci ref. AWSM** | msg, STEKON, Munich Re, Concordia | ottonova | — | — |

---

# ICP 1: Ubezpieczenia (Insurance)

*Primary and reinsurance — główny rynek AWSM od 16 lat.*

### Firmografia

| Cecha | Opis |
|-------|------|
| **Wielkość** | 200-5000+ FTEs |
| **Struktura** | AG, GmbH, VVaG (mutual) — regulowane przez BaFin |
| **Lokalizacja** | Bawaria, Nadrenia Północna-Westfalia, Hesja, Hamburg |
| **Roczny budżet IT** | €5-50M+ |
| **Developerzy in-house** | 10-80, potrzebują 3-15 dodatkowych |
| **Dojrzałość outsourcingowa** | Wysoka — 74% już outsourcuje; mają procedury VAIT |

### Technografia

| Obszar | Stack / Standard |
|--------|-----------------|
| **Języki / frameworki** | Java (dominant), Angular, Spring, J2EE, OR-Mapping |
| **Bazy danych** | Oracle, DB2, PostgreSQL |
| **Platformy core** | msg nexinsure, msg life |
| **Compliance** | VAIT (BaFin), Solvency II, BSI Grundschutz, ISO 27001, IDD |
| **Chmura** | Azure (częsty wybór ubezpieczycieli), trend: powolna migracja |
| **Metodyki** | Scrum, SAFe, waterfall dla projektów regulowanych |

### JTBD

**Functional:** "Scale my dev team when I can't hire locally." / "Stay compliant with BaFin/VAIT while outsourcing."
**Emotional:** "Trust that communication won't be a problem — we've been burned before."
**Social:** "Show the Vorstand I made a safe, cost-effective sourcing decision."

### Buying Triggers

| Trigger | Pilność |
|---------|---------|
| Nie mogę obsadzić roli Java >3 mies. — rekrutacja w DE trwa 4-6 mies. | 🔴 Wysoka |
| Nowy projekt (np. wymiana systemu polisowego, cloud migration) | 🔴 Wysoka |
| Deadline regulacyjny (VAIT, Solvency II, EIOPA) | 🔴 Wysoka |
| Presja CFO na redukcję kosztów IT | 🟡 Średnia |
| Nieudany outsourcing wcześniej (UA, IN — komunikacja nie działała) | 🟡 Średnia |

### Personas

**Klaus — CTO**
- Firma: 200-2000 FTEs, ubezpieczenia
- Trigger: nie może znaleźć 5 Java devów od roku
- Ból: "Agencje nie dostarczają. Projekty stoją."
- Obawa: "Jak polski zespół ogarnie nasze regulacje i legacy?"
- Kanały: LinkedIn, Xing, Clutch, konferencje IT in Insurance

**Markus — IT Director**
- Ból: "Spędzam 50% czasu na rekrutacji, nie na zarządzaniu"
- Chce: "Niech ktoś weźmie odpowiedzialność za ludzi, ja się skupię na architekturze"
- Obawa: "Będę musiał micro-managować polski zespół?"

**Johann — Technical Project Lead (msg/STEKON)**
- Ból: backlog na 6 sprintów, zespół nie nadąża
- Chce: ludzi zrozumiejących domain insurance bez 3-mies. ramp-upu
- Kanały: msg partner network, LinkedIn

---

# ICP 2: Fintech / Insurtech

*Młodsi gracze, cloud-native, szybsze decyzje. Ottonova to referencja AWSM w tym segmencie.*

### Firmografia

| Cecha | Opis |
|-------|------|
| **Wielkość** | 20-200 FTEs (startupy scale-up do Series C) |
| **Struktura** | GmbH, AG (często backed VC) |
| **Lokalizacja** | Berlin, Monachium, Hamburg — hubs fintechowe |
| **Roczny budżet IT** | €1-10M |
| **Developerzy in-house** | 5-30, potrzebują 2-10 dodatkowych |
| **Dojrzałość outsourcingowa** | Średnia — znają model, mniej formalności |

### Technografia

| Obszar | Stack / Standard |
|--------|-----------------|
| **Języki / frameworki** | Node.js, Python, Java, React, TypeScript |
| **Bazy danych** | PostgreSQL, MongoDB, AWS DynamoDB |
| **Infrastruktura** | Cloud-native (AWS, Azure, GCP) |
| **Compliance** | GDPR, BaFin (lżej niż insurance), PCI DSS (płatności) |
| **DevOps** | Docker, Kubernetes, GitHub Actions, CI/CD pełne |
| **Metodyki** | Scrum, Shape Up, Lean |

### JTBD

**Functional:** "Ship features faster without hiring 10 people in Berlin."
**Emotional:** "Stay lean — don't become a hiring machine before product-market fit."
**Social:** "Show investors capital-efficient growth (less on payroll, more on dev)."

### Buying Triggers

| Trigger | Pilność |
|---------|---------|
| Series A/B funding — need to scale dev team 2x | 🔴 Wysoka |
| Nowa funkcja / vertical — time-to-market krytyczny | 🔴 Wysoka |
| Berlin hiring impossible (5 os. w 6 mies. = nie do znalezienia) | 🟡 Średnia |
| Presja burn rate — CFO każe ograniczać koszty | 🟡 Średnia |

### Persona

**Lena — CTO fintechu (30-100 FTEs)**
- Trigger: dostała round, ma 12 mies. na delivery, potrzebuje 5 devów
- Ból: "W Berlinie nie ma seniorów, a agencje chcą €100-130/h"
- Chce: "Polski zespół, €50-70/h, komunikacja po angielsku, start w 3 tygodnie"
- Obawa: "Czy oni ogarniają compliance? PCI DSS? BaFin?"
- Kanały: LinkedIn, Twitter/X, Product Hunt, Hacker News, podcasty founderskie
- Różnica vs. insurance: mniej formalności, szybsza decyzja, angielski > niemiecki

---

# ICP 3: Usługi Finansowe (Financial Services / Banking)

*Banki, kasy oszczędnościowe, asset managers — regulowane przez BaFin (MaRisk, KWG).*

### Firmografia

| Cecha | Opis |
|-------|------|
| **Wielkość** | 500-10000+ FTEs |
| **Struktura** | AG, Sparkasse, Genossenschaftsbank — regulowane przez BaFin |
| **Lokalizacja** | Frankfurt, Berlin, Hamburg, Düsseldorf, Monachium |
| **Roczny budżet IT** | €10-200M+ |
| **Developerzy in-house** | 30-200+, potrzebują 5-20+ dodatkowych |
| **Dojrzałość outsourcingowa** | Wysoka — banki outsourcują od dekad |

### Technografia

| Obszar | Stack / Standard |
|--------|-----------------|
| **Języki / frameworki** | Java, .NET, COBOL (mainframe), Angular, React |
| **Bazy danych** | Oracle, DB2, SQL Server |
| **Platformy core** | SAP Banking, własne systemy transakcyjne, mainframe |
| **Compliance** | MaRisk (BaFin), KWG, GDPR, PCI DSS, ISO 27001 |
| **Chmura** | Ostrożna — głównie hybrid cloud, private cloud (regulacje) |
| **Metodyki** | SAFe, waterfall, ITIL |

### JTBD

**Functional:** "Execute digital transformation while keeping the lights on."
**Emotional:** "Don't let legacy tech debt kill our ability to compete with fintechs."
**Social:** "Be seen as modernizing — not just cutting costs."

### Buying Triggers

| Trigger | Pilność |
|---------|---------|
| Digital transformation program — wymiana core banking | 🔴 Wysoka |
| Presja konkurencyjna (fintechy, neobanki) | 🟡 Średnia |
| MaRisk / compliance — potrzeba devów do projektów regulacyjnych | 🟡 Średnia |
| M&A — integracja systemów dwóch banków | 🟡 Średnia |

### Persona

**Thomas — Head of IT (Bank, 1000+ FTEs)**
- Firma: tradycyjny bank, legacy mainframe, powolne zmiany
- Trigger: zarząd każe zrobić digital transformation, ale IT walczy z długiem technicznym
- Ból: "Mamy 40-letnie systemy COBOL, a młode devy nie chcą tego dotykać"
- Chce: "Kogoś, kto ogarnia zarówno nowe (Java/cloud) jak i legacy"
- Obawa: "Outsourcing do Polski — czy BaFin to zaakceptuje? Czy dane klientów będą bezpieczne?"
- Kanały: konferencje banking IT (Frankfurt), CIO circles, LinkedIn
- Różnica vs. insurance: większe legacy (COBOL, mainframe), szerszy stack, więcej compliance

---

# ICP 4: ERP / SAP

*Niemieckie Mittelstand z SAP ECC, które muszą migrować do S/4HANA. Duży, niezagospodarowany rynek.*

### Firmografia

| Cecha | Opis |
|-------|------|
| **Wielkość** | 50-2000 FTEs (Mittelstand) |
| **Struktura** | GmbH, AG — prywatne lub family-owned |
| **Lokalizacja** | Całe DACH — głównie Badenia-Wirtembergia, Bawaria, NRW |
| **Roczny budżet IT** | €1-15M |
| **Developerzy in-house** | 0-20 (często brak własnych SAP devów) |
| **Dojrzałość outsourcingowa** | Średnia — znają model z produkcji, niekoniecznie z IT |

### Technografia

| Obszar | Stack / Standard |
|--------|-----------------|
| **Platforma** | SAP ECC 6.0 → S/4HANA migration |
| **Języki / frameworki** | ABAP, SAPUI5, Fiori, Java (SAP BTP) |
| **Bazy danych** | HANA (docelowo), Oracle, SQL Server (przed migracją) |
| **Compliance** | Branżowe (produkcja, logistyka), GDPR, ISO |
| **Dostawcy SAP** | SAP itself, IBM, Accenture, Itelence, i mniejsi partnerzy |
| **Wyzwanie** | SAP kończy support ECC 6.0 w 2027 — deadline migration |

### JTBD

**Functional:** "Migrate from SAP ECC to S/4HANA before 2027 deadline."
**Emotional:** "Stop worrying about unsupported legacy ERP while running the business."
**Social:** "Show the Geschäftsführung we're managing the S/4HANA transition responsibly."

### Buying Triggers

| Trigger | Pilność |
|---------|---------|
| SAP kończy support ECC 6.0 w 2027 — S/4HANA migration | 🔴 Wysoka |
| Obecny partner SAP nie daje rady — szukają alternatywy | 🟡 Średnia |
| Potrzeba ABAP/Fiori devów, ale nie ma ich na rynku DE | 🟡 Średnia |
| Nowa funkcjonalność (e-invoicing, compliance, AI w ERP) | 🟡 Średnia |
| Presja audytora / biegłego rewidenta | 🟡 Średnia |

### Persona

**Friedrich — IT Leiter (Mittelstand, 200-1000 FTEs)**
- Firma: producent maszyn / części, SAP ECC od 15 lat
- Trigger: SAP kończy support ECC 2027; musi migrować do S/4HANA, ale nie ma ABAP devów
- Ból: "Accenture chce €200/h za ABAP developera. Nie stać nas."
- Chce: "Polski zespół ABAP/Fiori za €50-70/h, który ogarnia S/4HANA"
- Obawa: "Czy polscy devowie znają SAP? ABAP? Fiori? Czy będą rozumieć nasze procesy biznesowe?"
- Kanały: SAP User Group (DSAG), LinkedIn, polecenia od msg/STEKON
- Różnica vs. insurance: brak BaFin, większy focus na SAP, mniejsze firmy, krótsza decyzja

### Rynek SAP w Polsce

Polska ma jeden z najgłębszych talent poolów SAP w Europie:
- Liczne centra SAP (IBM, Accenture, Capgemini, SAP Labs)
- ABAP, SAPUI5/Fiori, SAP BTP, SAP S/4HANA — dostępne kompetencje
- Stawki ABAP: €40-70/h vs. €100-200/h w DE
- S/4HANA migration = największy projekt IT w historii Mittelstand

---

# Shared: Buying Process

### Mapa interesariuszy (cross-vertical)

| Rola | Wpływ | Co ich interesuje |
|------|-------|-------------------|
| **CTO / VP Engineering** | Ocenia, rekomenduje | Jakość kodu, dopasowanie stacku, integracja |
| **IT Director / Head of Dev** | Kieruje wyborem | Szybkość reakcji, komunikacja, daily mgmt |
| **Managing Director / CEO** | Akceptuje | Trust, partnership, reference clients |
| **Financial Director / CFO** | Zatwierdza budżet | Koszt vs. DE, ROI, przewidywalność |
| **Compliance / Data Privacy** | Veto | Regulacje (VAIT, MaRisk, GDPR), data protection |
| **Information Security Officer** | Veto | ISO 27001, BSI, Bezpieczeństwo danych |
| **Technical Project Lead** | Użytkownik codzienny | Szybkie dopasowanie kandydatów, kompetencje |

### Przebieg procesu (cross-vertical)

| Faza | Ubezpieczenia | Fintech | Usługi Finansowe | ERP/SAP |
|------|--------------|---------|-----------------|---------|
| **Research** | Clutch, msg network, LinkedIn | LinkedIn, Twitter, YC/VC network | Clutch, Gartner, CIO circles | DSAG, SAP partner network |
| **Ewaluacja** | 3 reference calls + compliance review | 1-2 referencje, tech screening | Formalny RFP, compliance due diligence | Tech assessment ABAP/Fiori |
| **Decyzja** | Vorstand + Compliance approval | CTO solo lub z CEO | IT + Compliance + Zarząd | IT Leiter + GF |
| **Timeline** | 3-6 mies. | 1-3 mies. | 3-6 mies. | 2-4 mies. |
| **Pilot** | 1-2 devów, 3 mies. trial | 2-3 devów, 1-2 sprinty | 2-3 devów, 3-6 mies. | 1-2 ABAP devów, 3 mies. |

### Kryteria wyboru (ważność)

| Kryterium | Ubezp. | Fintech | Fin. Serv. | ERP/SAP |
|-----------|--------|---------|-----------|---------|
| Cena / value | #1 | #1 | #2 | #1 |
| Referencje / trust | #2 | #3 | #1 | #2 |
| Szybkość dostarczenia | #3 | #2 | #4 | #3 |
| Komunikacja (DE/EN) | #4 | #1 (EN) | #3 (DE) | #3 (DE) |
| Znajomość branży | #5 | #4 | #5 | #5 |
| Compliance | Bariera | Niska | Bariera | Niska |

---

# Shared: Market Context 2026

| Czynnik | Ubezpieczenia | Fintech | Usługi Finansowe | ERP/SAP |
|---------|--------------|---------|-----------------|-------------|
| **Popyt na devów** | 137k otwartych ról IT w DE — dotyczy wszystkich verticali | | | |
| **Polski talent pool** | 400k developerów, 60k firm IT, wysoka jakość (Top 3 world coding) | | | |
| **Oszczędność kosztów** | Nearshore PL = 35-50% kosztów DE | | | |
| **Rynek nasycony?** | 74% outsourcuje, tylko 6% planuje *nowy* sourcing | Rynek młody, dużo nowych kontraktów | Banki outsourcują od dekad — zmiana partnerów | S/4HANA tworzy NOWY popyt (deadline 2027) |
| **Regulacje** | VAIT — bariera, ale AWSM umie | Lżejsze — zaleta | MaRisk — podobnie do VAIT | Brak BaFin — łatwiej |
| **Trendy** | Cloud migration, AI w insurance | Scale-up, funding rounds | Digital transformation, open banking | SAP ECC → S/4HANA, AI w ERP |

---

# Shared: Rekomendacje dla marketingu i sprzedaży

| # | Rekomendacja | Dla kogo |
|---|-------------|----------|
| 1 | **Targetuj firmy, które już outsourcują** — nie edukuj, tylko pokaż różnicę | Ubezpieczenia, Fin. Serv. |
| 2 | **S/4HANA migration wave** — największy organiczny popyt w historii Mittelstand. Przygotuj ofertę SAP/ABAP/Fiori | ERP/SAP |
| 3 | **Gotowy pakiet compliance** — VAIT / MaRisk dokumentacja dla BaFin. Usuwa barierę wejścia | Ubezpieczenia, Fin. Serv. |
| 4 | **Case studies z liczbami** — "4 Java devów w 3 tyg. vs. 6 mies. w DE = €XXXk savings" | Wszystkie |
| 5 | **Pricing:** "35-50% taniej niż niemiecki developer" — język CFO | Wszystkie |
| 6 | **Referencje msg/STEKON** — 7+ lat relacji. Używaj w każdym materiale | Ubezpieczenia, ERP/SAP |
| 7 | **Content dla fintechów** — angielski, nie niemiecki. Rozmawiaj o scale, nie o compliance | Fintech |
| 8 | **msg partner network** — kluczowy kanał dystrybucji do ubezpieczeń | Ubezpieczenia |
| 9 | **Wzmocnij kompetencje cloud** (Azure) — trend we wszystkich verticalach | Wszystkie |
| 10 | **Target trigger "nie mogę zatrudnić od 3+ mies."** — najsilniejszy pain point we wszystkich verticalach | Wszystkie |
