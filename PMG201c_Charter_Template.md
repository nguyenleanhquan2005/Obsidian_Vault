# 📋 PMG201c – SỞ DÀN Ý & TEMPLATE ĐẦY ĐỦ (14 REQUIREMENTS)
## Fill-in-the-blank cho mọi đề IT và Non-IT

> [!important]
> **Cách dùng:** Đọc đề → highlight thông tin → điền vào `[...]`
> Chỗ có `* Tip:` là gợi ý cách nghĩ, **KHÔNG chép vào bài thi**
> Chỗ có `* IT:` / `* Non-IT:` = gợi ý riêng cho từng loại đề

---

# ⚡ BƯỚC ĐẦU TIÊN: ĐỌC ĐỀ VÀ TÁCH 5 NHÓM THÔNG TIN

```
┌─────────────────────────────────────────────────────────┐
│  ĐỌC ĐỀ → TÌM 5 THỨ NÀY → MỌI TEMPLATE ĐỀU CÓ ĐỦ DATA │
└─────────────────────────────────────────────────────────┘

  🏷️  TÊN & BẢN CHẤT:  "build app / organize event / develop system"
  👥  AI DÙNG:          "students / customers / participants / staff"
  📋  LÀM GÌ:           "register / submit / track / pay / attend / manage"
  🚧  GIỚI HẠN:         duration + budget + quality metrics + scope limits
  🎯  MỤC TIÊU SỐ:      "500 users / $15,000 revenue / 90% satisfaction"
```

---

---

# 1️⃣ PROJECT CHARTER

### 🧠 Hiểu đúng: Trả lời 4 câu hỏi lớn
```
WHY   → Vì sao project này ra đời? (Justification)
WHAT  → Project cần tạo ra / làm được gì? (Requirements)
HOW FAR → Giới hạn là gì? (Constraints: Scope/Time/Cost/Quality)
IF    → Giả định điều gì là đúng? (Assumptions)
```

### ✏️ TEMPLATE:

```
PROJECT NAME: [Tên project – lấy từ đề hoặc tự đặt tên hay]

─── PURPOSE / JUSTIFICATION ───────────────────────────────
Currently, [đối tượng] face the challenge of [vấn đề].
* Tip: Đề không nói vấn đề → tự chọn: "lack of", "inefficient", "no existing solution"
* IT:     "students rely on a desktop-only system not optimized for mobile"
* Non-IT: "the community lacks a dedicated platform/event/facility for..."

The [tên project] aims to [mục tiêu chính từ đề].
This will [lợi ích 1] and [lợi ích 2].
* Tip: Lợi ích IT:     "improve UX", "increase engagement", "reduce manual workload"
* Tip: Lợi ích Non-IT: "promote community well-being", "generate sponsorship revenue"

─── HIGH-LEVEL REQUIREMENTS ────────────────────────────────
- [Feature/Deliverable 1 từ đề]
- [Feature/Deliverable 2 từ đề]
- [Feature/Deliverable 3 từ đề – tự thêm cái obvious]
* IT thêm:     "Available on iOS [X]+ and Android [X]+"  |  "SSO login integration"
* Non-IT thêm: "All required government permits obtained" | "Safety protocols in place"

─── CONSTRAINTS ────────────────────────────────────────────
Scope:    Covers [những gì làm]. Excludes [những gì KHÔNG làm].
Time:     Project must be completed within [X months/weeks].
Cost:     Total budget must not exceed $[BAC].  [+ điều kiện đặc biệt từ đề]
Quality:  [Quality metric 1 từ đề]  |  [Quality metric 2]  |  [Tự thêm 1 nếu cần]

─── ASSUMPTIONS ─────────────────────────────────────────────
- [Người phê duyệt] will approve the charter by [Week X].
- The team of [X members] will be available full-time throughout the project.
- [External dependency] will be provided/ready by [Week X].
- [Beta testers / volunteers / participants] will be available for [phase/activity].
* IT:     "LMS/IT dept will provide API access by Week 2"
* Non-IT: "City permits will be granted within 5 business days of application"
```

---

---

# 2️⃣ WBS (Work Breakdown Structure)

### 🧠 Hiểu đúng: Cây phân rã công việc, bắt buộc đến Level 3
```
Level 1 = Tên project
Level 2 = Các PHASE (luôn đủ 5: Initiating / Planning / Executing / M&C / Closing)
Level 3 = Tasks trong mỗi phase
Level 4 = Sub-tasks (càng chi tiết càng tốt điểm)
```

### ✏️ TEMPLATE:

