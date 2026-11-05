# Åpent Forskningsarkiv – nettside versjon 2

Dette er en statisk nettside på norsk med 12 adskilte forskningsprosjekter. Versjon 2 beholder utseende, søk, filter og prosjektvinduer fra versjon 1, og legger til felt for forskningsspørsmål, åpne spørsmål, dokumenter og testprotokoller.

## Viktig om innholdet
Prosjektoversiktene er basert på opplysninger i samtalen, ikke på uavhengig bekreftede vitenskapelige resultater. **Ingen testprotokoller, PDF-er eller matematiske bevis er fabrikkert eller automatisk publisert.** `records` og `documents` er tomme til dokumentasjon faktisk legges inn.

## Legg til et dokument
1. Legg en kontrollert PDF i `documents/`, f.eks. `documents/q-notat.pdf`.
2. Åpne `projects.json` og finn riktig prosjekt etter `id`.
3. Legg inn i `documents`-listen: `{"title":"Q – notat","path":"documents/q-notat.pdf","date":"2026-11-05","type":"PDF"}`.
4. Last opp både PDF-en og oppdatert `projects.json` til samme GitHub-repositorium.

## Registrer en faktisk utført test
I `research.records` for riktig prosjekt, legg inn for eksempel:

```json
{
  "title": "Testnummer og kort tittel",
  "date": "ÅÅÅÅ-MM-DD",
  "summary": "Metode, reelt resultat og begrensninger",
  "classification": "Analytisk modellresultat / numerisk test / fysisk måling / moteksempel",
  "source": "Kilde, dokumentnavn eller kontrollbar referanse"
}
```

Ikke legg inn tester som bare er omtalt, men ikke dokumentert med kontrollerbart grunnlag. Behold positive, negative og uavklarte funn. Ikke merk 100 % uten fullstendig bevis for den presise matematiske påstanden eller tilstrekkelig uavhengig fysisk bekreftelse.

## Publiser på GitHub Pages
Repository: `forskningsarkiv`. Under Settings → Pages: **Deploy from a branch**, **main**, **/(root)**. Trykk Save bare når innstillingen er endret. Nettsiden blir normalt tilgjengelig på `https://btm92nj7n2-star.github.io/forskningsarkiv/`.

**Viktig:** Last opp *filene inne i ZIP-arkivet* til roten av GitHub-repositoriet, ikke en ekstra mappe med hele prosjektet. Eksisterende filer skal erstattes med nye versjoner.

## Teknikk
Vanlig HTML/CSS/JavaScript og `projects.json`. Ingen database, server eller API-nøkkel. `fetch` krever publisert nettsted eller lokal HTTP-server. Dokumentlenker er begrenset til relative lokale filbaner.
