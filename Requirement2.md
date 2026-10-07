Audit my existing Resume Analyzer website and enhance it based on the feature requirements below.

IMPORTANT:

Do NOT rebuild the website from scratch.

First inspect the existing application and identify:

1. What features already exist
2. What features are partially implemented
3. What features are missing
4. What features are broken or not working correctly
5. What features can be improved

Then implement only the missing or incomplete functionality.

Do not remove or break existing functionality.

Preserve the existing design language, navigation, components, data structures and working features wherever possible.

---

# PRIMARY PRODUCT PURPOSE

The application should help a user answer:

> "I am currently a Tester. I want to become a Test Architect. What is missing from my resume, what should I add, and how can I make my resume stronger for the target role?"

It should combine:

**Resume Analysis + ATS Analysis + Career Gap Analysis + Target Role Analysis + AI-Like Writing Analysis + Resume Improvement Suggestions**

---

# 1. RESUME INPUT

Check whether the application supports:

### Upload

- PDF
- DOC
- DOCX
- TXT

### Paste

Large text box where users can paste their resume.

The user should be able to use either:

**Upload Resume**

OR

**Paste Resume Text**

Check:

- File validation
- File size validation
- Loading/progress indicator
- File name display
- Remove/replace file
- Error handling
- Empty input validation

If already implemented, test it rather than replacing it.

---

# 2. CURRENT ROLE

Check whether there is a field:

**Current Role**

Example:

`Tester`

It should support:

- Free text
- Suggested roles
- Editing
- Clear/reset

Suggested roles can include:

- Tester
- QA Engineer
- Automation Tester
- Senior QA Engineer
- QA Lead
- Test Lead
- Test Architect
- QA Manager
- Test Manager
- SDET
- Engineering Manager

Do not restrict users to predefined roles.

---

# 3. TARGET ROLE

Check whether there is:

**Target Role**

Example:

`Test Architect`

Support:

- Free text
- Suggested roles
- Multiple target roles
- Add/remove target role

Example:

Current Role:

**Tester**

Target Role:

**Test Architect**

This must be a core part of the analysis.

---

# 4. OPTIONAL JOB DESCRIPTION

Check whether the user can paste an optional Job Description.

Label:

**Target Job Description — Optional**

If provided, perform:

- ATS matching
- Keyword matching
- Skills matching
- Responsibility matching
- Experience matching
- Career-gap analysis

If no job description is provided, the application must still work using the target-role competency model.

---

# 5. MAIN ANALYSIS

Check whether the main CTA clearly communicates the purpose.

Preferred:

**Analyze My Career Gap**

or

**Analyze Resume & Career Gap**

After analysis, show a progress indicator while processing.

Handle failures gracefully.

---

# 6. OVERALL SCORE DASHBOARD

Check whether the dashboard displays meaningful scores.

At minimum:

### Overall Resume Score

Example:

**78 / 100**

### Target Role Readiness

Example:

**58%**

### ATS Compatibility

Example:

**82%**

### Skills Match

Example:

**71%**

### Experience Match

Example:

**64%**

### AI-Like Writing Indicator

Example:

**31%**

Use visual gauges/progress indicators.

Important:

These should be described as:

**AI-generated directional assessments**

They must NOT be presented as guaranteed or scientifically precise measurements.

---

# 7. CURRENT ROLE → TARGET ROLE

This is one of the most important features.

Show:

**Current Role**

Tester

↓

**Target Role**

Test Architect

Then provide a career-gap analysis.

Create three categories:

### 🟢 Strongly Demonstrated

Capabilities clearly supported by the resume.

### 🟡 Partially Demonstrated

Some evidence exists but the resume does not demonstrate the full capability.

### 🔴 Not Found / Needs Evidence

The resume does not contain sufficient evidence.

Example:

### Strong

- Functional Testing
- Automation
- Selenium
- API Testing
- SQL

### Partial

- Automation Framework
- CI/CD
- Technical Leadership

### Not Found

- Test Architecture
- Test Strategy
- Quality Engineering Strategy
- Governance
- Mentoring
- Architecture Decision Making

---

# 8. TARGET ROLE COMPETENCY MODEL

If the target role is:

**Test Architect**

the system should evaluate areas such as:

### Technical

- Automation Architecture
- Test Framework Design
- API Automation
- CI/CD
- Test Data Management
- Environment Strategy

### Architecture

