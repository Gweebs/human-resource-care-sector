# Installation Guide

This guide explains how to use this repository with ChatGPT and Codex.

The repository can be used in three ways:

1. As a reference pack in ChatGPT
2. As a local project in Codex
3. As a reusable Codex skill

## 1. Use With ChatGPT

Use this option when you want ChatGPT to help draft or review HR disciplinary documents using the repository material.

### Option A: Upload The Files

1. Download the repository from GitHub.
2. Upload the relevant files into ChatGPT.
3. Tell ChatGPT which file to use as the main source.

Good starting files:

| Task | Upload |
|---|---|
| Full process guidance | `process/master-brief.md`, `process/process-map.md`, `process/decision-tree.md` |
| Care-sector guidance | `care-sector/care-sector-master-brief.md`, `care-sector/care-sector-version.md` |
| Welfare meeting record | `templates/welfare-meeting-record.md`, `process/absence-management-and-bradford-factor.md` |
| Investigation support | `care-sector/care-sector-investigations-guide.md`, `process/checklist.md` |
| Policy drafting | `templates/policy-template-formal.md`, `handbook/handbook-integration-notes.md` |
| Figma guide | `figma/figma-disciplinary-process-guide.md` |
| Skills for Care context | `sources/skills-for-care-managing-people.md` |

Example prompt:

```text
Use these uploaded files as the source. Draft a matter of concern note for a care assistant who has repeatedly missed care notes. Keep it informal, factual, and suitable for a UK care home manager.
```

### Option B: Use The GitHub Link

Give ChatGPT the repository link and ask it to review the files if web or connector access is available.

Repository:

```text
https://github.com/Gweebs/human-resource-care-sector
```

Example prompt:

```text
Use the repository at https://github.com/Gweebs/human-resource-care-sector as the source. Explain the disciplinary escalation route for a UK care-sector manager.
```

If ChatGPT cannot access the repository directly, upload the relevant files instead.

## 2. Use Locally With Codex

Use this option when you want Codex to work directly with the project files.

Clone the repository:

```bash
git clone https://github.com/Gweebs/human-resource-care-sector.git
cd human-resource-care-sector
```

Then ask Codex to use the repository as the source.

Example prompt:

```text
Use the local files in this repository as the source. Draft a manager guide for records of conversation, supervision, matters of concern, investigation, outcome, and appeal.
```

Good local starting points:

```text
README.md
INDEX.md
process/master-brief.md
care-sector/care-sector-master-brief.md
figma/figma-disciplinary-process-guide.md
```

## 3. Install The Reusable Codex Skill

Use this option when you want the disciplinary process pack available as a reusable Codex skill.

The skill is here:

```text
skills/care-sector-hr-disciplinary/
```

Copy it into your Codex skills directory:

```bash
cp -R skills/care-sector-hr-disciplinary ~/.codex/skills/
```

Restart Codex if needed.

Then invoke the skill:

```text
$care-sector-hr-disciplinary
```

Example prompt:

```text
Use $care-sector-hr-disciplinary to draft a disciplinary investigation plan for a medication documentation concern in a UK care home.
```

## 4. Validate The Skill

If you have the Codex skill validation script available, run:

```bash
python3 ~/.codex/skills/.system/skill-creator/scripts/quick_validate.py ~/.codex/skills/care-sector-hr-disciplinary
```

Expected result:

```text
Skill is valid!
```

If that script is not available, check manually that these files exist:

```text
~/.codex/skills/care-sector-hr-disciplinary/SKILL.md
~/.codex/skills/care-sector-hr-disciplinary/agents/openai.yaml
~/.codex/skills/care-sector-hr-disciplinary/references/process.md
~/.codex/skills/care-sector-hr-disciplinary/references/care-sector.md
~/.codex/skills/care-sector-hr-disciplinary/references/handbook-alignment.md
~/.codex/skills/care-sector-hr-disciplinary/references/templates-and-outputs.md
~/.codex/skills/care-sector-hr-disciplinary/references/sources-and-boundaries.md
```

## 5. Recommended First Prompts

For ChatGPT:

```text
Use the uploaded repository files as the source. I need a plain English guide for UK care home managers on records of conversation, supervision, matters of concern, investigations, disciplinary meetings, outcomes, and appeals.
```

For Codex in the repository:

```text
Use this repository as the source. Review the disciplinary process pack and create a copy-ready manager checklist for care-sector disciplinaries.
```

For the installed skill:

```text
Use $care-sector-hr-disciplinary to draft a record of conversation for a repeated lateness concern affecting handover.
```

## 6. Use Boundaries

This repository and skill provide HR process and drafting support. They are not legal advice.

Check current Acas, GOV.UK, local policy, contract wording, safeguarding duties, CQC requirements, and legal advice where needed, especially for:

- dismissal
- summary dismissal
- gross misconduct
- safeguarding
- medication errors
- falsified records
- whistleblowing
- discrimination
- sickness or disability
- protected characteristics
- agency, bank, or contractor status

Next step: open `README.md` for the repository overview or `skills/care-sector-hr-disciplinary/SKILL.md` for the reusable skill.
