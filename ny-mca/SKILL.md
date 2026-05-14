---
name: ny-mca
description: Use for legal analysis, litigation work, drafting, issue spotting, or research involving New York merchant cash advance (MCA) disputes, including loan-vs-purchase recharacterization, usury, CPLR 4518 business records challenges, and breach-of-contract defenses.
---

# New York Merchant Cash Advance — Source Map

Use this skill when the user wants legal analysis, litigation support, drafting,
issue spotting, or research related to merchant cash advance disputes under New
York law. This skill maps bundled primary sources that can ground the analysis.

Read the relevant linked statutes and cases under `references/` before giving
substantive legal analysis. Do not rely only on the map summaries when the exact
source text matters.

## Path Resolution

All relative paths in this skill are relative to this skill directory, not the
user's current working directory.

When opening linked primary sources, first identify the directory containing
this `SKILL.md`, then resolve paths such as `references/...` against that
directory.

## Output Source Links

When citing bundled authorities in an answer, include clickable public source
links where available.

- For CourtListener cases, use the `source_url` field in the source file's YAML
  frontmatter.
- For Justia and Google Scholar cases, use the `source_url` field in the source
  file's YAML frontmatter.
- For statutes, use the `source` field in the source file's YAML frontmatter.
- Prefer linking the case name, statute, or citation in the prose rather than
  listing raw URLs separately. Do NOT link to the local file — link to the URL
  so the user can visit the actual primary source.

---

## I. Statutory Framework

### Usury Statutes

- [N.Y. General Obligations Law § 5-501](<references/statutes/NY/GOB/5-501.txt>) — Rate of interest; definitions
- [N.Y. General Obligations Law § 5-511](<references/statutes/NY/GOB/5-511.txt>) — Usurious contracts void
- [N.Y. General Obligations Law § 5-521](<references/statutes/NY/GOB/5-521.txt>) — Defense of usury; corporate borrowers and criminal usury exception
- [N.Y. Banking Law § 14-a](<references/statutes/NY/BNK/14-A.txt>) — Maximum rate of interest
- [N.Y. Penal Law § 190.40](<references/statutes/NY/PEN/190.40.txt>) — Criminal usury in the second degree (25% threshold)

### Civil Practice

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

- [Loan vs. Purchase — The Three-Factor Test](<topics/loan-vs-purchase.md>) — Whether an MCA is a disguised loan; usury; reconciliation; finite term; bankruptcy recourse. 19 cases covering both sides, including the foundational Court of Appeals and substance-over-form authorities and recent trial and appellate decisions.
- [Usury Calculation](<topics/usury-calculation.md>) — How to compute the effective annual interest rate using `python3 -c`; single agreements and stacked deals where proceeds pay down a prior balance. Read this before performing any APR math.
- [Breach Proof and Summary Judgment Mechanics](<topics/breach-proof.md>) — What MCA plaintiffs must prove after surviving the usury fight; prima facie burden on breach and damages; how factual disputes on damages defeat summary judgment. 5 core cases with a strong 2025 Fourth Department line.
- [Business Records — CPLR 4518](<topics/business-records.md>) — Foundation requirements for payment histories and ACH records; third-party records; affiant qualifications. 6 core cases.
