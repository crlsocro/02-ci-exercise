# CI 


I denne leksjonen skal vi se på viktige prinsipper som 

- Trunk based development 
- Feature branch
- Branch Locking 
- Pull request


## Før dere starter

- Dere trenger en GitHub Konto
- Fork dette repositoriet inn i deres egen konto
- Følg disse instruksjonene for å konfigurere GitHub og Travis OBS! Les den siste setningern! :-)  <https://docs.travis-ci.com/user/tutorial/#to-get-started-with-travis-ci-using-github> NB! Gjør bare de tre første stegene ! 

## Konfigurer travis 

- Enten gi Trvis tilgang til alle repositories , eller bare deres fork at dette repositoriet. 


# Slå på følgende Branch protection rules for ditt repo

- Naviger til repositoriet ditt i GitHub
- Velg "Settings"
- Velg "Branches"
- Lag en ny "Branch Protection Rule" for Branch "main" (alle) 
- Velg: Require pull request reviews before merging
- Velg : Require status checks to pass before merging. Hvis dere ikke ser noen verdier i feltet "Search for status checks" skriv "travis". 

# Kontroller 

Nå vil flyten din bli omtrent som som følger

- Sjekk ut master og "pull" siste versjon av koden
- Lag en ny branch for din feature
- Implementer kode og test i din branch 
- Når du er fornøyd med funksjonaliteten. Rebase branchen din interaktivt mot master. Fjern unødvenige commits, og skriv gode kommentarer
 ```
 git rebase -i master
 ```
- Push din branch
```
   git push --force
```
- Gå til github og lag en ny Pull request
- Se at travis bygger koden for din pull request og k
- Forsøk gjerne å fremprovosere en feil ved å få en unit test til å feile. Det skal da bli umulig å Merge 
pull request til master.

# Løs "The Bowling Kata"

Gå sammen to og to. Dere får 15 minutter der dere kan planlegge oppgaven sammen. Velg et reposutory en av dere har laget. 

Regler:

- Ingen commits på master
- Det oppfordres til mange feature brancher og pull requests - men dere må selv bruke skjønn. 
 
