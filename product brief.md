# Product Brief: AI Project Planner

## Executive Summary 
AI Project Planner er en nettbasert prototype av et KI-basert beslutningsstøtteverktøy for prosjektledere i bygg- og anleggsbransjen.Verktøyet skal hjelpe prosjektledere med å forstå hvordan endringer i en fremdriftsplan kan påvirke resten av prosjektet, og utforske ulike tiltak før en beslutning tas. Løsningen kombinerer programmeringsbasert analyse av aktiviteter og avhengigheter med KI-støttet forklaring og scenarioanalyse.
Målet er ikke å erstatte prosjektlederens vurderinger, men å gjøre det enklere å få oversikt over konsekvenser og sammenligne mulige tiltak.

**Problemstilling:** Hvordan kan KI brukes til å analysere endringer i en fremdriftsplan og gi prosjektledere beslutningsstøtte om mulige konsekvenser og tiltak?

## The Problem
Bygg- og anleggsprosjekter kan variere betydelig i størrelse, type og kompleksitet. Fremdriftsplaner kan inneholde mange aktiviteter som er avhengige av hverandre. Når en aktivitet blir forsinket eller en annen forutsetning i prosjektet endres, må prosjektlederen vurdere hvordan dette kan påvirke etterfølgende aktiviteter og prosjektets sluttidspunkt. Noen aktiviteter kan gjennomføres parallelt, andre kan omorganiseres, og ressurser kan eventuelt flyttes for å redusere konsekvensene. Det kan derfor være krevende å raskt få oversikt over hvilke aktiviteter som påvirkes, hvor store konsekvensene kan bli og hvilke tiltak som kan være aktuelle. Idag støttes slike vurderinger blant annet av prosjektstyringsverktøy, regneark og prosjektlederens egen erfaring og kompetanse. Intervjuer med prosjektledere skal brukes til å undersøke hvordan dette faktisk gjøres i praksis, og hvor det finnes et reelt behov for beslutningsstøtte.

## The Solution
AI Project Planner skal la prosjektlederen arbeide med en forenklet fremdriftsplan som inneholder et begrenset antall sentrale variabler, for eksempel:

- aktiviteter
- planlagt start og slutt
- varighet
- avhengigheter mellom aktiviteter
- status
- forsinkelser
- milepæler

Når en endring oppstår, skal systemet analysere hvordan denne kan påvirke fremdriftsplanen. Løsningen består av to hoveddeler.

### Programmeringsbasert konsekvensanalyse
Systemet skal bruke definerte regler og prosjektdata til å beregne hvilke aktiviteter som kan bli påvirket av en endring, og hvordan en endring kan forplante seg gjennom fremdriftsplanen.Denne delen skal baseres på prosjektdata og programmeringslogikk, ikke på at KI gjetter hvilke aktiviteter som påvirkes.

### KI-støttet scenarioanalyse
KI skal bruke prosjektkonteksten og resultatene fra konsekvensanalysen til å forklare situasjonen, identifisere relevante vurderinger og hjelpe prosjektlederen med å utforske ulike tiltak. Dersom en aktivitet for eksempel blir forsinket med ti dager, kan prosjektlederen teste ulike alternativer, som å øke bemanningen, endre rekkefølgen på aktiviteter eller akseptere forsinkelsen.Systemet skal deretter kunne vise og forklare mulige konsekvenser og avveininger ved de ulike alternativene. KI skal gi beslutningsstøtte og ikke ta beslutninger på vegne av prosjektlederen.

## What Makes This Different?
Prosjektet skal ikke forsøke å konkurrere med etablerte systemer innen bygg og anlegg på bredden av funksjonalitet.I stedet fokuserer prototypen på en konkret beslutningssituasjon:

> **Hva skjer med prosjektet dersom en viktig forutsetning endres, og hvilke tiltak kan prosjektlederen vurdere?**
Verdien ligger i kombinasjonen av:
1. strukturert fremdriftsplandata
2. programmeringsbasert analyse av aktiviteter og avhengigheter
3. KI-støttet forklaring og scenarioanalyse
4. mulighet til å utforske og sammenligne alternative tiltak

