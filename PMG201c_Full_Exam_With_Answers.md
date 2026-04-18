# 📘 PMG201c – 2 FULL PRACTICE EXAMS (14 Requirements Each)
## With Step-by-Step Guidance & Complete Model Answers

> [!important]
> These two exams cover **all 14 topic areas** examined in PMG201c.
> **Critical Path** and **EVM** sections include fully worked numerical solutions.
> Scoring guide per section is indicated. Total = 100 points each exam.

---

# 🖥️ EXAM 1 – IT / APP TOPIC
## Project: "FPT EduGo" – University Mobile E-Learning App

**Scenario:**
FPT University wants to develop a mobile application called **"FPT EduGo"** to improve the learning experience for students. The app allows students to access lecture videos, submit assignments, take online quizzes, track their academic progress, and communicate with instructors via in-app messaging. The app must be available on both iOS and Android platforms.

**Key constraints:**
- **Duration:** 6 months (24 weeks)
- **Budget (BAC):** $80,000
- **Quality:** Minimum 4.0/5.0 star rating on app stores within the first 3 months; 99% uptime; response time < 2 seconds
- **Scope:** Mobile app only (iOS + Android); excludes web version in this phase

---

## ✅ REQUIREMENT 1 – PROJECT CHARTER (5 pts)

### 📋 What to write:
A Project Charter is the formal document that **authorizes the project**. It must include: project name, purpose/justification, high-level requirements, constraints, assumptions, and key stakeholders.

### 🧭 Guidance:
- Keep it narrative (paragraph + bullet), not just a list
- Justification = WHY the project exists (problem it solves)
- Constraints = time, cost, scope, quality limits
- Assumptions = things you assume to be true without proof

### ✅ Model Answer:

**Project Name:** FPT EduGo – Mobile E-Learning Application

**Purpose & Justification:**
Currently, FPT University students rely on a desktop-only LMS that is not optimized for mobile use. Survey data shows that 78% of students prefer accessing study materials on their smartphones. The FPT EduGo project will address this gap by delivering a dedicated, offline-capable mobile learning app, improving student engagement and academic outcomes. This directly supports FPT University's strategic goal of becoming a top digital-first university by 2027.

**High-Level Requirements:**
- Students can stream/download lecture videos for offline viewing
- Students can submit assignments and receive graded feedback in-app
- Instructors can post announcements and respond to student messages
- The system integrates with the existing LMS database (SSO login)
- Available on iOS 14+ and Android 10+

**Constraints:**
- Scope: Mobile app only; web portal excluded from this phase
- Time: Must be launched within 6 months (24 weeks)
- Budget: Total project budget must not exceed $80,000
- Quality: App Store rating ≥ 4.0/5.0; crash rate < 0.5%; no data breach

**Assumptions:**
- FPT IT department will provide API access to the existing LMS within Week 2
- All team members are available full-time for the project duration
- Student beta testers (50 volunteers) will be available in Week 20

---

## ✅ REQUIREMENT 2 – WBS (Work Breakdown Structure) (8 pts)

### 📋 What to write:
A hierarchical decomposition of all project work. Must reach Level 3 minimum (Level 4 preferred).

### 🧭 Guidance:
- Level 1 = Project Name
- Level 2 = Phases (Initiating, Planning, Executing, Monitoring & Controlling, Closing)
- Level 3 = Major tasks per phase
- Level 4 = Sub-tasks (specific, assignable units of work)

### ✅ Model Answer:

```
1. FPT EduGo – Mobile E-Learning App
  1.1 Initiating
      1.1.1 Develop project charter
      1.1.2 Identify stakeholders and create register
      1.1.3 Conduct kick-off meeting
      1.1.4 Obtain project charter approval from sponsor

  1.2 Planning
      1.2.1 Define scope management plan
      1.2.2 Create time management plan & Gantt chart
      1.2.3 Create cost management plan & budget breakdown
      1.2.4 Create risk management plan
      1.2.5 Create communication plan
      1.2.6 Create quality management plan
      1.2.7 Create HR & resource plan
      1.2.8 Obtain final PMP approval

  1.3 Executing
      1.3.1 Requirements Gathering
            1.3.1.1 Conduct student & instructor interviews
            1.3.1.2 Analyze current LMS pain points
            1.3.1.3 Finalize SRS (Software Requirements Specification)
      1.3.2 System & UI/UX Design
            1.3.2.1 Create system architecture diagram
            1.3.2.2 Design database schema
            1.3.2.3 Design wireframes & UI prototypes
            1.3.2.4 Obtain design approval from Product Owner
      1.3.3 Backend Development
            1.3.3.1 Develop authentication & SSO integration
            1.3.3.2 Develop course content management APIs
            1.3.3.3 Develop assignment submission & grading module
            1.3.3.4 Develop messaging & notification service
      1.3.4 Frontend (Mobile) Development
            1.3.4.1 Develop iOS app (Swift)
            1.3.4.2 Develop Android app (Kotlin)
            1.3.4.3 Integrate offline video caching feature
      1.3.5 API Integration & Testing
            1.3.5.1 Connect frontend to backend APIs
            1.3.5.2 Integrate with existing LMS database
      1.3.6 QA & Testing
            1.3.6.1 Unit testing
            1.3.6.2 Integration testing
            1.3.6.3 UAT with beta user group (50 students)
            1.3.6.4 Performance & load testing
      1.3.7 Deployment & Launch
            1.3.7.1 Deploy backend to cloud (AWS)
            1.3.7.2 Submit app to Apple App Store
            1.3.7.3 Submit app to Google Play Store
            1.3.7.4 Conduct official app launch ceremony

  1.4 Monitoring & Controlling
      1.4.1 Track progress via weekly status reports
      1.4.2 Conduct EVM analysis at Weeks 8, 16
      1.4.3 Manage change requests
      1.4.4 Monitor risk register

  1.5 Closing
      1.5.1 Conduct lessons-learned session
      1.5.2 Produce final project report
      1.5.3 Archive all project documentation
      1.5.4 Formal team celebration
```

---

## ✅ REQUIREMENT 3 – DELIVERABLES & MILESTONES (5 pts)

### 📋 What to write:
Identify key milestones (major checkpoints) and the deliverables produced at each. Include completion criteria.

### ✅ Model Answer:

| # | Milestone | Deliverables | Completion Criteria |
|---|-----------|--------------|---------------------|
| 1 | Project Initiated (Week 1) | Approved Project Charter, Stakeholder Register, Kick-off minutes | Charter signed by Sponsor; all key stakeholders identified |
| 2 | Planning Complete (Week 3) | Project Management Plan (all sub-plans) | PMP reviewed & approved by sponsor; team briefed |
| 3 | Design Approved (Week 8) | SRS document, System architecture, UI/UX wireframes, DB schema | Product Owner approves design; no open critical issues |
| 4 | Development Complete (Week 18) | Functional backend APIs, iOS & Android app builds | All modules developed; code reviewed & merged to main branch |
| 5 | UAT Passed (Week 22) | UAT report, bug-fix log, performance test report | 95% of test cases pass; 0 critical/high-severity bugs open |
| 6 | Project Closed (Week 24) | Live app on stores, final report, lessons learned | App published; sign-off from all stakeholders |

