---
name: ny-mca
description: Use for legal analysis, litigation work, drafting, issue spotting, or research involving New York merchant cash advance (MCA) disputes, including loan-vs-purchase recharacterization, usury, defense-side motions to dismiss, default judgment or judgment-by-confession vacatur, CPLR 4518 business records challenges, and breach-of-contract defenses.
---

# New York Merchant Cash Advance — Source Map

Use this skill when the user wants legal analysis, litigation support, drafting,
issue spotting, or research related to merchant cash advance disputes under New
York law. This skill maps bundled primary sources that can ground the analysis.

Read the relevant linked statutes and cases under `references/` before giving
substantive legal analysis. Topic annotations and case headnotes are routing
aids only; do not rely on them when the exact source text matters.

## Source Links — REQUIRED

ALWAYS include clickable public source links when citing cases or statutes in
any response. This is not optional.

Topic files are pre-formatted to make this trivial. Each case is listed as:

```
[Case Name](<PUBLIC_URL>) ([bundle](<../references/cases/<id>/>)) — ...
```

When citing, **copy the case-name link verbatim** — the URL in that link is
the canonical public source. Do not modify, shorten, or substitute it. Do not
invent URLs to LexisNexis, Westlaw, or any other source. The `[bundle]` link
points to the local case folder containing `opinion.md`, `metadata.yaml`, and
`headnotes.txt` — open it only when you need the full opinion or extra
metadata.

For statutes, use the linked path in this SKILL.md and cite using the
`source_url` field inside that source file's metadata.

If a citation in a topic file is missing its public URL for any reason, fall
back to the `source_url` field in the case's `metadata.yaml`. Never fabricate
a URL.

## Path Resolution

All relative paths in this skill are relative to this skill directory, not the
user's current working directory.

When opening linked primary sources, first identify the directory containing
this `SKILL.md`, then resolve paths such as `references/...` against that
directory.

## Case Bundles

All cases live under `references/cases/<case-id>/`, where the case ID is a
stable source-derived ID. CourtListener cases use the format
`cl-<opinion-id>-<slug>` (e.g.
`cl-9432148-crystal-springs-capital-inc-v-big-thicket-coin-llc`); other
sources use IDs like `justia-2021-ny-slip-op-50221-u`,
`gs-2019-ny-slip-op-32651`, or `manual-2022-us-dist-lexis-100837`.

Each case folder contains:

- `metadata.yaml` — normalized metadata, citations, court/date, and public
  `source_url`
- `headnotes.txt` — short neutral headnote for triage
- `opinion.md` — full converted opinion text

When a topic links to a case folder, read `headnotes.txt` first if you only need
to decide whether the case is relevant. Read `metadata.yaml` for full citation
details (and for the `source_url` of non-CourtListener cases when the topic
file does not inline it — see Source Links above). Read `opinion.md` before
relying on the case for legal analysis, quotes, drafting, or any contested
proposition.

---

## I. Statutory Framework

### Usury Statutes

- [N.Y. General Obligations Law § 5-501](<references/statutes/NY/GOB/5-501.txt>) — Rate of interest; definitions
- [N.Y. General Obligations Law § 5-511](<references/statutes/NY/GOB/5-511.txt>) — Usurious contracts void
- [N.Y. General Obligations Law § 5-521](<references/statutes/NY/GOB/5-521.txt>) — Defense of usury; corporate borrowers and criminal usury exception
- [N.Y. Banking Law § 14-a](<references/statutes/NY/BNK/14-A.txt>) — Maximum rate of interest
- [N.Y. Penal Law § 190.40](<references/statutes/NY/PEN/190.40.txt>) — Criminal usury in the second degree (25% threshold)

### Civil Practice

- [CPLR § 317](<references/statutes/NY/CVP/317.txt>) — Defense by person to whom summons was not personally delivered
- [CPLR § 3211](<references/statutes/NY/CVP/3211.txt>) — Motion to dismiss
- [CPLR § 3218](<references/statutes/NY/CVP/3218.txt>) — Judgment by confession
- [CPLR § 4518](<references/statutes/NY/CVP/4518.txt>) — Business records exception to hearsay rule
- [CPLR § 5015](<references/statutes/NY/CVP/5015.txt>) — Relief from judgment or order (vacatur)

### Uniform Commercial Code

- [N.Y. U.C.C. § 9-109](<references/statutes/NY/UCC/9-109.txt>) — Article 9 scope; sales of accounts and payment intangibles

---

## II. Topics

Read the topic file relevant to the user's question before giving substantive
analysis. Each topic file contains a doctrinal overview, case annotations with
distinguishing details, and practical guidance.

- [Loan vs. Purchase — The Three-Factor Test](<topics/loan-vs-purchase.md>) — Whether an MCA is a disguised loan; usury; reconciliation; finite term; bankruptcy recourse. Covers both sides, including foundational Court of Appeals and substance-over-form authorities and recent trial and appellate decisions.
- [Usury Calculation](<topics/usury-calculation.md>) — How to compute the effective annual interest rate using `python3 -c`; single agreements and stacked deals where proceeds pay down a prior balance. Read this before performing any APR math.
- [Defense-Side Motions to Dismiss](<topics/defense-motion-to-dismiss.md>) — CPLR 3211 dismissal and opposition strategy for MCA defendants; documentary-evidence usury motions, pleading-stage limits, jurisdiction/capacity challenges, and individual-guarantor personal jurisdiction.
- [Default Judgments and Judgments by Confession](<topics/default-vacatur.md>) — CPLR 317, CPLR 5015, interest-of-justice vacatur, CPLR 3218 judgments by confession, plenary-action requirements, and MCA-specific vacatur cases.
- [Breach Proof and Summary Judgment Mechanics](<topics/breach-proof.md>) — What MCA plaintiffs must prove after surviving the usury fight; prima facie burden on breach and damages; how factual disputes on damages defeat summary judgment. 5 core cases with a strong 2025 Fourth Department line.
- [Business Records — CPLR 4518](<topics/business-records.md>) — Foundation requirements for payment histories and ACH records; third-party records; affiant qualifications. 6 core cases.
