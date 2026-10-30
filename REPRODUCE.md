# How this repository was made (German-speaking Community of Belgium)

This file is written by the build on 2026-10-30, the day the source data was retrieved.

## Sources

| Source | Address | Retrieved | Licence |
| --- | --- | --- | --- |
| Parlament der Deutschsprachigen Gemeinschaft: Rechtsgrundlagen der Deutschsprachigen Gemeinschaft, 9. aktualisierte Auflage, August 2026 | <https://pdg.be/desktopdefault.aspx/tabid-4037/> | 2026-10-30 | Official acts are excluded from copyright (Code of Economic Law, Art. XI.172 §2); the PDFs carry "Alle Rechte vorbehalten", which covers the edition, not the official texts. |

Every word of law in this repository comes from these sources. Lexifina reads them and records each act's dated versions, and the laws that made each change, in one corpus file. This repository is built from that file.

## What is in it

| Act | Title | Versions | Span |
| --- | --- | ---: | --- |
| `gesetz-1983-12-31` | 31. DEZEMBER 1983 GESETZ ÜBER INSTITUTIONELLE REFORMEN FÜR DIE DEUTSCHSPRACHIGE GEMEINSCHAFT | 1 | 2024-06-09 to 2024-06-09 |
| `dekret-1994-01-17` | 17. JANUAR 1994 – DEKRET ZWECKS AUSÜBUNG DER BEFUGNISSE DER WALLONISCHEN REGION IN DER ANGELEGENHEIT „DENKMÄLER UND LANDSCHAFTEN“ DURCH DIE DEUTSCHSPRACHIGE GEMEINSCHAFT | 1 | 2016-01-01 to 2016-01-01 |
| `dekret-1999-05-10` | 10. MAI 1999 – DEKRET ZUR AUSÜBUNG DER BEFUGNISSE DER WALLONISCHEN REGION IN DEN ANGELEGENHEITEN BESCHÄFTIGUNG UND AUSGRABUNGEN DURCH DIE DEUTSCHSPRACHIGE GEMEINSCHAFT | 1 | 2016-01-01 to 2016-01-01 |
| `dekret-2004-06-01` | 1. JUNI 2004 – DEKRET ÜBER DIE AUSÜBUNG GEWISSER ZUSTÄNDIGKEITEN DER WALLONISCHEN REGION IM BEREICH DER UNTERGEORDNETEN BEHÖRDEN DURCH DIE DEUTSCHSPRACHIGE GEMEINSCHAFT | 1 | 2026-01-01 to 2026-01-01 |
| `dekret-2014-03-31` | 31. MÄRZ 2014 – DEKRET ÜBER DIE AUSÜBUNG DER ZUSTÄNDIGKEITEN DER WALLONISCHEN REGION IM BEREICH DES TOURISMUS DURCH DIE DEUTSCHSPRACHIGE GEMEINSCHAFT | 1 | 2014-07-01 to 2014-07-01 |
| `dekret-2015-12-15` | 15. DEZEMBER 2015 – DEKRET ZUR ABÄNDERUNG VERSCHIEDENER DEKRETE IM HINBLICK AUF DIE AUSÜBUNG GEWISSER BEFUGNISSE DER WALLONISCHEN REGION IN DEN ANGELEGENHEITEN BESCHÄFTIGUNG UND DENKMALSCHUTZ DURCH DIE DEUTSCHSPRACHIGE GEMEINSCHAFT | 1 | 2016-01-01 to 2016-01-01 |
| `dekret-2019-04-29-energie` | 29. APRIL 2019 – DEKRET ÜBER DIE AUSÜBUNG GEWISSER ZUSTÄNDIGKEITEN DER WALLONISCHEN REGION IM BEREICH DER ENERGIE DURCH DIE DEUTSCHSPRACHIGE GEMEINSCHAFT | 1 | 2020-01-01 to 2020-01-01 |
| `dekret-2019-04-29-raumordnung` | 29. APRIL 2019 – DEKRET ÜBER DIE AUSÜBUNG DER ZUSTÄNDIGKEITEN DER WALLONISCHEN REGION IM BEREICH DER RAUMORDNUNG UND GEWISSER VERBUNDENER BEREICHE DURCH DIE DEUTSCHSPRACHIGE GEMEINSCHAFT | 1 | 2020-01-01 to 2020-01-01 |
| `dekret-2019-04-29-wohnungswesen` | 29. APRIL 2019 – DEKRET ÜBER DIE AUSÜBUNG DER ZUSTÄNDIGKEITEN DER WALLONISCHEN REGION IM BEREICH DES WOHNUNGSWESENS DURCH DIE DEUTSCHSPRACHIGE GEMEINSCHAFT | 1 | 2020-01-01 to 2020-01-01 |

