# Søknadssystem

*Dette er et foreløpig utkast*

Kommunikasjon mellom søknadssystem og arkiv vha Fiks-Arkiv protokollen.

Merk at Fiks-Protokoll/Fiks-IO er utelatt i modellen for å forenkle den. Den er meldingssystem som ligger mellom søknadssystem og arkivsystem.
Alle meldinger vil gå via Fiks-Protokoll.

## Meldingsutveksling

![sekvensdiagram](meldingsutveksling.png)

Forklaring til diagram

*1) Arkivmelding som oppretter saksmappe i arkivet. 

*2) Arkivmelding som oppretter en eller flere journalposter på saksmappen man opprettet. Feltet `<regel>` definerer hvilken regel som skal brukes for forhåndsdefinerte verdier på journalpost og dokumenter. Se mer under [Meldingsdetaljer](#meldingsdetaljer) -> [Arkivmelding](#arkivmelding) -> [Regel](#regel)

*3) En endring blir gjort på en søknad eller prosessen som krever å bli arkivert. Oppdater melding for journalpost(er) eller saksmappe

*4) Søknadsprosess er ferdig og avsluttes. Arkivmelding sendes for saksmappe og evt journalpost(er). I denne overføringen sendes følgende: Annonse, offentlig søkerliste, utvidet søkerliste, innstillingsvedtak og eventuelle notater og dokumenter som er vedlagt rekrutteringsprosjektet

## Meldingsdetaljer

### Arkivmelding

#### Regel
Feltet `<regel>` bestemmer hvilket regelsett som skal brukes for system som sender inn arkivmelding.
Referanse til regelsettet med  standardverdier ref gammelt skjemamottak.

#### Oppdatering