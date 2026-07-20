# 📝 PMG201c – ANSWER KEY (All 5 Practice Exam Sets)

> [!important]
> ❗ This is a reference answer for study purposes. In your real exam, always rephrase in your own words and stay closely tied to the specific scenario given!

---

## 🏫 EXAM 1 – STUDENT CLUB MANAGEMENT SYSTEM – ANSWERS

**Scenario Summary:** Build an online Club Management System (CMS) for FPT University | 4 months | $12,000 | ≥200 active student users in Month 1 | System uptime ≥99.5% | Response time <2s

---

### Request 1 (20%) – Stakeholders

| # | Name / Role | Detailed Responsibilities | Internal / External | Power/Interest Grid | Management Strategy |
|---|-------------|--------------------------|---------------------|---------------------|---------------------|
| 1 | **Project Sponsor** (FPT University Board) | Approves the $12,000 budget, signs off the project charter, makes strategic decisions for the project, and authorizes any major scope changes. Acts as the highest authority when disputes arise. | External | High Power / High Interest | **Manage Closely** – weekly status updates, involved in all key decisions |
| 2 | **Project Manager (PM)** | Plans the full 4-month schedule, allocates resources, tracks progress and budget, manages risks, and submits weekly status reports to the Sponsor. Ensures the project is delivered on time and within scope. | Internal | High Power / High Interest | **Manage Closely** – daily standups, controls overall progress |
| 3 | **Developer Team** | Designs system architecture, implements backend/frontend code, integrates the database, and ensures non-functional requirements are met (response time <2s, uptime ≥99.5%). Also responsible for unit testing. | Internal | Low Power / High Interest | **Keep Informed** – daily task updates, flag technical blockers immediately |
| 4 | **QA / Tester** | Writes the test plan and test cases for all modules (club registration, activity tracking, attendance, dashboard). Performs performance, load, and stress testing to verify uptime ≥99.5%. | Internal | Low Power / High Interest | **Keep Informed** – test results shared after each sprint |
| 5 | **Club Administrators** | Primary power users of the admin side – manage activity schedules, take attendance, generate club reports. Provide functional requirements during the analysis phase and validate features during UAT. | External | Low Power / High Interest | **Keep Informed** – sprint demos, collect feedback after each iteration |
| 6 | **Students** | End users who register and join clubs through the system. Provide UX feedback. Success target: ≥200 active student users in the first month after launch. | External | Low Power / High Interest | **Keep Informed** – notified via email/portal when system goes live |
| 7 | **University IT Department** | Manages campus server infrastructure, ensures integration with FPT's existing systems, and is responsible for maintaining uptime ≥99.5% at the infrastructure level. | Internal | High Power / Low Interest | **Keep Satisfied** – notified of technical requirements, avoid conflicts with other university systems |

---

### Request 2 (20%) – RACI Matrix

**Roles:** PM = Project Manager | BA = Business Analyst | Dev = Developer | QA = Tester | PO = Product Owner (FPT management representative)

| # | Task / Activity | PM | BA | Dev | QA | PO |
|---|----------------|----|----|-----|----|----|
| 1 | Collect & document system requirements | C | R | I | I | A |
| 2 | Design system architecture | C | C | A/R | I | C |
| 3 | Set up server & database infrastructure | A | I | R | I | I |
| 4 | Develop Club Registration module | I | C | A/R | I | C |
| 5 | Develop Activity Tracking module | I | C | A/R | I | C |
| 6 | Develop Attendance Management module | I | C | A/R | I | C |
| 7 | Develop University Dashboard & Reports | C | C | A/R | I | C |
| 8 | Integrate frontend & backend | A | I | R | C | I |
| 9 | System testing & bug fixing | C | I | R | A | C |
| 10 | Performance & stress testing (uptime verification) | C | I | C | A/R | I |
| 11 | User Acceptance Testing (UAT) with Club Admins | A | C | I | R | C |
| 12 | System deployment & go-live | A | I | R | C | I |

> [!tip]
> ✅ Each task has exactly **1 "A"**. All four symbols R / A / C / I are present in the table.

---

### Request 3 (30%) – 3 SMART Goals

**Goal 1: Achieve ≥ 200 active student users on the CMS within the first 30 days after launch.**

- **Specific:** The goal is to attract and retain FPT students using the CMS to register for clubs and participate in activities during the first month of operation.
- **Measurable:** Success is defined as ≥ 200 unique student accounts that have logged in and performed at least one action (club registration or activity view) within the 30 days following go-live.
- **Attainable:** Feasible given FPT University's large student population. The marketing effort will be supported by club administrators and the IT Department via email notifications and the student portal.
- **Relevant:** The number of active users is the primary KPI in the project charter and directly measures whether the system is serving the student community as intended.
- **Time-bound:** Must be achieved within **30 days after the official go-live date**.

---

**Goal 2: Maintain system uptime ≥ 99.5% and response time < 2 seconds throughout the first month of operation.**

- **Specific:** The CMS must operate stably (≤ ~3.6 hours of downtime per month) and respond to every user request in fewer than 2 seconds under a load of 200 concurrent users.
- **Measurable:** Monitored using an uptime tool (e.g., Uptime Robot). QA team performs load testing with 200 virtual users (VUs) and records all response time results.
- **Attainable:** Achievable if the system is deployed on a reliable cloud provider (AWS/Azure) with caching enabled. The IT Department commits to supporting the infrastructure.
- **Relevant:** Uptime and speed are core non-functional requirements confirmed by the Project Sponsor. Failing to meet these thresholds constitutes a quality failure.
- **Time-bound:** Measured and reported throughout the **entire first month of operation** (30 days post-launch).

---

**Goal 3: Complete 100% of all system modules (Club Registration, Activity Tracking, Attendance, University Dashboard) and pass all test cases before go-live.**

- **Specific:** All four core functional modules must be fully developed, tested, and approved before deploying to production.
- **Measurable:** 100% of unit, integration, system, and UAT test cases must pass. Zero critical or high-severity bugs may remain open at go-live.
- **Attainable:** Feasible with a team of 4 developers and 2 QA over 4 months if the sprint plan is followed consistently.
- **Relevant:** Software quality directly impacts user experience and the ability to reach the 200-user target. Missing features = system cannot operate.
- **Time-bound:** All testing must be completed and signed off by **end of Month 3**, allowing Month 4 for UAT and deployment buffer.