```
1. [Tên Project]

   1.1 Initiating
       1.1.1 Develop project charter
       1.1.2 Identify stakeholders & create stakeholder register
       1.1.3 Conduct kick-off meeting
       1.1.4 Obtain project charter approval from [Sponsor]

   1.2 Planning
       1.2.1 Develop Scope Management Plan
       1.2.2 Develop Time Management Plan & Gantt Chart
       1.2.3 Develop Cost Management Plan & budget
       1.2.4 Develop Risk Management Plan
       1.2.5 Develop Communication Plan
       1.2.6 Develop Quality Management Plan
       1.2.7 Develop HR & Resource Plan
       1.2.8 Obtain PMP approval

   1.3 Executing
       1.3.1 [Phase/Workstream 1 từ đề – VD: Analysis / Permitting]
             1.3.1.1 [Sub-task cụ thể]
             1.3.1.2 [Sub-task cụ thể]
       1.3.2 [Phase/Workstream 2 – VD: Design / Sponsorship]
             1.3.2.1 ...
       1.3.3 [Phase/Workstream 3 – VD: Development / Logistics]
             1.3.3.1 ...
       1.3.4 [Phase/Workstream 4 – VD: Testing / Marketing]
       1.3.5 [Phase/Workstream 5 – VD: Launch / Event Day]

       * IT Workstreams thường là:
         Requirements → Design → Backend Dev → Frontend Dev → API Integration → QA → Deployment

       * Non-IT Workstreams thường là:
         Permits → Sponsorship → Registration/Marketing → Logistics → Volunteer → Event Day

   1.4 Monitoring & Controlling
       1.4.1 Weekly progress tracking & status reports
       1.4.2 EVM analysis at [milestone weeks]
       1.4.3 Risk monitoring & issue log
       1.4.4 Change request management

   1.5 Closing
       1.5.1 Lessons learned session
       1.5.2 Final project report
       1.5.3 Archive all documentation
       1.5.4 [Formal handover / Ceremony / Thank-you communications]
```

---

---

# 3️⃣ DELIVERABLES & MILESTONES

### 🧠 Hiểu đúng: Milestone = CỘT MỐC quan trọng | Deliverable = SẢN PHẨM bàn giao tại mốc đó
```
Luôn có đủ: Initiating → Planning → [Giữa dự án] → Pre-launch/Pre-event → Closing
Completion Criteria = điều kiện để coi milestone là "xong" (ai ký? tỉ lệ bao nhiêu?)
```

### ✏️ TEMPLATE:

```
| # | Milestone            | Deliverables                        | Completion Criteria                    |
|---|----------------------|-------------------------------------|----------------------------------------|
| 1 | Project Initiated    | Approved project charter,           | Charter signed by [Sponsor];           |
|   | (Week [X])           | stakeholder register, kick-off mins | all key stakeholders identified        |
|---|----------------------|-------------------------------------|----------------------------------------|
| 2 | Planning Complete    | Project Management Plan             | PMP approved by sponsor;               |
|   | (Week [X])           | (all sub-plans)                     | team fully briefed                     |
|---|----------------------|-------------------------------------|----------------------------------------|
| 3 | [Mid milestone]      | [Deliverable từ đề]                 | [Ai approve? Tỉ lệ pass?]             |
|   | (Week [X])           | [VD: SRS doc / Permits granted]     | [VD: "Signed off by PO / City dept"]  |
|---|----------------------|-------------------------------------|----------------------------------------|
| 4 | [Pre-launch/event]   | [Deliverable từ đề]                 | [Điều kiện cụ thể]                    |
|   | (Week [X])           | [VD: Completed app / All logistics] | [VD: "0 critical bugs open"]          |
|---|----------------------|-------------------------------------|----------------------------------------|
| 5 | Project Closed       | Final report, lessons learned,      | Formal sign-off from all stakeholders; |
|   | (Week [X])           | archived documentation              | all outstanding payments settled       |

* Tip: IT thường có:    Design approved | Dev complete | UAT passed | App live
* Tip: Non-IT thường có: Permits secured | Sponsors confirmed | Logistics ready | Event complete
```

---

---

# 4️⃣ RACI MATRIX

### 🧠 Hiểu đúng: Mỗi task = ai làm (R), ai chịu trách nhiệm (A), ai tư vấn (C), ai được báo cáo (I)
```
QUY TẮC BẮT BUỘC:
✅ Mỗi task có đúng 1 chữ A (không được 2 A)
✅ Mỗi task có ít nhất 1 chữ R
✅ Dùng đủ cả 4 ký hiệu R / A / C / I
✅ Ít nhất 10 tasks
```

### ✏️ XÁC ĐỊNH ROLES TRƯỚC:

```
IT Roles thường dùng:      PM | BA | Dev | QA | PO (Product Owner)
Non-IT Roles thường dùng:  PM | Coordinator | Marketing | [Domain expert] | Sponsor rep

* Tip: Tự chọn 4-5 roles phù hợp với scenario.
* Tip: PM thường A hoặc C ở hầu hết tasks, hiếm khi R (PM quản lý, không làm trực tiếp)
* Tip: PO/Sponsor thường A ở các task liên quan yêu cầu, C hoặc I ở kỹ thuật
```

### ✏️ TEMPLATE:

```
| Task / Activity                 | [Role 1] | [Role 2] | [Role 3] | [Role 4] | [Role 5] |
|---------------------------------|----------|----------|----------|----------|----------|
| 1. Develop Project Charter      | A/R      | C        | I        | I        | C        |
| 2. [Task từ phase Initiating]   | A        | R        | I        | I        | C        |
| 3. [Task từ phase Planning]     | A/R      | C        | I        | I        | I        |
| 4. [Task Executing – Analysis]  | C        | A/R      | I        | I        | C        |
| 5. [Task Executing – Design]    | C        | C        | A/R      | I        | C        |
| 6. [Task Executing – Build 1]   | I        | I        | A/R      | C        | I        |
| 7. [Task Executing – Build 2]   | I        | I        | A/R      | C        | I        |
| 8. [Task Executing – QA/Check]  | C        | C        | I        | A/R      | C        |
| 9. [Task – Stakeholder output]  | C        | I        | I        | A/R      | A        |
| 10. [Launch / Event execution]  | A        | C        | R        | R        | I        |
| 11. [Post-project / Reporting]  | A/R      | I        | I        | I        | C        |
| 12. [Communication / Marketing] | C        | I        | I        | I        | A/R      |

* Tip: Viết tasks theo đúng thứ tự WBS của bạn → nhất quán và dễ chấm
* Tip: "A/R" nghĩa là 1 người vừa accountable vừa responsible (OK khi team nhỏ)
* Tip: Đừng để 1 cột toàn R hoặc toàn I → không realistic
```

---

---

# 5️⃣ SMART GOALS

### 🧠 Hiểu đúng: Mỗi goal = CỤ THỂ + ĐO ĐƯỢC + KHẢ THI + LIÊN QUAN + CÓ DEADLINE
```
Luôn phân tích RIÊNG TỪNG TIÊU CHÍ S-M-A-R-T, không gộp chung
Ít nhất 3 goals. Mỗi goal nên liên quan 1 khía cạnh khác nhau: User / Quality / Business
```

### ✏️ TEMPLATE (lặp lại cho mỗi goal):

```
GOAL [X]: [Câu tóm tắt goal – nên có con số cụ thể]
* Tip: IT:     "Achieve X active users within Y days of launch"
* Tip: Non-IT: "Register X participants by [date]" / "Score Y% in satisfaction survey"
* Tip: Câu tóm tắt = câu M (Measurable) viết ngắn gọn

- S (Specific):    [Ai, làm gì, ở đâu, mục tiêu cụ thể là gì?]
  * Tip: Trả lời "WHO does WHAT" – không dùng từ mơ hồ như "improve" mà nói rõ "increase X from Y to Z"

- M (Measurable):  [Đo bằng số liệu gì? Tool/metric nào? Ngưỡng cụ thể?]
  * Tip: IT:     "tracked via Firebase Analytics", "measured in Jira", "% in app store"
  * Tip: Non-IT: "measured through post-event survey", "tracked via registration portal"

- A (Attainable):  [Tại sao con số này khả thi? Dựa trên gì?]
  * Tip: Không nói "it is achievable" → phải giải thích: "based on [benchmark / resources / experience]"
  * Tip: IT:     "Feasible with a 3-person dev team and 6-month timeline"
  * Tip: Non-IT: "Based on similar events in comparable cities attracting [X] participants"

- R (Relevant):    [Goal này liên quan đến mục tiêu lớn hơn của project/tổ chức như thế nào?]
  * Tip: Kết nối goal với KPI của dự án:
         "This directly impacts [revenue / user adoption / brand reputation / sponsorship value]"

- T (Time-bound):  [Deadline cụ thể là khi nào?]
  * Tip: Nêu rõ "by end of Week X" hoặc "within [Y] months of launch"
  * Tip: Mỗi goal nên có deadline khác nhau (không phải tất cả cùng deadline)
```

---

---

# 6️⃣ RISK MANAGEMENT

### 🧠 Hiểu đúng: Rủi ro = thứ CÓ THỂ xảy ra (chưa xảy ra). Mitigation ≠ Contingency
```
Mitigation   = Làm TRƯỚC khi rủi ro xảy ra để giảm khả năng / tác động
Contingency  = Làm SAU khi rủi ro đã xảy ra để khắc phục

Ít nhất 3 risks, mỗi risk thuộc 1 domain khác nhau:
  Risk 1: Về chi phí / ngân sách
  Risk 2: Về tiến độ / nhân sự
  Risk 3: Về kỹ thuật / logistics / bên ngoài (tùy đề)
```

### ✏️ TEMPLATE:

```
| # | Risk Name        | Description              | Prob   | Impact | Mitigation Plan           | Contingency Plan           |
|---|------------------|--------------------------|--------|--------|---------------------------|----------------------------|
| 1 | Budget Overrun   | Actual costs exceed BAC  | Medium | High   | Add 10% buffer; estimate  | Negotiate scope cut with   |
|   |                  | due to underestimation   |        |        | carefully; weekly tracking| sponsor; defer features    |
|---|------------------|--------------------------|--------|--------|---------------------------|----------------------------|
| 2 | [Schedule risk]  | [Mô tả rủi ro tiến độ]   | [P]    | [I]    | [Giảm thiểu – làm trước]  | [Khắc phục – sau khi xảy] |
|   | VD: Key member   | Lead dev/coordinator     | Low    | High   | Cross-train team members; | Hire backup contractor;    |
|   | leaves project   | resignation mid-project  |        |        | document all work weekly  | brief replacement in 1 wk  |
|---|------------------|--------------------------|--------|--------|---------------------------|----------------------------|
| 3 | [External risk]  | [Rủi ro ngoài tầm kiểm  | [P]    | [I]    | [Phòng ngừa]              | [Ứng phó]                  |
|   | IT: API delay    | soát: permit denied,     |        |        |                           |                            |
|   | Non-IT: Weather  | system downtime, etc.]   |        |        |                           |                            |

* IT risks thường gặp:
  - API integration delay from external system
  - App Store rejection due to policy violation
  - Scope creep (stakeholders add features)
  - Performance issues under high user load

* Non-IT risks thường gặp:
  - Permit rejected / delayed by government
  - Sponsor withdrawal after signing
  - Low participant/customer registration
  - Weather / force majeure on event day
  - Key volunteer/staff unavailability
```

---

---

# 7️⃣ STAKEHOLDERS & ROLES

### 🧠 Hiểu đúng: Stakeholder = ai bị ảnh hưởng bởi project hoặc có thể ảnh hưởng đến project
```
Phân loại:  Internal (trong tổ chức làm project) | External (ngoài tổ chức)
Power/Interest Grid: 4 ô → 4 chiến lược quản lý
Ít nhất 5 stakeholders, gồm cả internal và external
```

### 📊 Power/Interest Grid (nhớ thuộc):
```
              HIGH INTEREST         LOW INTEREST
HIGH POWER  | Manage Closely   |  Keep Satisfied  |
LOW POWER   | Keep Informed    |  Monitor         |
```

### ✏️ TEMPLATE:

```
| Stakeholder        | Role & Responsibility                    | Type     | Power | Interest | Strategy        |
|--------------------|------------------------------------------|----------|-------|----------|-----------------|
| [Sponsor/Director] | Funds project; approves major decisions; | External | High  | High     | Manage Closely  |
|                    | signs off on deliverables                |          |       |          | (biweekly brief)|
| Project Manager    | Plans, executes, monitors all activities;| Internal | High  | High     | Manage Closely  |
|                    | manages team, budget, risks              |          |       |          | (core role)     |
| [Technical lead]   | [Trách nhiệm kỹ thuật cụ thể trong proj] | Internal | Med   | High     | Keep Informed   |
| IT: Dev Team       | Designs and codes the application        | Internal | Low   | High     | Keep Informed   |
| Non-IT: [Expert]   | [Domain expert: safety, logistics, etc.] | Internal | Med   | High     | Keep Informed   |
| [End Users]        | Primary users; participate in testing/   | External | Low   | High     | Keep Informed   |
| IT: Students       | UAT; provide feedback for improvement    |          |       |          | (surveys, beta) |
| [External authority| Grants permits; reviews compliance;      | External | High  | Low      | Keep Satisfied  |
| Non-IT: Govt dept] | enforces regulations                     |          |       |          | (formal reports)|
| [Another Internal] | [Eg: Marketing, Finance, QA team]        | Internal | Low   | Med      | Monitor         |

* Tip: Mô tả "Role & Responsibility" phải gắn với PROJECT CỤ THỂ trong đề
        Không viết chung chung "manages the project" → viết rõ "manages the 6-month app dev project for FPT University"
* Tip: Có đủ: 1 Sponsor + 1 PM + 2-3 Internal specialists + 1-2 External
```

---

---

# 8️⃣ USER STORIES

### 🧠 Hiểu đúng: Mô tả tính năng từ GÓC NHÌN NGƯỜI DÙNG, không phải góc nhìn developer
```
Format chuẩn:
  "As a [role/user type], I want [feature/action] so that [benefit/reason]."

Kèm theo: ≥ 2 Acceptance Criteria (AC) = điều kiện để coi story là "done"
Acceptance Criteria thường bắt đầu bằng: "The system/The user can..."

≥ 5 User Stories, mỗi story về 1 tính năng/hoạt động khác nhau
```

### ✏️ TEMPLATE (lặp lại cho mỗi story):

