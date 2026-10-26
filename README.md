# Gulf CV Skill (UAE & KSA)

An open-source [Agent Skill](https://docs.claude.com) that teaches an AI assistant to write, tailor and review CVs for jobs in the Gulf (GCC), with a focus on the **United Arab Emirates** and **Saudi Arabia**.

Gulf recruiters filter candidates on eligibility details (visa status, nationality, location, notice period) before they read experience. Most CV templates are built for US or European markets and miss these fields. This skill fixes that.

## What it does

- Asks for the Gulf-specific details a CV needs (visa/Iqama status, notice period, attestation, languages)
- Produces **two versions** of every CV:
  - **ATS version:** single column, no photo, no date of birth, for company portals and multinationals
  - **Direct version:** adds photo and personal details, for recruiters, agencies and regional job boards
- Puts recruiter filter fields in plain text in the top third of page one
- Applies UAE rules (visa status, MOFA degree attestation, Bayt/GulfTalent/Naukrigulf keywords)
- Applies KSA rules (Vision 2030 alignment, SSCO-compatible job titles, Professional Accreditation, Iqama transferability)
- Never invents facts, dates or credentials; lists open questions instead

## Repository layout

```
gulf-cv-skill/
├── gulf-cv/
│   └── SKILL.md      the skill
├── README.md
└── LICENSE
```

## Installation

**Claude.ai (web or desktop):** zip the `gulf-cv` folder and upload it as a custom skill in Settings. It then loads automatically when you ask for a UAE or Saudi CV.

**Claude Code:** copy the `gulf-cv` folder into your skills directory (for example `~/.claude/skills/gulf-cv/`).

**Other agents:** any tool that supports the `SKILL.md` format can load the folder directly. You can also paste the contents of `SKILL.md` into a system prompt.

## Example prompts

- "Write a Gulf CV for a data analyst role in Dubai. Here is my current CV: ..."
- "Tailor my CV to this Riyadh job posting and give me both versions."
- "Review my CV for Saudi Arabia jobs. What would a Gulf recruiter reject?"

## Disclaimer

This skill is based on recruiter guides, CV services and job-board advice published in 2025 and 2026, cross-checked where they disagree. It is not legal or immigration advice. Gulf hiring rules (Emiratisation, Saudization, visa types, attestation steps) change, so confirm requirements with the employer or official government sources before applying.

## Research sources

The skill is written in original wording, informed by:

- VisualCV: Gulf CV (GCC) guide
- LoopCV: Gulf CV format vs Western resumes
- Labeeb: UAE and Saudi ATS CV guides
- ATS Verification: UAE and Saudi Arabia resume format guides (2026)
- Jobera, Saudi Life Guide, Resumly: Saudi CV guides
- Hireflow: ATS checks for UAE job seekers
- Gulf News: Saudi Professional Accreditation Programme
- Boskalis Careers: degree attestation for the UAE

## Contributing

Issues and pull requests are welcome, especially for other GCC countries (Qatar, Kuwait, Oman, Bahrain) or rule changes.

## License

MIT. See [LICENSE](LICENSE).
