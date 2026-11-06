# German-speaking Community of Belgium: law in git

Part of [lexifina/global-law](https://github.com/lexifina/global-law), one git history for every country's law: this is the law of German-speaking Community of Belgium, Belgium, which global-law reads at `belgium/german-speaking-community/acts/`.

The law of the German-speaking Community of Belgium (Deutschsprachige Gemeinschaft, Ostbelgien) in git: one file per article, in the form the Community's Parliament publishes it. `git blame` and `tools/on.py` work as in the other repositories of the shared design.

It follows the shared design of [lexifina/global-law](https://github.com/lexifina/global-law), which places it at `be-dg/`. The federal law is in [lexifina/belgium-law](https://github.com/lexifina/belgium-law).

The text is in German, the official language of the Community.

## What this repository holds

**Current text only, no history yet.** 9 acts, one version each: the Community's basic institutional statute (the Law of 31 December 1983 on institutional reforms for the German-speaking Community, in the official German translation of its coordination) and the decrees by which the Community exercises powers of the Walloon Region. The Community's other decrees are not included yet.

| Folder | Act | Files | History |
| --- | --- | ---: | --- |
| `gesetz-1983-12-31/` | 31. DEZEMBER 1983 GESETZ ÜBER INSTITUTIONELLE REFORMEN FÜR DIE DEUTSCHSPRACHIGE GEMEINSCHAFT | 99 | current text, dated 9 June 2024 |
| `dekret-1994-01-17/` | 17. JANUAR 1994 – DEKRET ZWECKS AUSÜBUNG DER BEFUGNISSE DER WALLONISCHEN REGION IN DER ANGELEGENHEIT „DENKMÄLER UND LANDSCHAFTEN“ DURCH DIE DEUTSCHSPR | 5 | current text, dated 1 January 2016 |
| `dekret-1999-05-10/` | 10. MAI 1999 – DEKRET ZUR AUSÜBUNG DER BEFUGNISSE DER WALLONISCHEN REGION IN DEN ANGELEGENHEITEN BESCHÄFTIGUNG UND AUSGRABUNGEN DURCH DIE DEUTSCHSPRAC | 18 | current text, dated 1 January 2016 |
| `dekret-2004-06-01/` | 1. JUNI 2004 – DEKRET ÜBER DIE AUSÜBUNG GEWISSER ZUSTÄNDIGKEITEN DER WALLONISCHEN REGION IM BEREICH DER UNTERGEORDNETEN BEHÖRDEN DURCH DIE DEUTSCHSPRA | 7 | current text, dated 1 January 2026 |
| `dekret-2014-03-31/` | 31. MÄRZ 2014 – DEKRET ÜBER DIE AUSÜBUNG DER ZUSTÄNDIGKEITEN DER WALLONISCHEN REGION IM BEREICH DES TOURISMUS DURCH DIE DEUTSCHSPRACHIGE GEMEINSCHAFT | 4 | current text, dated 1 July 2014 |
| `dekret-2015-12-15/` | 15. DEZEMBER 2015 – DEKRET ZUR ABÄNDERUNG VERSCHIEDENER DEKRETE IM HINBLICK AUF DIE AUSÜBUNG GEWISSER BEFUGNISSE DER WALLONISCHEN REGION IN DEN ANGELE | 12 | current text, dated 1 January 2016 |
| `dekret-2019-04-29-energie/` | 29. APRIL 2019 – DEKRET ÜBER DIE AUSÜBUNG GEWISSER ZUSTÄNDIGKEITEN DER WALLONISCHEN REGION IM BEREICH DER ENERGIE DURCH DIE DEUTSCHSPRACHIGE GEMEINSCH | 6 | current text, dated 1 January 2020 |
| `dekret-2019-04-29-raumordnung/` | 29. APRIL 2019 – DEKRET ÜBER DIE AUSÜBUNG DER ZUSTÄNDIGKEITEN DER WALLONISCHEN REGION IM BEREICH DER RAUMORDNUNG UND GEWISSER VERBUNDENER BEREICHE DUR | 7 | current text, dated 1 January 2020 |
| `dekret-2019-04-29-wohnungswesen/` | 29. APRIL 2019 – DEKRET ÜBER DIE AUSÜBUNG DER ZUSTÄNDIGKEITEN DER WALLONISCHEN REGION IM BEREICH DES WOHNUNGSWESENS DURCH DIE DEUTSCHSPRACHIGE GEMEINS | 8 | current text, dated 1 January 2020 |

## Source

"Rechtsgrundlagen der Deutschsprachigen Gemeinschaft", 9th updated edition (August 2026), edited by the legal service of the Parliament of the German-speaking Community and published at <https://pdg.be/desktopdefault.aspx/tabid-4037/>: Abschnitt II (the Law of 31 December 1983) and Abschnitt III (decrees exercising regional powers). Each text opens with "Allgemeine Hinweise": its publication in the Belgisches Staatsblatt, the day it took effect and its amendments.

## Dates

- Each act has one commit, the "oldest version available", dated at **noon, Europe/Brussels**, on the latest in-force day its "Allgemeine Hinweise" name on or before the retrieval day (the act's own in-force day, or the day its last amendment took effect). It is credited to the publisher.
- The amendment notes are kept in the commit message, not in the law files.

## Files

`<act>/art-005.md` is Art. 5, `art-005-001.md` Art. 5.1, `art-054-bis.md` Art. 54bis; `gliederung.md` holds the headings (TITEL, KAPITEL, ABSCHNITT). The first line is the article number; then one paragraph per line. Square brackets mark wording that an amendment inserted or replaced, and `[...]` wording it repealed, as in the printed coordination; the footnote numbers that name each amendment are left out.

## How it is checked

- Every act is read back from git on the day of its version and the day before (`tools/check_repo.py`); both must match `corpus.json`.
- The letters and digits of the whole repository text (titles, notes, headings and articles, in order) equal those of the body text of the PDF, read a second time with a separate PDF parser.

## Limits

This is not an official publication. The binding text is the one published in the Belgisches Staatsblatt / Moniteur belge. There is no earlier version: the history of these acts before the current text is not recorded here.