```
US-[XX]: [Tên tính năng ngắn gọn]
Title:  [1 cụm từ mô tả]
Story:  "As a [role], I want to [hành động cụ thể] so that [lý do / lợi ích]."

        * Tip: [role]   = student / participant / instructor / manager / organizer / customer
        * Tip: [action] = lấy từ danh sách tính năng trong đề (register, track, submit, view...)
        * Tip: [benefit]= "I can [lợi ích trực tiếp]" hoặc "I do not have to [bất tiện hiện tại]"

Acceptance Criteria:
- AC1: [Điều kiện cụ thể và kiểm tra được – dùng số liệu nếu có]
        * VD IT:     "The system displays confirmation within 5 seconds of submission"
        * VD Non-IT: "Participant receives email confirmation within 10 minutes of registration"
- AC2: [Điều kiện thứ 2 – thường về edge case hoặc error handling]
        * VD: "If the file exceeds [X]MB, an error message is displayed"
        * VD: "If registration is full, user sees 'Waitlist' button instead of 'Register'"
- AC3: [Thêm AC3 nếu cần – thường về UI/UX hoặc data retention]

* IT User Story topics thường dùng:
  Login/Auth | View content | Submit assignment | Track progress |
  Receive notification | Message instructor | Download offline | View results

* Non-IT User Story topics thường dùng:
  Online registration | Receive confirmation | Track status | Check schedule |
  View route/map | Submit feedback | Receive results/certificate | Contact organizer
```

---

---

# 9️⃣ ORGANIZATIONAL STRUCTURE

### 🧠 Hiểu đúng: Chọn 1 trong 3 loại và GIẢI THÍCH TẠI SAO PHÙ HỢP với project này
```
Functional   → Công việc routine, ổn định, nhân viên thuộc phòng ban cố định
Matrix       → Dự án cần chia sẻ nguồn lực từ nhiều phòng ban
Projectized  → Dự án ngắn hạn, scope rõ ràng, cần PM có toàn quyền
```

### ✏️ TEMPLATE:

```
CHOSEN STRUCTURE: [Functional / Matrix (Weak/Balanced/Strong) / Projectized]

JUSTIFICATION:
The [project name] adopts a [structure] organizational structure because:

1. [Lý do 1 – về đặc điểm của project]
   * IT short project (< 6 months, clear scope) → "Projectized: team needs full dedication"
   * Non-IT event using city dept staff      → "Matrix: resources shared with other programs"
   * Routine operations / no clear end date  → "Functional: stable, repeatable work"

2. [Lý do 2 – về quyền hạn PM]
   * Projectized: "PM requires full authority over budget and team decisions"
   * Matrix:      "PM coordinates across departments without permanent reassignment"

3. [Lý do 3 – về nguồn lực]
   * Projectized: "Team members are dedicated full-time to this project only"
   * Matrix:      "Specialists from [dept A] and [dept B] are shared across projects"

COMPARISON TABLE (luôn vẽ bảng này – dễ lấy điểm):

| Characteristic      | Functional   | Matrix (Strong) | Projectized  |
|---------------------|--------------|-----------------|--------------|
| PM Authority        | Little/None  | Moderate-High   | High/Total   |
| Resource Sharing    | By function  | Shared          | Dedicated    |
| Budget Control      | Func. Mgr    | Mixed           | PM           |
| PM Role             | Part-time    | Full-time       | Full-time    |
| Best For            | Routine ops  | Shared resources| Focused proj |
| ✅ CHOSEN REASON    |              |                 | [X]          |
```

---

---

# 🔟 COMMUNICATION PLAN

### 🧠 Hiểu đúng: Ai cần biết gì, bao giờ, qua kênh nào, ai gửi?
```
Cần đủ:     Nội dung (Information) | Mục đích (Purpose) | Tần suất (Frequency)
            Phương thức (Method/Format) | Người gửi (Responsible)
Luôn có:    Internal (PM ↔ team), Executive (PM → Sponsor), External (PM → End users)
```

### ✏️ TEMPLATE:

```
| Stakeholder  | Information             | Purpose               | Frequency      | Method/Format          | Responsible   |
|--------------|-------------------------|-----------------------|----------------|------------------------|---------------|
| [Sponsor /   | Budget status,          | Executive oversight;  | [Monthly /     | [Formal report / email | PM            |
|  Director]   | milestone completion,   | support key decisions | Bi-weekly]     |  / 30-min meeting]     |               |
|              | risk flags              |                       |                |                        |               |
|--------------|-------------------------|-----------------------|----------------|------------------------|---------------|
| [Core Team]  | Sprint goals, task list,| Coordinate daily work,| [Daily /       | [Standup meeting /     | PM / Scrum    |
| IT: Dev team | blockers, decisions     | remove impediments    | Weekly]        |  Jira / Slack]         | Master        |
|              |                         |                       |                |                        |               |
|--------------|-------------------------|-----------------------|----------------|------------------------|---------------|
| [Specialist] | Domain updates relevant | Align specialized     | [Weekly /      | [Email / shared docs / | PM / Lead     |
| IT: QA/BA    | to their workstream     | work with project     | As needed]     |  Sprint review]        |               |
| Non-IT: Safety                                                                                                                 |
|--------------|-------------------------|-----------------------|----------------|------------------------|---------------|
| [End Users]  | Progress updates,       | Manage expectations;  | [Bi-weekly /   | [Email newsletter /    | [Marketing /  |
| IT: Students | launch info, how-to     | drive adoption/engage | Weekly in      |  Social media /        |  BA]          |
| Non-IT: Parti| guides, event updates   |                       | final phase]   |  In-app notification]  |               |
|--------------|-------------------------|-----------------------|----------------|------------------------|---------------|
| [External    | Compliance docs,        | Maintain legal        | [As needed /   | [Formal letter /       | PM /          |
|  Authority]  | coordination requests   | requirement & safety  | Key milestones]|  Official meetings]    | Coordinator   |

* Tip: Tần suất nên TĂNG DẦN khi gần deadline (VD: từ weekly → daily trong race week)
* Tip: Sprint review / standup = IT; Volunteer briefing / weekly debrief = Non-IT
```

