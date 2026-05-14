# DocketDrafter Skills

Public legal research and drafting skills from [DocketDrafter](https://www.docketdrafter.com/).

These skills are meant to be installed and used by an AI coding agent such as
Codex or Claude Code. You do not need to understand GitHub to use them. Give
your agent the link to this repository and the prompt below.

## Install

Paste this into Codex, Claude Code, or another coding agent:

```text
Install the DocketDrafter public skills from this GitHub repository:

https://github.com/DocketDrafter/docketdrafter-skills

After installing, tell me which skills are available and where you installed
them. Do not modify my case files or working documents unless I ask you to.
```

## Update

Paste this into Codex, Claude Code, or another coding agent when you want to
check for updates:

```text
Check whether my installed DocketDrafter skills are up to date with:

https://github.com/DocketDrafter/docketdrafter-skills

If they are outdated, update the installed skill files from the repository.
Before changing anything, show me:

1. where the skills are installed,
2. what files will change,
3. whether any local files appear modified.

Do not overwrite my case files or working documents. Do not overwrite locally
modified skill files without asking me first.
```

## Available Skills

### New York Merchant Cash Advance

Folder: `ny-mca`

Use this skill for New York merchant cash advance disputes, including:

- Loan-vs-purchase recharacterization
- Civil and criminal usury analysis
- Business records issues under CPLR 4518
- Confession-of-judgment and vacatur issues
- Breach-of-contract proof and damages disputes

The skill includes a source map, topic guides, statutes, and case materials so
your agent can ground its analysis in primary legal authorities.

## How To Use A Skill

After installation, ask your agent a normal legal-work question. For example:

```text
Use the New York merchant cash advance skill to analyze whether this agreement
could be recharacterized as a loan under New York law. Read the relevant bundled
authorities before answering, cite the sources you rely on, and identify what
facts would matter most.
```

You can also ask for drafting help:

```text
Use the New York merchant cash advance skill to draft argument points for an
opposition to summary judgment. Focus on usury, reconciliation, finite term,
recourse, and business-records foundation issues. Cite the authorities you rely
on.
```

## Important Notes For Lawyers

These skills are research and drafting aids. They are not a substitute for a
lawyer's professional judgment.

Before filing or sending work product, verify:

- The governing law and venue
- The current status of every cited case, statute, and rule
- Whether any authority has been amended, reversed, limited, distinguished, or
  superseded
- Whether the facts in your matter match the cases being cited
- Whether local rules, judge-specific rules, deadlines, and procedural posture
  change the analysis

AI tools can make mistakes, omit contrary authority, or misunderstand a record.
Treat the output as a draft research memo, not as final legal advice.

## License

This repository is licensed under the [MIT License](LICENSE).

## Support

Learn more at [docketdrafter.com](https://www.docketdrafter.com/).
