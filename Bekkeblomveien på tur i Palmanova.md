# Bekkeblomveien på tur i Palmanova

En liten statisk nettside med interaktivt kart, listevisning, filtrering og sommerlig reise-/aktivitetsinnhold for Palmanova.

## Filstruktur

Pass på at dette ligger i prosjektmappen:

```text
.
├── index.html
├── README.md
└── assets/
    ├── images/
    ├── css/
    └── js/
```

Hvis du bare har én fil, er det nok at `index.html` ligger i rotmappen.

## Krav

- Git installert.
- GitHub-konto.
- En repository på GitHub.

## Opprett repo på GitHub

For en vanlig prosjekt-side kan repoet hete hva som helst, for eksempel:

```text
bekkeblomveien-palmanova
```

Da blir adressen normalt:

```text
https://ditt-brukernavn.github.io/bekkeblomveien-palmanova/
```

Hvis du vil ha en personlig hovedside, må repoet hete:

```text
ditt-brukernavn.github.io
```

Da blir adressen normalt:

```text
https://ditt-brukernavn.github.io/
```

## Kopier-paste Git-kommandoer

Åpne terminal i mappen med `index.html`, og kjør dette:

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/DITT_BRUKERNAVN/DITT_REPO_NAVN.git
git push -u origin main
```

Bytt ut:

- `DITT_BRUKERNAVN` med GitHub-brukernavnet ditt.
- `DITT_REPO_NAVN` med navnet på repoet ditt.

Eksempel:

```bash
git remote add origin https://github.com/olaeksempel/bekkeblomveien-palmanova.git
```

## Slå på GitHub Pages

1. Gå til repoet på GitHub.
2. Velg **Settings**.
3. Gå til **Pages**.
4. Under **Build and deployment**, velg:
   - **Source:** Deploy from a branch
   - **Branch:** `main`
   - **Folder:** `/ (root)`
5. Trykk **Save**.

Etter noen minutter blir siden tilgjengelig på GitHub Pages-adressen.

## Oppdatere siden senere

Når du endrer filer lokalt, kjør:

```bash
git add .
git commit -m "Oppdatering av siden"
git push
```

GitHub Pages oppdateres automatisk etter push.

## Hvis du får problemer

### 1. Siden viser ikke index.html
Sjekk at filen heter nøyaktig:

```text
index.html
```

ikke `Index.html` eller `index.htm`.

### 2. Ingen oppdatering på nettsiden
Prøv:

```bash
git status
git log --oneline --max-count=5
git push
```

### 3. Feil remote
Se hva som er satt:

```bash
git remote -v
```

Hvis du må endre remote:

```bash
git remote set-url origin https://github.com/DITT_BRUKERNAVN/DITT_REPO_NAVN.git
```

## Nyttig kommando hvis du starter på nytt

Hvis du allerede har et git-oppsett og vil nullstille og koble repoet riktig:

```bash
git remote remove origin
git remote add origin https://github.com/DITT_BRUKERNAVN/DITT_REPO_NAVN.git
git branch -M main
git push -u origin main
```

## Resultat

Når alt er satt opp riktig, blir nettsiden publisert automatisk på GitHub Pages.