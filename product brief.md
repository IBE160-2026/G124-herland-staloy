## 1. Produktidé

AI Project Planner er en webbasert prototype på et KI-basert styrings- og beslutningsstøtteverktøy for prosjektledere i bygg- og anleggsbransjen.
Verktøyet skal hjelpe prosjektledere med å forstå hvordan endringer i en fremdriftsplan kan påvirke resten av prosjektet, og gjøre det mulig å utforske ulike tiltak før en beslutning tas.
Produktet kombinerer en programmatisk analyse av fremdriftsplanen med KI-basert analyse og forklaring. Den programatiske delen skal håndtere beregninger knyttet til aktiviteter og avhengigheter, mens KI-en skal bidra med tolkning, scenarioanalyse og beslutningsstøtte.
KI-en skal ikke ta beslutninger på vegne av prosjektlederen. Målet er å gjøre relevant prosjektinformasjon og mulige konsekvenser enklere å forstå og vurdere.

## 2. Problem
Prosjekter i bygg- og anleggsbransjen varierer betydelig i størrelse, type og kompleksitet. Fremdriftsplaner kan inneholde mange aktiviteter som er avhengige av hverandre.
Når en aktivitet blir forsinket eller andre forutsetninger endres, må prosjektlederen vurdere hvordan dette påvirker resten av prosjektet. Noen aktiviteter kan bli direkte forsinket, mens andre kan gjennomføres parallelt eller flyttes. Det kan også være mulig å redusere konsekvensene gjennom endret ressursbruk eller rekkefølge på aktiviteter.
Det kan derfor være krevende å raskt få oversikt over:

- hvilke aktiviteter som påvirkes
- hvor stor konsekvensen kan bli
- hvilke avhengigheter som er relevante
- hvilke tiltak som kan redusere konsekvensene
- hvordan ulike tiltak kan påvirke prosjektets videre fremdrift

### Problemstilling
> **Hvordan kan KI brukes til å analysere endringer i en fremdriftsplan og gi prosjektledere beslutningsstøtte om mulige konsekvenser og tiltak?**

## 3. Målgruppe
Primær målgruppe er prosjektledere i bygg- og anleggsbransjen som har ansvar for planlegging og oppfølging av prosjektets fremdrift.
Produktet skal utvikles med utgangspunkt i erfaringer fra prosjektledere som arbeider med ulike typer og størrelser på prosjekter.

## 4. Løsningen

Brukeren skal kunne registrere eller velge et prosjekt med en forenklet fremdriftsplan.
Fremdriftsplanen skal bestå av et begrenset sett sentrale egenskaper, for eksempel:
- aktiviteter
- planlagt start og slutt
- varighet
- avhengigheter mellom aktiviteter
- status
- forsinkelser
- milepæler
Når en endring oppstår, skal systemet analysere hvordan endringen påvirker fremdriftsplanen.

Løsningen består av to hoveddeler:

### 4.1 Programmatisk konsekvensanalyse
Systemet skal bruke informasjon om aktiviteter, varighet og avhengigheter til å beregne hvilke aktiviteter som potensielt påvirkes av en endring.
Dette kan blant annet brukes til å beregne:
- hvilke etterfølgende aktiviteter som påvirkes
- hvordan forsinkelsen forplanter seg gjennom planen
- mulig påvirkning på prosjektets planlagte ferdigstillelsesdato
- hvilke aktiviteter som ligger på eller nær kritisk linje
Beregningene skal baseres på definerte regler og prosjektdata, og ikke overlates til KI-modellen alene.

### 4.2 KI-basert beslutningsstøtte
KI-en skal bruke resultatene fra konsekvensanalysen sammen med prosjektets registrerte kontekst til å:
- forklare hva endringen kan innebære
- identifisere relevante forhold prosjektlederen bør undersøke
- foreslå mulige tiltak
- sammenligne ulike handlingsalternativer
- beskrive mulige avveininger mellom tiltakene

## 5. Scenarioanalyse
En sentral funksjon i prototypen skal være muligheten til å undersøke ulike scenarioer.
Eksempel:
En aktivitet i et prosjekt blir forsinket med 10 dager.Prosjektlederen kan undersøke ulike alternativer, for eksempel:
- øke bemanningen
- endre rekkefølgen på aktiviteter
- omdisponere tilgjengelige ressurser
- akseptere forsinkelsen

Systemet skal analysere hvert scenario basert på prosjektets registrerte forutsetninger.
Resultatet kan blant annet vise:
- hvilke aktiviteter som påvirkes
- mulig påvirkning på ferdigstillelsesdato
- hvilke ressurser som berøres
- hvilke nye avhengigheter eller utfordringer som kan oppstå
- hvilke avveininger som følger av tiltaket
Scenarioanalysen skal presenteres som et beslutningsgrunnlag og ikke som en sikker prediksjon av hva som faktisk vil skje.

