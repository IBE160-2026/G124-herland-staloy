# Tilbakemelding på product brief

| | |
|---|---|
| **Gruppe** | G124 – G124-herland-staloy |
| **Product brief** | `product brief.md` (commit `e40e38d`) |
| **Tilbakemelding fra** | Faglærer i IBE160 (utarbeidet med KI-støtte) |
| **Dato** | 2026-10-06 |

Vurdert fil: `product brief.md` i repoets rot, som er den eneste briefen. Det finnes ennå ikke PRD, arkitektur eller epics. Tips: gi gjerne fila et navn uten mellomrom, for eksempel `product-brief.md`, siden mellomrom i filnavn ofte skaper problemer i kommandolinjen og lenker.

## Samlet vurdering

- **Godt utgangspunkt med justeringer.** Gruppen kan gå videre og innarbeide punktene under.

**Det som er bra:**

1. Dere har gjort et svært viktig valg riktig: konsekvensanalysen skal være «programmeringsbasert … ikke på at KI gjetter hvilke aktiviteter som påvirkes», mens KI brukes til å forklare og utforske tiltak. Det gjør kjernen kontrollerbar og testbar.
2. Avgrensningen er moden. Dere fokuserer på én beslutningssituasjon («Hva skjer med prosjektet dersom en viktig forutsetning endres?»), og Out of scope-listen er lang og konkret (økonomi, kontrakter, BIM, ERP, automatiske beslutninger). Planen om intervjuer med prosjektledere gir et godt faglig grunnlag og stoff til refleksjonsrapporten.

**De viktigste endringene:**

1. Skriv ned reglene for konsekvensanalysen. Hvordan forplanter en forsinkelse seg? Bestem for eksempel at v1 bare har avhengigheten «B starter når A er ferdig», og at sluttidspunktet beregnes ved å gå gjennom aktivitetene i rekkefølge (kritisk linje). Lag to–tre små eksempelplaner med 8–15 aktiviteter der dere har regnet ut fasit for hånd. Det blir både krav og tester.
2. Bestem hvordan tiltakene påvirker planen. «Øke bemanningen», «endre rekkefølgen» og «akseptere forsinkelsen» må få en konkret virkning i beregningen, for eksempel at brukeren angir ny varighet for en aktivitet, eller flytter en avhengighet. Ellers blir scenariosammenligningen bare KI-tekst, og den kan dere ikke kontrollere.
3. Ikke la intervjuene blokkere utviklingen. Briefen sier flere steder at variabler og forskjeller «skal avklares gjennom intervjuer». Velg et standardsett med variabler nå (aktivitet, varighet, avhengighet, status, forsinkelse, milepæl), og bruk intervjuene til å justere senere. Gjør også suksesskriteriet om «praktisk relevans» konkret, for eksempel at minst to prosjektledere prøver et testscenario og gir tilbakemelding.

## Vanskelighetsgrad og gjennomførbarhet

### Vurdert vanskelighetsgrad

- **Vanskelig**

**Sammenlignbart med:** 3) KI-styrt simulering av prosjektledelse (byggeprosjekt) (vanskelig). Briefen bygger på dette forslaget, men avgrenser det til fremdrift og tiltak ved endringer, uten kost, risiko og ressursallokering. Avgrensningen gjør prosjektet mer overkommelig, men domenelogikken må fortsatt være riktig, og det holder det på vanskelig nivå.

**Begrunnelse:**

| Faktor | Nivå (lav / middels / høy) | Kommentar |
|---|---|---|
| Domenelogikk – hvor mange og hvor kompliserte regler og beregninger må stemme? | Høy | Forplantning av forsinkelser gjennom avhengigheter, nytt sluttidspunkt, milepæler og virkning av tiltak. Må være faglig riktig. |
| Datamodell – antall entiteter og relasjoner mellom dem | Middels | Prosjekt, aktivitet, avhengighet, milepæl, endring og scenario. Avhengighetene danner et nettverk. |
| Brukere, roller og innlogging | Lav | Én rolle (prosjektleder). Innlogging er ikke nevnt og trengs neppe i v1. |
| KI-funksjonalitet i appen, f.eks. kall til språkmodell, prompts i koden og håndtering av usikre svar | Middels | KI forklarer resultater og hjelper med å vurdere tiltak, basert på beregnede data. Godt avgrenset. |
| Integrasjoner og eksterne tjenester, f.eks. API-er, betaling og e-post | Lav | Bare språkmodell-API. Integrasjoner er utelatt. |
| Sanntid, samtidighet eller flere brukere som påvirker hverandre | Lav | Ingen. |
| Filhåndtering, f.eks. opplasting, PDF-lesing og eksport | Lav | Ingen er beskrevet. Planer kan legges inn manuelt eller lastes fra eksempeldata. |
| Sikkerhet og personvern | Lav | Fiktive eller anonymiserte prosjektdata. Pass på at eventuell data fra intervjuer ikke legges i repoet. |