---

---

# 1️⃣1️⃣ GANTT CHART

### 🧠 Hiểu đúng: Timeline = activities + thời gian bắt đầu + kết thúc
```
Trong bài thi viết tay: vẽ bảng (table) với cột = tuần/tháng, hàng = activities
Điền ██ hoặc X hoặc /// vào ô tương ứng với thời gian activity diễn ra
Cột cuối "Monitoring & Control" thường kéo suốt dự án
```

### ✏️ TEMPLATE:

```
Tổng duration: [X] weeks

| Activity                      | W1-2 | W3-4 | W5-6 | W7-8 | W9-12 | W13-16 | W17-20 | W21-24 |
|-------------------------------|------|------|------|------|-------|--------|--------|--------|
| Initiating (Charter, Kickoff) | ████ |      |      |      |       |        |        |        |
| Planning (all sub-plans)      | ████ | ████ |      |      |       |        |        |        |
| [Executing: Phase 1]          |      |      | ████ | ████ |       |        |        |        |
| [Executing: Phase 2]          |      |      |      | ████ | ████  |        |        |        |
| [Executing: Phase 3 – Build]  |      |      |      |      | ████  | ████   |        |        |
| [Executing: Phase 4 – Test]   |      |      |      |      |       | ████   | ████   |        |
| [Executing: Phase 5 – Launch] |      |      |      |      |       |        |        | ████   |
| Monitoring & Control          | ████ | ████ | ████ | ████ | ████  | ████   | ████   | ████   |
| Closing                       |      |      |      |      |       |        |        | ████   |

* Tip: Phases không nhất thiết tuần tự – Design có thể overlap với Early Dev
* Tip: Số tuần trong mỗi phase = (thời gian từ WBS của bạn)
* IT:     Req(2w) → Design(3w) → Dev(6w) → QA(3w) → Launch(1w)  [common pattern]
* Non-IT: Permit(4w) → Sponsor(6w) → Registration(8w) → Logistics(6w) → Event(1w)
```

---

---

# 1️⃣2️⃣ CRITICAL PATH METHOD ⭐ PHẢI LẤY TRỌN ĐIỂM

### 🧠 Hiểu đúng: Tìm đường dài nhất trong mạng hoạt động = thời gian tối thiểu hoàn thành project
```
Float = 0 → Critical (nằm trên Critical Path)
Float > 0 → Non-critical (có thể trễ tối đa Float mà không ảnh hưởng project)
```

### 📐 CÔNG THỨC (thuộc lòng):

```
FORWARD PASS (trái → phải):
  ES (task đầu tiên) = 0
  EF = ES + Duration
  Nếu task có NHIỀU predecessors: ES = MAX(EF của tất cả predecessors)

BACKWARD PASS (phải → trái):
  LF (task cuối cùng) = Project Duration = EF của task cuối
  LS = LF - Duration
  Nếu task có NHIỀU successors: LF = MIN(LS của tất cả successors)

FLOAT = LS - ES  (hoặc LF - EF, kết quả như nhau)
CRITICAL PATH = tất cả tasks có Float = 0
```

### ✏️ TEMPLATE ĐỂ GIẢI:

```
BƯỚC 1: Liệt kê tất cả activities và vẽ sơ đồ phụ thuộc

BƯỚC 2: FORWARD PASS
┌──────────┬──────────────┬────────┬──────────┬────────┐
│ Activity │ Predecessors │   ES   │ Duration │   EF   │
├──────────┼──────────────┼────────┼──────────┼────────┤
│ A        │ –            │   0    │   [dur]  │  [EF]  │
│ B        │ A            │  [EF_A]│   [dur]  │  [EF]  │
│ C        │ A            │  [EF_A]│   [dur]  │  [EF]  │
│ D        │ B, C         │MAX(...)│   [dur]  │  [EF]  │
│ ...      │ ...          │  ...   │   ...    │  ...   │
└──────────┴──────────────┴────────┴──────────┴────────┘
  Project Duration = EF của task cuối cùng

BƯỚC 3: BACKWARD PASS
┌──────────┬────────────┬────────┬──────────┬────────┐
│ Activity │ Successors │   LF   │ Duration │   LS   │
├──────────┼────────────┼────────┼──────────┼────────┤
│ [Last]   │ –          │ [=EF]  │   [dur]  │  [LS]  │
│ ...      │ ...        │MIN(...)│   ...    │  ...   │
│ A        │ B, C       │MIN(...)│   [dur]  │  [LS]  │
└──────────┴────────────┴────────┴──────────┴────────┘

BƯỚC 4: TÍNH FLOAT & XÁC ĐỊNH CRITICAL PATH
┌──────────┬────┬────┬────┬────┬────────┬───────────┐
│ Activity │ ES │ EF │ LS │ LF │ Float  │ Critical? │
├──────────┼────┼────┼────┼────┼────────┼───────────┤
│ A        │    │    │    │    │ [LS-ES]│ ✅/❌     │
│ B        │    │    │    │    │        │           │
│ ...      │    │    │    │    │        │           │
└──────────┴────┴────┴────┴────┴────────┴───────────┘

CRITICAL PATH: [Task] → [Task] → [Task] → ... → End
PROJECT DURATION: [X] weeks/days

BƯỚC 5: TRẢ LỜI CÂU HỎI PHỤ (nếu có)
  Crashing:     Chỉ rút ngắn task trên Critical Path | Ưu tiên task DÀI NHẤT trước
  Fast Tracking: Làm song song 2 tasks vốn FS        | Không tốn tiền nhưng TĂNG rủi ro
```

