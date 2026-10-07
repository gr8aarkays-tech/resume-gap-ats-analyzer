Build a modern web application called:

# Resume Career Gap & AI Writing Analyzer

## Core Purpose

The application must analyze a user's resume and answer TWO major questions:

### 1. Career Gap Analysis

**"I am currently a [Current Role]. I want to become a [Target Role]. What is missing from my resume/profile, and what should I add?"**

Example:

Current Role:
**Tester**

Target Role:
**Test Architect**

The application should analyze the resume against the expectations of a Test Architect and identify:

- Missing skills
- Missing responsibilities
- Missing technical capabilities
- Missing architecture experience
- Missing leadership experience
- Missing strategic responsibilities
- Missing tools/technologies
- Missing achievements
- Missing certifications
- Missing terminology
- Missing evidence of ownership
- Missing evidence of decision-making
- Missing evidence of mentoring/leadership

It must distinguish between:

**Already demonstrated**

**Partially demonstrated**

**Not found in resume**

Never assume the user has experience that is not present.

---

# 2. AI-WRITING ANALYSIS

The application must separately analyze whether parts of the resume contain:

- Generic language
- AI-like phrasing
- Excessive buzzwords
- Repetitive sentence structures
- Generic professional statements
- Overly polished/fabricated-sounding language
- Keyword stuffing
- Repetitive action verbs
- Corporate clichés
- Lack of specific evidence

IMPORTANT:

Do NOT claim that the application can scientifically determine whether text was written by AI.

Call this:

**AI-Like Writing Indicator**

not:

**AI Detector**

The result should be presented as an estimated writing-style signal.

---

# USER INPUT

Create a clean input screen.

## Resume

Allow:

### Upload

Supported:

- PDF
- DOC
- DOCX
- TXT

Drag and drop interface.

Also provide:

**Paste Resume Text**

with a large text area.

User can either upload a file or paste the resume.

---

# CURRENT ROLE

Field:

**What is your current role?**

Example:

`Tester`

Allow free text and role suggestions.

Examples:

- Tester
- QA Engineer
- Senior QA Engineer
- Automation Tester
- QA Lead
- Test Lead
- Test Architect
- QA Manager

---

# TARGET ROLE

Field:

**What role are you targeting?**

Example:

`Test Architect`

Allow free text.

Allow multiple target roles:

`+ Add Target Role`

---

# OPTIONAL JOB DESCRIPTION

Add:

**Have a specific job description?**

Optional textarea.

If provided, perform:

1. Career Gap Analysis
2. Target Role Analysis
3. Job Description Match
4. ATS Keyword Analysis

If not provided, use a role competency model generated from the target role.

---

# MAIN BUTTON

Large button:

**Analyze My Career Gap**

Secondary button:

**Analyze Resume Only**

---

# RESULT DASHBOARD

After analysis, show a dashboard.

## HEADER

Current Role:

**Tester**

↓

Target Role:

**Test Architect**

---

# SECTION 1 — OVERALL CAREER READINESS

Large circular gauge:

# 58%

**Target Role Readiness**

Below:

> Your resume currently demonstrates approximately 58% of the capabilities expected for a Test Architect.

Important:

Call this an:

**AI-generated directional assessment**

not an objective certification.

---

# SECTION 2 — WHAT YOU ALREADY HAVE

Title:

## Strongly Demonstrated

Show cards.

Example for Tester → Test Architect:

🟢 Test Execution  
🟢 Functional Testing  
🟢 Defect Management  
🟢 Test Automation  
🟢 API Testing  
🟢 SQL  
🟢 Selenium  
🟢 CI/CD

Each item should show evidence from the resume.

Example:

### Test Automation
**Strong**

Evidence:

"Created and maintained Selenium automation framework..."

Do not simply say the keyword exists.

Explain why the resume demonstrates the capability.

---

# SECTION 3 — PARTIALLY DEMONSTRATED

Title:

## You Have Some Evidence — Strengthen It

Example:

🟡 Automation Architecture

Current evidence:

"Developed automation scripts using Selenium."

Problem:

This demonstrates automation experience but does not clearly demonstrate architecture ownership.

Recommendation:

> Add examples of framework design, reusable components, design patterns, reporting architecture, CI/CD integration, framework governance or technical decisions — only if you actually performed these activities.

---

# SECTION 4 — MISSING FROM RESUME

Title:

# What You Need to Add for the Target Role

This is the most important section.

For Tester → Test Architect, evaluate areas such as:

### Architecture & Framework Design

Status:

🔴 Not Found

Recommendation:

> If you have designed automation frameworks, describe the architecture, design principles, reusable components, reporting, configuration, test data management and CI/CD integration you owned.

---

### Test Strategy

Status:

🔴 Not Found

Recommendation:

> Add examples where you defined test strategy, automation strategy, regression strategy, risk-based testing or quality approach.

---

### Technical Leadership

Status:

🟡 Partially Demonstrated

Recommendation:

> Show technical decisions you made, frameworks you designed, tools you evaluated and standards you introduced.

---

### Mentoring

Status:

🔴 Not Found

Recommendation:

> If applicable, mention mentoring junior testers, conducting technical training, code reviews or helping team members adopt automation practices.

---

### CI/CD Integration

Status:

🟡 Partially Demonstrated

Recommendation:

> Explain how automation was integrated into Jenkins/GitHub Actions/Azure DevOps or other pipelines, if applicable.

---

### Quality Engineering Strategy

Status:

🔴 Not Found

Recommendation:

> Add examples of defining quality engineering practices across the team or project, if you have done this.

---

# SECTION 5 — TEST ARCHITECT COMPETENCY MATRIX

Create a detailed matrix.

| Capability | Resume Evidence | Target Requirement | Gap |
|---|---|---|---|
| Manual Testing | Strong | Medium | 🟢 |
| Automation | Strong | High | 🟢 |
| Framework Design | Partial | Very High | 🟡 |
| Test Architecture | Missing | Very High | 🔴 |
| Test Strategy | Missing | Very High | 🔴 |
| CI/CD | Partial | High | 🟡 |
| API Testing | Strong | High | 🟢 |
| Database Testing | Strong | Medium | 🟢 |
| Design Patterns | Missing | High | 🔴 |
| Technical Leadership | Partial | High | 🟡 |
| Mentoring | Missing | Medium | 🔴 |
| Quality Governance | Missing | High | 🔴 |
| Risk Management | Partial | High | 🟡 |
| Stakeholder Management | Partial | High | 🟡 |

The exact competency model should change based on the selected target role.

---

# SECTION 6 — WHAT SHOULD I ADD TO MY RESUME?

Create the most actionable section:

# Recommended Resume Additions

Divide recommendations into:

### 🔴 High Priority

Things that could materially improve target-role positioning.

### 🟠 Medium Priority

Useful supporting evidence.

### 🟢 Low Priority

Polishing items.

Every recommendation must contain:

**What is missing**

**Why it matters**

**What type of evidence to add**

**Where to add it**

**Example structure**

---

# IMPORTANT — DO NOT INVENT EXPERIENCE

For example, if the user is a Tester and the resume does NOT show architecture experience:

DO NOT generate:

> "Designed enterprise-wide test architecture for 50 applications."

Instead say:

> "If you have designed automation frameworks, add a bullet describing the architecture, reusable components and technical decisions you owned."

The tool must help the user **document real experience**, not manufacture experience.

---

# SECTION 7 — EXPERIENCE TRANSFORMATION

For each important existing resume bullet, provide:

### Current

"Worked on Selenium automation."

### Problem

"Shows tool usage but does not demonstrate architecture or ownership."

### How to strengthen it

"If accurate, describe what you designed, owned, improved or standardized."

### Example Structure

"Designed and maintained a reusable Selenium automation framework supporting [X] applications, integrating [CI/CD/tooling] and improving [measurable outcome]."

Important:

If the metric is unknown, show:

`[add measurable result if available]`

Do NOT invent numbers.

---

# SECTION 8 — AI-LIKE WRITING ANALYSIS

Create a separate dashboard card:

# AI-Like Writing Indicator

Large gauge:

**34%**

Then:

### Human-like indicators

66%

### AI-like indicators

34%

Add disclaimer:

> This is a writing-style estimate, not proof that AI was used. AI detection is inherently uncertain.

---

# AI-LIKE ANALYSIS

Analyze:

- Generic phrases
- Repetitive structures
- Excessive buzzwords
- Overuse of words like "results-driven", "proven", "dynamic", "innovative"
- Generic claims without evidence
- Similar sentence patterns
- Excessive adjectives
- Repeated action verbs
- Artificially polished language
- Keyword stuffing

---

# SECTION 9 — REDUCE AI-LIKE WRITING

This is a major feature.

Title:

# Make My Resume More Natural

Show:

### Original

"Results-driven and highly accomplished professional with a proven track record of delivering innovative quality solutions and driving excellence across complex environments."

AI-like indicator:

🔴 High

Problems:

- Generic
- Buzzword-heavy
- No evidence
- Too many broad claims

Then show:

### Suggested Natural Version

"QA professional with experience in automation, test engineering and improving quality practices across complex applications."

AI-like indicator:

🟢 Lower

Important:

The rewrite must preserve the user's actual facts.

Do not introduce new achievements.

---

# SECTION 10 — BEFORE / AFTER AI WRITING SCORE

Show:

### Before

AI-like indicators:

**67%**

### After

AI-like indicators:

**24%**

Use a visual comparison.

Show exactly which sentences were changed.

---

# SECTION 11 — NATURAL WRITING RULES

Allow the user to select:

☑ Keep my original meaning

☑ Do not add achievements

☑ Do not invent metrics

☑ Keep technical terminology

☑ Keep company/product names

☑ Keep my actual experience

☑ Avoid corporate buzzwords

☑ Avoid overly polished language

☑ Use natural professional language

