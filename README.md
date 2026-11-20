# SkillBridge: Career Readiness Portal

Skill gap analysis and career readiness for engineering students, the faculty who mentor them, and the teams who run career services. One single-file web app with three role-based views.

![Student skill gap analysis](screenshots/student-gap.png)

## What it does

| Role | What they get |
|------|---------------|
| **Student** | Profile, academics, marks and certificates; readiness score with badge; skill gap against a target role with a learning roadmap; analytics and what-if simulator; interview prep; opportunities with eligibility check; ATS resume export |
| **Faculty** | Mentee roster, readiness distribution, widest skill gaps, risk flags, mentor notes and meetings |
| **Administrator** | Batch and department comparison, placement outcomes, skill supply against employer demand, mentor assignment, account access |

| Faculty insights | Administrator: skills |
|---|---|
| ![Faculty insights](screenshots/faculty-insights.png) | ![Admin skills](screenshots/admin-skills.png) |

## Run it

No build step. Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000   # then visit http://localhost:8000
```

## Demo accounts

| Role | Username | Password |
|------|----------|----------|
| Student | `ananya.s` | `Student@2026` |
| Student | `rahul.m` | `Student@2026` |
| Faculty | `prof.nair` | `Faculty@2026` |
| Faculty | `prof.thomas` | `Faculty@2026` |
| Administrator | `admin` | `Admin@2026` |

## Limitations (prototype)

- **Sample data.** Cohort figures for faculty and administrators are synthetic.
- **Not secure authentication.** Sign-in and data storage run in the browser (`localStorage`). A real deployment needs a backend, college single sign-in and privacy controls for student data.
- **Interview tutor.** The Socratic tutor calls an AI service and works only where that service is available. Hosted on GitHub Pages it will not respond until you add your own backend proxy. Never put an API key in this file.
- Readiness weights are set by design and should be validated against past placement outcomes.

## Tech

Single HTML file with vanilla JavaScript and inline SVG charts. Fonts load from Google Fonts.