---

## ✅ REQUIREMENT 4 – RACI MATRIX (8 pts)

### 📋 What to write:
A responsibility assignment matrix with ≥ 10 tasks. Roles: PM, BA, Dev, QA, PO.

### 🧭 Guidance:
- Each task: exactly **1 A** (accountable)
- Each task: at least **1 R** (responsible, does the work)
- C = consulted before decisions; I = informed of outcome

### ✅ Model Answer:

| Task / Activity | PM | BA | Dev | QA | PO |
|-----------------|----|----|-----|----|----|
| 1. Develop Project Charter | A | C | I | I | C |
| 2. Conduct Requirements Gathering | C | A/R | I | I | C |
| 3. Create SRS Document | I | A/R | C | C | C |
| 4. Design System Architecture | C | C | A/R | I | C |
| 5. Design UI/UX Wireframes | I | C | A/R | I | C |
| 6. Backend Development | I | I | A/R | C | I |
| 7. Frontend (Mobile) Development | I | I | A/R | C | I |
| 8. API Integration | C | I | A/R | C | I |
| 9. QA & Testing | C | C | I | A/R | C |
| 10. UAT with Beta Users | C | C | I | A/R | A |
| 11. App Store Submission | A | I | R | C | I |
| 12. Create Communication Plan | A/R | C | I | I | C |
| 13. Conduct EVM Analysis | A/R | I | I | I | I |
| 14. Final Project Report | A/R | C | I | I | I |

---

## ✅ REQUIREMENT 5 – SMART GOALS (8 pts)

### 📋 What to write:
Write 3 SMART goals. Each must have all 5 criteria (S, M, A, R, T) analyzed individually.

### ✅ Model Answer:

**Goal 1: Achieve 1,000 active users within 60 days of app launch.**
- **S (Specific):** Grow the number of FPT University students who actively use the FPT EduGo app at least 3 times per week
- **M (Measurable):** Track via Firebase Analytics: 1,000 users with ≥ 3 sessions/week within 60 days
- **A (Attainable):** FPT University has 15,000 enrolled students; 1,000 is a realistic 6.7% adoption target achievable through campus marketing
- **R (Relevant):** Active user count is the primary KPI measuring the app's value and ROI
- **T (Time-bound):** Achieved within 60 days post-launch (i.e., by end of Week 24)

**Goal 2: Maintain app store rating ≥ 4.0/5.0 stars within the first 3 months after launch.**
- **S (Specific):** Ensure quality of UX, performance, and core features satisfies student and instructor users
- **M (Measurable):** Average store rating on Apple App Store and Google Play Store ≥ 4.0 stars based on ≥ 200 reviews
- **A (Attainable):** Achievable with rigorous UAT, bug fixes pre-launch, and a quick-response feedback team post-launch
- **R (Relevant):** Store rating directly reflects user satisfaction and influences adoption by other students
- **T (Time-bound):** By end of Month 3 post-launch (approximately Week 36 from project start)

**Goal 3: Ensure 100% of critical test cases pass before the app is released to production.**
- **S (Specific):** All test cases classified as "critical" or "high priority" in the QA test plan must achieve passing status
- **M (Measurable):** 0 open critical/high-severity defects at the time of App Store submission; tracked in Jira
- **A (Attainable):** Feasible with a dedicated 3-person QA team, 3 weeks of testing, and dev team support
- **R (Relevant):** Releasing a buggy app damages FPT's brand reputation and drives negative reviews
- **T (Time-bound):** All critical tests passed by end of Week 22 (before app submission in Week 23)

---

## ✅ REQUIREMENT 6 – RISK MANAGEMENT (8 pts)

### ✅ Model Answer:

| # | Risk Name | Description | Probability | Impact | Mitigation Plan | Contingency Plan |
|---|-----------|-------------|-------------|--------|-----------------|------------------|
| 1 | API Integration Delay | FPT IT department delays providing LMS API access past Week 2 | Medium | High | Formally request API access in Week 1 with signed SLA; assign BA as liaison | Use mock APIs for development; negotiate extended timeline with sponsor |
| 2 | Key Developer Resignation | Lead developer leaves mid-project, causing knowledge loss | Low | High | Document all code with wikis; conduct weekly knowledge-sharing sessions | Cross-train backup developer; hire freelancer via Upwork with 1-week onboarding |
| 3 | App Store Rejection | Apple or Google rejects app submission due to policy violations | Low | High | Review App Store guidelines before development starts; conduct compliance checklist in QA phase | Revise submission based on rejection reasons; allocate 1-week buffer at end of schedule |
| 4 | Scope Creep | Stakeholders request additional features (web version, AI tutor) mid-project | High | Medium | Implement formal change request process from Week 1; PM must approve all scope changes | Defer new features to Phase 2; document them in Product Backlog |
| 5 | Performance Issues Under Load | App crashes when >500 users login simultaneously | Medium | High | Conduct load testing in Week 21 using JMeter; design for horizontal scaling on AWS | Activate auto-scaling groups on AWS; schedule off-peak maintenance window |

---

## ✅ REQUIREMENT 7 – STAKEHOLDERS & ROLES (5 pts)

### 📋 What to write:
Identify ≥ 5 stakeholders. Include: role, type (internal/external), Power/Interest position, management strategy.

### ✅ Model Answer:

| Stakeholder | Role & Responsibility | Type | Power | Interest | Strategy |
|-------------|----------------------|------|-------|----------|----------|
| University Dean (Sponsor) | Provides funding & authorization; approves major decisions; signs off on deliverables | External | High | High | **Manage Closely** – weekly briefings, formal status reports |
| Project Manager | Plans, executes, monitors all project activities; manages team & budget | Internal | High | High | **Manage Closely** – core decision-maker |
| Business Analyst (BA) | Gathers requirements from students & instructors; produces SRS; bridges business & tech | Internal | Medium | High | **Keep Informed** – daily standups, sprint reviews |
| Development Team (Dev) | Designs and codes backend APIs and mobile frontend (iOS/Android) | Internal | Low | High | **Keep Informed** – sprint planning, backlog grooming |
| FPT IT Department | Provides LMS API access & server infrastructure; reviews architecture | Internal | High | Medium | **Keep Satisfied** – formal access requests, shared technical documentation |
| Students (End Users) | Primary users of the app; participate in UAT & provide feedback | External | Low | High | **Keep Informed** – beta testing invitations, feedback surveys |
| App Store Review Team (Apple/Google) | Reviews and approves app submissions | External | High | Low | **Keep Satisfied** – comply with guidelines, submit complete packages |

---

## ✅ REQUIREMENT 8 – USER STORIES (8 pts)

