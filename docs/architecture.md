# FBI Application Guide — Architecture

## A document collection, not software

```text
0 - Title and Contents.{docx,pdf}
Step1/  1-1 … 1-4
Step2/  2-1
Step3/  3-1 … 3-4
Step4/  4-1
Step5/  5-1
Step6/  6-1 … 6-3
Step7/  7-1
Step8/  8-1
Step9/  9-1, 9-2
images/
```

No build, no code, no dependencies. The organisation *is* the product — the value added over
the source material is arrangement and sequencing.

## The numbering carries the structure

Files are named `<step>-<item> - <title>`, so `3-4 - N-400 Instructions` is the fourth item of
Step 3. The folder and the filename prefix agree, which means a file dragged out of its folder
still says where it belongs.

That redundancy is worth keeping. A loose PDF in a downloads folder is otherwise unidentifiable.

## Both formats, on purpose

Every document ships as `.docx` and `.pdf`. Not redundancy — different jobs:

| Format | For |
|---|---|
| `.docx` | Filling in worksheets, adapting the resume guide, annotating |
| `.pdf` | Reading and sharing with fixed layout |

Step 3's citizenship worksheets and Step 1's Federal Resume Guide are the clearest case: they
are templates meant to be completed, so an editable copy is the point rather than a
convenience.

## Repeated titles are not duplicates

"Testing Overview" appears in Steps 2, 5, and 6 because testing happens at several points in
the process. Each covers its own phase.

## Provenance

The material is compiled from publicly available United States federal sources — the FBI,
FBIJobs, and USCIS. This repository arranges and republishes; it does not author.

That distinction drives the licensing question in
[`internal/known-issues.md`](./internal/known-issues.md): a licence granted here cannot cover
material that originated elsewhere.

## No currency mechanism

Nothing records when a document was collected, which version it came from, or whether the
source has since changed. There is no dated index and no link from a file back to the page it
came from.

For a reference tracking a process whose requirements change, that is the most consequential
structural gap — see [Roadmap](./roadmap.md).

## Images

`images/` holds illustrations, including the process diagram used as the README hero. That one
is now served from `.github/icons/` so it renders consistently across GitHub and any mirror.
