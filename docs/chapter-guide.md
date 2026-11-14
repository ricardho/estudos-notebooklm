# 📖 Chapter Guide — CTFL v4.0.1

**English** | [Português](chapter-guide.pt-BR.md)

A summary of the **ISTQB CTFL v4.0.1** syllabus, organized by chapter, with the exam weight of each chapter and the points that come up most often.

> **Sources:** *ISTQB Certified Tester Foundation Level Syllabus v4.0.1* (2024-09-15) and *ISTQB Exam Structures & Rules Tables v1.18* (2026-05-27), both at [istqb.org](https://istqb.org/). This guide is a study summary and does not replace the official syllabus.

---

## 🎯 The exam

| Item | Value |
|---|---|
| Questions | 40 (multiple choice, 1 point each) |
| Pass mark | 26 correct answers (65%) |
| Duration | 60 minutes (75 minutes when taken in a non-native language, +25%) |

### Weight of each chapter

| Chapter | Questions | K1 | K2 | K3 |
|---|:---:|:---:|:---:|:---:|
| 1. Fundamentals of Testing | 8 | 2 | 6 | 0 |
| 2. Testing Throughout the Software Development Lifecycle | 6 | 2 | 4 | 0 |
| 3. Static Testing | 4 | 2 | 2 | 0 |
| **4. Test Analysis and Design** | **11** | 0 | 6 | **5** |
| **5. Managing the Test Activities** | **9** | 1 | 5 | **3** |
| 6. Test Tools | 2 | 1 | 1 | 0 |
| **Total** | **40** | **8** | **24** | **8** |

**K-levels (knowledge levels):**
- **K1 — Remember:** recognize a term or concept.
- **K2 — Understand:** explain, compare, classify, give examples.
- **K3 — Apply:** use a technique in a concrete situation (for example, derive boundary values).

💡 **Strategy:** chapters 4 and 5 are worth 20 of the 40 questions, and all 8 K3 questions are in them. Practice the techniques with the [K3 exercises](k3-exercises.md).

---

## 1. Fundamentals of Testing — 8 questions

**Sections:** 1.1 What is Testing? · 1.2 Why is Testing Necessary? · 1.3 Testing Principles · 1.4 Test Activities, Testware and Test Roles · 1.5 Essential Skills and Good Practices in Testing

**Test objectives** (examples): evaluate work products, trigger failures and find defects, ensure required coverage, reduce the risk of inadequate quality, verify requirements, provide information for decisions, build confidence and validate that the test object works as stakeholders expect.

**Testing vs debugging:** testing triggers failures (dynamic testing) or finds defects directly (static testing). **Debugging** finds the cause of a failure, analyzes it and fixes it. **Confirmation testing** and **regression testing** follow the fix.

**Testing vs QA:** testing is **quality control** — product-oriented and corrective. **QA** (quality assurance) is **process**-oriented and preventive, and it is everyone's responsibility.

**Error → defect → failure:**
- **Error (mistake):** a human action that produces an incorrect result.
- **Defect (fault, bug):** an imperfection in a work product. It can be in code, a requirement or a test script.
- **Failure:** the system does not do what it should (or does something it shouldn't) when a defect is executed. Failures can also come from environmental conditions, such as radiation.
- **Root cause:** the fundamental reason for a problem, identified through root cause analysis.

**The 7 principles:**
1. Testing shows the presence, not the absence, of defects.
2. Exhaustive testing is impossible.
3. Early testing saves time and money.
4. Defects cluster together (Pareto principle).
5. Tests wear out (formerly the "pesticide paradox").
6. Testing is context dependent.
7. Absence-of-defects fallacy: defect-free software may still fail to meet users' needs.

**Test process activities:** planning · monitoring and control · analysis ("**what** to test") · design ("**how** to test") · implementation · execution · completion.

**Roles:** the **test management role** (planning, monitoring, control and completion) and the **testing role** (analysis, design, implementation and execution).

**Whole team approach:** any team member with the necessary skills can perform any task, and everyone is responsible for quality.

**Independence of testing:** it helps find different kinds of defects because of different biases, but it can isolate testers from the team and make developers lose their sense of responsibility for quality.

---

## 2. Testing Throughout the SDLC — 6 questions

**Sections:** 2.1 Testing in the Context of a Software Development Lifecycle · 2.2 Test Levels and Test Types · 2.3 Maintenance Testing

**Test-first approaches:**
- **TDD:** the test comes before the code.
- **ATDD:** tests are derived from the acceptance criteria.
- **BDD:** behavior is described in natural language, usually in the Given/When/Then format.

**DevOps:** CI/CD, fast feedback, automation and automated regression tests. **Shift left:** testing earlier in the lifecycle, for example by reviewing requirements and writing tests before code. **Retrospectives:** a mechanism for continuous process improvement.

**The 5 test levels:**

| Level | Focus |
|---|---|
| Component testing (unit) | A component in isolation, usually done by developers |
| Component integration testing | Interfaces and interactions between components |
| System testing | Behavior of the whole system, functional and non-functional |
| System integration testing | Interfaces with other systems and external services |
| Acceptance testing | Validation and readiness for deployment: UAT, operational, contractual, regulatory, alpha and beta |

**The 4 test types:** functional ("what") · non-functional ("how well" — ISO/IEC 25010: performance efficiency, compatibility, usability, reliability, security, maintainability, portability and safety) · black-box (specification-based) · white-box (structure-based). All of them can be applied at any level.

**Confirmation vs regression:**
- **Confirmation testing:** confirms that the original defect was fixed.
- **Regression testing:** confirms that the change caused no adverse side effects. It is a strong candidate for automation.

**Maintenance testing:** triggered by modifications, by upgrades or migrations of the operational environment and by the retirement of the system.

---

## 3. Static Testing — 4 questions

**Sections:** 3.1 Static Testing Basics · 3.2 Feedback and Review Process

**Static vs dynamic testing:** static testing **does not execute** the software. It finds **defects directly**, including in documents, and can find things dynamic testing cannot, such as unreachable code or maintainability problems. Dynamic testing triggers **failures**.

**Review process:** planning → review initiation → individual review → communication and analysis → fixing and reporting.

**Review roles:**
- **Manager:** decides what is reviewed and provides the resources.
- **Author:** creates and fixes the work product.
- **Moderator (facilitator):** runs the review meetings.
- **Scribe (recorder):** records anomalies and decisions.
- **Reviewer:** performs the review.
- **Review leader:** takes overall responsibility for the review; decides who takes part, when and where.

**Review types** (from least to most formal):

| Type | Led by | Key point |
|---|---|---|
| Informal review | — | No defined process or formal documented output; goal: detect anomalies |
| Walkthrough | **Author** | Many objectives: educate, gain consensus, generate ideas, detect anomalies |
| Technical review | **Moderator** | Technically qualified reviewers; consensus and technical decisions |
| Inspection | — | **The most formal**: follows the complete process, collects metrics, and the author **cannot** be the review leader or scribe |

---

## 4. Test Analysis and Design — 11 questions (5 K3)

**Sections:** 4.1 Test Techniques Overview · 4.2 Black-box · 4.3 White-box · 4.4 Experience-based · 4.5 Collaboration-based Test Approaches

| Category | Techniques | K-level |
|---|---|---|
| Black-box | Equivalence partitioning · Boundary value analysis (**2-value and 3-value**) · Decision table testing · State transition testing | **K3** |
| White-box | Statement testing · Branch testing | K2 |
| Experience-based | Error guessing · Exploratory testing · Checklist-based testing | K2 |
| Collaboration-based | Collaborative user story writing · Acceptance criteria · **ATDD** | K2 / **K3** (ATDD) |

**Points that come up most often:**
- **Boundary value analysis** only applies to **ordered** partitions.
  - **2-value:** the boundary and its closest neighbor in the adjacent partition.
  - **3-value:** the boundary and both of its neighbors.
- **Branch coverage subsumes statement coverage:** 100% branch coverage guarantees 100% statement coverage, but not the other way around.
- **State transitions:** all transitions coverage (which also attempts invalid transitions) is stronger than valid transitions (0-switch) coverage, which in turn is stronger than all states coverage.
- **User stories:** the 3 C's (Card, Conversation, Confirmation) and INVEST (Independent, Negotiable, Valuable, Estimable, Small, Testable).
- **Acceptance criteria:** can be **scenario-oriented** (Given/When/Then) or **rule-oriented** (verification list or input-output table).

➡️ Practice with the [K3 exercises](k3-exercises.md).

---

## 5. Managing the Test Activities — 9 questions (3 K3)

**Sections:** 5.1 Test Planning · 5.2 Risk Management · 5.3 Test Monitoring, Test Control and Test Completion · 5.4 Configuration Management · 5.5 Defect Management

**Entry vs exit criteria:**
- **Entry criteria:** preconditions for starting an activity.
- **Exit criteria:** what must be achieved to declare the activity complete.

In Agile, exit criteria correspond to the *Definition of Done*, and entry criteria to the *Definition of Ready*.

**Estimation techniques (K3):**
- **Estimation based on ratios:** uses data from previous projects, for example the ratio between development and test effort.
- **Extrapolation:** projects the remaining work from measurements of the current project.
- **Wideband Delphi:** experts estimate in isolation and repeat until they reach consensus. Planning Poker is a variant.
- **Three-point estimation:** **E = (a + 4m + b) / 6** and **SD = (b − a) / 6**.

**Test case prioritization (K3):** **risk**-based, **coverage**-based (including additional coverage) or **requirements**-based. Always respect **dependencies**: if a high-priority test depends on a low-priority one, the low-priority test runs first.

**Test pyramid:** the higher the layer, the lower the granularity, the lower the isolation and the longer the execution time.

**Testing quadrants (Marick):**

| | Support the team | Critique the product |
|---|---|---|
| **Business facing** | **Q2**: functional tests, examples, user story tests, UX prototypes, API testing, simulations | **Q3**: exploratory, usability, UAT |
| **Technology facing** | **Q1**: component and component integration (automated, in CI) | **Q4**: smoke tests and non-functional (except usability) |

**Risk:**
- **Risk level** = **likelihood × impact** in the quantitative approach, or a **risk matrix** in the qualitative approach.
- **Project risks** affect the management of the project, such as schedule, people and suppliers.
- **Product risks** affect the quality of the product.

**Defect report (K3):** identifier, title, date/author, test object and environment, context, description of the failure with steps to reproduce, expected vs actual results, severity, priority, status and references.

---

## 6. Test Tools — 2 questions

**Sections:** 6.1 Tool Support for Testing · 6.2 Benefits and Risks of Test Automation

- **Benefits of automation:** time saved on repetitive work, more consistency, objective measurements, easier access to information, faster feedback and more time for testers to design new, deeper tests.
- **Risks of automation:** unrealistic expectations, wrong time and cost estimates, using a tool where manual testing is more appropriate, relying too much on the tool, vendor dependency, abandoned open-source tools, incompatibility with the platform and choosing a tool that does not comply with regulatory or safety requirements.

---

📚 See also: [K3 exercises](k3-exercises.md) · [PT ↔ EN glossary](glossary.md) · [README](../README.md)