### 📋 What to write:
At least 5 User Stories in the format: **"As a [role], I want [feature] so that [benefit]."**
Each story needs ≥ 2 Acceptance Criteria.

### ✅ Model Answer:

**US-01: Offline Video Access**
> *As a student, I want to download lecture videos for offline viewing so that I can study without a WiFi connection.*
- **AC1:** Student can tap "Download" on any video and access it from the "My Downloads" section without internet
- **AC2:** Downloaded videos have a storage indicator and can be deleted to free up phone storage
- **AC3:** Downloaded content expires after 30 days and must be re-downloaded

**US-02: Assignment Submission**
> *As a student, I want to submit my assignment files (PDF, DOCX) through the app so that I do not need to physically go to campus.*
- **AC1:** Student can select files from phone storage and upload up to 50MB per submission
- **AC2:** After submission, student receives an in-app confirmation notification with timestamp
- **AC3:** Student can view submission status (Submitted / Graded) and attached feedback from the instructor

**US-03: Progress Tracking**
> *As a student, I want to see my course completion percentage and quiz scores so that I can monitor my academic progress.*
- **AC1:** Dashboard displays a progress bar (0–100%) per enrolled course, updated in real time
- **AC2:** Quiz results are displayed with correct answers highlighted after submission

**US-04: Instructor Announcements**
> *As an instructor, I want to post announcements to my class so that all enrolled students are notified immediately.*
- **AC1:** Instructor can compose and publish a text announcement (max 1,000 characters) within 3 clicks
- **AC2:** All enrolled students receive a push notification within 30 seconds of the announcement being published

**US-05: In-App Messaging**
> *As a student, I want to send a direct message to my instructor so that I can ask questions without using personal email.*
- **AC1:** Student can initiate a message thread with any of their current-semester instructors
- **AC2:** Instructor receives a read-receipt notification; response appears in the same thread
- **AC3:** Message history is retained for the duration of the academic semester

---

## ✅ REQUIREMENT 9 – ORGANIZATIONAL STRUCTURE (3 pts)

### 📋 What to write:
Choose and justify the organizational structure type (Functional / Matrix / Projectized).

### ✅ Model Answer:

**Chosen structure: Projectized**

**Justification:**
The FPT EduGo project adopts a **Projectized** organizational structure for the following reasons:

1. **Short, fixed timeline (6 months):** The project requires full team dedication without sharing resources across departments. A Functional structure would create bottlenecks as employees split attention.
2. **Clear, defined scope:** The deliverable is a specific app — the team can be fully focused without ambiguity.
3. **PM needs full authority:** In a Projectized structure, the PM has high-to-total authority over the team, budget, and schedule decisions. This is critical for a fast-moving software sprint environment.
4. **Agile/Scrum compatibility:** Scrum operates best in a Projectized environment where cross-functional team members are dedicated full-time to the project.

| Characteristic | Functional | Matrix (Strong) | **Projectized ✅** |
|---------------|------------|-----------------|-------------------|
| PM Authority | Little/None | Moderate-High | **High to Total** |
| Resource Availability | Shared | Moderate | **Dedicated** |
| Budget Control | Functional Mgr | Mixed | **PM** |
| Best for | Routine ops | Shared resources | **Short, focused projects** |

---

## ✅ REQUIREMENT 10 – COMMUNICATION PLAN (8 pts)

### ✅ Model Answer:

| Stakeholder | Information | Purpose | Frequency | Method/Format | Responsible |
|-------------|-------------|---------|-----------|---------------|-------------|
| University Dean (Sponsor) | Project status, budget vs. actual, milestones achieved | Maintain executive awareness & decision support | Bi-weekly | Formal PDF status report + 30-min meeting | PM |
| Development Team | Sprint goals, task assignments, blockers | Coordinate daily work, remove impediments | Daily | Standup meeting (15 min) via Google Meet + Jira updates | Scrum Master / PM |
| Business Analyst | Requirements updates, design change requests | Ensure alignment between requirements and development | Weekly | Sprint review + shared Google Docs | PM |
| QA Team | Test results, bug reports, UAT schedule | Track quality metrics, assign bug fixes | Weekly | Jira bug tracker + weekly QA report | QA Lead |
| Students (Beta Testers) | App download link, feedback forms, issue reporting | Collect real-user feedback pre-launch | Once (UAT phase, Week 20–22) | Email + in-app feedback form | BA |
| FPT IT Department | API access requests, infrastructure specs | Coordinate technical integrations | As needed | Email + technical documentation | Dev Lead |

---

## ✅ REQUIREMENT 11 – GANTT CHART (5 pts)

### 📋 What to write:
Show all main activities on a timeline. In markdown, use a table with weeks.

### ✅ Model Answer:

| Activity | W1 | W2 | W3 | W4 | W5 | W6 | W7 | W8 | W9-12 | W13-18 | W19-20 | W21-22 | W23 | W24 |
|----------|----|----|----|----|----|----|----|----|-------|--------|--------|--------|-----|-----|
| A: Requirements Gathering | ██ | ██ | | | | | | | | | | | | |
| B: System & DB Design | | | ██ | ██ | ██ | | | | | | | | | |
| C: Database Design | | | ██ | ██ | | | | | | | | | | |
| D: Backend Development | | | | | | ██ | ██ | ██ | ██ | | | | | |
| E: Frontend Development | | | | | | ██ | ██ | ██ | | | | | | |
| F: API Integration | | | | | | | | | | ██ | ██ | | | |
| G: QA & Testing | | | | | | | | | | | | ██ | ██ | |
| H: Deployment & Launch | | | | | | | | | | | | | ██ | ██ |
| Monitoring & Control | ██ | ██ | ██ | ██ | ██ | ██ | ██ | ██ | ██ | ██ | ██ | ██ | ██ | ██ |

> [!note]
> This is a simplified representation. In real exams, a timeline bar chart or table with exact week spans is sufficient.

---

## ✅ REQUIREMENT 12 – CRITICAL PATH METHOD (15 pts) ⭐ MUST SCORE FULL MARKS

### 📋 What to write:
Given a network diagram, calculate ES, EF, LS, LF, Float for all activities. Identify the Critical Path and total project duration.

### 🔢 Network Diagram (Activity-on-Node):

```
Activities and durations (weeks):
A(2) → B(3)  [B depends on A]
A(2) → C(2)  [C depends on A]
B(3) → D(4)  [D depends on B AND C]
C(2) → D(4)
B(3) → E(3)  [E depends on B]
D(4) → F(2)  [F depends on D AND E]
E(3) → F(2)
F(2) → G(3)  [G depends on F]
G(3) → H(1)  [H depends on G]
```

### 🧭 Step-by-Step Guidance:

**Step 1 – Forward Pass** (left to right, take MAX when multiple predecessors)
- ES of first task = 0
- EF = ES + Duration
- If a task has multiple predecessors: ES = MAX of all predecessor EFs

