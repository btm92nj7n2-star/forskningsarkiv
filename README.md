# Åpent Forskningsarkiv – nettside versjon 1

Dette er en skreddersydd statisk nettside på norsk. Den inneholder 12 prosjektoversikter, søk, kategorifilter, prosjektvinduer og en forskningsmetodeside.

## Viktig om innhold
Prosjektbeskrivelsene er basert på samtalens opplysninger, **ikke** uavhengig verifiserte vitenskapelige resultater. Ingen testlogger, datoer, publikasjoner eller PDF-er er oppdiktet. Dokumentarkivet er tomt til dokumenter blir gjennomgått og lagt inn.

## Test på egen datamaskin
Åpne terminal i mappen og kjør:
`python -m http.server 8000`
Åpne deretter `http://localhost:8000` i nettleseren.

Merk: `index.html` kan ikke bare dobbeltklikkes for full funksjon fordi nettleseren normalt blokkerer lokal innlesing av `projects.json`.

## Gratis publisering med GitHub Pages
1. Lag en GitHub-konto og et nytt offentlig repository, for eksempel `forskningsarkiv`.
2. Last opp **filene inni denne mappen** til hovednivået i repositoryet.
3. Åpne Settings → Pages → Build and deployment, velg Deploy from a branch, `main`, `/ (root)`, og lagre.
4. Vent til GitHub viser publiseringsadressen. Nettsiden kan senere knyttes til et eget domene.

## Legg til dokumenter
1. Lag en mappe `docs` og legg PDF-er der.
2. Åpne `projects.json` og finn ønsket prosjekt.
3. Endre `documents: []` til eksempelvis:
   `"documents": [{"title": "Forskningsnotat – gjennomgått versjon", "path": "docs/notat.pdf"}]`
4. Last opp filene på nytt.

## Tilpasninger
- Nettsidens navn: `index.html` (søk etter «ÅPENT FORSKNINGSARKIV»)
- Tekster og prosjekter: `projects.json`
- Farger og design: `style.css`
- Interaktivitet: `app.js`

Nettsiden krever ingen database og lagrer ingen besøkendes data. Google Fonts lastes eksternt; fjern `@import` i `style.css` om du vil unngå ekstern fontinnlasting.

## Neste versjon
Egen side per teori, publiseringshistorikk, norsk/engelsk, DOI/kilder, matematiske formler, PDF-visning og versjonerte testprotokoller.
Oppdatert 5. november 2026