---

---

# 1️⃣3️⃣ EVM (Earned Value Management) ⭐ PHẢI LẤY TRỌN ĐIỂM

### 📐 TOÀN BỘ CÔNG THỨC (thuộc lòng):

```
CÁC GIÁ TRỊ ĐẦU VÀO (đề cho):
  BAC  = Budget at Completion (tổng ngân sách)
  BDAC = Budgeted Duration at Completion (tổng thời gian kế hoạch)
  AC   = Actual Cost (chi phí thực tế tại thời điểm đánh giá)
  t    = thời điểm đánh giá (VD: tháng 6 của dự án 12 tháng)
  %    = phần trăm công việc hoàn thành THỰC TẾ

BƯỚC TÍNH (theo thứ tự này):
  PV   = BAC × (t / BDAC)              → Kế hoạch chi bao nhiêu đến giờ?
  EV   = BAC × %complete               → Giá trị thực sự tạo ra là bao nhiêu?
  CV   = EV - AC                       → +: under budget | -: over budget
  SV   = EV - PV                       → +: ahead | -: behind schedule
  CPI  = EV / AC                       → >1: tốt (under) | <1: xấu (over)
  SPI  = EV / PV                       → >1: tốt (ahead) | <1: xấu (behind)
  EAC  = BAC / CPI                     → Tổng chi phí dự kiến khi xong
  ETC  = EAC - AC                      → Cần thêm bao nhiêu tiền?
  VAC  = BAC - EAC                     → +: dư | -: vượt ngân sách khi xong
  EDAC = BDAC / SPI                    → Dự kiến xong sau bao lâu?
```

### ✏️ TEMPLATE ĐỂ GIẢI:

```
GIVEN:  BAC=$[X] | BDAC=[Y] months | Evaluated at month [t] | AC=$[Z] | %complete=[%]

┌────────┬───────────────────────────┬──────────────────┬─────────────────────────────────────┐
│ Metric │ Formula                   │ Calculation      │ Interpretation                      │
├────────┼───────────────────────────┼──────────────────┼─────────────────────────────────────┤
│ PV     │ BAC × (t / BDAC)          │ [X]×([t]/[Y])=   │ Planned to spend $[PV] by month [t] │
│ EV     │ BAC × %complete           │ [X]×[%]=         │ Work worth $[EV] has been completed  │
│ CV     │ EV - AC                   │ [EV]-[AC]=       │ [+: Under / -: Over] budget by $[│CV│]│
│ SV     │ EV - PV                   │ [EV]-[PV]=       │ [+ Ahead / - Behind] schedule by $  │
│ CPI    │ EV / AC                   │ [EV]/[AC]=       │ [>1: Good / <1: Bad]: $1→$[CPI] val │
│ SPI    │ EV / PV                   │ [EV]/[PV]=       │ Running at [SPI×100]% planned speed │
│ EAC    │ BAC / CPI                 │ [X]/[CPI]=       │ Total predicted final cost = $[EAC] │
│ ETC    │ EAC - AC                  │ [EAC]-[AC]=      │ Still needs $[ETC] to complete       │
│ VAC    │ BAC - EAC                 │ [X]-[EAC]=       │ [+: surplus / -: deficit] = $[VAC]  │
│ EDAC   │ BDAC / SPI                │ [Y]/[SPI]=       │ Will finish in [EDAC] months        │
└────────┴───────────────────────────┴──────────────────┴─────────────────────────────────────┘

OVERALL STATUS:
  Cost:     [OVER / UNDER] BUDGET  (CPI=[X] [< / >] 1)
  Schedule: [AHEAD / BEHIND]       (SPI=[X] [> / <] 1)
  Forecast: Final cost = $[EAC], which [exceeds/is below] BAC by $[|VAC|]
  Duration: Will finish [X] months [early/late] ([EDAC] vs [BDAC] planned)

PM ACTIONS (luôn đề xuất ít nhất 2):
  If over budget:  "Audit spending categories / Negotiate with vendors / Reduce scope"
  If behind sched: "Apply schedule crashing / Fast tracking / Add resources"
  If both bad:     Escalate to sponsor immediately + corrective action plan
```