- Framework Architecture
- Design Patterns
- Reusable Components
- Scalability
- Maintainability
- Tool Evaluation

### Strategy

- Test Strategy
- Automation Strategy
- Quality Strategy
- Risk-Based Testing
- Quality Governance

### Leadership

- Technical Leadership
- Mentoring
- Code Reviews
- Standards
- Technical Decision Making

### Business

- Stakeholder Management
- Quality Metrics
- Risk Communication
- Release Planning

The competency model must change according to the target role.

Do NOT hardcode Test Architect competencies for every role.

---

# 9. "WHAT IS MISSING FROM MY RESUME?"

Check whether the application provides actionable recommendations.

For every missing capability show:

### Capability

**Test Strategy**

### Status

🔴 Not Found

### Why It Matters

Explain why the capability matters for the target role.

### What to Add

Explain the type of real experience the user should document.

### Where to Add

Example:

`Professional Experience`

### Example Structure

Provide a sample structure, but do NOT invent the user's experience.

For example:

> If you have owned test strategy, describe the scope, decisions made, approach followed and outcome.

Important:

NEVER fabricate:

- Experience
- Projects
- Metrics
- Technologies
- Certifications
- Job responsibilities
- Employers

Use wording such as:

**"If applicable..."**

**"If you have this experience..."**

**"Not found in the provided resume."**

---

# 10. EXPERIENCE GAP ANALYSIS

Add a table like:

| Target Responsibility | Resume Evidence | Status | Recommendation |
|---|---|---|---|
| Test Strategy | Limited | 🟡 | Add strategy ownership |
| Automation Architecture | Strong | 🟢 | Add architecture details |
| Quality Governance | Not found | 🔴 | Add if applicable |
| Technical Leadership | Partial | 🟡 | Add decision-making examples |
| Mentoring | Not found | 🔴 | Add if applicable |

This must be based on actual resume evidence.

---

# 11. SKILLS GAP

Check whether the application distinguishes:

### Present

Skills clearly found.

### Partial

Related skills/evidence found.

### Missing

No evidence found.

Example:

**Present**

Selenium  
Java  
API Testing  
SQL

**Partial**

CI/CD  
Playwright

**Missing**

Test Architecture  
Quality Governance

Do not treat keyword presence alone as proof of expertise.

---

# 12. SEMANTIC MATCHING

Do NOT rely only on exact keyword matching.

Example:

Resume:

> "Designed reusable automation components."

Target requirement:

> "Automation Framework Architecture"

The system should recognize these as semantically related.

Show:

🟡 **Related evidence found**

Then explain:

> Your resume indicates related experience, but the architecture ownership is not explicit.

This is important.

---

# 13. ATS ANALYSIS

Check for:

- ATS readability
- Standard section headings
- Contact information
- Skills
- Experience
- Education
- Certifications
- Dates
- Formatting
- Tables
- Columns
- Images
- Icons
- Headers/footers
- Parsing problems

Display:

### ATS Score

**82 / 100**

Show warnings and recommendations.

Do not claim that the score guarantees compatibility with every ATS.

---

# 14. JOB DESCRIPTION MATCHING

If a Job Description is provided:

Display:

### Job Match

**78%**

Then:

### Matched

🟢 Selenium  
🟢 API Testing  
🟢 SQL

### Partially Matched

🟡 CI/CD  
🟡 Leadership

### Missing

🔴 Test Architecture  
🔴 Quality Strategy

Also distinguish:

**Keyword Found**

from:

**Demonstrated Experience**

This prevents keyword stuffing.

---

# 15. MISSING KEYWORDS

Create a keyword section.

Categorize:

### Technical

Test Architecture  
Automation Framework  
CI/CD

### Strategy

Test Strategy  
Quality Engineering  
Risk Management

### Leadership

Technical Leadership  
Mentoring  
Stakeholder Management

For every keyword explain:

**Why it matters**

**Where it could naturally appear**

Do not recommend keywords simply to increase the score.

---

# 16. ACHIEVEMENT ANALYSIS

Analyze experience bullets.

Check whether each bullet demonstrates:

- Action
- Ownership
- Technology
- Scope
- Complexity
- Result
- Business impact
- Quantifiable outcome

Example:

Current:

> Worked on Selenium automation.

Show:

### Achievement Strength

**42 / 100**

Problems:

- Limited ownership
- No scope
- No outcome
- No measurable impact

Then provide:

### How to Strengthen