Den konkrete forskjellen mellom eksisterende verktøy og den foreslåtte løsningen skal undersøkes nærmere gjennom intervjuer med prosjektledere og relevante personer innen KI og digitalisering.

## Hvem løsningen er for
Den primære målgruppen er prosjektledere i bygg- og anleggsbransjen som har ansvar for planlegging og oppfølging av prosjektets fremdrift.Prosjektet skal utvikles med innspill fra prosjektledere som arbeider med ulike typer og størrelser på prosjekter. Dette er viktig fordi hvilke faktorer som er relevante i et mindre byggeprosjekt, kan være annerledes enn i et større og mer komplekst prosjekt.

Intervjuene skal blant annet undersøke:
- hvordan prosjektledere arbeider med fremdriftsplaner i dag
- hvordan de vurderer konsekvensene av forsinkelser
- hvilke avhengigheter som er viktigst
- hvilke faktorer som påvirker valg av tiltak
- hvordan behovene varierer mellom ulike prosjektstørrelser og prosjekttyper
- hvor KI kan gi nyttig beslutningsstøtte

## Success Criteria
Prototypen skal anses som vellykket dersom:
- en prosjektleder kan opprette eller velge en forenklet fremdriftsplan
- systemet kan analysere en konkret endring i fremdriftsplanen
- systemet kan identifisere relevante berørte aktiviteter i definerte testscenarioer
- systemet kan forklare mulige konsekvenser på en forståelig måte
- brukeren kan teste minst to alternative tiltak
- systemet kan sammenligne de ulike scenarioene
- prosjektledere opplever at prototypen har praktisk relevans som beslutningsstøtte

Løsningen skal testes gjennom forhåndsdefinerte scenarioer og tilbakemeldinger fra prosjektledere.

## Scope

### In scope for the first version

Minimumsversjonen skal gjøre det mulig å:

1. opprette eller velge et prosjekt
2. se en forenklet fremdriftsplan
3. registrere en endring eller forsinkelse
4. beregne hvilke aktiviteter som kan bli påvirket
5. få en KI-støttet analyse
6. velge et mulig tiltak
7. generere en scenarioanalyse
8. sammenligne minst to mulige tiltak

### Out of scope for the first version

Prototypen skal ikke forsøke å bli et komplett prosjektstyringssystem.
Følgende er derfor utenfor prosjektets omfang:

- full økonomistyring
- fakturering
- kontraktsadministrasjon
- juridiske vurderinger
- BIM-integrasjon
- automatisk innhenting av data fra byggeplass
- integrasjon med ERP- eller eksisterende prosjektstyringssystemer
- automatisk kommunikasjon med entreprenører og andre aktører
- automatiske beslutninger
- ressursallokering på tvers av flere prosjekter
- modellering av alle faktorer som kan påvirke et byggeprosjekt

Prosjektet skal benytte et begrenset antall variabler og avhengigheter. Hvilke variabler som skal prioriteres, skal avklares gjennom intervjuer med prosjektledere og vurderes opp mot prosjektets tidsmessige og tekniske rammer.

## Vision
Dersom konseptet viser seg å ha praktisk verdi, kan AI Project Planner videreutvikles til et bredere beslutningsstøtteverktøy for prosjektledere i bygg- og anleggsbransjen. En videreutviklet løsning kan inkludere flere typer avvik og risikoer, mer prosjektdata, data fra faktiske prosjekter og mer avansert scenarioanalyse.
På lengre sikt kan løsningen bidra til at prosjektledere tidligere kan identifisere mulige konsekvenser av endringer og undersøke alternative tiltak før problemer utvikler seg videre.Studentprosjektet skal fokusere på å demonstrere kjerneideen gjennom en avgrenset og fungerende prototype.
