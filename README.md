# Case Crackers with Claude

**Author:** Nik Bear Brown
**Publisher:** Bear Brown, LLC
**Status:** Draft
**Started:** 2026-05-08

## Structure

```
book.md                 ← book description and high-level outline (planning)
outline.md              ← starter table of contents (planning)
vision.md               ← Tic TOC Phase 1: vision and positioning
architecture.md         ← Tic TOC Phase 2: learning architecture
chapters-spec.md        ← Tic TOC Phase 3: chapter specifications
risks.md                ← Tic TOC Phase 4: scope, market, risks
pantry/                 ← scratch storage for fragments, snippets, leftovers
chapters/
    00-frontmatter.md   ← copyright, dedication, preface
    01-introduction.md  ← Chapter 0 / Introduction
    02-chapter-01.md    ← Chapter 1
    ...
    04-chapter-03.md    ← Chapter 3
    99-back-matter.md   ← acknowledgments, about the author, notes, references, index
```

## Planning Documents

| File | Purpose |
|------|---------|
| `book.md` | One-sentence pitch, the argument, the gap, the reader, high-level outline. |
| `outline.md` | Chapter-level table of contents — keep in sync with `chapters/`. |
| `vision.md` | Tic TOC Phase 1 — book concept, type, learner profile, thesis, field positioning. |
| `architecture.md` | Tic TOC Phase 2 — learning outcomes, sequencing, three-act arc, prerequisites. |
| `chapters-spec.md` | Tic TOC Phase 3 — per-chapter specs, cases, contested claims, coverage gaps. |
| `risks.md` | Tic TOC Phase 4 — comparable texts, features, out of scope, adoption risks. |
| `pantry/` | Scratch storage for fragments and snippets that don't yet belong in a chapter. |

These files are for planning only. They are not compiled into the EPUB.

The four Tic TOC files are templated with `[NEEDS HUMAN INPUT]` markers
and a `*Phase N output from Tic TOC*` header signature. Run Tic TOC's
`/scaffold silent` to fill them from `book.md`, `outline.md`, `pantry/`,
and `chapters/`. Or build them section-by-section through the interactive
phase commands (`/i1` → `/m4`).

## Chapters

| File | Title | Status |
|------|-------|--------|
| 00-frontmatter.md | Front Matter (copyright, dedication, preface) | ☐ |
| 01-introduction.md | Introduction | ☐ |
| 02-chapter-01.md | Chapter 1 | ☐ |
| 03-chapter-02.md | Chapter 2 | ☐ |
| 04-chapter-03.md | Chapter 3 | ☐ |
| 99-back-matter.md | Back Matter (acknowledgments, notes, references, index) | ☐ |

## Build

```bash
./build.sh
```

Output goes to `output/` (gitignored).

## Figures

```bash
./graphs.sh
```

Processes `<!-- → [TYPE: description] -->` comments in every chapter:
- Tabular figures → classed markdown tables (`.infographic-table`, `.comparison-table`, `.data-table`)
- Non-tabular figures → placeholder images in `images/`, ready to replace
- CSS log appended to `styles/kindle-book.css` on each run

Review `chapters/*-updated.md`, then promote:
```bash
for f in chapters/*-updated.md; do mv "$f" "${f/-updated/}"; done
```

## Styles

| File | Purpose |
|------|---------|
| `styles/kindle.css` | Shared base — typography, figure table classes. Do not edit per book. |
| `styles/kindle-book.css` | Book-specific overrides. Edit freely. `graphs.sh` appends its log here. |

## Publish