---

### Request 4 (30%) – Risk Register

| # | Risk Name & Description | Probability | Impact | Mitigation Plan | Contingency Plan |
|---|------------------------|-------------|--------|-----------------|-----------------|
| 1 | **Low User Adoption Risk:** Students are unaware of or uninterested in the new CMS, resulting in fewer than 200 active users in the first month. | Medium | High | Partner with club administrators and the IT Portal team to promote the system at least 2 weeks before launch. Conduct demo/workshop sessions for Club Admins prior to go-live. | If fewer than 100 users are active after the first 2 weeks → PM triggers an emergency email blast to all students and negotiates a 2-week target extension with the Sponsor. |
| 2 | **Technical Performance Risk:** The system fails to meet uptime ≥99.5% or response time <2s due to server overload or unoptimized code. | Medium | High | Conduct load testing from Week 10 of the project using 300 VUs (50% above target). Implement a Redis caching layer. Select a cloud provider with an SLA of ≥99.9%. | If downtime occurs → switch to backup server immediately. PM notifies the Sponsor within 1 hour. Dev team hotfixes within 4 hours. |
| 3 | **Budget Overrun Risk:** Development and infrastructure costs exceed $12,000 due to scope creep or inaccurate labor estimates. | Low | High | Build a detailed budget breakdown from Day 1 with a 10% contingency reserve ($1,200). Enforce a formal Change Control Process: all scope changes require PM + Sponsor approval before implementation. Track EVM weekly. | If costs exceed budget by >10% → PM calls an emergency meeting with the Sponsor to cut scope (e.g., defer advanced reporting module to Phase 2) or request a budget increase. |
| 4 | **Key Staff Departure Risk:** A lead developer or BA resigns or is reassigned during the project, disrupting schedule and knowledge continuity. | Low | High | Enforce regular knowledge sharing and documentation. Every module must have at least 2 developers who understand how to maintain it (no single point of failure). | If it occurs → PM immediately escalates to the Sponsor to request a replacement resource. Uses the 2-week contingency buffer built into the schedule to absorb the impact. |

---
---

## 📱 EXAM 2 – FOOD DELIVERY APP FOR CAMPUS – ANSWERS

**Scenario Summary:** Campus Food Delivery App (CampusEats) | 6 months | $20,000 | $30,000 revenue target in first 6 months of operation | User satisfaction ≥85%

---

### Request 1 (20%) – Project Charter Statement

**1. Project Name:** Campus Food Delivery Application (CampusEats)

**2. Project Purpose / Justification:**
Students at FPT University currently face difficulties ordering food from campus canteens and stalls due to long queues, limited menu visibility, and the absence of electronic payment options. The CampusEats project is undertaken to:
- Digitize the entire campus food ordering and fulfillment process, improving convenience for students.
- Allow students to browse menus, place orders, and track them in real time from their mobile devices.
- Increase revenue for campus food vendors through improved order management and higher throughput.
- Generate sustainable revenue for the student startup team through a transaction-based commission model.

**3. Project Constraints:**

| Constraint Type | Description |
|----------------|-------------|
| **Scope** | The system includes: a mobile app (iOS + Android) for student ordering; a web dashboard for vendor order management; real-time order tracking; and electronic payment integration (VNPay/MoMo). Out of scope: last-mile delivery logistics (students collect food at designated pickup points). |
| **Time** | The project must be completed within exactly **6 months**, including development, testing, and launch. |
| **Cost/Budget** | Total development and operational budget is capped at **$20,000**. Revenue target: **$30,000 in the first 6 months** of post-launch operation. |
| **Quality** | User satisfaction score (measured via post-purchase survey) must reach **≥ 85%**. The app must be stable (no crashes) with a response time of < 3 seconds for all core actions. |

---

### Request 2 (20%) – Cost/Budget Items

| # | Cost Item | Description | Estimated Amount | Estimation Method & Person in Charge |
|---|-----------|-------------|-----------------|--------------------------------------|
| 1 | **Mobile App Development (iOS + Android)** | Full development of all app functions: login, menu browsing, order placement, real-time tracking, and payment integration. | $8,000 | **Bottom-up:** Estimated per module – Login: $500, Menu: $1,000, Order: $2,000, Tracking: $2,000, Payment: $2,500. Person in charge: **Lead Developer**. |
| 2 | **Backend API & Database Development** | Server-side API (Node.js/Django), database design, and cloud infrastructure setup (AWS). | $4,000 | **Parametric:** 2 developers × 2 months × $1,000/month. Person in charge: **Backend Developer + PM**. |
| 3 | **Vendor Web Dashboard** | Web interface for food vendors to manage incoming orders, confirm orders, and track status. | $2,500 | **Bottom-up:** UI design ($500) + Frontend dev ($1,500) + Testing ($500). Person in charge: **Frontend Developer**. |
| 4 | **UI/UX Design** | Design of all user interfaces for the mobile app and vendor dashboard, including wireframes, prototypes, and design assets. | $1,500 | **Analogous:** Based on a comparable app design project completed previously. Person in charge: **UI/UX Designer**. |
| 5 | **Testing & Quality Assurance** | Comprehensive testing: functional, performance, and UAT with real student users. | $1,500 | **Parametric:** 1 QA engineer × 1.5 months × $1,000/month. Person in charge: **QA Lead**. |
| 6 | **Marketing & Launch Activities** | Pre-launch promotion: social media campaign, posters, on-campus event, and first-order discount vouchers to drive adoption. | $1,500 | **Expert Judgment:** Estimated with input from a Marketing advisor. Design ($300) + Advertising ($700) + Event ($500). Person in charge: **Marketing Lead**. |
| 7 | **Contingency Reserve** | Buffer for unforeseen cost overruns (10% of total estimated budget). | $1,000 | **Percentage of Total:** 10% × $10,000 (items 1–6). Person in charge: **PM**. |

**Estimated Total: ~$20,000** ✅

---

### Request 3 (30%) – Communication Plan

**Stakeholders Selected:**

