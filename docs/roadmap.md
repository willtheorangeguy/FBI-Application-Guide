# FBI Application Guide — Roadmap

Gaps and limitations, observed from the repository. Concrete defects are in
[`internal/known-issues.md`](./internal/known-issues.md).

## The currency problem

Nothing records when a document was collected, which version it came from, or where it came
from. For a reference that tracks a process whose requirements genuinely change — eligibility
criteria, testing standards, fitness scoring — that is the most consequential gap here.

A dated manifest mapping each file to its source URL and retrieval date would let a reader
judge whether a document is still worth trusting, and would make refreshing the collection a
mechanical job rather than a research one.

## Licensing needs settling

The documents originate with federal agencies rather than with this repository, so the content
licence does not straightforwardly apply to them. See
[`internal/known-issues.md`](./internal/known-issues.md).

## Gaps

**No index of what is inside.** `0 - Title and Contents` exists, but there is no plain-text or
Markdown listing, so the collection cannot be searched or previewed from the browser — every
file is a binary that must be downloaded and opened.

**Stages 2, 5, and 6 all say "Testing Overview"** with nothing in the filename distinguishing
which phase each covers. Correct, and needlessly ambiguous.

**No coverage of outcomes.** The collection ends at the training academy overview; there is
nothing on what follows.

**Images are undescribed.** `images/` holds eleven numbered JPEGs with no captions and no
reference from any documentation, so their purpose is unclear.

## Non-goals

- **Being authoritative.** [fbijobs.gov](https://fbijobs.gov/) is the source of truth; this is
  an orientation aid.
- **Advice.** The collection arranges published material; it does not interpret it or
  recommend anything.
- **Automation.** There is no scraper and no update job, and adding one would need care given
  the material's provenance.