**Step 2 – Backward Pass** (right to left, take MIN when multiple successors)
- LF of last task = Project Duration (= EF of last task)
- LS = LF − Duration
- If a task has multiple successors: LF = MIN of all successor LSs

**Step 3 – Calculate Float**
- Float = LS − ES (or equivalently LF − EF)
- If Float = 0 → the task is **on the Critical Path**

**Step 4 – Identify Critical Path**
- Trace all tasks where Float = 0 from Start to End

### ✅ Model Answer:

**FORWARD PASS:**

| Task | Predecessors | ES | Duration | EF |
|------|-------------|----|---------|----|
| A | – | 0 | 2 | **2** |
| B | A | 2 | 3 | **5** |
| C | A | 2 | 2 | **4** |
| D | B, C | MAX(5, 4) = **5** | 4 | **9** |
| E | B | 5 | 3 | **8** |
| F | D, E | MAX(9, 8) = **9** | 2 | **11** |
| G | F | 11 | 3 | **14** |
| H | G | 14 | 1 | **15** |

➡️ **Project Duration = 15 weeks**

---

**BACKWARD PASS:**

| Task | Successors | LF | Duration | LS |
|------|-----------|----|---------|----|
| H | – | **15** | 1 | **14** |
| G | H | 14 | 3 | **11** |
| F | G | 11 | 2 | **9** |
| D | F | 9 | 4 | **5** |
| E | F | 9 | 3 | **6** |
| B | D, E | MIN(5, 6) = **5** | 3 | **2** |
| C | D | 5 | 2 | **3** |
| A | B, C | MIN(2, 3) = **2** | 2 | **0** |

---

**FULL TABLE WITH FLOAT:**

| Task | ES | EF | LS | LF | Float | Critical? |
|------|----|----|----|----|-------|-----------|
| A | 0 | 2 | 0 | 2 | **0** | ✅ YES |
| B | 2 | 5 | 2 | 5 | **0** | ✅ YES |
| C | 2 | 4 | 3 | 5 | **1** | ❌ No |
| D | 5 | 9 | 5 | 9 | **0** | ✅ YES |
| E | 5 | 8 | 6 | 9 | **1** | ❌ No |
| F | 9 | 11 | 9 | 11 | **0** | ✅ YES |
| G | 11 | 14 | 11 | 14 | **0** | ✅ YES |
| H | 14 | 15 | 14 | 15 | **0** | ✅ YES |

> [!important]
> **Critical Path: A → B → D → F → G → H**
> **Total Project Duration: 2 + 3 + 4 + 2 + 3 + 1 = 15 weeks**

**Non-critical activities:**
- C has Float = 1 week (can be delayed up to 1 week without affecting the project)
- E has Float = 1 week (same)

**Crashing question:** If the project must finish in 13 weeks (reduce by 2 weeks):
- Only crash activities **on the Critical Path**
- Best choice: crash **D (Backend Dev, 4 weeks)** first → it's the longest task on the critical path → most reduction per resource added
- Then crash **G (QA, 3 weeks)** if still needed

---

## ✅ REQUIREMENT 13 – EVM (Earned Value Management) (15 pts) ⭐ MUST SCORE FULL MARKS

### 🔢 Given Data:
- **BAC** (Budget at Completion) = **$80,000**
- **BDAC** (Planned Duration) = **24 weeks**
- **Status Date:** End of Week **10**
- **AC** (Actual Cost at Week 10) = **$38,000**
- **% Work Completed** = **45%**

### 🧭 Step-by-Step Guidance:

1. **PV** = BAC × (Elapsed Time / Total Time) → how much should have been spent by now?
2. **EV** = BAC × % Complete → how much value has been earned?
3. **CV** = EV − AC → positive = under budget; negative = over budget
4. **SV** = EV − PV → positive = ahead of schedule; negative = behind
5. **CPI** = EV / AC → > 1 good; < 1 bad
6. **SPI** = EV / PV → > 1 good; < 1 bad
7. **EAC** = BAC / CPI → predicted total cost
8. **ETC** = EAC − AC → how much more money is needed?
9. **VAC** = BAC − EAC → expected budget surplus/deficit at end
10. **EDAC** = BDAC / SPI → predicted final duration

### ✅ Model Answer:

| Metric | Formula | Calculation | Result | Interpretation |
|--------|---------|------------|--------|---------------|
| **PV** | BAC × (10/24) | 80,000 × 0.4167 | **$33,333** | Planned to spend $33,333 by Week 10 |
| **EV** | BAC × 45% | 80,000 × 0.45 | **$36,000** | Work worth $36,000 has been completed |
| **CV** | EV − AC | 36,000 − 38,000 | **−$2,000** | ❌ Over budget by $2,000 |
| **SV** | EV − PV | 36,000 − 33,333 | **+$2,667** | ✅ Ahead of schedule |
| **CPI** | EV / AC | 36,000 / 38,000 | **0.947** | Every $1 spent yields only $0.947 in value |
| **SPI** | EV / PV | 36,000 / 33,333 | **1.08** | Project is running at 108% planned speed |
| **EAC** | BAC / CPI | 80,000 / 0.947 | **$84,477** | Predicted total cost at completion |
| **ETC** | EAC − AC | 84,477 − 38,000 | **$46,477** | Still needs $46,477 to finish |
| **VAC** | BAC − EAC | 80,000 − 84,477 | **−$4,477** | Will exceed budget by ~$4,477 |
| **EDAC** | BDAC / SPI | 24 / 1.08 | **~22.2 weeks** | Will finish ~1.8 weeks ahead of schedule |

**Overall Project Status Summary:**
- 🔴 **Cost:** OVER BUDGET (CPI = 0.947 < 1) → spending $1 but generating only $0.947 in earned value
- 🟢 **Schedule:** AHEAD OF SCHEDULE (SPI = 1.08 > 1) → progressing faster than planned
- ⚠️ **Forecast:** Final cost expected to reach $84,477, exceeding the $80,000 BAC by **$4,477**
- ✅ **Duration Forecast:** Project will finish approximately **1.8 weeks early**

**PM Action Required:**
1. Investigate why costs are running 5.3% over budget (check if developers are working overtime)
2. Consider reallocating the schedule buffer to reduce unnecessary spending
3. Report CPI = 0.947 to sponsor immediately as it is approaching the critical threshold

---

## ✅ REQUIREMENT 14 – QA/QC PLAN (5 pts)

### 📋 What to write:
Describe the quality management approach including prevention, appraisal, and failure costs + specific QA activities.

### ✅ Model Answer:

**Quality Standards:**
- App Store rating ≥ 4.0/5.0 within 3 months post-launch
- Crash rate < 0.5% (tracked via Firebase Crashlytics)
- 100% of critical test cases pass before production release
- API response time < 2 seconds under normal load (≤ 500 concurrent users)

**Quality Cost Categories (applied to this project):**