| # | Stakeholder | Type |
|---|-------------|------|
| 1 | **Project Team** (Developers + QA + Designer) | Project-Internal |
| 2 | **University Management** (FPT Administration) | Organization-Internal |
| 3 | **Food Vendors** (Campus canteen & stall owners) | External |

---

**Stakeholder 1: Project Team (Project-Internal)**

| Information | Purpose | Frequency | Method/Format | Responsible |
|-------------|---------|-----------|---------------|-------------|
| Sprint progress, task status, blockers | Synchronize daily progress, detect issues early | Daily | 15-minute Daily Standup – Google Meet | PM |
| Sprint review & retrospective results | Evaluate sprint output, improve team process | Bi-weekly (every 2 weeks) | Sprint Meeting – Jira/Trello board review | PM + Team |
| Technical decisions and architectural changes | Align on technical direction, prevent rework | As needed | Slack #tech-discuss channel | Lead Developer |

---

**Stakeholder 2: University Management (Organization-Internal)**

| Information | Purpose | Frequency | Method/Format | Responsible |
|-------------|---------|-----------|---------------|-------------|
| Monthly project status report (budget spent, milestones achieved) | Keep management informed and on-track; request approvals when needed | Monthly | Formal PDF report via email | PM |
| Launch announcement & go-live notification | Official notice so the university can support promotion | Once (2 weeks before launch) | Email + Brief presentation meeting | PM |
| Issue escalation (budget overrun, scope change) | Request approval for significant decisions | As needed | Formal email + meeting request | PM |

---

**Stakeholder 3: Food Vendors (External)**

| Information | Purpose | Frequency | Method/Format | Responsible |
|-------------|---------|-----------|---------------|-------------|
| App features & vendor dashboard walkthrough | Ensure vendors understand how to manage orders via the system | Once (2 weeks before launch) | In-person training workshop + PDF user manual | BA + PM |
| Weekly sales report via dashboard | Help vendors monitor revenue and manage their menu effectively | Weekly (post-launch) | Automated email report generated by the system | System (Automated) |
| System updates & maintenance notices | Notify vendors of scheduled downtime in advance | As needed (48h notice minimum) | Email + In-app notification | PM |

---

### Request 4 (30%) – Milestones & Activity Sequence

**3 Main Project Milestones:**

| # | Milestone | Deliverable |
|---|-----------|-------------|
| M1 | **Requirements & Design Complete** (End of Month 1) | Approved SRS document; UI/UX prototype signed off by all stakeholders |
| M2 | **App Development Complete & Internal Testing Passed** (End of Month 5) | Fully working app (all modules); test report with zero critical bugs |
| M3 | **Official Launch & Satisfaction Target Achieved** (End of Month 6) | Live app on App Store & Google Play; post-launch survey showing ≥85% satisfaction |

**Selected Milestone: M2 – App Development Complete & Internal Testing Passed**

**≥10 Activities & Dependency Sequence:**

| # | Activity | Duration | Predecessor | Relationship |
|---|----------|----------|-------------|--------------|
| 1 | Set up development environment & GitHub repository | 3 days | – | – |
| 2 | Design database schema | 4 days | 1 | FS |
| 3 | Develop backend API (core endpoints) | 15 days | 2 | FS |
| 4 | Develop user authentication module | 5 days | 2 | SS (parallel with Activity 3) |
| 5 | Develop Menu & Browse module (mobile) | 10 days | 4 | FS |
| 6 | Develop Order Placement module (mobile) | 10 days | 3 | FS |
| 7 | Develop Real-time Order Tracking module | 8 days | 6 | FS |
| 8 | Integrate payment gateway (VNPay/MoMo) | 7 days | 6 | SS (parallel with Activity 7) |
| 9 | Develop Vendor Web Dashboard | 10 days | 3 | SS (parallel with Activity 5) |
| 10 | Integration testing (frontend ↔ backend) | 7 days | 5, 7, 8, 9 | FS (all modules must be ready) |
| 11 | Performance & load testing | 5 days | 10 | SS (begins alongside Activity 10) |
| 12 | Bug fixing & regression testing | 7 days | 11 | FS |

> **Dependency Notes:**
> - A4 **SS** A3: Authentication module starts in parallel with backend API development after DB schema is done.
> - A8 **SS** A7: Payment integration can begin at the same time as Tracking module development.
> - A9 **SS** A5: Vendor Dashboard developed in parallel with mobile Menu module to save time.
> - A10 **FS** all modules: Integration testing only starts once every module is complete.

---
---

## 🏥 EXAM 3 – ONLINE HEALTH TRACKING PLATFORM – ANSWERS

**Scenario Summary:** HealthTrack Pro – daily health data logging + AI recommendations + sharing with doctors | 8 months | $50,000 | HIPAA compliant | 500 active users in first 3 months post-launch

---

### Request 1 (20%) – Stakeholders

| # | Name & Role | Detailed Responsibilities | Internal/External | Power/Interest Grid | Management Strategy |
|---|-------------|--------------------------|-------------------|---------------------|---------------------|
| 1 | **Project Sponsor** (Healthcare Startup CEO) | Provides the $50,000 budget, approves the project charter, sets business strategy, and approves all major scope changes. Final decision-maker on Go/No-Go for launch. | Internal | High Power / High Interest | **Manage Closely** – bi-weekly meetings, milestone reviews |
| 2 | **Project Manager (PM)** | Plans and controls the 8-month timeline, manages the $50,000 budget, coordinates team, submits weekly EVM reports, and manages HIPAA compliance risks. | Internal | High Power / High Interest | **Manage Closely** – full ownership of project execution |
| 3 | **HIPAA Compliance Officer** | Reviews all features that involve Protected Health Information (PHI) before each release. Ensures the system meets all HIPAA Security Rule safeguards: access control, encryption, audit logs, automatic logoff, emergency access. | Internal | High Power / High Interest | **Manage Closely** – mandatory review gate before each release |
| 4 | **AI/ML Engineer** | Develops and trains the machine learning model that generates personalized health recommendations (diet, exercise, sleep) based on user data. Ensures recommendation accuracy and clinical safety. | Internal | Low Power / High Interest | **Keep Informed** – updated on any requirement changes affecting AI inputs/outputs |
| 5 | **End Users (Patients / Health-conscious individuals)** | Log daily health data (heart rate, blood pressure, weight), receive AI recommendations, and share health reports with their doctors. Provide feedback during beta testing. Target: 500 active users in first 3 months. | External | Low Power / High Interest | **Keep Informed** – newsletter, beta program invitations, onboarding guide |
| 6 | **Doctors / Healthcare Providers** | Receive patient health reports via the platform, analyze trends, and provide clinical guidance. Key stakeholders for validating the clinical value of the AI recommendations. | External | Low Power / High Interest | **Keep Informed** – private demos, feedback collection on report usefulness |
| 7 | **Cloud Infrastructure Provider** (AWS/Azure) | Provides HIPAA-eligible cloud services (with a signed Business Associate Agreement). Ensures data encryption at rest and in transit meets HIPAA standards. | External | High Power / Low Interest | **Keep Satisfied** – clear SLA contract, regular monitoring |