Upload `output/case-crackers-with-claude.epub` to [KDP](https://kdp.amazon.com).

---

## What This Book Is

<!-- TODO: populate from chapter content -->

---

## Who This Book Is For

reader's roadmap)

This file is a stub. Sections 1–10 and 12–13 are placeholders for a later pass.
Section 11 (A note about AI) is substantive and written.

A good model for the full version: Pearl's "The Mind Over Data" introduction,
Molnar's Interpretable ML introduction. Both are argument-first and tell the
reader exactly what to expect from each chapter.
-->

# Introduction

<!-- [1] COLD OPEN
     A specific named scene with real stakes.
     No "this book will...", no throat-clearing.

---

## How to Read It

<!-- TODO: populate from chapter content -->

---

## Table of Contents

| Chapter | Title | File |
|---------|-------|------|
| Intro | Introduction | [chapters/00-introduction.md](chapters/00-introduction.md) |
| Intro | Introduction | [chapters/01-introduction.md](chapters/01-introduction.md) |
| 1 | Chapter 1 — Understanding the Case Interview Structure | [chapters/01-understanding-the-case-interview-structure.md](chapters/01-understanding-the-case-interview-structure.md) |
| 2 | Chapter 2 — Strategic Approach to Case Interviews | [chapters/02-strategic-approach-to-case-interviews.md](chapters/02-strategic-approach-to-case-interviews.md) |
| 3 | Chapter 3 — Essential Guidelines for Interview Success | [chapters/03-essential-guidelines-for-interview-success.md](chapters/03-essential-guidelines-for-interview-success.md) |
| 5 | Chapter 5 — Value Chain Analysis | [chapters/05-value-chain-analysis.md](chapters/05-value-chain-analysis.md) |
| 6 | Chapter 6 — Market Entry Framework | [chapters/06-market-entry-framework.md](chapters/06-market-entry-framework.md) |
| Intro | Chapter 7 — New Product Introduction Framework | [chapters/07-new-product-introduction-framework.md](chapters/07-new-product-introduction-framework.md) |
| 8 | Chapter 8 — Pricing Framework | [chapters/08-pricing-framework.md](chapters/08-pricing-framework.md) |
| 9 | Chapter 9 — Growth Framework | [chapters/09-growth-framework.md](chapters/09-growth-framework.md) |
| 10 | Chapter 10 — Mergers & Acquisitions Framework | [chapters/10-mergers-and-acquisitions-framework.md](chapters/10-mergers-and-acquisitions-framework.md) |
| 11 | Chapter 11 — Due Diligence Framework | [chapters/11-due-diligence-framework.md](chapters/11-due-diligence-framework.md) |
| 12 | Chapter 12 — Common Frameworks: SWOT and PESTEL | [chapters/12-common-frameworks-swot-pestel.md](chapters/12-common-frameworks-swot-pestel.md) |
| 13 | Chapter 13 — Strategic Frameworks: Porter's Five Forces and Value Chain | [chapters/13-strategic-frameworks-porters-five-forces-value-chain.md](chapters/13-strategic-frameworks-porters-five-forces-value-chain.md) |
| 14 | Chapter 14 — BCG Matrix Framework | [chapters/14-bcg-matrix-framework.md](chapters/14-bcg-matrix-framework.md) |
| 15 | Chapter 15 — BCG Matrix, TAM/SAM/SOM, and Portfolio Strategy | [chapters/15-bcg-matrix-tam-sam-som-portfolio-strategy (1).md](chapters/15-bcg-matrix-tam-sam-som-portfolio-strategy (1).md) |
| 15 | Chapter 15 — BCG Matrix, TAM/SAM/SOM, and Portfolio Strategy | [chapters/15-bcg-matrix-tam-sam-som-portfolio-strategy.md](chapters/15-bcg-matrix-tam-sam-som-portfolio-strategy.md) |
| 16 | Chapter 16 — Marketing Frameworks: 5C's, 4P's, and 4A's | [chapters/16-marketing-frameworks-5cs-4ps-4as.md](chapters/16-marketing-frameworks-5cs-4ps-4as.md) |
| 17 | Chapter 17 — Miscellaneous Frameworks: VRIO, AMO, STP, and 4V's | [chapters/17-miscellaneous-frameworks-vrio-amo-stp-4vs.md](chapters/17-miscellaneous-frameworks-vrio-amo-stp-4vs.md) |
| 19 | Chapter 19 — The Landscape of Case Interviews: Formats, Types, and What Each Is Testing | [chapters/19-the-landscape-of-case-interviews.md](chapters/19-the-landscape-of-case-interviews.md) |
| 20 | Chapter 20 — Reading the Room: McKinsey, BCG, and Bain Interview Styles | [chapters/20-reading-the-room-mckinsey-bcg-bain-interview-styles.md](chapters/20-reading-the-room-mckinsey-bcg-bain-interview-styles.md) |

---

## Signature Simulations

<!-- TODO: populate from chapter content -->

---

## Copyright

Copyright © 2026 Nik Bear Brown. All rights reserved.

Published by Bear Brown, LLC.

No part of this publication may be reproduced, distributed, or transmitted
in any form or by any means without the prior written permission of the
publisher, except in the case of brief quotations in critical reviews and
certain other noncommercial uses permitted by copyright law.

ISBN: [INSERT ISBN]