> If accurate, describe what you automated, what you owned, the scope, technologies used and measurable outcome.

Do not invent numbers.

---

# 17. AI-LIKE WRITING ANALYSIS

Check whether this feature already exists.

If not, implement:

## AI-Like Writing Indicator

Example:

**34%**

Analyze:

- Generic wording
- Buzzwords
- Repetitive sentence structures
- Overly polished language
- Generic claims
- Lack of evidence
- Repeated phrases
- Corporate clichés
- Keyword stuffing

Do NOT call this a definitive AI detector.

Display:

> This is an AI-like writing style estimate, not proof that AI was used.

---

# 18. REDUCE AI-LIKE WRITING

This is a mandatory feature.

For suspicious sections show:

### Original

> Results-driven professional with a proven track record of delivering innovative solutions...

### Problems

- Generic
- Buzzword-heavy
- No evidence
- Formulaic

### Suggested Natural Version

Generate a more natural professional version while:

- Preserving facts
- Preserving meaning
- Preserving technical terminology
- Not adding achievements
- Not adding metrics
- Not adding experience
- Avoiding unnecessary synonyms
- Avoiding corporate buzzwords

Show:

**Before AI-like indicator: 72%**

**After AI-like indicator: 28%**

Again, clearly state that this is a style estimate.

---

# 19. BEFORE / AFTER COMPARISON

Allow users to compare:

### Original Resume

vs.

### Improved Resume

Highlight changed sentences.

For every change provide:

**Why changed**

Example:

> Reduced generic language and added specificity without introducing new facts.

Allow:

**Accept**

**Reject**

**Edit**

---

# 20. "MAKE MY RESUME MORE NATURAL"

Add a button:

**Make My Resume More Natural**

Options:

☑ Keep my facts  
☑ Keep my terminology  
☑ Don't invent metrics  
☑ Don't invent achievements  
☑ Avoid buzzwords  
☑ Keep professional tone  
☑ Preserve my writing style

Allow:

- Entire resume
- Selected section
- Selected bullet

---

# 21. RESUME SECTION ANALYSIS

Evaluate:

- Summary
- Skills
- Experience
- Projects
- Achievements
- Certifications
- Education
- Leadership

For each section show:

**Score**

**Problems**

**Recommendations**

---

# 22. PROFESSIONAL SUMMARY

Check:

- Current role clarity
- Target role alignment
- Seniority
- Technical strengths
- Leadership
- Achievements
- Differentiation

Provide:

**Summary Score**

and:

**What is missing**

Do not automatically rewrite unless requested.

---

# 23. CAREER READINESS

Create:

# Target Role Readiness

Example:

**58%**

Break down:

Technical capability  
Architecture capability  
Leadership  
Strategy  
Management  
Stakeholder management  
Domain alignment

Use a radar chart or horizontal bars.

---

# 24. TOP ACTIONS

Generate:

# Top 10 Resume Improvements

Example:

1. Add automation framework ownership.
2. Demonstrate architecture decisions.
3. Add test strategy experience.
4. Highlight CI/CD integration.
5. Add technical leadership examples.
6. Add mentoring experience.
7. Show measurable impact.
8. Add quality engineering initiatives.
9. Strengthen stakeholder management evidence.
10. Reduce generic/AI-like language.

The recommendations must be specific to:

**Current Role + Target Role + Resume**

They must NOT be generic advice.

---

# 25. PRIORITY SYSTEM

Use:

🔴 High Priority

🟠 Medium Priority

🟢 Low Priority

High-priority recommendations should be capabilities that materially affect target-role readiness.

---

# 26. ACCEPT / REJECT / EDIT

For every generated suggestion provide:

**✓ Accept**

**✕ Reject**

**✎ Edit**

Never overwrite the original resume without user approval.

---

# 27. MASTER RESUME

If the current application already supports resume versions, preserve it.

If not, consider adding:

### Master Resume

A comprehensive repository of the user's genuine:

- Experience
- Skills
- Projects
- Achievements
- Certifications
- Technologies
- Leadership experience

Then allow the system to generate role-specific versions:

**Test Architect Resume**

**QA Manager Resume**

**Automation Architect Resume**

**SDET Resume**

without inventing information.

This can be marked as a Phase 2 feature if implementing it now would significantly change the existing architecture.

---

# 28. MULTIPLE TARGET ROLES

Allow:

Current Role:

**Tester**

Target Roles:

- Test Architect
- QA Lead
- SDET
- QA Manager

Show:

| Target Role | Readiness |
|---|---:|
| SDET | 78% |
| QA Lead | 71% |
| Test Architect | 58% |
| QA Manager | 42% |

This helps the user understand realistic career paths.

---

# 29. CAREER ROADMAP

For a selected target role, optionally show:

**Current Role**

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

Clearly distinguish:

**Possible career progression**

from:

**Required career progression**

Do not imply that every user must follow this exact path.

---

# 30. SCORE IMPROVEMENT

After the user accepts recommendations, recalculate:

Before:

ATS: 67  
Target Role: 54  
AI-like Writing: 61%

After:

ATS: 82  
Target Role: 76  
AI-like Writing: 29%

Show:

**What improved?**

But do not artificially increase scores simply because text was changed.

Scores must be recalculated from the updated content.

---

# 31. REPORT EXPORT

Provide:

**Download Analysis Report**

Report should include:

- Overall score
- ATS score
- Target Role Readiness
- Skills gap
- Competency matrix
- Experience gaps
- Missing keywords
- AI-like writing analysis
- Before/after examples
- Recommendations
- Action plan

---

# 32. UI / UX AUDIT

While auditing the existing website, check:

### Usability

- Is the purpose immediately clear?
- Can the user understand what to enter?
- Is Current Role clearly separated from Target Role?
- Is the Analyze button obvious?
- Are results easy to understand?

### Visual hierarchy

Important information should appear first:

1. Target Role Readiness
2. Career Gap
3. Missing Capabilities
4. ATS
5. AI-like Writing
6. Detailed recommendations

### Responsive design

Test:

- Desktop
- Tablet
- Mobile

Fix overflow, broken cards, unreadable charts and tables.

---

# 33. DO NOT DUPLICATE EXISTING FEATURES

Before implementing anything:

Create an internal feature audit:

| Feature | Status | Action |
|---|---|---|
| Resume Upload | Existing | Keep |
| Paste Text | Existing | Keep |
| Current Role | Missing | Add |
| Target Role | Existing | Improve |
| ATS Score | Existing | Keep |
| Career Gap | Missing | Add |
| AI Writing | Partial | Improve |
| Natural Rewrite | Missing | Add |

Then implement only:

**Missing**

and

**Incomplete**

items.

Do not create duplicate components.

---

# 34. DO NOT BREAK EXISTING DATA

Preserve:

- Existing resume data
- Existing analysis results
- Existing user preferences
- Existing APIs
- Existing authentication
- Existing navigation
- Existing database structures

If an existing API can perform a required function, reuse it instead of creating another API.

---

# 35. FINAL AUDIT SCREEN

Add an internal/admin-style development summary after implementation:

## Feature Audit

### Existing & Working

List features that were already implemented.

### Improved

List features that were enhanced.

### Added

List newly implemented features.

### Still Pending

List features that require external API/backend support or are intentionally deferred.

### Bugs Fixed

List issues found and fixed.

Do not display this to normal end users unless a developer/debug mode exists.

---

# MOST IMPORTANT PRODUCT PRINCIPLE

The application should NOT be optimized simply to produce the highest ATS score.

The primary goal is:

**"Help the user understand the genuine gap between their current professional profile and their target role."**

The secondary goal is:

**"Help the user present their genuine experience more clearly and naturally."**

The system must never encourage the user to fabricate experience merely to improve a score.

---

# FINAL USER EXPERIENCE

The ideal flow is:

UPLOAD RESUME

↓

CURRENT ROLE

Tester

↓

TARGET ROLE

Test Architect

↓

OPTIONAL JOB DESCRIPTION

↓

ANALYZE

↓

### RESULTS

Target Role Readiness: **58%**

↓

### WHAT YOU ALREADY HAVE

Automation  
Selenium  
API Testing  
SQL

↓

### WHAT NEEDS STRENGTHENING

Framework Architecture  
CI/CD  
Technical Leadership

↓

### WHAT IS NOT FOUND

Test Strategy  
Quality Governance  
Architecture Ownership

↓

### WHAT TO ADD IF YOU HAVE THIS EXPERIENCE

Specific recommendations

↓

### ATS ANALYSIS

82%

↓

### AI-LIKE WRITING

34%

↓

### MAKE IT MORE NATURAL

Before → After

↓

### TOP 10 ACTIONS

Prioritized recommendations

↓

### DOWNLOAD REPORT