---

### Request 2 (20%) – 3 SMART Goals

**Goal 1: Achieve 500 active users on HealthTrack Pro within 3 months of launch (Month 9 to Month 11 of the project).**

- **Specific:** Attract and retain 500 real user accounts that actively use the app at least 3 times per week to log health data during the first 3 months of operation.
- **Measurable:** The platform analytics system will track unique accounts with ≥ 3 health data log sessions per week across 3 consecutive months after launch.
- **Attainable:** Achievable through a multi-channel launch strategy: partnerships with 5 outpatient clinics, a beta program with enrolled doctors, and digital marketing through health and wellness online communities.
- **Relevant:** Active user count is the core KPI demonstrating product-market fit and is the primary metric for attracting the next round of investor funding for the startup.
- **Time-bound:** Measured at the **end of Month 3 post-launch** (Month 11 of the project, assuming launch at Month 8).

---

**Goal 2: Achieve full HIPAA compliance certification before the go-live date (end of Month 7).**

- **Specific:** The entire system must satisfy all 5 required HIPAA Security Rule safeguard categories: access control, audit controls, data integrity, transmission security (TLS 1.3 in transit, AES-256 at rest), and automatic logoff.
- **Measurable:** An independent HIPAA compliance consultant will conduct a formal audit with a Pass/Fail result across all 5 categories. Target: 100% Pass with zero critical findings.
- **Attainable:** Feasible within the $50,000 budget by leveraging AWS HIPAA Eligible Services and engaging a HIPAA consultant starting Month 5 of the project.
- **Relevant:** HIPAA compliance is a mandatory legal requirement for any U.S.-based healthcare application. Non-compliance means no launch and severe legal liability.
- **Time-bound:** The HIPAA audit must be completed and a Pass result received by **Month 7, Week 4** — one month before go-live.

---

**Goal 3: The AI recommendation engine must achieve ≥ 80% clinical accuracy as evaluated by doctors during the beta testing phase (Months 6–7).**

- **Specific:** The AI engine must generate health suggestions (diet, exercise, rest) that a panel of 5 partner doctors rates as "clinically appropriate" for at least 80 out of 100 test recommendation samples.
- **Measurable:** 5 doctors evaluate 100 AI-generated recommendations sampled from 50 test user profiles. A "clinically appropriate" rating from a doctor counts as a passing result. Target: ≥ 80/100 ratings are "appropriate."
- **Attainable:** Achievable by the AI/ML Engineer using publicly available clinical health datasets for model training, combined with iterative doctor feedback loops to fine-tune the model.
- **Relevant:** AI recommendation quality is the primary Unique Selling Point (USP) of HealthTrack Pro. Low accuracy damages user trust and undermines the platform's core value proposition.
- **Time-bound:** Clinical validation must be completed during the **beta testing phase: Month 6 – Month 7**.

---

### Request 3 (30%) – Work Breakdown Structure (WBS)

```
1. HealthTrack Pro Platform
│
├── 1.1 Initiating
│   ├── 1.1.1 Develop and submit project charter
│   ├── 1.1.2 Conduct project kick-off meeting
│   ├── 1.1.3 Identify stakeholders & create stakeholder register
│   ├── 1.1.4 Conduct initial HIPAA compliance gap assessment
│   └── 1.1.5 Obtain project charter approval from Sponsor
│
├── 1.2 Planning
│   ├── 1.2.1 Create Scope Management Plan
│   ├── 1.2.2 Create Time Management Plan (8-month schedule)
│   ├── 1.2.3 Create Cost Management Plan ($50,000 budget)
│   ├── 1.2.4 Create Risk Management Plan (including HIPAA risks)
│   ├── 1.2.5 Create Quality Management Plan
│   ├── 1.2.6 Create Resource Management Plan (AI/ML, Dev, QA)
│   └── 1.2.7 Finalize and obtain approval of Project Management Plan
│
├── 1.3 Executing
│   ├── 1.3.1 Analysis & Requirements
│   │   ├── 1.3.1.1 Conduct user research with patients and doctors
│   │   ├── 1.3.1.2 Define functional requirements (health logging, AI, sharing)
│   │   ├── 1.3.1.3 Define HIPAA security and compliance requirements
│   │   └── 1.3.1.4 Create Software Requirements Specification (SRS)
│   │
│   ├── 1.3.2 System Design
│   │   ├── 1.3.2.1 Design overall system architecture (HIPAA-compliant)
│   │   ├── 1.3.2.2 Design database schema (encrypted PHI storage)
│   │   ├── 1.3.2.3 Design mobile app UI/UX
│   │   └── 1.3.2.4 Design AI recommendation engine architecture
│   │
│   ├── 1.3.3 Development
│   │   ├── 1.3.3.1 Develop user authentication & access control module
│   │   ├── 1.3.3.2 Develop Health Data Logging module (heart rate, BP, weight)
│   │   ├── 1.3.3.3 Develop AI Recommendation Engine
│   │   ├── 1.3.3.4 Develop Doctor Report Sharing module
│   │   ├── 1.3.3.5 Develop HIPAA audit logging & data encryption layer
│   │   └── 1.3.3.6 Develop notification & health reminder system
│   │
│   ├── 1.3.4 Testing
│   │   ├── 1.3.4.1 Unit testing (per module)
│   │   ├── 1.3.4.2 Integration testing
│   │   ├── 1.3.4.3 External HIPAA security audit (compliance consultant)
│   │   ├── 1.3.4.4 AI accuracy clinical validation (5-doctor review panel)
│   │   └── 1.3.4.5 User Acceptance Testing (beta user cohort)
│   │
│   └── 1.3.5 Deployment & Launch
│       ├── 1.3.5.1 Deploy to HIPAA-eligible cloud environment (AWS)
│       ├── 1.3.5.2 Configure monitoring, alerting, and backup
│       └── 1.3.5.3 Execute official go-live launch plan
│
├── 1.4 Monitoring & Controlling
│   ├── 1.4.1 Monitor and control project scope (change request process)
│   ├── 1.4.2 Track schedule and budget using EVM (weekly)
│   ├── 1.4.3 Continuously monitor HIPAA compliance status
│   └── 1.4.4 Track user adoption KPI (target: 500 active users in 3 months)
│
└── 1.5 Closing
    ├── 1.5.1 Conduct lessons learned session with all team members
    ├── 1.5.2 Create and submit final project report
    ├── 1.5.3 Archive all project documentation
    └── 1.5.4 Obtain formal project closure sign-off from Sponsor
```