| Category | Example Activities |
|----------|--------------------|
| **Prevention** | Code review standards (Google style guide), UI design peer reviews, sprint planning with clear acceptance criteria, developer training on OWASP security |
| **Appraisal** | Unit testing (Jest/JUnit), integration testing, code coverage reports (target ≥ 80%), load testing with JMeter, weekly QA sprint reviews |
| **Internal Failure** | Bug fixes found before release (tracked in Jira), rework of rejected UI screens, regression testing after patches |
| **External Failure** | App Store 1-star reviews, crashes reported by live users, emergency hotfixes post-launch ← **Most expensive! Avoid by investing in prevention.** |

**Key QA Activities by Phase:**

| Phase | QA Activity | Owner |
|-------|-------------|-------|
| Design | Prototype review with 10 student users | BA + QA |
| Development | Daily automated unit tests via CI/CD pipeline (GitHub Actions) | Dev |
| Pre-launch | Full regression test; UAT with 50 beta students (3 cycles) | QA |
| Post-launch | Monitor Firebase Crashlytics weekly for 30 days | QA Lead |

---
---

# 🌽 EXAM 2 – NON-IT TOPIC
## Project: "City Marathon 2026" – Annual 10K City Running Event

**Scenario:**
The City Sports Department wants to organize the **"City Marathon 2026"** — an annual running event open to all citizens. The event features a **10K race** and **5K fun run**, targeting **2,000 registered participants**. The event will be held on a single day (Race Day). The project involves securing city permits, attracting corporate sponsors, marketing the event, recruiting volunteers, procuring equipment and medals, setting up a medical safety team, and managing event-day operations.

**Key constraints:**
- **Duration:** 8 months of planning (32 weeks); Race Day = end of Week 32
- **Budget (BAC):** $150,000
- **Quality:** ≥ 90% participant satisfaction score; 0 serious medical incidents; 95% content completion by viewers/listeners (for online streaming)
- **Scope:** Physical race event + live social media stream; excludes any virtual/remote participation mode

---

## ✅ REQUIREMENT 1 – PROJECT CHARTER (5 pts)

### ✅ Model Answer:

**Project Name:** City Marathon 2026

**Purpose & Justification:**
The city's public health statistics show a 23% increase in sedentary lifestyle diseases over the past 5 years. The City Sports Department, in partnership with local businesses, will organize the City Marathon 2026 to promote active living, community engagement, and local tourism. The event will also generate sponsorship revenue to fund future city sports programs and attract national media coverage that boosts the city's brand.

**High-Level Requirements:**
- Minimum 2,000 registered participants (10K and 5K categories)
- City streets on the designated route must be closed safely for 4 hours on Race Day
- Two aid stations per kilometer; hydration and medical teams stationed throughout the route
- Live streaming on official social media channels (Facebook, YouTube)

**Constraints:**
- **Scope:** Physical race only; no virtual participation mode; social media livestream included
- **Time:** All planning activities must be completed within 32 weeks; Race Day is fixed
- **Budget:** Total not to exceed $150,000 (all categories: prizes, equipment, marketing, logistics)
- **Quality:** Participant satisfaction survey score ≥ 90%; zero serious medical incidents

**Assumptions:**
- City government will grant all route permits by Week 6
- A minimum of 5 corporate sponsors will be secured by Week 12
- At least 300 volunteers will be recruited by Week 20

---

## ✅ REQUIREMENT 2 – WBS (8 pts)

### ✅ Model Answer:

```
1. City Marathon 2026
  1.1 Initiating
      1.1.1 Develop project charter
      1.1.2 Identify stakeholders and create register
      1.1.3 Conduct kick-off meeting with city government
      1.1.4 Obtain project charter approval

  1.2 Planning
      1.2.1 Scope management plan
      1.2.2 Budget & cost management plan
      1.2.3 Risk management plan
      1.2.4 Communication plan
      1.2.5 Quality management plan
      1.2.6 Procurement plan (medals, equipment, apparel)
      1.2.7 Volunteer management plan

  1.3 Executing
      1.3.1 Permitting & Route
            1.3.1.1 Conduct route survey
            1.3.1.2 Apply for city traffic permits
            1.3.1.3 Liaise with police & municipality for road closure
      1.3.2 Sponsorship
            1.3.2.1 Develop sponsorship packages & pitch deck
            1.3.2.2 Approach and negotiate with corporate sponsors
            1.3.2.3 Sign sponsorship agreements
      1.3.3 Registration & Participants
            1.3.3.1 Build online registration portal
            1.3.3.2 Manage registration windows (Early Bird, Regular, Late)
            1.3.3.3 Send race kits and bib numbers to participants
      1.3.4 Marketing & Promotion
            1.3.4.1 Design event branding (logo, banner, T-shirt)
            1.3.4.2 Run social media campaigns (Facebook, Instagram)
            1.3.4.3 Press release to local media
            1.3.4.4 Set up event livestreaming system
      1.3.5 Volunteers
            1.3.5.1 Recruit volunteers (target: 300)
            1.3.5.2 Train volunteers (route guides, aid station support)
            1.3.5.3 Assign volunteer roles on Race Day
      1.3.6 Equipment & Logistics
            1.3.6.1 Procure medals, trophies, finisher T-shirts
            1.3.6.2 Set up timing gates and chip system
            1.3.6.3 Arrange portable restrooms, tents, sound system
      1.3.7 Medical & Safety
            1.3.7.1 Contract ambulance and paramedic teams
            1.3.7.2 Set up aid stations along the route
            1.3.7.3 Prepare emergency response protocol
      1.3.8 Race Day Execution
            1.3.8.1 Set up start/finish line structures
            1.3.8.2 Conduct pre-race briefing for volunteers
            1.3.8.3 Manage race start, timing, and route monitoring
            1.3.8.4 Post-race medal ceremony & participant departure

  1.4 Monitoring & Controlling
      1.4.1 Weekly budget tracking
      1.4.2 Sponsor payment follow-up
      1.4.3 Participant registration count monitoring
      1.4.4 Risk monitoring and issue log

  1.5 Closing
      1.5.1 Participant satisfaction survey analysis
      1.5.2 Financial reconciliation & final budget report
      1.5.3 Lessons learned session
      1.5.4 Archive all documents
      1.5.5 Thank-you communications to sponsors & volunteers
```

---

## ✅ REQUIREMENT 3 – DELIVERABLES & MILESTONES (5 pts)

### ✅ Model Answer:

| # | Milestone | Deliverables | Completion Criteria |
|---|-----------|--------------|---------------------|
| 1 | Project Initiated (Week 2) | Approved Project Charter, Stakeholder Register | Charter signed by City Sports Director |
| 2 | City Permits Secured (Week 6) | Signed traffic permit, police coordination agreement, road closure plan | All required permits received from city government |
| 3 | Sponsorship Closed (Week 12) | ≥ 5 signed sponsorship agreements; at least $40,000 sponsor income confirmed | All agreements signed; invoices issued |
| 4 | Registration & Marketing Complete (Week 20) | 2,000 registered participants; completed marketing campaign | Registration target met; all bibs & race kits dispatched |
| 5 | Logistics Ready (Week 28) | Medals, timing chips, tents, restrooms, medical teams, volunteers all confirmed | Race-day readiness checklist 100% complete |
| 6 | Event Complete & Project Closed (Week 34) | Post-race satisfaction survey report, final budget report, lessons learned | Survey score ≥ 90%; all payments settled; archive complete |

