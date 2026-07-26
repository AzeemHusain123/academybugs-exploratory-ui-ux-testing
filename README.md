# AcademyBugs.com — Exploratory UI/UX & Functional Testing

Unscripted exploratory testing of [AcademyBugs.com](https://academybugs.com) — a uTest-built practice site with 25 real bugs deliberately planted across five categories. This project focuses on UI/UX-driven bug discovery using established usability heuristics, alongside general black-box exploratory techniques.

## 📋 Project Summary

| | |
|---|---|
| **Application Under Test** | AcademyBugs.com (uTest practice site) |
| **Testing Type** | Unscripted Exploratory Testing (Session-Based Test Management approach) |
| **Framework Used** | Nielsen's 10 Usability Heuristics + general error-guessing techniques |
| **Bugs Documented** | 18 (across all 5 site categories) |
| **Bugs Officially Registered** | 17 out of 25 planted bugs |
| **Tools Used** | Chrome DevTools (responsive layout check only — no root-cause analysis performed in this project) |

## 🎯 What This Project Demonstrates

- **Exploratory testing / Session-Based Test Management (SBTM)** — testing without pre-written scripts, guided instead by a test charter and structured heuristics
- **UI/UX-specific defect identification** using Nielsen's Usability Heuristics as a defensible framework, rather than subjective "this looks off" impressions
- **Verification over assumption** — the standout finding (Grand Total calculation error) was confirmed by manually recalculating displayed values rather than relying on visual impression alone
- **Coverage discipline** — using the site's own five bug categories (Functional, Visual, Content, Performance, Crash) as a checklist to avoid over-focusing on just one type of defect

## 🐞 Key Findings

| Category | Bugs Found | Highlight |
|---|---|---|
| Functional | 4 | Grand Total calculation error — $100 discrepancy, mathematically verified |
| Visual | 4 | Search box overlapping footer logo; loading spinner overlapping site header |
| Content | 5 | Untranslated Russian text; Lorem Ipsum placeholder left in product description |
| Performance | 2 | Billing address section stuck on an unresolved loading spinner |
| Crash | 3 | Three different actions (currency change, password retrieval, comment posting) each triggered a ~5-second site lockout |

Full details, expected vs. actual results, and screenshot evidence for each are in [Bug Reports Part 1](docs/AcademyBugs_Bug_Reports_Part_01.pdf) and [Part 2](docs/AcademyBugs_Bug_Reports_Part_02.pdf).

## 📁 Repository Structure

```
academybugs-exploratory-ui-ux-testing/
├── docs/
│   ├── AcademyBugs_Bug_Reports_Part_01.pdf
│   ├── AcademyBugs_Bug_Reports_Part_02.pdf
│   └── AcademyBugs_Exploratory_Testing_Summary.pdf
└── evidence/
    └── (18 screenshots referenced in the bug reports)
```

## 📄 Documents

- **[Bug Reports — Part 1](docs/AcademyBugs_Bug_Reports_Part_01.pdf)** — Content Bugs and Visual Bugs, with steps to reproduce, expected/actual results, and embedded screenshot evidence.
- **[Bug Reports — Part 2](docs/AcademyBugs_Bug_Reports_Part_02.pdf)** — Functional, Performance, and Crash Bugs, plus the Summary Table.
- **[Exploratory Testing Summary](docs/AcademyBugs_Exploratory_Testing_Summary.pdf)** — Test charter, approach, heuristics-to-findings mapping, session results, and coverage gaps.
- The `evidence/` folder holds the original screenshots as a backup reference, since they're already embedded directly in the Bug Reports PDFs.

## 🛠️ Methodology Note

This project intentionally differs from a scripted, requirement-based testing approach — there was no pre-written test plan or RTM, since AcademyBugs.com is a fixed practice environment rather than an application with evolving requirements. Instead, the focus was on demonstrating structured *exploratory* testing: using a clear charter, applying a recognized usability framework, and documenting findings with the same rigor as scripted test cases, just without the upfront script.

## 👤 Tester

**Azeem** — [LinkedIn](#) | [GitHub](#)

---
*Testing performed against a publicly available practice site (AcademyBugs.com by uTest), intentionally designed for QA skill-building and bug-hunting practice.*
