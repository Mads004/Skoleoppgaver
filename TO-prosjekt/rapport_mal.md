
# Engelsk-språklig applikasjon

## Behovsanalyse

#### Hvilke utfordringer har brukeren?
#### Hvilke interesser har brukeren?

Brukeren har vanskelig for å lære seg språk, spesielt engelsk.
Hun observerer at engelsk er et nyttig språk, som kommer igjen i mange sammenhenger.
Brukeren liker spill og har konkurranse-instinkt. Motivasjonen øker når man ser fremgang i læringen, i form av poeng og økt mestringsfølelse.

## Applikasjon

#### Hva er applikasjonen?

Applikasjonen er et TRUE-FALSE spill, som skal gi brukeren ett riktig svar og et feil svar.
Brukeren starter med 0 poeng og får ett poeng for riktig svar.
Når alle 10 spørsmålene er stilt, får man en poeng-Score, og gis muligheten til å starte igjen.
Det skal være to måter å visualisere spørsmålet på:

1. Et bilde. Hva er dette på engelsk? Deretter svaralternativer.
2. Fortelle et ord på norsk, og deretter spørre hva det heter på engelsk.
Her skal det være et tekstfelt, som brukeren skal skrive inn.

## Fremgangsmøte

#### Database

Skal lage en MYSQL - database som lagrer hvor mange poeng spilleren har etter endt spill.

  Forslag til tabell 1 - Person:

  | BrukerID       | Brukernavn    | Passord |
  | -------------- |:-------------:| -------:|
  | 1              | 20.08.1991    | 3       |

  Forslag til tabell 2 - Spill:

  | spillID        | Dato          | Poeng | Person |
  | -------------- |:-------------:| -----:| -----: |
  | 1              | 20.08.1991    | 3     | 1      |

  Person-kolonnen i Spill - tabellen er en fremmednøkkel som skal fylles
  på med primærnøkkelen fra Person-tabellen for hvert spill.
  Person-tabellen skal brukes til innlogging.

#### HTML, CSS og Javascript

- Spillet trenger en innloggingsside, som kobler opp informasjon fra databasen
med informasjonen i innloggingsfeltet.
- Stylingen er "clean", med et stort bakgrunnsbilde på alle slides.
- Spillet skal ha en velkommen side (start spillet-side) og start spillet-knapp.
- Når man har svart, så kommer det opp at brukeren har tatt riktig eller feil.
Spilleren blir "tvunget" med til neste spørsmål.
- På Hver side skal det stå hvor langt spilleren har kommet i spillet.
For eksempel 1/10 på først slide, 2/10 på andre slide.

#### Node - backend service.

- Trenger database-tilkobling, og kan både hente og oppdatere databasen.
- Node kan brukes på to måter:
1. Som backend service og API-calls.
2. Som webserver.

Dette har jeg ikke bestemt meg for enda.
