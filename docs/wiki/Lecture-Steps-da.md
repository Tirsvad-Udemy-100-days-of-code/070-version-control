[English](Lecture-Steps) · **Dansk** · [Bahasa Melayu](Lecture-Steps-ms)

# Forelæsningstrin

## 1. Installer Git og Git Bash

**Hvad vi gjorde:** Hentede Git til Windows, accepterede licensen, beholdt standardvalgene (Git Bash afkrydset) og satte Git Bash som standardprofil i terminalen i VS Code. Mac-brugere springer over: Bash er allerede installeret.

![Installer Git og Git Bash](https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/raw/branch/main/docs/images/01-install-git.png?v=950192e)

**Hvad vi lærte:** En fungerende `git`-kommando og en Unix-lignende shell på Windows, så alle senere kommandoer i kurset virker ens på alle systemer.

## 2. Hvad er versionsstyring?

**Hvad vi gjorde:** Versionsstyring gemmer versioner (gemmepunkter) af dine filer. Hvis kode går i stykker, sammenligner du med en tidligere version og ruller tilbage. Git understøtter også kloning, forking, pull requests og sammenfletning.

![Hvad er versionsstyring?](https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/raw/branch/main/docs/images/02-version-control.png?v=950192e)

**Hvad vi lærte:** Forståelsen af, at intet går tabt: hver ændring er et trin, der kan gendannes, så det er trygt at eksperimentere.

## 3. Lokal versionsstyring

**Hvad vi gjorde:** I en mappe `Story` kørte vi `git init`, oprettede `chapter1.txt`, tilføjede den til staging med `git add`, gemte med `git commit -m "Complete chapter 1"` (nutid), så historikken med `git log`, sammenlignede med `git diff` og gendannede en fil med `git checkout -- <fil>`.

![Lokal versionsstyring](https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/raw/branch/main/docs/images/03-local-git.png?v=950192e)
![Lokal versionsstyring](https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/raw/branch/main/docs/images/03b-diff-restore.png?v=950192e)

**Hvad vi lærte:** Forskellen på arbejdsmappen og staging-området, hvordan man laver en commit, læser historikken og fortryder uønskede ændringer.

## 4. GitHub og eksterne repositories

**Hvad vi gjorde:** Oprettede en GitHub-konto og et tomt repository (offentligt eller privat), forbandt det lokale repository med `git remote add origin <url>` og uploadede med `git push -u origin main`. Skærmbilledet pusher til et lokalt bare-repository, så det virker offline.

![GitHub og eksterne repositories](https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/raw/branch/main/docs/images/04-remote-push.png?v=950192e)

**Hvad vi lærte:** En ekstern kopi som backup og til deling, samt betydningen af `origin` og `main`-grenen.

## 5. Filen .gitignore

**Hvad vi gjorde:** Oprettede `.gitignore` før første commit og skrev `secrets.txt`, `.DS_Store`, `*.pyc` og `.venv/` ind. Git holder så op med at vise filerne og committer dem aldrig. Skabeloner pr. sprog: github.com/github/gitignore.

![Filen .gitignore](https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/raw/branch/main/docs/images/05-gitignore.png?v=950192e)

**Hvad vi lærte:** Hvordan man holder adgangskoder og API-nøgler ude af lokale og offentlige repositories, og at jokertegn og `#`-kommentarer virker i filen.

## 6. Grene og sammenfletning

**Hvad vi gjorde:** Oprettede grenen `alien-plot` med `git branch`, skiftede med `git checkout`, lavede commits dér, skiftede tilbage til `main` og samlede arbejdet med `git merge alien-plot`. Valgfri øvelse: learngitbranching.js.org.

![Grene og sammenfletning](https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/raw/branch/main/docs/images/06-branching.png?v=950192e)

**Hvad vi lærte:** Eksperimenter og nye funktioner kan leve adskilt fra `main`, som forbliver stabil, og flettes først ind, når de virker.

## 7. Forking og pull requests

**Hvad vi gjorde:** Gennemgik de fire områder (arbejdsmappe, staging-område, lokalt repository, eksternt repository). En fork er din egen kopi af en andens repository; efter ændringer opretter du en pull request, hvor du beder ejeren om at flette. Kun ejeren kan flette.

![Forking og pull requests](https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/raw/branch/main/docs/images/08-four-areas.png?v=950192e)
![Forking og pull requests](https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/raw/branch/main/docs/images/07-fork-pull-request.png?v=950192e)

**Hvad vi lærte:** Hvordan open source-samarbejde fungerer: foreslå ændringer uden at røre originalen, gennemse hinandens kode og bidrage til projekter.