**Hva vanskelighetsgraden betyr for dere:**

- _Vanskelig:_ Et vanskelig prosjekt gir større mulighet for toppkarakter, men også større risiko. Definer en minimal versjon som sikkert kan bli ferdig, og legg resten i tydelige trinn etterpå.

### Gjennomførbarhet med BMAD og Claude Code

| Spørsmål | Vurdering (OK / risiko / stor risiko) | Kommentar |
|---|---|---|
| **Tid og omfang** – kan v1 realistisk bli ferdig og stabil i løpet av semesteret, med tid til flere iterasjoner? | Risiko | De åtte stegene i v1 henger godt sammen og er overkommelige med forenklet plan og én avhengighetstype. Intervjuer og justeringer tar også tid. |
| **BMAD-flyten** – er briefen konkret nok til at PRD, arkitektur og stories kan lages uten store hull, og blir det overkommelig mange stories? | Risiko | Flyten er tydelig, men beregningsreglene og tiltakenes virkning mangler. Uten dem vil KI fylle hullene i PRD-en. |
| **Egnet for Claude Code** – bruker løsningen en vanlig, godt dokumentert teknologistakk som Claude Code håndterer godt, eller krever den nisjeteknologi, spesialmaskinvare eller mye manuell konfigurasjon? | OK | Webapp med tabeller, en enkel tidslinje og beregninger er godt egnet. Kritisk linje er en kjent algoritme som Claude Code kan implementere. |
| **Kontroll på KI-ens arbeid** – kan gruppen selv avgjøre om koden gjør det riktige? Krever domenet kunnskap gruppen ikke har, f.eks. avanserte beregninger eller fagregler, så er det vanskelig å kvalitetssikre. | Risiko | Mulig, men bare hvis dere har håndregnede eksempler. Bruk intervjuene til å sjekke at eksemplene er realistiske. |
| **Testbarhet** – finnes det tydelige regler og forventede resultater som tester kan skrives mot? | Risiko | «Identifisere relevante berørte aktiviteter i definerte testscenarioer» er et godt utgangspunkt. Lag scenarioene med fasit, så blir dette en styrke. |
| **Kjørbar for sensor** – kan appen kjøres lokalt etter README, uten gruppens nøkler, betalte kontoer eller egen infrastruktur? | Risiko | Beregningen kan kjøre uten KI. Planlegg at appen viser beregnede resultater også uten nøkkel, og at KI-forklaringen har en testmodus. |
| **Avhengigheter og kostnader** – krever løsningen betalte API-er, f.eks. språkmodeller, og finnes det en plan for kostnad, testmodus eller mock-data? | Risiko | Krever språkmodell for forklaring og scenarioanalyse. Ingen plan for nøkkel og kostnad ennå. |

**Konklusjon om gjennomførbarhet:**

- **Gjennomførbart med justert omfang.** Se forslagene under.

**Forslag til justering av omfang eller vanskelighetsgrad:**

1. V1: én avhengighetstype (slutt-til-start), eksempelprosjekter med 8–15 aktiviteter, registrering av én forsinkelse, beregning av berørte aktiviteter og nytt sluttidspunkt, og KI-forklaring av resultatet. La «opprette prosjekt» være valgfritt, og start med å velge blant ferdige eksempelprosjekter.
2. Tiltak og scenariosammenligning i neste trinn, der hvert tiltak er en konkret endring i planen (ny varighet, fjernet eller flyttet avhengighet) som beregnes på nytt, og KI forklarer forskjellene mellom scenarioene.

## Hvorfor product brief er viktig for mappen

Product brief er utgangspunktet for PRD, arkitektur, stories og til slutt koden. Del 1 av mappen vurderes blant annet på om sensor kan følge en sporbar vei fra plan til ferdig app. Den vurderes også på om appen gjør det dere har beskrevet, om den er testet, om den er godt designet, og om den kan kjøres etter README. Et uklart, for stort eller for lite brief gjør alt dette vanskeligere senere. Det er mye enklere å rette nå enn sent i semesteret.

## 1. Gjennomgang av briefens deler

