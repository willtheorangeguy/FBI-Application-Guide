# Known Issues — FBI-Application-Guide

Concrete defects and gaps found while writing this repository's documentation in
August 2026. **Nothing here was changed** — each one needs a code, configuration, or
licensing decision rather than a documentation one.

Ordered by severity. See [`docs/roadmap.md`](../roadmap.md) for the narrative version,
which also covers deliberate non-goals.

**4 open:** 1 medium, 3 low.

## 1. CC BY 4.0 is applied to documents that originated with federal agencies

**Severity:** Medium
**Where:** `CONTENT_LICENSE.md`

**What:** The repository ships a Creative Commons Attribution 4.0 licence covering the content. The content is compiled from publicly available United States federal material — FBI, FBIJobs, and USCIS documents including the Federal Resume Guide and N-400 instructions.

**Why it matters:** CC BY 4.0 is a **grant**, and these documents were not this repository's to grant. It is the same problem the transcript archives had before they were given a provenance notice instead: applying a licence to third-party material asserts rights that are not held. US federal works are generally free of copyright, which makes the practical risk low and the statement no more accurate.

**Suggested fix:** Replace with a provenance notice on the model of the `*-Transcripts` repositories — stating where the material came from, that no rights in it are claimed, and that the MIT licence covers only the compilation and any original writing.

## 2. The feature list claimed a firearms manual that is not in the repository

**Severity:** Low
**Where:** `README.md` (previous version), Key Features

**What:** It listed "Includes the Glock 19 and 22 User Manual". No such file is tracked or present on disk.

**Why it matters:** A documented inclusion that does not exist, in a guide people may be downloading specifically for its contents.

**Suggested fix:** Removed from the feature list in this sweep. Recorded in case the document was meant to be added rather than the claim removed.

## 3. The README file tree did not match the actual filenames

**Severity:** Low
**Where:** `README.md` (previous version), How To Use

**What:** The tree listed `1-3 - FAQ.docx` beside `1-4 - FAQ.pdf` — the real file is `1-4 - FAQ.docx` — and `4-1 - Meet and Greet`, where the real file is `4-1 - Meet and Greet Session`.

**Why it matters:** A hand-maintained listing that had drifted from the directory it describes.

**Suggested fix:** Replaced with a stage table in `docs/usage.md` that describes coverage rather than restating filenames, so it cannot drift the same way.

## 4. The official FBI seal was used as the project logo

**Severity:** Low
**Where:** `README.md` (previous version), logo and credits table

**What:** The logo hot-linked the Seal of the Federal Bureau of Investigation from Wikimedia Commons.

**Why it matters:** 18 U.S.C. 709 restricts use of the FBI seal in a manner conveying the impression of official approval, and this is an explicitly unofficial guide. Separately, hot-linking Wikimedia is a fragile external dependency.

**Suggested fix:** Removed from the header in this sweep and replaced with a text heading plus an explicit Attribution section. Worth a look at the remaining credits-table usage.

---

## Also, across every repository

**`.bandit` is present on disk but untracked in git.** Verified in PyWorkout, treklogger,
skyscanner-cli, booking-cli, piggy, and aibot — the config file exists locally in each but
`git ls-files` does not know about it, so none of it reached GitHub.

The August 2026 security sweep therefore looks complete locally and landed nowhere. Worth
checking across all 44 repositories it covered.