---

## ✅ REQUIREMENT 4 – RACI MATRIX (8 pts)

### ✅ Model Answer:

**Roles:** PM (Project Manager), WC (Workstream Coordinator), MK (Marketing Team), VOL (Volunteer Coordinator), SA (Safety & Medical Advisor), SP (Sponsor Relations Officer)

| Task / Activity | PM | WC | MK | VOL | SA | SP |
|-----------------|----|----|----|----|----|----|
| 1. Develop Project Charter | A/R | C | I | I | I | I |
| 2. Route Survey & Permit Application | A | R | I | I | C | I |
| 3. Negotiate & Sign Sponsorship Deals | C | I | I | I | I | A/R |
| 4. Build Online Registration Portal | A | R | C | I | I | I |
| 5. Design Event Branding (logo, T-shirt) | C | I | A/R | I | I | C |
| 6. Run Social Media Campaign | I | I | A/R | I | I | C |
| 7. Recruit & Train Volunteers | C | C | I | A/R | C | I |
| 8. Procure Medals & Equipment | A | R | I | I | I | C |
| 9. Set Up Medical Aid Stations | C | C | I | C | A/R | I |
| 10. Set Up Race Timing System | A | R | I | I | I | I |
| 11. Conduct Pre-Race Volunteer Briefing | C | C | I | A/R | R | I |
| 12. Manage Race Day Operations | A/R | R | R | R | R | I |
| 13. Issue Post-Race Surveys | C | I | A/R | I | I | I |
| 14. Produce Final Budget Report | A/R | I | I | I | I | C |

---

## ✅ REQUIREMENT 5 – SMART GOALS (8 pts)

### ✅ Model Answer:

**Goal 1: Register exactly 2,000 participants (10K + 5K combined) by Week 20.**
- **S:** Achieve 1,400 registrations for 10K and 600 for 5K categories via online registration portal
- **M:** Count tracked through registration system dashboard; target = 2,000 confirmed paid registrants
- **A:** Feasible based on city population of 800,000; similar regional marathons consistently attract 1,500–2,500 runners
- **R:** Participant count directly drives event ticket revenue and sponsor satisfaction metrics
- **T:** All registrations closed by end of Week 20; race kits shipped by Week 24

**Goal 2: Achieve a participant satisfaction score of ≥ 90% in the post-race survey.**
- **S:** Measure overall satisfaction with event organization, route, medical support, and facilities
- **M:** Collect post-race surveys from at least 60% of finishers within 48 hours; score ≥ 90% "Satisfied" or "Very Satisfied"
- **A:** Achievable through high-quality logistics, well-trained volunteers, and real-time issue resolution on Race Day
- **R:** Satisfaction score builds the event's reputation and increases future-year registration demand
- **T:** Survey distributed within 24 hours of Race Day; results compiled by Week 33

**Goal 3: Secure ≥ $40,000 in corporate sponsorship revenue by Week 12.**
- **S:** Sign agreements with at least 5 corporate sponsors across Title, Gold, and Silver tiers
- **M:** Total confirmed sponsorship cash value ≥ $40,000 (invoiced and with signed contracts)
- **A:** Realistic based on 3 major local businesses already expressing initial interest in Week 1
- **R:** Sponsorship revenue funds 27% of the total budget, making it critical for financial viability
- **T:** All agreements signed and initial payments received by end of Week 12

---

## ✅ REQUIREMENT 6 – RISK MANAGEMENT (8 pts)

### ✅ Model Answer:

| # | Risk Name | Description | Probability | Impact | Mitigation Plan | Contingency Plan |
|---|-----------|-------------|-------------|--------|-----------------|------------------|
| 1 | Permit Rejection / Delay | City government delays or denies traffic permit for the race route | Medium | High | Submit permit applications in Week 2 (12 weeks before needed); engage city sports liaison officer early | Propose an alternative route with shorter road closure; negotiate a revised event date |
| 2 | Insufficient Participant Registration | Registration falls below 2,000 by Week 18 | Medium | High | Launch Early Bird discount pricing; run targeted social media ads; partner with running clubs and gyms | Add a corporate team relay category; offer last-minute group discounts to companies |
| 3 | Sponsor Withdrawal | A major sponsor cancels their deal after signing | Low | High | Include penalty clauses in sponsorship contracts; secure 2 backup sponsors in pipeline | Activate backup sponsors immediately; reduce non-critical event expenses (e.g., smaller prize pool) |
| 4 | Bad Weather on Race Day | Heavy rain, extreme heat, or storm creates safety hazard | Medium | High | Include weather clause in city permit; monitor weather forecasts from Week 30; develop rain contingency plan | Delay race start by 2 hours; activate indoor shelter points along route; issue refunds if force majeure declared |
| 5 | Medical Emergency During Race | Participant suffers cardiac arrest or serious injury | Low | Very High | Station AED devices and trained paramedics every 2km; all volunteers trained in basic first aid | Full emergency response protocol activated; ambulance on standby; direct hospital coordination |

---

## ✅ REQUIREMENT 7 – STAKEHOLDERS & ROLES (5 pts)

### ✅ Model Answer:

| Stakeholder | Role | Type | Power | Interest | Management Strategy |
|-------------|------|------|-------|----------|---------------------|
| City Sports Director (Sponsor) | Provides funding authority; approves major decisions; signs off on deliverables | External | High | High | **Manage Closely** – monthly formal reports + key milestone briefings |
| Project Manager | Plans and oversees all workstreams; manages budget, risks, and team | Internal | High | High | **Manage Closely** – core decision-maker |
| Corporate Sponsors | Fund the event; provide prizes and in-kind support; expect brand visibility | External | High | Medium | **Keep Satisfied** – regular exposure reports, sponsor activation meetings |
| Participants (Runners) | The primary end users; their satisfaction = event success | External | Low | High | **Keep Informed** – weekly email newsletters, social media updates, race day info packs |
| Local Police & Traffic Authority | Manage road closure, traffic diversion, crowd control | External | High | Low | **Keep Satisfied** – formal coordination meetings, signed city agreements |
| Volunteer Team (300 people) | Operate aid stations, guide routes, manage registration — essential Race Day resource | Internal | Low | High | **Keep Informed** – training sessions, Race Day briefing packs |
| Local Media & Press | Cover the event; drive awareness; livestream | External | Low | Medium | **Monitor** – press releases, media passes, real-time race updates |

---

## ✅ REQUIREMENT 8 – USER STORIES (8 pts)

### ✅ Model Answer:

**US-01: Online Registration**
> *As a participant, I want to register and pay for the race online so that I can secure my spot without visiting any office.*
- **AC1:** Registration form accepts personal details, T-shirt size, emergency contact, and online payment (credit card / e-wallet)
- **AC2:** Participant receives a confirmation email with race reference number within 5 minutes of payment
- **AC3:** Registration portal remains open until Week 20 or until 2,000 spots are filled (whichever comes first)

**US-02: Digital Bib Number**
> *As a participant, I want to receive my race bib number and starting time digitally so that I can prepare my race kit in advance.*
- **AC1:** Bib number and QR code sent via email and SMS 2 weeks before Race Day
- **AC2:** QR code is scannable at event check-in gate for verification in < 10 seconds

**US-03: Live Race Tracking**
> *As a family member of a participant, I want to track the runner's real-time position on the race route so that I can cheer them on at key points.*
- **AC1:** Live tracking page accessible on mobile browser via unique tracking link sent before race
- **AC2:** Runner's position updates every 60 seconds on an interactive map
- **AC3:** Finish time and position are displayed within 5 minutes of crossing the finish line

**US-04: Aid Station Information**
> *As a participant, I want to know the locations of all water and medical aid stations on the route so that I can plan my race strategy.*
- **AC1:** Route map with all aid station markers is published on the event website by Week 28
- **AC2:** Aid station locations are also printed on the physical race instruction card included in the race kit

**US-05: Post-Race Results**
> *As a participant, I want to receive my official race time and ranking after the event so that I can share my achievement.*
- **AC1:** Official results published on the event website within 2 hours of race completion
- **AC2:** Participant receives personalized results certificate via email, downloadable as PDF, within 24 hours

---

## ✅ REQUIREMENT 9 – ORGANIZATIONAL STRUCTURE (3 pts)

### ✅ Model Answer:

**Chosen Structure: Matrix (Strong)**

**Justification:**
The City Marathon 2026 is organized by the City Sports Department, which is a **functional organization** that also runs other city programs year-round. Because the event is a temporary project requiring specialists from multiple departments (marketing staff, safety officers, procurement officers) who will return to their regular roles after the event, a pure Projectized structure is impractical.

A **Strong Matrix** structure is chosen because:
1. **PM has significant authority** to direct cross-functional staff (marketing, safety, logistics) toward project objectives without those staff permanently switching departments
2. **Shared resources** (e.g., city marketing team also handles other events simultaneously) can be efficiently managed
3. **Budget control** is shared between PM and department heads, which satisfies city government governance requirements

| Characteristic | Functional | **Matrix (Strong) ✅** | Projectized |
|---------------|------------|----------------------|-------------|
| PM Authority | Little/None | **Moderate to High** | Total |
| Resource sharing | Yes | **Yes** | No |
| Staff return to dept. after project | Yes | **Yes** | No |
| Best for | Routine ops | **Multi-dept. projects** | Focused, short projects |

---

## ✅ REQUIREMENT 10 – COMMUNICATION PLAN (8 pts)

### ✅ Model Answer:

| Stakeholder | Information | Purpose | Frequency | Method/Format | Responsible |
|-------------|-------------|---------|-----------|---------------|-------------|
| City Sports Director | Budget status, milestone completion, risk flags | Executive oversight & approval of key decisions | Monthly | Formal PDF report + 30-min briefing | PM |
| Corporate Sponsors | Brand placement updates, registration count, event media coverage preview | Maintain sponsor confidence & relationship | Bi-weekly | Email brief + sponsor portal dashboard | Sponsor Relations Officer |
| Registered Participants | Race schedule, route map, weather updates, bib numbers | Keep participants informed and engaged | Weekly (from Week 20 onward) | Email newsletter + Facebook/Instagram updates | Marketing Team |
| Volunteers | Training schedule, role assignments, race day reporting points | Coordinate Race Day volunteer operations | Bi-weekly (from Week 18); daily in Race Week | WhatsApp group + printed briefing packs | Volunteer Coordinator |
| Police & Traffic Authority | Road closure timeline, emergency contact list, route layout | Ensure legal compliance and safety coordination | Monthly + 1 week before Race Day | Formal meetings + shared documentation | PM + WC |
| Local Media | Press releases, event highlights, interview scheduling | Drive public awareness and media coverage | At key milestones (launch, Week 20, Race Week) | Press releases via email; press conference in Race Week | Marketing Team |

---

## ✅ REQUIREMENT 11 – GANTT CHART (5 pts)

### ✅ Model Answer:

| Activity | W1-4 | W5-8 | W9-12 | W13-16 | W17-20 | W21-24 | W25-28 | W29-32 | W33-34 |
|----------|------|------|-------|--------|--------|--------|--------|--------|--------|
| A: Route Survey & Permit | ████ | ████ | | | | | | | |
| B: Sponsor Acquisition | | ████ | ████ | ████ | | | | | |
| C: Registration & Portal | | ████ | ████ | ████ | ████ | | | | |
| D: Marketing Campaign | | | | ████ | ████ | ████ | | | |
| E: Volunteer Recruitment | | | | ████ | ████ | ████ | | | |
| F: Equipment Procurement | | | | ████ | ████ | ████ | ████ | | |
| G: Medical Team Setup | | | | | | ████ | ████ | | |
| H: Race Day Execution | | | | | | | | | ████ |
| Monitoring & Control | ████ | ████ | ████ | ████ | ████ | ████ | ████ | ████ | |
| Closing | | | | | | | | | ████ |

---

## ✅ REQUIREMENT 12 – CRITICAL PATH METHOD (15 pts) ⭐ MUST SCORE FULL MARKS

### 🔢 Network Diagram:

```
Activities and durations (weeks):
A: Route Survey & Permit (4 weeks) → B and → C
B: Sponsor Acquisition (6 weeks)   → D and → F  [B depends on A]
C: Registration System (3 weeks)   → D and → E  [C depends on A]
D: Marketing Campaign (4 weeks)    → H           [D depends on B AND C]
E: Volunteer Recruitment (3 weeks) → G           [E depends on C]
F: Equipment Procurement (4 weeks) → H           [F depends on B]
G: Medical Team Setup (2 weeks)    → H           [G depends on E]
H: Race Day Execution (1 week)     → End         [H depends on D, F, AND G]
```

### ✅ FORWARD PASS:

| Task | Predecessors | ES | Duration | EF |
|------|-------------|----|---------|----|
| A | – | 0 | 4 | **4** |
| B | A | 4 | 6 | **10** |
| C | A | 4 | 3 | **7** |
| D | B, C | MAX(10, 7) = **10** | 4 | **14** |
| E | C | 7 | 3 | **10** |
| F | B | 10 | 4 | **14** |
| G | E | 10 | 2 | **12** |
| H | D, F, G | MAX(14, 14, 12) = **14** | 1 | **15** |

➡️ **Project Duration = 15 weeks** *(planning phase)*

### ✅ BACKWARD PASS:

| Task | Successors | LF | Duration | LS |
|------|-----------|----|---------|----|
| H | – | **15** | 1 | **14** |
| D | H | 14 | 4 | **10** |
| F | H | 14 | 4 | **10** |
| G | H | 14 | 2 | **12** |
| B | D, F | MIN(10, 10) = **10** | 6 | **4** |
| E | G | 12 | 3 | **9** |
| C | D, E | MIN(10, 9) = **9** | 3 | **6** |
| A | B, C | MIN(4, 6) = **4** | 4 | **0** |

### ✅ FULL TABLE WITH FLOAT:

| Task | ES | EF | LS | LF | Float | Critical? |
|------|----|----|----|----|-------|-----------|
| A | 0 | 4 | 0 | 4 | **0** | ✅ YES |
| B | 4 | 10 | 4 | 10 | **0** | ✅ YES |
| C | 4 | 7 | 6 | 9 | **2** | ❌ No |
| D | 10 | 14 | 10 | 14 | **0** | ✅ YES |
| E | 7 | 10 | 9 | 12 | **2** | ❌ No |
| F | 10 | 14 | 10 | 14 | **0** | ✅ YES |
| G | 10 | 12 | 12 | 14 | **2** | ❌ No |
| H | 14 | 15 | 14 | 15 | **0** | ✅ YES |

> [!important]
> **TWO Critical Paths (both = 15 weeks):**
> - **Path 1: A → B → D → H** (4+6+4+1 = 15 weeks)
> - **Path 2: A → B → F → H** (4+6+4+1 = 15 weeks)
>
> **Non-critical:** C (Float=2), E (Float=2), G (Float=2)

**Crashing question:** If Race Day is moved up and the project must finish in 13 weeks:
- Only crash on the Critical Path (A, B, D, F, H are critical)
- Best option: crash **B (Sponsor Acquisition, 6 weeks)** → it's the longest task on both critical paths → crashing it by 1 week reduces **both** paths simultaneously
- Then crash **D or F** (both 4 weeks) → choose the one with the lower crash cost per week

---

## ✅ REQUIREMENT 13 – EVM (Earned Value Management) (15 pts) ⭐ MUST SCORE FULL MARKS

### 🔢 Given Data:
- **BAC** = **$150,000**
- **BDAC** = **32 weeks**
- **Status Date:** End of Week **12**
- **AC** (Actual Cost at Week 12) = **$65,000**
- **% Work Completed** = **38%**

### ✅ Model Answer:

| Metric | Formula | Calculation | Result | Interpretation |
|--------|---------|------------|--------|---------------|
| **PV** | 150,000 × (12/32) | 150,000 × 0.375 | **$56,250** | Should have spent $56,250 by Week 12 |
| **EV** | 150,000 × 38% | 150,000 × 0.38 | **$57,000** | Work worth $57,000 has actually been done |
| **CV** | EV − AC | 57,000 − 65,000 | **−$8,000** | ❌ OVER BUDGET by $8,000 |
| **SV** | EV − PV | 57,000 − 56,250 | **+$750** | ✅ Slightly AHEAD of schedule |
| **CPI** | EV / AC | 57,000 / 65,000 | **0.877** | Every $1 spent earns only $0.877 in value |
| **SPI** | EV / PV | 57,000 / 56,250 | **1.013** | Running at ~101% of planned speed |
| **EAC** | BAC / CPI | 150,000 / 0.877 | **~$171,038** | Total predicted final cost |
| **ETC** | EAC − AC | 171,038 − 65,000 | **~$106,038** | Still needs ~$106,038 to finish |
| **VAC** | BAC − EAC | 150,000 − 171,038 | **−$21,038** | Expected to exceed budget by ~$21,038 |
| **EDAC** | BDAC / SPI | 32 / 1.013 | **~31.6 weeks** | Will finish ~0.4 weeks ahead of schedule |

**Overall Project Status Summary:**
- 🔴 **Cost:** OVER BUDGET (CPI = 0.877 < 1) → spending significantly more than planned; every $1 only delivers $0.877 in value
- 🟢 **Schedule:** SLIGHTLY AHEAD (SPI = 1.013 > 1) → work is progressing slightly faster than planned
- 🔴 **Forecast:** Final cost predicted at $171,038, exceeding the $150,000 BAC by **$21,038 (14%)**
- ✅ **Duration:** Expected to finish on time (31.6 weeks vs. 32 planned)

**PM Recommended Actions:**
1. 🚨 **Escalate cost overrun to City Sports Director immediately** — a 14% budget overrun ($21,038) requires executive authorization for budget adjustment
2. 💡 **Audit sponsor and equipment spending** — the biggest cost drivers likely include equipment procurement (F) and volunteer costs; negotiate bulk discounts with medal and apparel suppliers
3. 📌 **Freeze non-critical spending** — postpone any scope enhancements until the CPI is improved
4. 🔄 **Check if sponsorship revenue can close the gap** — if sponsors committed amounts are higher than projected cash inflow, accelerate invoicing

---

## ✅ REQUIREMENT 14 – QA/QC PLAN (5 pts)

### ✅ Model Answer:

**Quality Standards for City Marathon 2026:**
- Participant satisfaction survey score ≥ 90% ("Satisfied" + "Very Satisfied")
- Zero serious medical incidents during the event
- Online livestream uptime ≥ 95% throughout the race (3–4 hours)
- All aid stations stocked and operational 30 minutes before race start

**Quality Cost Categories:**

| Category | Activities |
|----------|-----------|
| **Prevention** | Volunteer training sessions (2x before Race Day); route safety inspection checklist; supplier pre-qualification for medals and timing chips; emergency response protocol development |
| **Appraisal** | Pre-event dry run / rehearsal in Race Week (Week 31); timing system stress test with 500 simulated participants; medical team readiness audit (Week 28); checklist review for all aid stations |
| **Internal Failure** | Volunteer corrected during training; sponsor package design rejected and revised; registration portal bugs fixed before going live |
| **External Failure** | Participant complains about incorrect timing result (must be manually corrected); medical incident during race (highest cost — legal, reputational damage); negative post-race media coverage ← **PREVENT AT ALL COSTS** |

**Key QA Activities Timeline:**

| Week | QA Activity | Owner |
|------|-------------|-------|
| Week 8 | Verify permit documentation meets all city requirements | PM + WC |
| Week 18 | Volunteer training session #1 — competency assessment | Volunteer Coordinator |
| Week 26 | Full equipment inspection: timing gates, medals, T-shirts | WC |
| Week 28 | Medical team readiness review; AED equipment check | Safety Advisor |
| Week 30 | Volunteer training session #2 + Race Day rehearsal | Volunteer Coordinator |
| Week 31 | End-to-end dry run: route, aid stations, timing system, livestream | PM + all leads |
| Week 33 | Post-race survey analysis; compile quality report | Marketing + PM |

---

*PMG201c – Full Practice Exam Set (IT + Non-IT) with Model Answers*
*Covers all 14 PMG201c examination topics | Created for FPT University students*
*⚠️ For study purposes only — not an official FPT examination paper*
