# Ancestor Research Inventory (ARI™) — Specification v1.0

**Published:** 2026-09-29
**Author:** Denyse Allen, Chronicle Makers (PA Ancestors LLC)
**Canonical home:** [chroniclemakers.com/ancestor-research-inventory/](https://chroniclemakers.com/ancestor-research-inventory/)
**License:** [CC BY 4.0](LICENSE). The ARI™ name is a trademark and is not licensed. See [TRADEMARKS.md](TRADEMARKS.md).

---

## 1. What an ARI is

An Ancestor Research Inventory holds everything found on **one ancestor**: the records, what they say, where they disagree, what was searched and not found, the researcher's own account of the work, and the result of the check run on it.

One inventory per ancestor. Seven sections, always in the same order. Plain markdown files that a person can read with no software and any AI tool can read today.

An ARI is a **report format**. It structures research; it makes no claim that the research is true. It does not certify anything.

### What this specification covers

- The file layout
- The seven sections, their order, and what each holds
- Why each section is in the format
- The shared vocabulary (confidence labels, result labels)
- The rules every ARI follows

### What this specification does not cover

- How conclusions are reached from the evidence
- The criteria of the Research Quality Check
- The tools that build an ARI

Those belong to Chronicle Makers' tools and are not published here. An ARI can be built by hand or by any tool. What this document defines is **what the finished report contains and why**.

---

## 2. File layout

```
[ancestor-name]-ARI/
├── index.md            1. Index
├── timeline.md         2. Timeline
├── sources/            3. Sources
│   ├── index.md
│   └── [one file per record].md
├── conflicts.md        4. Conflicts
├── log.md              5. Research log
├── narrative.md        6. Research narrative
└── quality-check.md    7. Research Quality Check
```

A single-document export (one long markdown or PDF file) is allowed. It keeps the same seven sections in the same order.

### Why plain files

A family tree lives on a platform, in the platform's format, for as long as someone pays. An ARI lives in files the researcher owns. Markdown opens in any text editor, reads cleanly as plain text, converts to any other format, and every AI tool reads it. Nothing about an ARI depends on an account staying open.

### Why a fixed order

When every ARI puts the same thing in the same place, any reader, and any tool, knows where to look without being told. The order also reads as an argument: **who** this person was → **what happened**, in order → the **evidence** → where the evidence **disagrees** → **how** the research was done → the **researcher's** account → the **status** of the whole.

---

## 3. The seven sections

### 1. Index — `index.md`

**Holds:** the identity page. Names and name variants, the settled facts of the life (birth, death, burial, spouses, parents, siblings, children), a confidence label and a source link on every fact, a short summary of settled facts only, and links to the other six sections.

**Why it is here:** a reader needs to know *who* in one page before anything else. It is the front door. Every fact on it points to a record, so the page can be checked line by line rather than trusted.

**Names get their own block** — the surname filed under and why, every spelling found and where, and every name the person carried through life with dates. A woman married twice, recorded under three surnames, is a findable ancestor with this block and a lost one without it.

**The summary holds settled facts only.** Open questions belong in the log and the conflicts, not on the front page.

### 2. Timeline — `timeline.md`

**Holds:** life events in date order. Each row: date · event · place · source link.

**Why it is here:** order exposes what a list of facts hides — the gap of twenty unrecorded years, the child born after the father's death, the move that happened before the deed says it did. Every event links to what establishes it.

### 3. Sources — `sources/`

**Holds:** one file per record examined, plus a `sources/index.md` table listing every record: type, date created, original or derivative, what it establishes.

Each source file carries, in this order:

1. **Citation** — complete, first, before anything else. It is what makes everything below it checkable.
2. **Classification** — original or derivative, provenance (who created it, when, why, who holds it now), and informant (who supplied the information, and what they could have known firsthand).
3. **Transcription** — the relevant portion, with uncertain readings marked.
4. **What it establishes** — each claim, with its confidence label, and where it feeds (index, timeline).

**Why it is here:** the evidence is the research. Every other section points back into this one.

**Why one file per record:** a census establishes residence, an approximate birth year, a marital status and a household all at once. Filing it under one event is arbitrary. Filing it under four breaks the record apart. One file per record, and the claims link out from it.

**Why sorted by the date the record was created** (not by record type, and not by the event it describes):
- One sort key. No case-by-case calls.
- Records made near the event rise to the top. A pension file stating a birth date sixty years later, a late biography, a funeral notice fall to the bottom — a reader can watch the evidence thin out.
- It reads in the same direction as the timeline.

**The index-entry flag.** Any source that is an index or other derivative standing in for a record nobody has examined carries a standing note: `INDEX ENTRY — ORIGINAL MUST BE OBTAINED`. It comes off when the original is in hand. The flag turns "keep looking" into a finite, completable task.

### 4. Conflicts — `conflicts.md`

**Holds:** every contradiction found between sources. For each: the sources in tension, and its status — **RESOLVED** with the conclusion, or **OPEN** with what would settle it.

**Why it is here:** a family tree shows one birth year. It never shows that three records gave three different ones. When the disagreement is hidden, the next researcher inherits a choice they cannot see. An ARI puts every disagreement on the page and says where it stands.

### 5. Research log — `log.md`

**Holds:**
- **Dated entries, newest first**, under ISO 8601 date headings: what was searched, how, and what came back.
- **Negative results**, every one, stating three things: the source searched · how it was searched · what was returned.
- **A record-group coverage table**: the record groups that exist for this person's place and era, the jurisdiction and dates of each, whether each was searched, and the result. The table names the authority it was built from.

**Why it is here:** what was searched and *not* found is the most-lost part of any research project. It lives in the researcher's head and nowhere else. Without it, the next person repeats every empty search.

**Why "how it was searched" is required:** *"She wasn't in the church records"* is not a finding. *"Searched the session minutes 1855–1875 for Boggs and every spelling variant, page by page, no entry"* is.

**Why the coverage table names its authority:** a list of record groups with no cited authority is an opinion about what exists. Naming where the list came from makes it checkable.

### 6. Research narrative — `narrative.md`

**Holds:** the researcher's own account of doing this research — how it started, where it stalled, what broke it open, what surprised them, what is still unfinished. Built from the field notes kept during the research.

**Why it is here:** everything else in an ARI is reference prose, researcher to researcher. This is the only section written in first person, and the only one in the researcher's own words. The chronicle is about the ancestor. This section is about the person who went looking. It is often the part family historians most want to write, and it is the part that disappears first when research is handed on as a tree.

### 7. Research Quality Check — `quality-check.md`

**Holds:** the record of the check run on this research: which check, the date run, who ran it, the result, and — if the result is NOT YET — the finite, named list of what is still missing.

**Why it is here:** the status of the research travels with the research. A reader opening an ARI knows at once whether the researcher considers it finished, and if not, exactly what is left.

**Why it is last:** it is a statement about the six sections before it.

The criteria of the Research Quality Check are not part of this specification. See [chroniclemakers.com/research-quality-check/](https://chroniclemakers.com/research-quality-check/).

---

## 4. Shared vocabulary

### Confidence labels

Every fact in the Index, Timeline and a source's *What it establishes* carries exactly one label. Six labels, in two groups.

**How strongly the evidence supports the fact**

| Label | Means |
|---|---|
| `proved` | The evidence establishes it and nothing contradicts it |
| `probable` | The evidence supports it; the reasoning is written down and the doubt is stated |
| `possible` | Something points to it, not enough to call it probable |

**Why the fact is not settled**

| Label | Means |
|---|---|
| `conflicted` | Two or more sources disagree, and the disagreement is unresolved |
| `unsupported` | **Searched and empty.** Someone looked where this fact should be recorded and it was not there |
| `open` | **Not yet investigated.** Nobody has looked |

`unsupported` and `open` are different findings. So are `possible` and `probable`. A scale that blurs either pair overstates what the evidence carries.

**A fact that cannot be traced to a record gets no label.** It is not a low-confidence fact. It is an unsourced claim, and it does not belong in the Index or Timeline.

### Result labels

The Research Quality Check section records one of two results:

| Result | Means |
|---|---|
| **COMPLETE FOR RIGHT NOW** | The research has done what the records in hand allow. Not "done forever." When a new record turns up, the ancestor opens again. |
| **NOT YET** | Something is still missing. The section lists what, as a finite, named list. |

Neither result certifies the research as true.

---

## 5. Rules every ARI follows

1. **One ancestor per inventory.**
2. **Seven sections, this order**, every time.
3. **Every fact traces to a record.** No source, no fact.
4. **Every fact carries one confidence label** from the vocabulary above.
5. **Negative results are recorded**, with source, method and return.
6. **Conflicts are stated**, never silently resolved.
7. **The ARI does not certify.** It describes and traces. The researcher reads it, checks it, and decides whether to stand behind it.
8. **Living persons.** An ARI records living people only with their knowledge. An ARI containing living people is not published or shared outside the household without their consent. Birth dates, addresses, medical detail and cause of death for anyone living are the researcher's to hold, not to post.

---

## 6. File metadata

Each file opens with YAML frontmatter:

```yaml
---
type: Ancestor Research Inventory   # or Timeline, Source, Conflicts, Research Log, Research Narrative, Research Quality Check
title: [Full name] ([birth year]–[death year])
description: One line.
tags: []
generated:
  by: human:[id]          # or the tool that produced it
  at: 2026-09-29T00:00:00Z
format: Ancestor Research Inventory v1.0 — Chronicle Makers · chroniclemakers.com/ancestor-research-inventory/
---
```

Source files add `resource:` (where the original lives) and a `verified:` block recording who checked the transcription against the image, and when. `generated.by` records whether a person or a tool produced the content, so a reader knows which lines were checked by a person.

---

## 7. Attribution

If you build a tool that reads or writes ARIs, teach the format, or publish an ARI:

- Call it the **Ancestor Research Inventory (ARI) from Chronicle Makers**
- Link to **[chroniclemakers.com/ancestor-research-inventory/](https://chroniclemakers.com/ancestor-research-inventory/)**
- Keep the `format:` line in the frontmatter

That is what CC BY 4.0 asks for, and it is how the next person finds the source.

**What you fill an ARI with is yours.** The license covers this specification and the templates. Your research, transcriptions, reasoning and narrative belong entirely to you.

---

*Ancestor Research Inventory (ARI™) · Chronicle Makers · Denyse Allen · chroniclemakers.com/ancestor-research-inventory/ · Specification v1.0, first published 2026-09-29 · CC BY 4.0*
