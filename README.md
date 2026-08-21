# MBA Brain

MBA Brain is based on the published Master in Business Administration (MBA) program at [Saudi Electronic University (SEU)](https://seu.edu.sa/en/programs/master-in-business-administration-mba/about/). The program is offered through the Business Administration Department in the College of Administrative and Financial Sciences.

SEU describes the MBA as a blended-learning program that combines traditional and distance learning. The published study plan presents an English-taught curriculum of 12 courses, each worth 3 credit hours, totaling 36 credit hours across 4 semesters and 2 academic years. The curriculum connects management, economics, finance, accounting, leadership, strategy, performance, organizational change, operations, information technology, research, and international management.

The repository maps the 12-course MBA curriculum and the 4-course Pre-MBA preparatory semester to the skills below:

| Curriculum component         | Skill IDs                                 |
| ---------------------------- | ----------------------------------------- |
| Pre-MBA preparatory semester | `MGT490`, `ECON490`, `ACCT490`, `STAT490` |
| MBA Year 1, Semester 1       | `ECON500`, `RES500`, `FIN500`             |
| MBA Year 1, Semester 2       | `MGT560`, `MGT520`, `MGT510`              |
| MBA Year 2, Semester 3       | `ACT500`, `MGT521`, `MGT530`              |
| MBA Year 2, Semester 4       | `ECOM500`, `MGT675`, `MGT672`             |

This is a study-oriented repository mapping, not an official SEU publication or a replacement for the university's current requirements and study plan.

## Installation

Run these commands from the project where you want the textbook skills to be available. Install all skills with the [`skills` CLI](https://skills.sh/):

```bash
npx skills add iTzFaisal/MBA-Brain
```

After installation, call a skill with your agent. For example:

```text
/FIN500-Principles-of-Finance Evaluate this project's investment using capital budgeting,
NPV, and WACC. Explain the assumptions and cite the relevant framework.
```

## Course Skills

Each link opens the skill's `SKILL.md`, which is the entrypoint and index for that course.

| Skill                                                  | Textbook                                                                                                                                    | Entry point                                                                                |
| ------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| `ACCT490-Principles-of-Accounting`                     | _Financial Accounting: Information for Decisions_                                                                                           | [Open skill](.claude/skills/ACCT490-Principles-of-Accounting/SKILL.md)                     |
| `ACT500-Managerial-Accounting`                         | _Managerial Accounting_                                                                                                                     | [Open skill](.claude/skills/ACT500-Managerial-Accounting/SKILL.md)                         |
| `ECOM500-Business-and-Information-Technology`          | _Information Technology for Management: Driving Digital Transformation to Increase Local and Global Performance, Growth and Sustainability_ | [Open skill](.claude/skills/ECOM500-Business-and-Information-Technology/SKILL.md)          |
| `ECON490-Microeconomics`                               | _Economics: Principles, Applications, and Tools_                                                                                            | [Open skill](.claude/skills/ECON490-Microeconomics/SKILL.md)                               |
| `ECON500-Global-Economics`                             | _International Economics_                                                                                                                   | [Open skill](.claude/skills/ECON500-Global-Economics/SKILL.md)                             |
| `FIN500-Principles-of-Finance`                         | _Foundations of Finance: The Logic and Practice of Financial Management_                                                                    | [Open skill](.claude/skills/FIN500-Principles-of-Finance/SKILL.md)                         |
| `MGT490-Principles-of-Management`                      | _Management: A Practical Introduction_                                                                                                      | [Open skill](.claude/skills/MGT490-Principles-of-Management/SKILL.md)                      |
| `MGT510-Strategy-Planning`                             | _Contemporary Strategy Analysis_                                                                                                            | [Open skill](.claude/skills/MGT510-Strategy-Planning/SKILL.md)                             |
| `MGT520-Managing-Performance-for-Results`              | _Performance Management_                                                                                                                    | [Open skill](.claude/skills/MGT520-Managing-Performance-for-Results/SKILL.md)              |
| `MGT521-Managing-Dynamic-Environment`                  | _Organizational Change: An Action-Oriented Toolkit_                                                                                         | [Open skill](.claude/skills/MGT521-Managing-Dynamic-Environment/SKILL.md)                  |
| `MGT530-Operations-Management`                         | _Operations Management_                                                                                                                     | [Open skill](.claude/skills/MGT530-Operations-Management/SKILL.md)                         |
| `MGT560-Leadership-Development`                        | _Leadership: Theory and Practice_                                                                                                           | [Open skill](.claude/skills/MGT560-Leadership-Development/SKILL.md)                        |
| `MGT672-Decision-Theory-within-the-Global-Marketplace` | _International Management: Culture, Strategy, and Behavior_                                                                                 | [Open skill](.claude/skills/MGT672-Decision-Theory-within-the-Global-Marketplace/SKILL.md) |
| `MGT675-Research-Project`                              | _Literature Reviews Made Easy: A Quick Guide to Success_                                                                                    | [Open skill](.claude/skills/MGT675-Research-Project/SKILL.md)                              |
| `RES500-Academic-Writing-and-Research-Skills`          | _Business Research Methods_                                                                                                                 | [Open skill](.claude/skills/RES500-Academic-Writing-and-Research-Skills/SKILL.md)          |
| `STAT490-Statistics`                                   | _Elementary Statistics_                                                                                                                     | [Open skill](.claude/skills/STAT490-Statistics/SKILL.md)                                   |

## Skill Layout

Each course skill contains:

- `SKILL.md`: entrypoint, core frameworks, topic index, and chapter map
- `chapters/`: detailed chapter references and worked applications
- `cheatsheet.md`: compact formulas, definitions, and decision rules
- `glossary.md`: terminology and concise definitions
- `patterns.md`: repeatable procedures, trade-offs, and anti-patterns

The same skill corpus is available in both `.claude/skills/` and `.agents/skills/` for compatible agent environments. Keep the two directories synchronized when editing a skill.

## DISCLAIMER

These files are textbook syntheses and study aids. They do not replace current legal, regulatory, accounting, statistical, tax, safety, or other professional guidance. Verify time-sensitive standards, evidence, and jurisdiction-specific requirements before relying on an answer.
