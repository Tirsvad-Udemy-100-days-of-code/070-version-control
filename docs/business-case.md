# Business Case: Version Control

## Metadata
| Key | Value |
| --- | --- |
| ID | BC-001 |
| CrossReference | [SA-001] |
| Language | en |
| Domain | education |

## Version History
| Date | Status | Author | Reviewer | Change | Commit |
| --- | --- | --- | --- | --- | --- |
| 2026-11-16 | Accepted | Jens Tirsvad Nielsen | AI as stand-in for S02 | Initial version; accepted with the Go verdict of the review record (autonomous, not independent) | [aec3ba3] |

---

## Executive Summary

Version Control is a set of study notes on version control with Git and GitHub (installing Git Bash, saving versions locally, pushing to a remote, ignoring files, branching and merging, forking with pull requests), kept as a README and a wiki with a PlantUML diagram per lecture step; the day has no programming. It is day 70 of the Udemy course *100 Days of Code: The Complete Python Pro Bootcamp* and is kept in a repository of its own so that the learner's progress is visible. The notes and the wiki in English, Danish and Malay already exist. What is missing is a written purpose, scope, owner and plan, a wiki page that tells a visitor where those documents are, and the common project baseline of the SQA and QC framework that the other projects of the portfolio follow. This Business Case justifies one short baseline project that adds those documents and metadata. It changes none of the lecture notes and none of the diagrams. The recommendation is to proceed.

## Methodological and Standards Foundation

The project follows the SQA (software quality assurance) and QC (quality control) framework mounted at `framework/`: artifact templates, QC checklists and the review process. Every QC criterion is tagged with an ISO/IEC 25010:2023 quality characteristic, and each review record gives evidence per criterion. Use cases and design artifacts follow Larman's *Applying UML and Patterns*; this baseline needs none, because it adds no software behaviour (the repository has no code). The Product Owner's language is English and the domain is education.

## Problem Statement

- The repository holds finished study notes, but nothing states why they exist, what is in and out of scope, who owns them or how their quality is judged.
- The notes exist in English, Danish and Malay, but nothing says that English is the authoritative text.
- The repository does not yet follow the common project baseline (framework submodule, `.gitmodules`, `.env.example`, registry), so it differs from the projects that already follow it.
- The licence is in the `LICENSE` file, but the README does not name it.

## Business Opportunity

A documented, framework-aligned repository makes the notes easy to understand, review and reuse, shows the learner's progress as a portfolio, and lets the same checks run on every project of the course. Wiki pages in three languages make the notes readable to a wider audience of learners.

## Objectives

- **O1.** Keep the lecture notes of Version Control intact: the lecture pages, the diagram sources and the README lecture section do not change.
- **O2.** Record the purpose, scope, stakeholders and plan of the project in a Business Case, a Stakeholder Analysis, a Project Plan and one milestone, each reviewed and accepted.
- **O3.** Keep the wiki in English, Danish and Malay and add a page, in each language, that tells where the project documents are.
- **O4.** State the licence in the README and adopt the current framework release.

## Scope

### In Scope

- Adopting the framework release in use across the portfolio (submodule, installed skills, hooks, `.gitmodules`, `.env.example`; no `.editorconfig`, because the repository has no source file of a code language).
- The baseline documents: Business Case, Stakeholder Analysis, Project Plan, one milestone, the traceability matrix and their review records.
- A Project Documents page in English, Danish and Malay in the existing wiki (`docs/wiki/`), and the sidebar and Home pages that link to it.
- The README, restored to the framework's README template, with the licence stated.

### Out of Scope

- Any change to the lecture pages (`docs/wiki/Lecture-*`), the diagram sources (`docs/diagrams/`) or the README section Lecture steps.
- A review of the lecture notes against a checklist (the framework has none for study notes; kept as an open issue of the Project Plan).
- Re-translating or rewriting the existing Danish and Malay lecture pages.
- Use cases, design artifacts and a domain dictionary.

## Expected Benefits

### Tangible Benefits

- One accepted Business Case, Stakeholder Analysis, Project Plan and milestone, with a review record for each.
- A wiki of three pages in each of three languages (Home, Lecture-Steps and Project-Documents), plus the sidebar.
- A README that has every section of the framework template.
- A README that names the licence and links the `LICENSE` file.

