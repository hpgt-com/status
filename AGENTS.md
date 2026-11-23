# AGENTS.md

Instruksjoner for kodeagenter og andre som jobber i repoet. Beskrivelsen av prosjektet står i [README.md](README.md).

## Prosjektet

Statussiden status.hpgt.com, laget med Upptime. GitHub Actions sjekker adressene, lagrer resultatene i repoet og
publiserer siden til GitHub Pages fra branchen `gh-pages`.

## Kommandoer

Repoet har ikke noe lokalt bygg. Adressene som sjekkes, står i `.upptimerc.yml`.

## Regler

- Følg de felles retningslinjene i https://github.com/hpgt-com/guidelines.
- Alle endringer går via pull request med grønne sjekker. Ikke push til `main`.
- Oppdater dokumentasjonen i samme pull request som endringen.
- Ingen hemmeligheter, tokens eller private opplysninger i repoet. Repoet er offentlig.
- Mappene `history/`, `api/` og `graphs/` og oversikten i `README.md` skrives av Upptime. De endres ikke for hånd.
- Arbeidsflytene er skrevet om fra Upptimes mal. De hentes ikke på nytt fra Upptime, og nye versjoner tas inn med en
  pull request.