| Del av brief | Status | Kommentar |
|---|---|---|
| Executive Summary – er det klart hva appen er, og hvilket problem den løser? | OK | Klart: beslutningsstøtte for prosjektledere når fremdriftsplanen endres, med en tydelig problemstilling. |
| The Problem – er problemet konkret, med reelle situasjoner og brukere? | Juster | Godt beskrevet, men generelt. Legg gjerne til et konkret eksempel, for eksempel en forsinket grunnmur som skyver tømrer, tak og elektro. |
| The Solution – beskriver løsningen brukeropplevelsen, ikke bare teknologi? | Juster | Skillet mellom beregning og KI er godt beskrevet. Beskriv også hva prosjektlederen ser på skjermen, og hvordan et tiltak legges inn og virker. |
| What Makes This Different – er vurderingen ærlig og realistisk? | OK | Ærlig: dere konkurrerer ikke på bredde, men på én beslutningssituasjon. |
| Who This Serves – er primærbrukerne tydelige, og vet vi hva de trenger? | OK | Prosjektledere i bygg og anlegg er tydelig, og intervjuplanen viser at dere vil forstå behovene. |
| Success Criteria – kan kriteriene faktisk sjekkes eller testes? | Juster | De fleste er testbare med definerte scenarioer. Gjør «praktisk relevans» konkret med antall testpersoner og hva de skal vurdere. |
| Scope – er det klart hva som er med i første versjon, og hva som ikke er det? | OK | Tydelige åtte steg og en svært god Out of scope-liste. |
| Vision – henger visjonen sammen med resten uten å blåse opp omfanget? | OK | Nøktern, og studentprosjektets avgrensning er tydelig. |

## 2. Utgangspunkt for del 1 av mappen

Punktene følger kriteriene i sensorveiledningen for del 1. Vektene i parentes viser hvor mye hvert kriterium teller i del 1.

| Kriterium i del 1 | Hva briefen bør legge til rette for | Status | Kommentar |
|---|---|---|---|
| **1. Prosess og KI-styring** (30 %) | Brief som er presis nok til at PRD og stories kan bygges direkte på den, slik at krav kan spores fra brief til kode. | Juster | Godt grunnlag, og briefen er allerede revidert én gang. Skriv inn beregningsreglene før PRD, og lagre promptene. Dokumenter også hva intervjuene endrer. |
| **2. Funksjonalitet og omfang** (20 %) | Realistisk omfang for gruppen og semesteret: en tydelig kjerneflyt som kan bli ferdig og stabil, og nok innhold til å vise reell funksjonalitet. | OK | Tydelig kjerneflyt med godt nok innhold, særlig med trinnvis utbygging. |
| **3. Kvalitetssikring og testing** (15 %) | Suksesskriterier og funksjoner som er konkrete nok til å bli testtilfeller. | Juster | Testscenarioer er planlagt. Lag dem med håndregnet fasit, så kan de bli automatiske tester av beregningen. |
| **4. Design og brukeropplevelse** (10 %) | Tydelige brukere og brukssituasjoner som designet kan bygges rundt, gjerne med de viktigste skjermbildene eller flytene skissert. | Juster | Tydelig bruker. Skisser fremdriftsplanen (tabell eller enkel tidslinje), hvordan berørte aktiviteter markeres, og hvordan scenarioer sammenlignes. |
| **5. Kodekvalitet og arkitektur** (10 %) | Teknologivalg som er begrunnet og ikke mer komplekse enn appen trenger. | OK | Ingen teknologi valgt ennå. Hold beregningslogikken i en egen, testbar del av koden, adskilt fra KI-kallene. |
| **6. README og kjørbarhet** (10 %) | Løsning som andre kan kjøre lokalt uten betalte kontoer, og uten tilgang til gruppens egne tjenester og nøkler. | Juster | Planlegg eksempelprosjekter som følger med, og testmodus for KI-forklaringen. |
| **7. Ryddighet i repoet** (5 %) | En plan for hvor hemmeligheter, testdata og dokumentasjon skal ligge. | Juster | Gi briefen et filnavn uten mellomrom, legg eksempelplaner i egen mappe, hold API-nøkler i `.env` utenfor Git, og ikke legg intervjunotater med personopplysninger i repoet. |

## 3. Neste steg for gruppen

1. Skriv ned reglene for hvordan forsinkelser forplanter seg, og lag to–tre eksempelplaner med håndregnet fasit.
2. Bestem hvordan hvert tiltak endrer planen i beregningen, og velg et standardsett med variabler nå.
3. Gjennomfør intervjuene parallelt med PRD-arbeidet, og bruk resultatene til å justere, ikke til å vente.

Oppdater product brief i repoet når dere har gjort endringene, slik at historikken viser hvordan planen utviklet seg. Det er en del av prosessen sensor ser etter.
