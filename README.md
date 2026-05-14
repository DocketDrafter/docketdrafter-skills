# DocketDrafter Skills

Public legal research and drafting skills from [DocketDrafter](https://www.docketdrafter.com/).

This repository is intended to be read by AI coding agents such as Codex or
Claude Code. A lawyer may simply provide this repository URL and ask the agent
to install the skill.

## Agent Install Instructions

When a user asks you to install this repository as a skill source, install each
top-level skill directory that contains a `SKILL.md`.

Repository URL:

```text
https://github.com/DocketDrafter/docketdrafter-skills
```

After installation, report:

- Which skills were installed
- Where they were installed
- Whether any files were skipped or already present

Do not modify the user's case files, working documents, or unrelated workspace
files while installing these skills.

## Agent Update Instructions

When a user asks you to update DocketDrafter skills, compare the installed skill
files against this repository.

Before changing files, report:

- Where the skills are installed
- Which files will change
- Whether any installed skill files appear locally modified

Do not overwrite locally modified skill files without asking the user first. Do
not modify the user's case files, working documents, or unrelated workspace
files while updating these skills.

## Available Skills

### New York Merchant Cash Advance

Folder: `ny-mca`

Installed skill name: `ny-mca`

This skill applies to New York merchant cash advance disputes, including:

- Loan-vs-purchase recharacterization
- Civil and criminal usury analysis
- Business records issues under CPLR 4518
- Confession-of-judgment and vacatur issues
- Breach-of-contract proof and damages disputes

The skill includes a source map, topic guides, statutes, and case materials so
the agent can ground analysis in primary legal authorities. Once installed, the
agent should invoke this skill automatically when the user's request involves
New York MCA issues.

## Legal Work Product Cautions

These skills are research and drafting aids. They are not a substitute for a
lawyer's professional judgment.

For any legal work product, the agent should remind the user to verify:

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