---

---

# 1️⃣4️⃣ QA/QC PLAN

### 🧠 Hiểu đúng: Có 4 loại chi phí chất lượng + các hoạt động QA cụ thể theo từng phase
```
Prevention  = Đầu tư TRƯỚC để tránh lỗi (training, standards, process docs)
Appraisal   = Kiểm tra TRONG khi làm (review, testing, audit)
Int. Failure = Lỗi phát hiện TRƯỚC khi bàn giao (rework, bug fix pre-launch)
Ext. Failure = Lỗi sau khi bàn giao (warranty, hotfix, customer complaint) ← TỐN NHẤT
```

### ✏️ TEMPLATE:

```
─── QUALITY STANDARDS ──────────────────────────────────────
(Lấy từ đề + tự thêm các tiêu chuẩn hiển nhiên)

  - [Quality metric 1 từ đề – VD: "App rating ≥ 4.0/5.0"]
  - [Quality metric 2 từ đề – VD: "Satisfaction ≥ 90%"]
  - [Tự thêm IT:     "Crash rate < 0.5% | Response time < 2s | 0 critical bugs at launch"]
  - [Tự thêm Non-IT: "Zero serious safety incidents | All aid stations operational 30 min before event"]

─── COST OF QUALITY TABLE ──────────────────────────────────

| Category               | Activities                                                    |
|------------------------|---------------------------------------------------------------|
| Prevention             | [Training cho team] | [Coding/process standards] |            |
|                        | [Design review sessions] | [Checklist creation]           |
| Appraisal              | [Peer code review] | [Test case execution] |                |
|                        | [Load/stress testing] | [Inspection/audit]               |
| Internal Failure       | [Bug fix before release] | [Rework of rejected design] |   |
|                        | [Regression testing after patches]                          |
| External Failure       | [Negative user reviews] | [Post-launch hotfixes] |          |
|  (Most expensive!)     | [Customer complaints] | [Safety incidents / legal risk]  |
|                        |  ← INVEST IN PREVENTION TO AVOID THESE                      |

─── QA ACTIVITIES TIMELINE ────────────────────────────────

| Phase / Week   | QA Activity                                    | Owner        |
|----------------|------------------------------------------------|--------------|
| Planning       | Create quality management plan & test plan     | PM / QA Lead |
|                | Define acceptance criteria for all features    | BA / QA      |
| Design phase   | Prototype review / Design walkthrough          | BA + QA      |
| Development    | Unit testing (automated, daily via CI/CD)      | Dev          |
| Pre-launch     | Integration testing | System testing            | QA           |
| UAT phase      | [Beta test with X users / Dry run / Rehearsal] | QA + Users   |
| Post-launch    | Monitor [Crashlytics / reviews / surveys]      | QA Lead      |
| Week [X]       | [QA activity cụ thể từ scenario]               | [Owner]      |

* IT:     Unit test → Integration → System → UAT → Post-launch monitoring
* Non-IT: Supplier check → Equipment inspection → Dry run → Event day monitoring → Survey
```

---

---

# 🚀 QUICK REFERENCE: MỌI ĐỀ ĐỀU CÓ THỂ ĐIỀN VÀO ĐÂY

## 📊 Bảng tra: Đề nói gì → Viết gì ở đâu

| Đề nói... | Requirement liên quan | Viết gì |
|-----------|----------------------|---------|
| "build / develop app" | Charter, WBS, User Stories | Platform (iOS/Android), SSO login, offline mode |
| "organize / plan event" | Charter, Deliverables, Risk | Permits, safety plan, volunteer plan, weather risk |
| "$X budget" | Charter Constraints, EVM | BAC = $X; add 10% buffer in Risk |
| "X months / weeks" | Charter, Gantt, CPM, EVM | BDAC = X; timeline in Gantt |
| "Y% satisfaction/rating" | Charter, SMART Goals, QA | Quality metric appears in all 3 |
| "students / participants use it" | Stakeholders, User Stories | End Users = Low power, High interest → Keep Informed |
| "existing system / current LMS" | Charter Assumptions, Risk | "API access by Week X" assumption + "API delay" risk |
| "free software only" | Charter Constraints | Cost constraint: "all software must be free/open-source" |
| "secure permits" | WBS (1.3.1), Deliverables, Risk | Permit as a milestone; "permit denial" risk |
| "train staff / volunteers" | WBS, RACI, User Stories | Training as deliverable; US for trained staff role |
| "sponsor / funding" | Stakeholders, Risk, ComPlan | Sponsor = High power; risk = "sponsor withdrawal" |
| "quality / integrity / no error" | SMART Goals, QA, Risk | Quality metric in Goals; QA prevention activities |

---

*PMG201c – 14 Requirements Complete Template*
*Dùng cho mọi đề IT và Non-IT | FPT University*
*For study purposes only*
