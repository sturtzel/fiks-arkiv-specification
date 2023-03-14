# Arkivmelding

**Meldingstype**

`no.ks.fiks.arkiv.v1.arkivering.arkivmelding`

Meldinger sendt med den meldingstypen skal være i henhold til skjema

**Skjema**

[no.ks.fiks.arkiv.v1.arkivering.arkivmelding.xsd](https://github.com/ks-no/fiks-arkiv-specification/blob/main/Schema/V1/no.ks.fiks.arkiv.v1.arkivering.arkivmelding.xsd)

**Definisjon**

Brukes for arkivering når man skal opprette mappe, saksmappe, journalpost, dokument osv i et arkiv.
Oppdatering eller endring på et arkivert objekt gjøres ved egen meldingstype.

## Innhold

Dokumentasjonen her er gruppert på objekter (complexType) i arkivmeldingen som f.eks. arkivmelding, mappe, saksmappe, journalpost, osv.

## arkivmelding 
Arkivmelding er topp objektet for arkivmelding meldingstypen og inneholder det som skal registreres av mapper og registreringer.

**Arv:** Nei

### Felter

### `system`
#### Definisjon
Identifiserer avsendersystem (f.eks. 'Veiconsult Veivedlikeholdssystem') og skal være entydig. `system` kan benyttes av arkivet for å sette opp standardverdier for arkiveringen fra fagsystemet.

### `regel`
#### Definisjon
Hvis denne er gitt verdi vil den referere til et regelsett som overstyrer standardverdiene gitt av `system`. Dette kan benyttes av fagsystemer som arkiverer flere typer journalposter og ønsker forskjellige standardverdier for disse, f.eks. ett regelsett for inngående søknader, et annet for svar på disse og et tredje for rapporter.
Kombinasjonen av `system` og `regel` skal være entydig.
Regel er referanse til regelsettet med standardverdier ref. gammelt skjemamottak, ref. formid i KS Resultat XML.

### `tidspunkt`
#### Definisjon
Tidspunkt for opprettelsen av arkivmeldingen hos avsendersystem.

### `antallFiler`
#### Definisjon
Totalt antall filer som følger med i arkivmeldingen.
Dette feltet skal vise totalt antall vedlagte filer, eksklusive arkivmelding.xml. 
Sender man bare arkivmelding.xml uten hoveddoument eller vedlegg skal `antallFiler` være 0. 

### `mappe`
#### Definisjon
Liste med `mappe` objekter og typer som arver fra `mappe`. Kan inneholde 0 til mange. Se mer om `mappe` lenger nede.

### `registrering`
#### Definisjon
Liste med `registrering` objekter og typer som arver fra `registrering`. Kan inneholde 0 til mange. Se mer om `registrering` lenger nede.


## mappe

#### Definisjon
En mappe kan inneholde andre mapper eller registreringer.

**Arv:** Nei

### Felter

---
### `systemID`
#### Definisjon
Se mer om datatypen i dokumentasjonen for [metadatakatalog.xsd](https://github.com/ks-no/fiks-arkiv-specification/tree/main/Dokumentasjon/V1/Meldinger/metadatakatalog)

---
### `mappeID`
#### Definisjon
Se mer om datatypen i dokumentasjonen for [metadatakatalog.xsd](https://github.com/ks-no/fiks-arkiv-specification/tree/main/Dokumentasjon/V1/Meldinger/metadatakatalog)

---
### `referanseForelderMappe`
#### Definisjon
Se mer om datatypen i dokumentasjonen for [metadatakatalog.xsd](https://github.com/ks-no/fiks-arkiv-specification/tree/main/Dokumentasjon/V1/Meldinger/metadatakatalog)

---
### `tittel`
#### Definisjon
Se mer om datatypen i dokumentasjonen for [metadatakatalog.xsd](https://github.com/ks-no/fiks-arkiv-specification/tree/main/Dokumentasjon/V1/Meldinger/metadatakatalog)

---
### `offentligTittel`
#### Definisjon
Se mer om datatypen i dokumentasjonen for [metadatakatalog.xsd](https://github.com/ks-no/fiks-arkiv-specification/tree/main/Dokumentasjon/V1/Meldinger/metadatakatalog)

---
### `beskrivelse`
#### Definisjon
Se mer om datatypen i dokumentasjonen for [metadatakatalog.xsd](https://github.com/ks-no/fiks-arkiv-specification/tree/main/Dokumentasjon/V1/Meldinger/metadatakatalog)

---
### `noekkelord`
#### Definisjon
Liste med `noekkelord`. Se mer om datatypen i dokumentasjonen for [metadatakatalog.xsd](https://github.com/ks-no/fiks-arkiv-specification/tree/main/Dokumentasjon/V1/Meldinger/metadatakatalog)

---
### `dokumentmedium`
#### Definisjon
Se mer om datatypen i dokumentasjonen for [metadatakatalog.xsd](https://github.com/ks-no/fiks-arkiv-specification/tree/main/Dokumentasjon/V1/Meldinger/metadatakatalog)

---
### `oppbevaringssted`
#### Definisjon
Liste med `oppbevaringssted`. Se mer om datatypen i dokumentasjonen for [metadatakatalog.xsd](https://github.com/ks-no/fiks-arkiv-specification/tree/main/Dokumentasjon/V1/Meldinger/metadatakatalog)

---
### `opprettetDato`
#### Definisjon
Se mer om datatypen i dokumentasjonen for [metadatakatalog.xsd](https://github.com/ks-no/fiks-arkiv-specification/tree/main/Dokumentasjon/V1/Meldinger/metadatakatalog)

---
### `opprettetAv`
#### Definisjon
Se mer om datatypen i dokumentasjonen for [metadatakatalog.xsd](https://github.com/ks-no/fiks-arkiv-specification/tree/main/Dokumentasjon/V1/Meldinger/metadatakatalog)

---
### `avsluttetDato`
#### Definisjon
Se mer om datatypen i dokumentasjonen for [metadatakatalog.xsd](https://github.com/ks-no/fiks-arkiv-specification/tree/main/Dokumentasjon/V1/Meldinger/metadatakatalog)

---
### `avsluttetAv`
#### Definisjon
Se mer om datatypen i dokumentasjonen for [metadatakatalog.xsd](https://github.com/ks-no/fiks-arkiv-specification/tree/main/Dokumentasjon/V1/Meldinger/metadatakatalog)

---
### `arkivdel`
#### Definisjon
Se mer om datatypen i dokumentasjonen for [metadatakatalog.xsd](https://github.com/ks-no/fiks-arkiv-specification/tree/main/Dokumentasjon/V1/Meldinger/metadatakatalog)

---
### `virksomhetsspesifikkeMetadata`
#### Definisjon
Definert som xs:anyType og er ikke bundet til noen datatype. Åpent for virksomhet å sette metadata om mappe.

---
### `part`
#### Definisjon
Liste med parter. Se mer om datatypen [`part` her]() 

---
### `kryssreferanse`
#### Definisjon
Liste med kryssreferanser. Se mer om datatypen [`kryssreferanse` her]()

---
### `merknad`
#### Definisjon
Liste med merknader. Se mer om datatypen [`merknad` her]()

---
### `skjerming`
#### Definisjon
Se mer om datatypen [`skjerming` her]()

---
### `gradering`
#### Definisjon
Se mer om datatypen [`gradering` her]()

---
### `klassifikasjon`
#### Definisjon
Se mer om datatypen [`klassifikasjon` her]()

---
### `referanseEksternNoekkel`
#### Definisjon
Se mer om datatypen i dokumentasjonen for [metadatakatalog.xsd](https://github.com/ks-no/fiks-arkiv-specification/tree/main/Dokumentasjon/V1/Meldinger/metadatakatalog)

---
### `mappe`
#### Definisjon
Liste med mapper under denne mappen.

---
### `registrering`
#### Definisjon
Liste med registreringer under denne mappen.

---
### `mappetype`
#### Definisjon
Se mer om datatypen i dokumentasjonen for [metadatakatalog.xsd](https://github.com/ks-no/fiks-arkiv-specification/tree/main/Dokumentasjon/V1/Meldinger/metadatakatalog)

---
## saksmappe

#### Definisjon

Saksmappe arver felter fra forelder typen `mappe`.

**Arv:** `mappe`

### Felter
*flere felter kommer*

---

## registrering
Her er feltene for objektet registrering. 

**Arv:** Nei

*felter kommer*

---
## journalpost
Her er feltene for objektet journalpost. Se også forelder typen `registrering` for arvet felter.

**Arv:** `registrering`

*felter kommer*




