# 3.Semester-Exam-Docs
Dette er et dokumentations projekt. 
Her dokumenteres projektet Rally Obedience, som er Team 2 3.semester projekt.

---
## MkDocs
Dokumentations projektet er udviklet med `MKDocs`
[MKDocs](https://www.mkdocs.org/) er en hurtig og simpel hjemmeside generator der er udviklet til dokumentations projekter.
Alle dokumentations filerne er skrevet i `MarkDown` sproget.
Og projektet har én enkelt `YAML` configurations fil, hvor Tema, Styling, CodeHighLight m.m - extensions kan tilføjes.

---
## hosting Github Pages
projektet bliver hosted via GitHub Pages og kan tilgås  [her](https://dmoof23-team2.github.io/3.Semester-Exam-Docs/)

For at anvende GitHub Pages, tilføjes folderen ved navn `.github`
Her placeres en ny folder ved navn `workflows`.
I workflows oprettes en fil ved navn `ci.yml`

I denne ci.yml findes coden til GitHub Actions.
GitHub Action står for at lytte til `pushes` til `master` eller `main` branchen.
Når der opfanges pushes til denne branche, kørers `pip install mkdoc-material`
og der publiseres gennem `mkdocs gh-deploy --force`.

---
## Set up
### Commands:
Create local env
```
python3 -m venv env
```

Activate local env
```
source env/bin/activate
```

Install packages
```
pip3 install -r requirements.txt 
```

Start local server
```
mkdocs serve
```

---

## Inspiraion
### Links:
[Inspiration kommer her fra](https://www.youtube.com/watch?v=Q-YA_dA8C20) <!-- target="_blank" -->
<br>
<br>
[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/reference/admonitions/) <!-- target="_blank" -->