### Intangible Benefits

- A visitor understands the purpose and scope within minutes.
- The learner can show the notes in a portfolio that looks the same for every project.
- Reviewing the project later is easier because every decision has a document.

## Strategic Alignment

The repository is the learner's portfolio of the 100 days of the course. The strategic goal is a portfolio in which every project is understandable, checked, licensed and documented in the same way. This project brings Version Control to that level.

## Success Criteria

| # | Criterion | Target | Measure |
| --- | --- | --- | --- |
| 1 | The notes are intact (O1) | 0 changed files under `docs/diagrams/` and `docs/wiki/Lecture-Steps*`; 0 changed lines in the README section Lecture steps | `git diff origin/main --stat -- docs/diagrams 'docs/wiki/Lecture-Steps*'` on the pull request branch is empty, and `git diff origin/main -- README.md` has no hunk between the headings Lecture steps and Requirements |
| 2 | The baseline documents are accepted (O2) | 4 of 4 documents `Accepted` with a `Go` review | Version History status and `RC-*` verdict of BC-001, SA-001, PP-001 and MIL-001 |
| 3 | The wiki exists in three languages (O3) | 3 languages with the same 3 pages, plus the sidebar | Files in `docs/wiki/` and the `QC-WIKI-001` review |
| 4 | The README follows the template (O2) | 0 findings | `framework/scripts/check-readme.sh` exits with code 0 |
| 5 | The licence is stated (O4) | The README License section names AGPL-3.0 and links `LICENSE`; `LICENSE` exists | The README and the file list |
| 6 | The change is merged with a green build (O1, O2) | 100 % of the CI (continuous integration) checks on the pull request pass | Status of the pull request on the git host |

## Risks

| Risk | Impact | Mitigation |
| --- | --- | --- |
| The documents drift from the notes as the notes change | Readers get wrong information | The scope states that the notes do not change; a later change reopens the documents (a new Version History row and a review) |
| The reviewer is also the author, so the review is not independent | A defect is missed | Every review record says `Mode: autonomous, not independent`, and the end-of-run summary lists it for challenge |
| A translation is wrong or unclear | Danish or Malay readers are misled | English is the authoritative text; the translations follow it page by page and are open to correction by a native reader |
| The wiki publication fails after the merge | The wiki is empty | The publication is checked on the host after the merge, and a failure is reported |

## Assumptions

- The Product Owner is the learner, who also reviews and merges (S01, S02).
- The course day is complete; no further lecture is planned for this project.
- The git host's scoped workflow publishes `docs/wiki/` to the repository wiki after a merge.
- The people the notes are for cannot be asked for interviews; their concerns are inferred from the course.

## Constraints

- The baseline is finished within one week, by 2026-11-23.
- Metadata keys, headings, IDs and statuses stay in English; the content is English (the Product Owner's language).
- The framework is private, so project documents do not link to its files in the README appendix.
- The repository is public, so the AI prompt log is ignored by git.
- The diagrams are written in PlantUML by the author; they are not frames of the course video, which is the instructor's material.

## Cost–Benefit Assessment

A qualitative assessment is justified: the project is unpaid, has one person, and its benefits (clarity, portfolio value, reuse) have no market price.

| Costs | Benefits |
| --- | --- |
| About one day of the author's and the AI assistant's time | Reviewed documents that explain the project |
| Reviewer time to read the end-of-run summary | A wiki in three languages |
| Upkeep of the documents when the notes change | A portfolio entry that matches the other projects |

## Stakeholders

| Stakeholder ID (SA) | Interest in this project |
| --- | --- |
| S01 | Owns the project and wants a documented, working portfolio entry |
| S02 | Reviews every document and merges the pull request |
| S03 | Wants to read the notes in their own language |
| S04 | Teaches the lectures that the notes summarise |

## Recommendation

Proceed. The cost is small, the risk is low and the benefit is a documented, reviewable and multilingual portfolio entry.

---

[SA-001]: ./stakeholder-analysis.md
[aec3ba3]: https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/commit/aec3ba3c8f9c552e3854ee195a68f64128e82cb6