**Milestones & Deliverables:**

| # | Milestone | Deliverables | Completion Criteria |
|---|-----------|--------------|---------------------|
| 1 | **Project Initiation Complete** (End Month 1) | Approved project charter, stakeholder register, initial HIPAA gap assessment report | All documents signed off by the Sponsor |
| 2 | **Planning Complete** (End Month 2) | Full Project Management Plan (all sub-plans approved) | PMP signed off; all team members briefed and onboarded |
| 3 | **Development & AI Complete** (End Month 6) | Fully working app (all modules); AI engine with ≥80% clinical accuracy from doctor panel review | Zero open critical bugs; AI clinical validation passed |
| 4 | **HIPAA Compliance Certified** (End Month 7) | External HIPAA audit report with Pass result | 100% compliance on all 5 safeguard categories; zero critical findings |
| 5 | **500 Active Users Achieved** (Month 11 – 3 months post-launch) | Live platform on App Store & Google Play; user adoption analytics report | 500 unique active accounts verified in platform analytics |

---

### Request 4 (30%) – Network Diagram Calculation

**Network:** Start → A(4) → B(3), A(4) → C(5), B(3) → D(6), C(5) → D(6), D(6) → E(4), D(6) → F(7), E(4) → G(5), F(7) → G(5), G(5) → End

**1. Forward Pass – ES and EF:**

| Activity | ES | Duration | EF | Note |
|---------|----|---------|----|------|
| A | 0 | 4 | 4 | Starts at project beginning |
| B | 4 | 3 | 7 | After A |
| C | 4 | 5 | 9 | After A |
| D | **9** | 6 | 15 | MAX(EF_B=7, EF_C=9) = **9** |
| E | 15 | 4 | 19 | After D |
| F | 15 | 7 | 22 | After D |
| G | **22** | 5 | 27 | MAX(EF_E=19, EF_F=22) = **22** |

**✅ Project Duration = 27 days**

**2. Backward Pass – LF, LS, and Float:**

| Activity | LF | LS | Float | Critical? |
|---------|----|----|-------|-----------|
| G | 27 | 22 | 0 | ✅ Critical |
| F | 22 | 15 | **0** | ✅ Critical |
| E | 22 | 18 | **3** | ❌ Not Critical |
| D | 15 | 9 | **0** | ✅ Critical |
| C | 9 | 4 | **0** | ✅ Critical |
| B | 9 | 6 | **2** | ❌ Not Critical |
| A | 4 | 0 | **0** | ✅ Critical |

**3. Critical Path:** **Start → A(4) → C(5) → D(6) → F(7) → G(5) → End**
**Total = 4 + 5 + 6 + 7 + 5 = 27 days** ✅

**4. Schedule Compression to 20 Days:**

Need to reduce **7 days** (from 27 → 20 days).

- **Technique recommended: Schedule Crashing** (adding resources), not Fast Tracking.
  - *Reason:* Fast tracking works by overlapping tasks that are currently sequential — but the critical path activities (A→C→D→F→G) all have hard Finish-to-Start (FS) dependencies where the output of each task directly feeds into the next. Overlapping them introduces unacceptable quality risk. Crashing is safer when budget allows.

- **First activity to crash: Activity F (duration = 7 days)**
  - *Reason:* F is on the Critical Path (Float = 0) AND has the longest duration. Crashing F provides the greatest schedule reduction per crash action before other paths become critical.
  - *After crashing F by 2 days:* F = 5 days → New duration = 25 days. Continue crashing D (6 days), then C (5 days), then G (5 days) in order of descending duration.

---
---

## 🎬 EXAM 4 – UNIVERSITY DIGITAL MEDIA CHANNEL – ANSWERS

**Scenario Summary:** FPT University Digital Media Channel (YouTube + Podcast + Newsletter) | 3 months | $500 (equipment & boosting only) | All software must be free/open-source | Target: 500 YouTube subscribers | Zero factual inaccuracy complaints

---

### Request 1 (20%) – Project Charter Statement

**1. Project Name:** FPT University Digital Media Channel (FPT-DMC)

**2. Justification:**
FPT University currently lacks a dedicated digital media channel to reach students, alumni, and the external community with timely, reliable content about campus events, research achievements, and career opportunities. The FPT-DMC project is undertaken to:
- **Fill the information gap:** Provide a professional, credible source of FPT University-specific news from a student perspective.
- **Build brand awareness:** Expand FPT University's digital presence and reputation among prospective students and the broader public.
- **Develop real-world skills:** Give students hands-on experience in journalism, video production, audio engineering, and content marketing.
- **Create a sustainable media community:** Develop a long-term platform that grows beyond the initial 3-month project cycle.

**3. Project Constraints:**