☑ Preserve my writing style

---

# SECTION 12 — ATS ANALYSIS

Show:

# ATS Compatibility

Example:

**84 / 100**

Analyze:

- Section headings
- Formatting
- Parsing
- Keywords
- Skills
- Job title alignment
- Experience relevance
- Education
- Certifications

If a job description exists, compare against it.

Show:

### Matched

✓ Selenium  
✓ API Testing  
✓ SQL  
✓ Automation

### Missing

❌ Test Architecture  
❌ Quality Strategy  
❌ Framework Design

---

# SECTION 13 — TARGET ROLE KEYWORDS

For the selected target role, generate a role-specific keyword map.

Example:

## Test Architect

### Architecture

Test Architecture  
Automation Framework  
Framework Design  
Design Patterns  
Reusable Components

### Quality

Quality Engineering  
Test Strategy  
Quality Strategy  
Risk-Based Testing  
Test Governance

### Technical

Selenium  
Playwright  
API Automation  
CI/CD  
Jenkins  
Git

### Leadership

Technical Leadership  
Mentoring  
Code Reviews  
Stakeholder Management

But:

Only recommend keywords that are genuinely relevant.

The system must never encourage keyword stuffing.

---

# SECTION 14 — CAREER ROADMAP

Show:

# Tester → Test Architect

Create a visual progression:

Tester

↓

Senior Tester

↓

Automation Engineer

↓

Senior Automation Engineer

↓

Test Lead

↓

Test Architect

Highlight:

**Your current position**

and

**Your target position**

Then show:

### Skills to develop

### Experience to demonstrate

### Resume evidence to add

### Possible certifications

### Leadership capabilities

---

# SECTION 15 — FINAL ACTION PLAN

Create:

# Your Top 10 Resume Improvements

Example:

1. Add automation framework ownership.
2. Demonstrate architecture decisions.
3. Add test strategy responsibilities.
4. Highlight CI/CD integration.
5. Add technical leadership examples.
6. Add mentoring experience.
7. Add design patterns/framework principles.
8. Add quality engineering initiatives.
9. Quantify measurable impact.
10. Reduce generic/AI-like wording.

Each item should link to the relevant resume section.

---

# SECTION 16 — FINAL DASHBOARD

At the top of the final result show:

┌─────────────────────────────────────┐
│ CURRENT ROLE                        │
│ Tester                              │
│                 ↓                   │
│ TARGET ROLE                        │
│ Test Architect                      │
└─────────────────────────────────────┘

### Career Readiness

# 58%

### ATS Score

# 78%

### Skills Match

# 64%

### Experience Match

# 61%

### AI-Like Writing Indicator

# 34%

Then:

🟢 **Strong Areas: 8**

🟡 **Needs Strengthening: 6**

🔴 **Missing/Not Found: 7**

---

# SECTION 17 — TWO DIFFERENT OUTPUT MODES

Provide two buttons:

### Analyze Only

Shows:

- Scores
- Gaps
- Missing skills
- Recommendations

### Improve My Resume

Generates:

**Suggested improved resume content**

but ALWAYS preserves:

- Existing facts
- Companies
- Dates
- Job titles
- Technologies
- Certifications
- Actual achievements

Never invent information.

---

# SECTION 18 — DOWNLOAD

Allow:

**Download Analysis Report**

PDF containing:

1. Current Role
2. Target Role
3. Career Readiness
4. Competency Matrix
5. Missing Skills
6. Resume Gaps
7. ATS Analysis
8. AI-Like Writing Analysis
9. Before/After writing examples
10. Recommended Resume Additions
11. Career Roadmap
12. Final Action Plan

Also provide:

**Copy Recommendations**

---

# UI DESIGN

Create a polished SaaS dashboard.

Use:

- Modern cards
- Circular gauges
- Progress bars
- Skill chips
- Green / yellow / red status indicators
- Expandable recommendations
- Before/after comparison
- Career progression diagram
- Interactive competency matrix
- Responsive design

Keep the interface simple enough that a user understands the result in less than 30 seconds.

---

# IMPORTANT DIFFERENTIATOR

The application is NOT just:

**"Is my resume ATS-friendly?"**

It is:

# "What is missing between who I am today and the role I want?"

And then:

# "How can I improve my resume without inventing anything?"

And finally:

# "How can I make my resume sound more naturally human while preserving my real experience?"

The complete workflow should therefore be:

**Upload/Paste Resume**

↓

**Enter Current Role**

↓

**Enter Target Role**

↓

**Optional Job Description**

↓

**Analyze Career Gap**

↓

**Identify Missing Capabilities**

↓

**Identify Missing Resume Evidence**

↓

**Identify ATS Gaps**

↓

**Identify AI-like Writing**

↓

**Suggest Natural Rewording**

↓

**Generate Prioritized Resume Improvement Plan**

↓

**Optionally generate improved resume content**

The application should prioritize **truthful, evidence-based recommendations** over simply maximizing ATS or AI-detection scores.