## 6. Brukerinvolvering
Prosjektledere skal involveres som domeneksperter i utviklingen av produktet.
Det skal gjennomføres samtaler med et utvalg prosjektledere for å undersøke:
- hvordan de arbeider med fremdriftsplaner i dag
- hvordan de vurderer konsekvensene av en forsinkelse
- hvilke typer avhengigheter som er viktigst
- hvilke faktorer de vurderer når de skal velge tiltak
- hvilke utfordringer som varierer mellom små og store prosjekter
- hvor KI kan gi nyttig beslutningsstøtte

Det kan også innhentes perspektiver fra personer med ansvar for KI, digitalisering eller teknologi.
Funnene skal brukes til å prioritere hvilke variabler, funksjoner og scenarioer som skal inngå i prototypen.

## 7. Hva som skiller løsningen
Produktet skal ikke forsøke å konkurrere med etablerte prosjektstyringssystemer på bredde eller antall funksjoner.
Prototypen skal undersøke en mer avgrenset problemstilling:

> **Hvordan kan en prosjektleder raskt undersøke hva som skjer med fremdriftsplanen når en forutsetning endres, og utforske ulike tiltak før en beslutning tas?**
Verdien i løsningen ligger derfor i kombinasjonen av:
1. strukturert fremdriftsdata
2. programmatisk konsekvensberegning
3. KI-basert forklaring og scenarioanalyse
4. mulighet til å sammenligne alternative tiltak

## 8. Minimum Viable Product
Første versjon skal være en enkel webbasert prototype.
En bruker skal kunne:
1. opprette eller velge et prosjekt
2. se en forenklet fremdriftsplan
3. registrere en endring eller forsinkelse
4. få beregnet hvilke aktiviteter som påvirkes
5. få en KI-basert analyse av situasjonen
6. velge et mulig tiltak
7. få en scenarioanalyse av tiltaket
8. sammenligne minst to mulige handlingsalternativer
MVP-en skal demonstrere hovedideen og trenger ikke være et komplett prosjektstyringssystem.

## 9. Avgrensning
Prosjektet skal ikke utvikle et komplett prosjektstyringssystem. Fokus skal være på fremdriftsplanlegging, konsekvensanalyse og scenarioanalyse.
Følgende omfattes ikke av første versjon:
- fullstendig økonomistyring
- fakturering
- kontraktsadministrasjon
- juridiske vurderinger
- BIM-integrasjon
- automatisk innhenting av data fra byggeplass
- integrasjon med ERP- eller andre prosjektstyringssystemer
- automatisk kommunikasjon med entreprenører
- automatisk beslutningstaking
- ressursallokering på tvers av flere prosjekter
- modellering av alle mulige forhold som kan påvirke et byggeprosjekt

Et begrenset antall variabler og avhengigheter skal prioriteres basert på brukerinvolveringen.

## 10. Teknologi
Produktet skal utvikles som en webbasert applikasjon ved hjelp av relevante programmerings- og webutviklingsteknologier.
Løsningen skal inneholde:
- en datamodell for prosjekt og aktiviteter
- programmatisk logikk for å analysere aktiviteter og avhengigheter
- en KI-integrasjon for analyse og scenarioarbeid
- et brukergrensesnitt for registrering og visualisering av prosjektinformasjon

Valg av konkrete teknologier og KI-modell fastsettes som en del av den tekniske utviklingen.

## 11. Data og personvern
Prototypen skal utvikles med syntetiske eller anonymiserte prosjektdata.Konfidensiell informasjon fra faktiske prosjekter skal ikke legges inn i KI-modellen. Erfaringer fra prosjektledere skal brukes til produktutviklingen uten at konfidensiell informasjon om konkrete prosjekter, kunder eller ansatte eksponeres.

## 12. Begrensninger ved KI
KI-genererte analyser kan være feil eller basert på et ufullstendig informasjonsgrunnlag. KI-en skal derfor ikke brukes som eneste grunnlag for faktiske prosjektbeslutninger. Scenarioanalysene skal forstås som mulige konsekvenser basert på registrerte forutsetninger, og ikke som sikre prognoser. Prosjektlederen beholder beslutningsansvaret og skal kunne vurdere KI-ens forslag kritisk.

## 13. Suksesskriterier
Prototypen skal anses som vellykket dersom:
- en prosjektleder enkelt kan registrere en forenklet fremdriftsplan
- systemet kan analysere en konkret endring i fremdriftsplanen
- systemet kan identifisere relevante berørte aktiviteter
- konsekvensberegningen fungerer på definerte testscenarioer
- KI-en kan forklare mulige konsekvenser på en forståelig måte
- brukeren kan teste og sammenligne minst to tiltak
- scenarioene presenteres på en oversiktlig måte
- prosjektledere opplever at løsningen kan gi praktisk verdi som beslutningsstøtte

## 14. Forventet resultat
Resultatet skal være en fungerende prototype av AI Project Planner.
Prototypen skal demonstrere hvordan programmering, webutvikling og KI kan kombineres for å utvikle et praktisk styrings- og beslutningsstøtteverktøy for prosjektledere i bygg- og anleggsbransjen.
Prosjektet skal også dokumentere hvilke behov og prioriteringer som ligger til grunn for løsningen, hvordan konsekvensanalysen er implementert, og hvordan KI-funksjonen er brukt og evaluert.