| Constraint Type | Description |
|----------------|-------------|
| **Scope** | Includes: setting up and operating 1 YouTube channel, 1 weekly podcast episode, and 1 weekly newsletter. Content topics: campus events, research achievements, and career opportunities. Excludes: live event streaming, other social media platforms (Facebook, TikTok, Instagram), and long-form documentary production. |
| **Time** | The continuous production cycle must be maintained for exactly **3 months** (12 weeks) with at least **1 content piece published per week**. |
| **Cost/Budget** | Total budget is **$500**, allocated exclusively for promotional boosting and physical equipment. All editing and production software **must be free or open-source** (e.g., DaVinci Resolve, Audacity, OBS, Canva free tier, Mailchimp free tier). |
| **Quality** | (1) **Zero verifiable complaints** of factual inaccuracy throughout all 12 weeks of operation. (2) All published episodes and articles must maintain **journalistic integrity** – every fact, quote, and statistic must be verified before publication. |

---

### Request 2 (20%) – Measurable Project Objectives

**Objective 1: Reach 500 YouTube subscribers by the end of Week 12 (end of the 3-month production cycle).**

**How it will be measured:**
- **Metric:** YouTube Studio Analytics → "Subscribers" total count (unique accounts).
- **Target:** ≥ 500 subscribers by the **last day of Week 12**.
- **Measurement tool:** YouTube Studio dashboard, reviewed by the PM every Friday.
- **Intermediate checkpoints:**
  - End of Week 4 (Month 1): ≥ 100 subscribers
  - End of Week 8 (Month 2): ≥ 300 subscribers
  - End of Week 12 (Month 3): ≥ 500 subscribers ← **Final success criterion**
- **Result:** ≥ 500 = SUCCESS | < 400 = FAIL → post-mortem analysis required.

---

**Objective 2: Maintain zero (0) verifiable complaints of factual inaccuracy throughout all 12 weeks of operation.**

**How it will be measured:**
- **Metric:** Number of formal factual inaccuracy complaints received via comments, direct messages, or formal written notice from individuals or organizations mentioned in the content.
- **Target:** 0 verified complaints from Week 1 through Week 12.
- **Measurement process:** The Technical Editor performs a 2-level fact-check (Content Creator → Technical Editor) on every piece of content before publication. After publication, PM monitors comments and feedback for the first 48 hours. Any complaint received is logged in the Issue Register and formally investigated.
- **Success:** 0 verified inaccuracies found in any published content throughout the full 12-week cycle.

---

### Request 3 (30%) – RACI Chart

**3 Project Roles:**

| Role | Description |
|------|-------------|
| **PM (Project Manager)** | Plans the 12-week production schedule, manages the $500 budget, tracks KPIs weekly (subscribers, completion rate, complaints), approves content before publication, and escalates issues. |
| **CC (Content Creator)** | Researches weekly topics, identifies and contacts sources, writes scripts/talking points, and drafts newsletter content. First line of responsibility for information accuracy. |
| **TE (Technical Editor)** | Fact-checks all content before publication, edits video (DaVinci Resolve) and audio (Audacity), manages platform uploads, and monitors and reports analytics. |

**RACI Matrix (≥10 Tasks):**

| # | Task / Activity / Deliverable | PM | CC | TE |
|---|-------------------------------|----|----|-----|
| 1 | Define 12-week content strategy & editorial calendar | A | R | C |
| 2 | Set up YouTube channel (branding, banner, description) | A | C | R |
| 3 | Set up podcast hosting platform (Anchor/Spotify) | A | I | R |
| 4 | Set up newsletter platform (Mailchimp free tier) | A | I | R |
| 5 | Procure equipment within $500 budget (microphone, ring light) | A | C | R |
| 6 | Research & select topic for each weekly episode | C | A/R | C |
| 7 | Write episode script & newsletter draft | I | A/R | C |
| 8 | Record video & audio episode | I | C | A/R |
| 9 | Edit video (DaVinci Resolve) & audio (Audacity) | C | I | A/R |
| 10 | Fact-check all content before publication | A | C | R |
| 11 | Upload video to YouTube (optimize title, tags, thumbnail) | A | I | R |
| 12 | Distribute podcast episode & send weekly newsletter | A | I | R |
| 13 | Monitor analytics (subscribers, views, completion rate) & report | A/R | I | C |
| 14 | Manage $500 promotional budget (YouTube Ads boosting) | A | I | C |

> [!tip]
> ✅ Each task has exactly **1 "A"**. All four symbols R / A / C / I are present. ✅

---

### Request 4 (30%) – Milestones & Activity Sequence

**3 Main Project Milestones:**

| # | Milestone | Deliverable | Target |
|---|-----------|-------------|--------|
| M1 | **Pre-Production Complete** – All platforms set up; Episode 1 published | YouTube channel live, podcast feed active, newsletter sent, Episode 1 published | End of Week 2 |
| M2 | **Mid-Production Checkpoint** – On track for 300 subscribers | 8 episodes published, Month 1–2 analytics report, 300 subscribers achieved | End of Week 8 |
| M3 | **Project Closeout** – 500 subscribers, 0 complaints, final report submitted | All 12 episodes published, 500+ subscribers, final analytics and project report | End of Week 12 |

**Selected Milestone: M1 – Pre-Production Complete (End of Week 2)**

**≥10 Activities & Dependency Sequence:**

| # | Activity | Duration | Predecessor | Relationship |
|---|----------|----------|-------------|--------------|
| 1 | Conduct kick-off meeting & assign team roles | 1 day | – | – |
| 2 | Define target audience & 3 content pillars (events, research, careers) | 2 days | 1 | FS |
| 3 | Create 12-week editorial calendar (1 topic per week) | 2 days | 2 | FS |
| 4 | Design channel branding: name, logo, color palette (Canva free) | 2 days | 2 | SS (parallel with Activity 3) |
| 5 | Set up YouTube channel (upload banner, write description, add links) | 1 day | 4 | FS |
| 6 | Set up podcast hosting platform (Anchor free) | 1 day | 4 | SS (parallel with Activity 5) |
| 7 | Set up newsletter on Mailchimp free (template + subscriber form) | 1 day | 4 | SS (parallel with Activity 5) |
| 8 | Procure equipment within budget (USB mic, ring light, webcam) | 3 days | 1 | FS |
| 9 | Install & test free software (DaVinci Resolve, Audacity, OBS) | 2 days | 8 | SS (can begin while awaiting equipment delivery) |
| 10 | Research & write script for Episode 1 | 3 days | 3 | FS (requires editorial calendar) |
| 11 | Record Episode 1 (video + audio) | 1 day | 8, 9, 10 | FS (equipment, software, and script must all be ready) |
| 12 | Edit Episode 1: video (DaVinci) + audio (Audacity) | 2 days | 11 | FS |
| 13 | Fact-check Episode 1 content | 1 day | 12 | FS |
| 14 | Publish Episode 1 to YouTube + podcast + send first newsletter | 1 day | 5, 6, 7, 13 | FS (all platforms ready + content approved) |