The build made 9 commits:

| Commits | Kind |
| ---: | --- |
| 9 | first version of an act |
| 0 | one law on its in-force day |
| 0 | changes no amendment note explains, credited to the publisher |

Other counts:
- 0 commits on the branch `zukunft`: laws not yet in force on 2026-10-30.
- 0 commits dated 1 January 1970: in force before 1970, with the real day in their `In-force` trailer.
- 9 laws in the record.
- 9 tags.

## Dates

Each commit is dated at noon (Europe/Brussels) on the day the change took effect. The other dates, enacted and published, are trailers.

When a law gives no date of its own, the default rule applies: Current text only: each act is dated by the latest in-force day its "Allgemeine Hinweise" name (the original in-force day or that of the last amendment) on or before the retrieval day. https://pdg.be/desktopdefault.aspx/tabid-4037/

## How the history is built

`tools/build.py` turns the corpus into this history in one pass: one commit per law, on the day it took effect. The same corpus always gives the same commit hashes. `tools/check_repo.py` reads every version back from git and compares it with the corpus. `tools/on.py` shows the law as it stood on any date. The corpus format is described in `tools/SCHEMA.md`.

- Corpus: sha256 `6ec75c21882c0e36568e689de4d97aeabc28b7b61aa6a5a92f692b48f08dbc48` (171004 bytes).
- Builder blob hashes (`git hash-object`): `build.py` `5d0eabdf207e7a114e8dbc8112ed3b044537b711`, `check.py` `5d719354ea4c62d240c93d2cae446307d81d9e81`, `on.py` `aff48cf1b68d50c7ba8f399ca32261871c301824`.
- Python 3.14.4; git version 2.53.0.

## Checks

9 versions of 9 acts read back from git on the day each took effect and on the day before: 0 mismatches. Trailers: 0 commits whose trailers git cannot parse. Health: 0 merge commits on main, 0 commit dates that go backwards, 0 commits dated after the build.

No second build of this corpus has been compared yet.

## Decisions made by hand

- Current text only: the Parliament publishes one coordinated text per act (9th edition, August 2026). Each act has one version, the oldest version available, dated by the latest in-force day the act's "Allgemeine Hinweise" name on or before the retrieval day, and credited to the publisher.
- Text is read from the PDF by font size: body text (10 pt) only; running headers (9 pt), footnotes (8 pt) and footnote markers (superscript) are left out. The square brackets that mark amended or inserted wording, and [...] for repealed wording, are kept as printed. Words hyphenated at a line end are joined.
- The "Allgemeine Hinweise" (publication, in-force day and amendment list) are the publisher's notes, kept as the version note, not as law text. Headings (TITEL, KAPITEL, ABSCHNITT) are kept in gliederung.md.
- The Law of 31 December 1983 is a federal law; it is included as the Community's basic institutional statute, in the official German translation of its unofficial coordination, as the Parliament publishes it.

## What AI did and did not do

The scripts that read the sources and build this repository were written by Claude Code running Claude Opus 5.5 (`claude-opus-5-5`) under Lexifina's direction.

No model wrote, translated or corrected legal text. No model runs at build time. Every word of law in this repository comes from the official sources above.

The commit messages are written by `build.py` from the source data.

Model use at data-build time:
- A model (Claude) wrote the parse code and chose which texts to include; it wrote no law text. Every word of law comes from the Parliament's own collection.
