# Quantum Trading

A **research platform** for finding a real trading edge while strictly
disciplining against **overfitting** and **systematic selection bias**. The point
is not to produce a pretty backtest — it is to tell a genuine effect from a lucky
one, and to stop an over-optimized hypothesis from going any further.

## How an idea travels

Every hypothesis goes through the same pipeline; it only moves one way, and each
step leaves a trail:

```
idea → hypothesis → data → screening → validation → paper → live → monitoring → research
```

## Platform layers

| Layer | Purpose |
|---|---|
| **Methodology** | Governing documents and rules of the game: validation protocol, hypothesis registry, trial accounting. Everything else obeys them. |
| **Data** | Append-only market-data ingestion and quality zones (RAW → CLEAN → RESEARCH). "Flag, don't fix" — raw data is never rewritten. |
| **Accounting** | Deterministic backtest accounting and config deduplication — the source of truth for the statistical gates. |
| **Infrastructure** | Reproducible cloud deployment by image pin: infrastructure knows the schedule, not the application code. |
| **Knowledge** | Distillation of books and papers into verified cheatsheets that feed the methodology. |

## Principles

- **Pre-registration** — hypotheses and known methodology gaps are recorded
  *before* the fact, so nothing can be justified after the result is in.
- **Append-only** — download, lose nothing, leave a trail.
- **A single quality gate** — the same checks locally, in pre-commit, and in CI.
- **Conventional Commits + automated releases** — versions and changelogs are
  machine-maintained.
- **Decisions via ADRs** — architectural decisions are immutable and superseded
  by new ones, never edited in place.

---

The organization's repositories are private.