> **Dependency Notes:**
> - A4 **SS** A3: Branding design starts in parallel with editorial calendar creation.
> - A6 **SS** A5 and A7 **SS** A5: Podcast and newsletter setup run in parallel after branding is complete.
> - A9 **SS** A8: Software installation begins while waiting for equipment delivery.
> - A14 **FS** (A5 + A6 + A7 + A13): Publication only happens when ALL platforms are live AND content has cleared fact-checking.

---
---

## 💰 EXAM 5 – EVM COMPREHENSIVE SCENARIO – ANSWERS

**Given:** BAC = $120,000 | BDAC = 12 months | Evaluation at Month 6 | AC = $55,000 | Actual % complete = 40%

---

### Request 1 (20%) – EVM Calculations

| Metric | Formula | Calculation | Result | Comment / Project Status |
|--------|---------|-------------|--------|--------------------------|
| **PV** | BAC × (elapsed / total) | $120,000 × (6/12) | **$60,000** | The planned value of work that should have been completed by Month 6. |
| **EV** | BAC × % complete | $120,000 × 40% | **$48,000** | The value of work actually accomplished, measured at the original planned rate. |
| **CV** | EV − AC | $48,000 − $55,000 | **−$7,000** | ❌ **OVER BUDGET** – The project is spending more than the value it is producing. |
| **SV** | EV − PV | $48,000 − $60,000 | **−$12,000** | ❌ **BEHIND SCHEDULE** – The project has accomplished $12,000 less work than planned at Month 6. |
| **CPI** | EV / AC | $48,000 / $55,000 | **0.87** | ❌ CPI < 1 → Over Budget. Every $1 spent is only producing $0.87 of value. |
| **SPI** | EV / PV | $48,000 / $60,000 | **0.80** | ❌ SPI < 1 → Behind Schedule. The project is progressing at only 80% of the planned rate. |
| **EAC** | BAC / CPI | $120,000 / 0.87 | **~$137,931** | ❌ The projected total cost at completion will exceed the original budget by ~$17,931. |
| **ETC** | EAC − AC | $137,931 − $55,000 | **~$82,931** | The estimated cost needed to complete the remaining work. |
| **VAC** | BAC − EAC | $120,000 − $137,931 | **−$17,931** | ❌ The project is projected to overspend by $17,931 at the end. |
| **EDAC** | BDAC / SPI | 12 / 0.80 | **15 months** | ❌ The project is projected to finish 3 months behind the planned 12-month schedule. |

---

### Request 2 (20%) – Overall Assessment & Corrective Actions

**1. Overall Project Status:**
- **Over Budget:** CPI = 0.87 < 1 → The project is spending more than it is producing. $7,000 more has been spent than the value received.
- **Behind Schedule:** SPI = 0.80 < 1 → Only 40% of work is complete, while 50% should have been done by Month 6. The project is behind by the equivalent of $12,000 in planned value.

**2. Will the project finish early or late? By how many months?**
- EDAC = 15 months → The project will finish **3 months late** (15 months vs. BDAC of 12 months).

**3. How much will the final cost exceed the BAC?**
- EAC = ~$137,931 → Final cost will **exceed the original budget by approximately $17,931** (~15% cost overrun).

**4. Recommended Corrective Actions (≥2):**

| # | Action | Rationale |
|---|--------|-----------|
| 1 | **Root Cause Analysis** – Call an immediate emergency meeting with all work package owners to identify the specific cause of CV = −$7,000 and SV = −$12,000. Analyze which modules are "burning" money without generating corresponding progress. | A CPI of 0.87 may be caused by scope creep, rework, or fundamentally wrong estimates. The PM cannot fix the problem without knowing the specific root cause. |
| 2 | **Scope Reduction** – Submit a formal Change Request to the Sponsor to defer non-critical features to Phase 2, reducing current workload and pulling the CPI back toward 1.0. | VAC = −$17,931 means the project will significantly overspend if nothing changes. Reducing scope is the most direct corrective lever available to the PM right now. |
| 3 | **Schedule Crashing or Timeline Re-baseline** – If the deadline is fixed: apply Schedule Crashing (add resources to critical path activities). If the deadline is flexible: negotiate a 1–2 month extension with the Sponsor. | SPI = 0.80 → 15 months to complete. PM must decide: pay more to finish on time (crashing) or negotiate more time. Either way, the Sponsor must be informed and consulted. |
| 4 | **Switch to Weekly EVM Reporting** – Implement weekly EVM tracking instead of monthly to detect negative trends earlier and intervene before they compound. | Discovering a worsening trend at Month 6 (the project's midpoint) is already very late. Weekly tracking would have surfaced these issues at Month 2–3, allowing earlier and less costly corrections. |

---

### Request 3 (30%) – Risk Register

| # | Risk Name & Description | Probability | Impact | Mitigation Plan | Contingency Plan |
|---|------------------------|-------------|--------|-----------------|------------------|
| 1 | **Scope Creep Risk:** Stakeholders continuously add new requirements or change existing ones outside the agreed scope baseline, causing the team to spend time and money that doesn't register as project progress in the EVM. This is the most common cause of a negative CV. | Medium | High | Enforce a **Formal Change Control Process** from Day 1: all scope changes must be documented, impact-assessed (cost and schedule), and approved by both PM and Sponsor before implementation. Conduct bi-weekly scope review meetings with the Sponsor. | If scope creep has already occurred → PM collects all undocumented changes, quantifies the additional cost and schedule impact, and submits a formal Change Request for Sponsor approval to either increase the BAC or remove an equivalent amount of existing scope. |
| 2 | **Technical Rework / Inefficiency Risk:** The development team encounters unanticipated technical problems (e.g., wrong architecture choice, high technical debt), requiring significant rework. This causes Actual Cost (AC) to rise without a corresponding increase in Earned Value (EV). | Medium | High | Conduct **technical spikes and proof-of-concept** for complex modules before committing to full development. Enforce mandatory code reviews before merging. Schedule an architectural review by a senior developer or architect every 2 sprints to catch technical debt early. | If significant rework is confirmed → PM identifies the affected module, brings in a senior contractor to accelerate fixes, re-estimates the remaining work (new ETC), updates the EAC, and presents a revised schedule to the Sponsor with a recovery plan. |
| 3 | **Inaccurate Initial Estimation Risk:** The original task-level estimates for the ERP system were overly optimistic and did not account for the actual complexity of enterprise integration, causing the CPI to be below 1.0 from the very beginning of the project. | High | High | Use **3-Point Estimation (PERT: (O + 4M + P) / 6)** for all future estimates instead of single-point estimates. Require expert review of all estimates before baselining. Add a **10–15% contingency reserve** to the overall budget. Reference analogous ERP project data to sanity-check estimates. | If fundamentally wrong estimates are confirmed → PM conducts a complete Bottom-up re-estimation of all remaining work packages, presents the revised EAC and ETC to the Sponsor, and works with the Sponsor to decide whether to fund the gap or cut scope to fit the original BAC. |

---

### Request 4 (30%) – Critical Path Method & Schedule Crashing

**Network:**
```
Path 1: A(5) → B(8) → D(6) → F(4) → End
Path 2: A(5) → C(3) → E(10) → F(4) → End
```

**1. Forward Pass – ES and EF:**

| Activity | ES | Duration | EF | Notes |
|---------|----|---------|----|-------|
| A | 0 | 5 | 5 | Starts at project beginning; on both paths |
| B | 5 | 8 | 13 | Path 1 only |
| C | 5 | 3 | 8 | Path 2 only |
| D | 13 | 6 | 19 | Path 1 only |
| E | 8 | 10 | 18 | Path 2 only |
| F | **19** | 4 | 23 | MAX(EF_D=19, EF_E=18) = **19** |

**Path Durations:**
- Path 1: A + B + D + F = 5 + 8 + 6 + 4 = **23 days** ← Critical
- Path 2: A + C + E + F = 5 + 3 + 10 + 4 = **22 days**

**2. Backward Pass – LF, LS, and Float:**

| Activity | LF | LS | Float | Critical? |
|---------|----|----|-------|-----------|
| F | 23 | 19 | 0 | ✅ Critical |
| D | 19 | 13 | **0** | ✅ Critical |
| E | 19 | 9 | **1** | ❌ Not Critical |
| B | 13 | 5 | **0** | ✅ Critical |
| C | 9 | 6 | **1** | ❌ Not Critical |
| A | 5 | 0 | **0** | ✅ Critical |

**Complete ES / EF / LS / LF / Float Table:**

| Activity | ES | EF | LS | LF | Float | Critical? |
|---------|----|----|----|----|-------|-----------|
| A | 0 | 5 | 0 | 5 | **0** | ✅ |
| B | 5 | 13 | 5 | 13 | **0** | ✅ |
| C | 5 | 8 | 6 | 9 | **1** | ❌ |
| D | 13 | 19 | 13 | 19 | **0** | ✅ |
| E | 8 | 18 | 9 | 19 | **1** | ❌ |
| F | 19 | 23 | 19 | 23 | **0** | ✅ |

**3. Critical Path:** **Start → A(5) → B(8) → D(6) → F(4) → End**
**Project Duration = 23 days**

**4. Which activity to crash first? (Target: reduce from 23 to 20 days — need 3 fewer days)**

- Only activities on the **Critical Path** (Float = 0) can be crashed: A, B, D, F.
- **Crash B (Duration = 8 days) first** — it is the longest activity on the Critical Path.
  - *Reason:* Crashing the longest critical activity provides the greatest potential schedule reduction per crash unit and is typically the most cost-effective first move.
  - After crashing B by 1 day: Path 1 = 22 days, Path 2 = 22 days → Both paths are now **co-critical**. From this point, you must crash both paths simultaneously.
  - Continue: crash B 1 more day AND crash E 1 day simultaneously → 21 days.
  - One final crash on both paths → 20 days achieved.

**5. Which activities can be Fast Tracked? What are the risks?**

- **Candidate pair: B and D (Path 1)** – Currently B must finish before D starts (FS). You could fast track by starting D's early preparation tasks (setup, design) before B is fully complete (20–30% overlap).
- **Candidate pair: C and E (Path 2)** – Similarly, E can begin its initial tasks while C is still in progress.

**Risks of Fast Tracking:**
| Risk | Explanation |
|------|-------------|
| **Rework Risk** | If B's output changes after D has already started, D may need to be redone, costing more time and money than the baseline sequential approach. |
| **Communication Overhead** | Teams working in parallel require significantly more coordination and communication, increasing the risk of misalignment and errors. |
| **Quality Risk** | Parallel pressure forces team members to work faster with less review time, potentially introducing defects that slow the project down later. |

---

## 📌 QUICK REFERENCE – PMG201c ANSWER FRAMEWORK

| Request Type | Checklist |
|-------------|-----------|
| **Stakeholders** | ≥5 people, both Internal AND External, describe responsibilities **specific to the scenario**, include Power/Interest Grid + Strategy |
| **RACI** | ≥10 tasks, each task has exactly **1 "A"**, all four symbols **R, A, C, I** must appear in the full table |
| **SMART Goals** | ≥3 goals, analyze **each criterion separately** (S, M, A, R, T), must include **specific numbers** |
| **Risk** | ≥3 risks, must include: Probability + Impact + **Mitigation** (before the risk occurs) + **Contingency** (after the risk occurs) |
| **WBS** | Level 1 = project name, Level 2 = Phases, Level 3 = Tasks, numbered correctly: 1.1.1, 1.1.2... |
| **Network/CPM** | Forward pass (take MAX with multiple predecessors) → Backward pass (take MIN with multiple successors) → Float = LF−EF → Critical = Float=0 |
| **EVM** | PV=BAC×(t/T), EV=BAC×%, CPI=EV/AC, SPI=EV/PV, EAC=BAC/CPI, ETC=EAC−AC, EDAC=BDAC/SPI |

---

*PMG201c Practice Exam Answers – FPT University – For study purposes only*
