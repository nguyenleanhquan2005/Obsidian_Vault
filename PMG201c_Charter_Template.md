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

## 🧠 Nguyên tắc vàng: Bạn TỰ SÁNG TẠO có căn cứ

```
❌ Suy nghĩ sai: "Đề không nói thì mình không biết, không viết được"
✅ Suy nghĩ đúng: "Đề cho scenario → mình đóng vai PM →
                   tự đặt chi tiết HỢP LÝ dựa trên thực tế"
```

---

## 🧩 BƯỚC 2: HỎI 5 CÂU NÀY TRƯỚC KHI VIẾT

```
❓ Câu 1: PROBLEM
   "Vấn đề hiện tại là gì mà project này ra đời để giải quyết?"
   → Đề nói "build X" → ngầm hiểu "hiện tại CHƯA CÓ X" hoặc "X hiện tại tệ"
   → Viết: "Currently, [users] lack / struggle with [vấn đề]..."

❓ Câu 2: WHO
   "Ai được hưởng lợi từ project này?"
   → Đó là End User / Beneficiary trong Justification
   → VD: "students will be able to...", "participants will benefit from..."

❓ Câu 3: WHAT
   "Project tạo ra cái gì cụ thể?"
   → High-Level Requirements – lấy từ đề rồi viết lại + thêm 2-3 cái obvious

❓ Câu 4: LIMITS
   "Project KHÔNG làm gì? Bị giới hạn bởi gì?"
   → Constraints: Scope, Time, Cost, Quality
   → Scope exclusion: thứ gì liên quan nhưng KHÔNG trong phạm vi

❓ Câu 5: CONDITIONS
   "Cần điều kiện gì để project có thể chạy?"
   → Assumptions – những điều bạn giả định là đúng/có sẵn
```

---

## 🖥️ TEMPLATE A – DỰ ÁN IT / APP / SOFTWARE

### 🔍 Cách đọc đề IT nhanh:
- Đề nói "build / develop / create" → đây là dự án làm ra sản phẩm phần mềm
- Tìm: ai dùng? (students, customers, staff) → đó là End User
- Tìm: làm được gì? (submit, track, pay, communicate) → High-Level Requirements
- Nếu đề nói "mobile app" → tự thêm: iOS + Android, offline mode, app store submission

### ✏️ Fill-in Template:

```
PROJECT NAME: [Tên project từ đề / tự đặt tên hay]
  * Tip: Nếu đề không đặt tên → tự đặt kiểu "[Tính năng chính] + [App/System/Platform]"
  * VD: "CampusEats – Food Delivery App" | "EduTrack – Student LMS Mobile App"

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

1. PURPOSE / JUSTIFICATION
   (Tại sao dự án này cần làm? Problem nó giải quyết là gì?)

   Currently, [đối tượng người dùng] face the challenge of [vấn đề đang tồn tại].
   * Tip: Đề không nói vấn đề → tự bịa: "students lack a centralized platform to...",
           "the current system is desktop-only and not mobile-friendly",
           "there is no digital solution for..."

   The [tên project] aims to [mục tiêu chính – copy/paraphrase từ đề].
   By implementing this solution, [lợi ích cụ thể – tự thêm 1-2 cái].
   * Tip: Lợi ích thường là: "improve user experience", "reduce processing time",
           "increase engagement", "support the organization's digital transformation"

   This project aligns with [tên tổ chức]'s strategic goal of [tự thêm mục tiêu lớn].
   * Tip: Tự thêm kiểu: "becoming a leading digital university by 20XX"
           hoặc "achieving full digital service delivery by 20XX"

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

2. HIGH-LEVEL REQUIREMENTS
   (App cần làm được những gì? Lấy từ đề + tự thêm obvious features)

   - [Feature 1 từ đề – viết lại rõ hơn]
   - [Feature 2 từ đề]
   - [Feature 3 từ đề]
   - [Tự thêm: User authentication / login with existing account (SSO)]
   - [Tự thêm: Notification system – push notifications or email alerts]
   - [Tự thêm: Available on iOS [version]+ and Android [version]+]
   * Tip: Đề nói "mobile app" → tự thêm platform specs là luôn đúng
   * Tip: Đề nói "connect to existing system" → tự thêm "SSO / API integration"

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

3. PROJECT CONSTRAINTS
   (BẮT BUỘC đủ 4 loại: Scope / Time / Cost / Quality)

   SCOPE:
   - The project covers: [những gì được làm – từ đề]
   - The project EXCLUDES: [những gì không làm – từ đề hoặc tự thêm]
   * Tip: Đề nói "mobile only" → "Web portal is excluded from this phase"
   * Tip: Nếu đề không nói exclusion → tự thêm:
           "Third-party payment gateway integration is excluded from Phase 1"

   TIME:
   - The project must be completed within [X months / weeks] from project start.
   * Tip: Lấy thẳng từ đề. Nếu đề không có → tự đặt hợp lý (3-6 tháng cho IT)

   COST / BUDGET:
   - Total project budget must not exceed $[BAC từ đề].
   - [Thêm: "Product manufacturing cost is excluded" nếu đề có nói]
   * Tip: Lấy thẳng từ đề. Con số nào cũng OK miễn là consistent.

   QUALITY:
   - [Lấy tất cả các yêu cầu chất lượng từ đề – thường là số %, rating, uptime]
   - App crash rate must be below [0.5% – tự đặt nếu đề không cho]
   - All user data must comply with [security standard – VD: OWASP / HIPAA nếu liên quan]
   * Tip: Đề hay nói: "rating ≥ 4.0", "uptime 99%", "response < 2s", "satisfaction > 90%"
   * Tip: Nếu đề không nói quality → tự thêm: "zero critical bugs at launch"

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

4. ASSUMPTIONS
   (Những điều bạn GIẢ ĐỊNH là đúng – 100% tự viết, không cần từ đề)

   - [Người phê duyệt / Sponsor] will approve the project charter by [Week X].
   - The development team of [X members] will be available full-time for the project duration.
   - [Bên liên quan kỹ thuật – VD: IT department / existing system team] will provide
     API / database access by [Week X].
   - [Số lượng] beta testers / users will be available for UAT during [Week X–Y].
   - All required licenses and third-party tools will be acquired within the project budget.

   * Tip: Assumption = điều kiện để project có thể chạy được
   * Tip: Luôn có assumption về: người phê duyệt, team availability,
           external dependency, test users, tools/licenses
```

---

## 🌿 TEMPLATE B – DỰ ÁN NON-IT (EVENT / CONSTRUCTION / SERVICE)

### 🔍 Cách đọc đề Non-IT nhanh:
- Đề nói "organize / plan / set up / establish / build" một thứ vật lý hoặc sự kiện
- Tìm: ai tham gia? (participants, visitors, customers) → End User
- Tìm: mục tiêu số học? (100 people, $30,000 revenue, 90% satisfaction) → Success Metrics
- Tìm: điều kiện đặc biệt? (permits, weather, safety, compliance) → Constraints/Risks

### ✏️ Fill-in Template:

```
PROJECT NAME: [Tên project từ đề / tự đặt]
  * Tip: Non-IT thường đặt kiểu: "[Tên sự kiện] 20XX" | "[Tên công trình] Project"
  * VD: "City Marathon 2026" | "FPT Annual Tech Fair" | "Community Garden Initiative"

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

1. PURPOSE / JUSTIFICATION

   [Tên tổ chức / cơ quan] has identified that [vấn đề hiện tại / cơ hội].
   * Tip: Đề nói "local media lacks coverage" → "Currently, the community lacks..."
   * Tip: Đề nói "promote health" → "Rising rates of [bệnh/vấn đề] in the community..."
   * Tip: Không biết vấn đề gì → tự chọn 1 trong:
           "lack of engagement", "inadequate facilities", "no existing solution",
           "growing demand for...", "increasing [số liệu tăng] in..."

   The [tên project] will [mục tiêu chính từ đề – viết lại bằng lời của bạn].
   Upon completion, this project will [lợi ích 1] and [lợi ích 2].
   * Tip: Lợi ích của Non-IT thường là:
           "promote community well-being", "generate sponsorship/economic value",
           "build brand/reputation for [tổ chức]", "attract [X] visitors/participants"

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

2. HIGH-LEVEL REQUIREMENTS

   - [Deliverable / Output chính 1 từ đề]
   - [Deliverable / Output chính 2 từ đề]
   - [Tự thêm: Permits and compliance với quy định địa phương]
   - [Tự thêm: Safety and emergency protocols must be established]
   - [Tự thêm: Post-event reporting / evaluation to be conducted]
   * Tip: Non-IT hay cần: permits, safety plans, volunteer plans, marketing, logistics

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

3. PROJECT CONSTRAINTS

   SCOPE:
   - The project covers: [hoạt động được thực hiện – từ đề]
   - The project EXCLUDES: [hoạt động không làm – tự thêm nếu đề không cho]
   * Tip: Non-IT thường exclude: "permanent facility construction",
           "virtual/online participation", "international participants"

   TIME:
   - All pre-event preparation activities must be completed by [Week X / Month X].
   - The [event/project] is scheduled for [ngày cụ thể hoặc "end of Week X"].
   * Tip: Đề nói "3-month period" → bạn convert ra weeks nếu cần

   COST / BUDGET:
   - Total budget must not exceed $[BAC từ đề].
   - [Thêm điều kiện đặc biệt từ đề – VD: "all software must be free/open-source",
     "inventory shrinkage must be below 2% of total inventory value"]

   QUALITY:
   - [Lấy tất cả quality metrics từ đề]
   * Tip: Non-IT quality thường là: satisfaction %, zero injuries, zero complaints,
           completion rate %, on-time delivery

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

4. ASSUMPTIONS

   - All required government permits and licenses will be obtained by [Week X].
   - [Tổ chức / cơ quan liên quan] will provide [resource cụ thể] without additional cost.
   - A minimum of [X] volunteers / staff will be recruited and trained before [Week X].
   - Weather and external conditions will be suitable for the event on the scheduled date.
   - Sponsors/partners will confirm their commitments by [Week X].

   * Tip: Non-IT assumptions thường về: permits, weather, volunteers, sponsors, venue access
```

---

## 📌 BẢNG TRA NHANH: "ĐỀ NÓI GÌ → CHARTER VIẾT GÌ"

| Đề nói... | → Bạn viết trong Charter... |
|-----------|---------------------------|
| "build a mobile app" | High-Level Req: "Available on iOS [X]+ and Android [X]+" |
| "students will use it" | Justification: "Currently, students lack a centralized platform to..." |
| "3-month project" | Constraint Time: "The project must be completed within 3 months (12 weeks)" |
| "$500 budget" | Constraint Cost: "Total budget must not exceed $500 for all categories" |
| "all software must be free" | Constraint Cost: "All software tools used must be free or open-source" |
| "90% satisfaction" | Constraint Quality: "User satisfaction score must exceed 90% based on post-surveys" |
| "500 subscribers goal" | Justification + SMART Goal: primary success metric |
| "existing system / current LMS" | Assumption: "[X] dept will provide API/database access by Week [X]" |
| "student volunteers / staff" | Assumption: "At least [X] volunteers available by Week [X]" |
| "one-day event" | Constraint Scope: "The event takes place on a single designated day" |
| "no web version" / "mobile only" | Constraint Scope: "Web portal is explicitly excluded from this phase" |
| "zero complaints / zero inaccuracies" | Constraint Quality: "Zero verifiable complaints of [error/incident]" |

---

## 🎓 VÍ DỤ ÁP DỤNG VỚI ĐỀ THẬT

### Đề gốc (Practical Exam – Fall 2025):
> *"You have developed a unique consumer product. Your project is to validate market viability through a temporary pop-up retail operation. Requires securing permits, designing display, managing inventory, training student sales staff, achieving $15,000 gross revenue. Operation must run for two consecutive weeks. Setup costs limited to $1,500. Inventory shrinkage below 2%. Customer satisfaction must exceed 90% positive feedback."*

### Áp dụng từng bước:

**Bước 1 – Highlight 5 thứ:**
| | Tìm được |
|-|---------|
| 🏷️ Tên | pop-up retail validation (đề cho) |
| ⏱️ Thời gian | 2 consecutive weeks (operation) |
| 💰 Ngân sách | $1,500 (setup/operational) |
| ⭐ Chất lượng | >90% positive feedback, shrinkage < 2% |
| 🔲 Scope | securing permits + display + inventory + training → goal $15,000 |

**Bước 2 – Hỏi 5 câu:**
- Problem → *"Chưa biết sản phẩm có khả thi trên thị trường chưa"*
- Who → *Consumers mua, tổ chức học được data thị trường*
- What → permits + display + inventory + training + sales
- Limits → Scope (retail only), Time (2 weeks), Cost ($1,500), Quality (90% + 2%)
- Conditions → *venue sẵn sàng, permits được duyệt, staff train xong trước ngày mở*

**Bước 3 – Kết quả viết vào bài:**

```
PROJECT NAME: Pop-Up Retail Market Validation

PURPOSE / JUSTIFICATION:
The organization has developed a unique consumer product but lacks real-world market
data to justify large-scale production investments. The Pop-Up Retail Market Validation
project will establish a temporary physical retail operation to interact directly with
target consumers, test product-market fit, and validate revenue potential.
A successful pop-up achieving the $15,000 revenue target will provide the evidence
required to secure further investment for full-scale production.

HIGH-LEVEL REQUIREMENTS:
- Secure all necessary retail permits and venue agreements prior to operation
- Design and build a professional product display booth
- Manage product inventory with shrinkage rate below 2% of total inventory value
- Train student sales staff on product knowledge, sales technique, and POS systems
- Achieve $15,000 in gross revenue over the two-week operation period
- Collect post-purchase customer feedback surveys from all buyers

CONSTRAINTS:
  Scope:  Covers only the temporary pop-up physical retail operation.
          Excludes online/e-commerce sales channels and post-pop-up distribution.
  Time:   The pop-up operation must run for exactly two consecutive weeks.
          All setup activities must be completed before Day 1 of operation.
  Cost:   Setup and operational costs must not exceed $1,500 (excluding product cost).
          Total inventory shrinkage must remain below 2% of total inventory value.
  Quality: Customer satisfaction must exceed 90% positive feedback on post-purchase
           surveys regarding product quality and retail experience.

ASSUMPTIONS:
- A suitable retail venue will be available for lease within budget by Week 1.
- All government/mall retail permits will be granted within 5 business days.
- Student sales staff (at least 4 people) will be available for full 2-week operation.
- Product inventory will be delivered to pop-up location before operation start date.
```

> [!tip]
> **So sánh:** Đề gốc chỉ ~5 dòng. Bài làm ~20 dòng.
> Phần thêm vào = những thứ "hiển nhiên" PM nào làm project này cũng phải biết.
> Giáo viên kiểm tra STRUCTURE & LOGIC, không kiểm tra số liệu thật.

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
       1.3.1 [Workstream 1 từ đề]
             1.3.1.1 [Sub-task cụ thể]
             1.3.1.2 [Sub-task cụ thể]
       1.3.2 [Workstream 2]
       1.3.3 [Workstream 3]
       1.3.4 [Workstream 4 – Testing / Marketing]
       1.3.5 [Workstream 5 – Launch / Event Day]

       * IT Workstreams:
         Requirements → Design → Backend Dev → Frontend Dev → API Integration → QA → Deployment

       * Non-IT Workstreams:
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

### 🧠 Hiểu đúng:
```
Milestone  = Cột mốc quan trọng (checkpoint)
Deliverable = Sản phẩm bàn giao tại mốc đó
Completion Criteria = Điều kiện để coi milestone là "xong" (ai ký? tỉ lệ bao nhiêu?)
Luôn có: Initiating → Planning → [Mid milestone] → Pre-launch/Pre-event → Closing
```

### ✏️ TEMPLATE:

```
| # | Milestone             | Deliverables                         | Completion Criteria                   |
|---|-----------------------|--------------------------------------|---------------------------------------|
| 1 | Project Initiated     | Approved project charter,            | Charter signed by [Sponsor];          |
|   | (Week [X])            | stakeholder register, kick-off mins  | all key stakeholders identified       |
| 2 | Planning Complete     | Project Management Plan              | PMP approved by sponsor;              |
|   | (Week [X])            | (all sub-plans)                      | team fully briefed                    |
| 3 | [Mid milestone]       | [Deliverable từ đề]                  | [Ai approve? Tỉ lệ pass?]            |
|   | (Week [X])            | VD: SRS doc / Permits granted        | VD: "Signed off by PO / City dept"   |
| 4 | [Pre-launch/event]    | [Deliverable từ đề]                  | [Điều kiện cụ thể]                   |
|   | (Week [X])            | VD: Completed app / All logistics    | VD: "0 critical bugs open"            |
| 5 | Project Closed        | Final report, lessons learned,       | Formal sign-off from all stakeholders |
|   | (Week [X])            | archived documentation               | all outstanding payments settled      |

* IT milestones:   Design approved | Dev complete | UAT passed | App live
* Non-IT milestone: Permits secured | Sponsors confirmed | Logistics ready | Event complete
```

---
---

# 4️⃣ RACI MATRIX

### 🧠 Quy tắc bắt buộc:
```
✅ Mỗi task có đúng 1 chữ A (không được 2 A)
✅ Mỗi task có ít nhất 1 chữ R
✅ Dùng đủ cả 4 ký hiệu R / A / C / I
✅ Ít nhất 10 tasks
```

### ✏️ XÁC ĐỊNH ROLES TRƯỚC:
```
IT Roles:     PM | BA | Dev | QA | PO (Product Owner)
Non-IT Roles: PM | Coordinator | Marketing | [Domain expert] | Sponsor rep

* PM thường A hoặc C, hiếm khi R (PM quản lý, không làm trực tiếp)
* PO/Sponsor thường A ở tasks liên quan yêu cầu, C hoặc I ở kỹ thuật
```

### ✏️ TEMPLATE:

```
| Task / Activity                 | [Role 1] | [Role 2] | [Role 3] | [Role 4] | [Role 5] |
|---------------------------------|----------|----------|----------|----------|----------|
| 1. Develop Project Charter      | A/R      | C        | I        | I        | C        |
| 2. [Task – Initiating]          | A        | R        | I        | I        | C        |
| 3. [Task – Planning]            | A/R      | C        | I        | I        | I        |
| 4. [Task – Analysis/Design 1]   | C        | A/R      | I        | I        | C        |
| 5. [Task – Analysis/Design 2]   | C        | C        | A/R      | I        | C        |
| 6. [Task – Build/Execute 1]     | I        | I        | A/R      | C        | I        |
| 7. [Task – Build/Execute 2]     | I        | I        | A/R      | C        | I        |
| 8. [Task – QA/Check]            | C        | C        | I        | A/R      | C        |
| 9. [Task – Stakeholder review]  | C        | I        | I        | A/R      | A        |
| 10. [Launch / Event execution]  | A        | C        | R        | R        | I        |
| 11. [Post-project / Reporting]  | A/R      | I        | I        | I        | C        |
| 12. [Communication/Marketing]   | C        | I        | I        | I        | A/R      |

* Viết tasks theo thứ tự WBS → nhất quán và dễ chấm
* "A/R" = 1 người vừa accountable vừa responsible (OK khi team nhỏ)
* Đừng để 1 cột toàn R hoặc toàn I → không realistic
```

---
---

# 5️⃣ SMART GOALS

### 🧠 Quy tắc:
```
Phân tích RIÊNG TỪNG TIÊU CHÍ S-M-A-R-T, KHÔNG gộp chung
Ít nhất 3 goals, liên quan 3 khía cạnh: User / Quality / Business/Revenue
```

### ✏️ TEMPLATE (lặp lại cho mỗi goal):

```
GOAL [X]: [Câu tóm tắt – nên có con số cụ thể]
* IT:     "Achieve X active users within Y days of launch"
* Non-IT: "Register X participants by [date]" / "Score Y% in satisfaction survey"

- S (Specific):   [Ai, làm gì, ở đâu, mục tiêu cụ thể?]
  * Không dùng "improve" → dùng "increase X from Y to Z"

- M (Measurable): [Đo bằng số liệu gì? Tool nào? Ngưỡng cụ thể?]
  * IT:     "tracked via Firebase Analytics / Jira / App Store rating"
  * Non-IT: "measured through post-event survey / registration portal"

- A (Attainable): [Tại sao con số này khả thi? Dựa trên gì?]
  * KHÔNG nói "it is achievable" → phải giải thích: "based on [benchmark / resources]"
  * IT:     "Feasible with a 3-person dev team and 6-month timeline"
  * Non-IT: "Based on similar events attracting [X] participants"

- R (Relevant):   [Goal này liên quan đến mục tiêu lớn hơn như thế nào?]
  * Kết nối với KPI: "directly impacts [revenue / adoption / reputation]"

- T (Time-bound):  [Deadline cụ thể?]
  * Nêu rõ "by end of Week X" hoặc "within [Y] months of launch"
  * Mỗi goal nên có deadline khác nhau
```

---
---

# 6️⃣ RISK MANAGEMENT

### 🧠 Phân biệt:
```
Mitigation  = Làm TRƯỚC khi rủi ro xảy ra → giảm khả năng / tác động
Contingency = Làm SAU khi rủi ro đã xảy ra → khắc phục hậu quả

Ít nhất 3 risks, mỗi risk 1 domain:
  Risk 1: Về chi phí / ngân sách
  Risk 2: Về tiến độ / nhân sự
  Risk 3: Về kỹ thuật / logistics / bên ngoài
```

### ✏️ TEMPLATE:

```
| # | Risk Name         | Description                | Prob   | Impact | Mitigation Plan             | Contingency Plan              |
|---|-------------------|----------------------------|--------|--------|-----------------------------|-------------------------------|
| 1 | Budget Overrun    | Costs exceed BAC due to    | Medium | High   | Add 10% buffer; estimate    | Negotiate scope cut with      |
|   |                   | underestimation             |        |        | carefully; weekly tracking  | sponsor; defer features       |
| 2 | [Schedule risk]   | [Mô tả rủi ro tiến độ]     | [P]    | [I]    | [Giảm thiểu – làm trước]   | [Khắc phục – sau khi xảy]   |
|   | VD: Key member    | Lead dev resignation        | Low    | High   | Cross-train; weekly doc     | Hire backup; 1-week onboarding|
| 3 | [External risk]   | [Rủi ro ngoài tầm kiểm     | [P]    | [I]    | [Phòng ngừa]               | [Ứng phó]                    |
|   | IT: API delay     | soát]                       |        |        |                             |                               |
|   | Non-IT: Weather   |                             |        |        |                             |                               |

* IT risks:    API delay | App Store rejection | Scope creep | Performance under load
* Non-IT risks: Permit denied | Sponsor withdrawal | Low registration | Bad weather
```

---
---

# 7️⃣ STAKEHOLDERS & ROLES

### 📊 Power/Interest Grid (thuộc lòng):
```
              HIGH INTEREST         LOW INTEREST
HIGH POWER  | Manage Closely   |  Keep Satisfied  |
LOW POWER   | Keep Informed    |  Monitor         |
```

### ✏️ TEMPLATE:

```
| Stakeholder         | Role & Responsibility                     | Type     | Power | Interest | Strategy        |
|---------------------|-------------------------------------------|----------|-------|----------|-----------------|
| [Sponsor/Director]  | Funds project; approves major decisions;  | External | High  | High     | Manage Closely  |
|                     | signs off on deliverables                 |          |       |          | (biweekly brief)|
| Project Manager     | Plans, executes, monitors all activities; | Internal | High  | High     | Manage Closely  |
|                     | manages team, budget, risks               |          |       |          | (core role)     |
| [Technical lead /   | [Trách nhiệm kỹ thuật / chuyên môn]       | Internal | Med   | High     | Keep Informed   |
|  Domain expert]     |                                           |          |       |          |                 |
| [End Users]         | Primary users; participate in UAT/testing | External | Low   | High     | Keep Informed   |
| IT: Students/Users  | or event; provide feedback                |          |       |          | (surveys, beta) |
| [External authority]| Grants permits; enforces compliance       | External | High  | Low      | Keep Satisfied  |
| Non-IT: Govt dept   |                                           |          |       |          | (formal reports)|
| [Support team]      | Marketing / Finance / QA support          | Internal | Low   | Med      | Monitor         |

* Mô tả phải gắn với PROJECT CỤ THỂ, không viết chung chung
* Phải có: 1 Sponsor + 1 PM + 2-3 Internal specialists + 1-2 External
```

---
---

# 8️⃣ USER STORIES

### 🧠 Format chuẩn:
```
"As a [role], I want [feature/action] so that [benefit/reason]."
+ ≥ 2 Acceptance Criteria (AC): điều kiện để story là "done"
  AC hay bắt đầu bằng: "The system displays..." / "User receives..." / "The [feature] allows..."
```

### ✏️ TEMPLATE (lặp lại cho mỗi story):

```
US-[XX]: [Tên tính năng ngắn gọn]
Story: "As a [role], I want to [hành động cụ thể] so that [lý do / lợi ích]."
       * [role]   = student / participant / instructor / manager / organizer
       * [action] = register, track, submit, view, download, message, receive...
       * [benefit]= "I can [lợi ích trực tiếp]" / "I do not have to [bất tiện cũ]"

Acceptance Criteria:
- AC1: [Điều kiện cụ thể và kiểm tra được – dùng số liệu nếu có]
        * IT:     "System displays confirmation within 5 seconds of submission"
        * Non-IT: "Participant receives email confirmation within 10 minutes"
- AC2: [Edge case hoặc error handling]
        * "If file exceeds [X]MB, an error message is displayed"
        * "If registration is full, user sees 'Waitlist' instead of 'Register'"
- AC3: [UI/UX hoặc data retention – optional nhưng tốt nếu có]

* IT story topics:   Login | View content | Submit | Track progress |
                     Notification | Message | Download offline | View results
* Non-IT topics:     Register | Get confirmation | Track status | View route/schedule |
                     Submit feedback | Receive results/certificate
```

---
---

# 9️⃣ ORGANIZATIONAL STRUCTURE

### 🧠 Chọn 1 trong 3 và GIẢI THÍCH tại sao PHÙ HỢP với project này:
```
Functional   → Công việc routine, ổn định, nhân viên thuộc phòng ban cố định
Matrix       → Dự án cần chia sẻ nguồn lực từ nhiều phòng ban
Projectized  → Dự án ngắn hạn, scope rõ, PM cần toàn quyền
```

### ✏️ TEMPLATE:

```
CHOSEN STRUCTURE: [Functional / Matrix (Weak/Balanced/Strong) / Projectized]

JUSTIFICATION:
The [project name] adopts a [structure] organizational structure because:

1. [Về đặc điểm project]
   * IT short project (< 6 months, clear scope)  → "Projectized: needs full dedication"
   * Non-IT using multi-dept staff               → "Matrix: resources shared across programs"
   * Routine / no clear end date                 → "Functional: stable, repeatable work"

2. [Về quyền hạn PM]
   * Projectized: "PM requires full authority over budget and team decisions"
   * Matrix:      "PM coordinates across departments without permanent reassignment"

3. [Về nguồn lực]
   * Projectized: "Team members are dedicated full-time to this project only"
   * Matrix:      "Specialists from [dept] are shared across ongoing programs"

COMPARISON TABLE:
| Characteristic   | Functional   | Matrix (Strong) | Projectized  |
|------------------|--------------|-----------------|--------------|
| PM Authority     | Little/None  | Moderate-High   | High/Total   |
| Resource Sharing | By function  | Shared          | Dedicated    |
| Budget Control   | Func. Mgr    | Mixed           | PM           |
| PM Role          | Part-time    | Full-time       | Full-time    |
| Best For         | Routine ops  | Shared resources| Focused proj |
| ✅ CHOSEN REASON |              |                 | [X]          |
```

---
---

# 🔟 COMMUNICATION PLAN

### 🧠 Cần đủ 5 cột:
```
Information | Purpose | Frequency | Method/Format | Responsible
Luôn có: Internal (PM ↔ team) | Executive (PM → Sponsor) | External (PM → End users)
```

### ✏️ TEMPLATE:

```
| Stakeholder  | Information           | Purpose             | Frequency    | Method/Format       | Responsible |
|--------------|-----------------------|---------------------|--------------|---------------------|-------------|
| [Sponsor]    | Budget status,        | Executive oversight | Monthly /    | Formal PDF report + | PM          |
|              | milestone, risk flags | & key decisions     | Bi-weekly    | 30-min meeting      |             |
| [Core Team]  | Sprint goals, tasks,  | Coordinate daily    | Daily /      | Standup / Jira /    | PM / Lead   |
| Dev/Coord    | blockers, decisions   | work, remove issues | Weekly       | Slack / Google Meet |             |
| [Specialist] | Domain updates        | Align specialized   | Weekly /     | Email / shared docs | Lead        |
| QA/BA/Safety | for their workstream  | work with project   | As needed    | Sprint review       |             |
| [End Users]  | Progress, launch info,| Manage expectations;| Bi-weekly /  | Email / Social media| Marketing   |
| Students /   | how-to, event updates | drive engagement    | Weekly near  | / In-app notif      | / BA        |
| Participants |                       |                     | launch       |                     |             |
| [External    | Compliance docs,      | Legal compliance    | As needed /  | Formal letter /     | PM /        |
|  Authority]  | coordination requests | & safety            | Key milestone| Official meetings   | Coordinator |

* Tần suất TĂNG DẦN khi gần deadline (from weekly → daily in final phase)
* IT: Sprint review / standup | Non-IT: Volunteer briefing / weekly debrief
```

---
---

# 1️⃣1️⃣ GANTT CHART

### 🧠 Trong bài thi viết tay:
```
Vẽ bảng: cột = tuần/tháng | hàng = activities
Điền ██ hoặc X vào ô tương ứng
"Monitoring & Control" kéo suốt dự án
```

### ✏️ TEMPLATE:

```
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

* IT:     Req(2w) → Design(3w) → Dev(6w) → QA(3w) → Launch(1w)
* Non-IT: Permit(4w) → Sponsor(6w) → Registration(8w) → Logistics(6w) → Event(1w)
* Phases có thể OVERLAP (Design overlap với early Dev = OK)
```

---
---

# 1️⃣2️⃣ CRITICAL PATH ⭐ PHẢI LẤY TRỌN ĐIỂM

### 📐 CÔNG THỨC (thuộc lòng):

```
FORWARD PASS (trái → phải):
  ES (task đầu tiên) = 0
  EF = ES + Duration
  Nếu task có NHIỀU predecessors: ES = MAX(EF của tất cả predecessors)

BACKWARD PASS (phải → trái):
  LF (task cuối cùng) = EF của task cuối (= Project Duration)
  LS = LF - Duration
  Nếu task có NHIỀU successors: LF = MIN(LS của tất cả successors)

FLOAT = LS - ES  (= LF - EF)
Float = 0 → CRITICAL | Float > 0 → Non-critical
```

### ✏️ TEMPLATE GIẢI (4 bước):

```
BƯỚC 1: Vẽ/liệt kê sơ đồ phụ thuộc

BƯỚC 2: FORWARD PASS
| Activity | Predecessors     | ES               | Duration | EF    |
|----------|------------------|------------------|----------|-------|
| A        | –                | 0                | [dur]    | [EF]  |
| B        | A                | [EF_A]           | [dur]    | [EF]  |
| C        | A                | [EF_A]           | [dur]    | [EF]  |
| D        | B, C             | MAX([EF_B],[EF_C])| [dur]   | [EF]  |
| ...      | ...              | ...              | ...      | ...   |
  → Project Duration = EF của task cuối cùng

BƯỚC 3: BACKWARD PASS
| Activity | Successors | LF                   | Duration | LS    |
|----------|------------|----------------------|----------|-------|
| [Last]   | –          | [= Project Duration] | [dur]    | [LS]  |
| ...      | ...        | MIN([LS successors]) | ...      | ...   |
| A        | B, C       | MIN([LS_B],[LS_C])   | [dur]    | [LS]  |

BƯỚC 4: FLOAT + CRITICAL PATH
| Activity | ES | EF | LS | LF | Float  | Critical? |
|----------|----|----|----|----|--------|-----------|
| A        |    |    |    |    | LS-ES  | ✅/❌     |
| B        |    |    |    |    |        |           |
| ...      |    |    |    |    |        |           |

CRITICAL PATH: [Task] → [Task] → ... → End   (Float = 0)
PROJECT DURATION: [X] weeks/days

CÂU HỎI PHỤ:
  Crashing:      Chỉ rút ngắn task trên Critical Path
                 Ưu tiên task DÀI NHẤT trước (giảm nhiều nhất)
  Fast Tracking: Làm song song 2 tasks vốn FS
                 Không tốn tiền thêm NHƯNG tăng rủi ro
```

---
---

# 1️⃣3️⃣ EVM ⭐ PHẢI LẤY TRỌN ĐIỂM

### 📐 TOÀN BỘ CÔNG THỨC:

```
INPUT từ đề:
  BAC  = Budget at Completion (tổng ngân sách)
  BDAC = Budgeted Duration at Completion (tổng thời gian kế hoạch)
  AC   = Actual Cost (chi phí thực tế tại thời điểm đánh giá)
  t    = thời điểm đánh giá
  %    = phần trăm công việc hoàn thành THỰC TẾ

TÍNH THEO THỨ TỰ NÀY:
  PV   = BAC × (t / BDAC)    → Kế hoạch chi bao nhiêu đến giờ?
  EV   = BAC × %complete     → Giá trị thực sự tạo ra?
  CV   = EV - AC             → + under budget | - over budget
  SV   = EV - PV             → + ahead | - behind schedule
  CPI  = EV / AC             → >1 tốt | <1 xấu
  SPI  = EV / PV             → >1 tốt | <1 xấu
  EAC  = BAC / CPI           → Tổng chi phí dự kiến khi xong
  ETC  = EAC - AC            → Cần thêm bao nhiêu tiền?
  VAC  = BAC - EAC           → + dư | - vượt ngân sách
  EDAC = BDAC / SPI          → Dự kiến xong sau bao lâu?
```

### ✏️ TEMPLATE GIẢI:

```
GIVEN: BAC=$[X] | BDAC=[Y] | Evaluated at [t] | AC=$[Z] | %complete=[%]

| Metric | Formula          | Calculation   | Result    | Interpretation                        |
|--------|------------------|---------------|-----------|---------------------------------------|
| PV     | BAC × (t/BDAC)   | [X]×([t]/[Y]) | $[PV]     | Planned to spend $[PV] by [t]         |
| EV     | BAC × %          | [X]×[%]       | $[EV]     | Work worth $[EV] has been completed   |
| CV     | EV - AC          | [EV]-[AC]     | $[CV]     | [+Under / -Over] budget by $[|CV|]    |
| SV     | EV - PV          | [EV]-[PV]     | $[SV]     | [+Ahead / -Behind] schedule           |
| CPI    | EV / AC          | [EV]/[AC]     | [CPI]     | $1 spent → $[CPI] in value            |
| SPI    | EV / PV          | [EV]/[PV]     | [SPI]     | Running at [SPI×100]% planned speed   |
| EAC    | BAC / CPI        | [X]/[CPI]     | $[EAC]    | Predicted total cost = $[EAC]         |
| ETC    | EAC - AC         | [EAC]-[AC]    | $[ETC]    | Still needs $[ETC] to complete        |
| VAC    | BAC - EAC        | [X]-[EAC]     | $[VAC]    | [+surplus / -deficit] = $[|VAC|]      |
| EDAC   | BDAC / SPI       | [Y]/[SPI]     | [EDAC]    | Will finish in [EDAC] [months/weeks]  |

SUMMARY (luôn viết đoạn này):
  Cost:     [OVER/UNDER] BUDGET (CPI=[X] [</> ] 1)
  Schedule: [AHEAD/BEHIND]      (SPI=[X] [>/< ] 1)
  Forecast: Final cost = $[EAC], [exceeds/below] BAC by $[|VAC|]
  Duration: Finish [X] [months/weeks] [early/late] ([EDAC] vs [BDAC] planned)

PM ACTIONS:
  Over budget:   "Audit spending / Negotiate with vendors / Reduce scope"
  Behind sched:  "Apply crashing / Fast tracking / Add resources"
  Both bad:      "Escalate to sponsor + corrective action plan"
```

---
---

# 1️⃣4️⃣ QA/QC PLAN

### 🧠 4 loại chi phí chất lượng:
```
Prevention  = Đầu tư TRƯỚC để tránh lỗi (training, standards, process docs)
Appraisal   = Kiểm tra TRONG khi làm (review, testing, audit)
Int. Failure = Lỗi phát hiện TRƯỚC bàn giao (rework, bug fix pre-launch)
Ext. Failure = Lỗi SAU bàn giao (warranty, hotfix, complaint) ← TỐN NHẤT, tránh tối đa
```

### ✏️ TEMPLATE:

```
─── QUALITY STANDARDS ──────────────────────────────────────
- [Quality metric 1 từ đề – VD: "App rating ≥ 4.0/5.0"]
- [Quality metric 2 từ đề – VD: "Satisfaction ≥ 90%"]
- [Tự thêm IT:     "Crash rate < 0.5% | Response < 2s | 0 critical bugs at launch"]
- [Tự thêm Non-IT: "Zero serious safety incidents | All stations ready 30 min before event"]

─── COST OF QUALITY ────────────────────────────────────────
| Category            | Activities                                                  |
|---------------------|-------------------------------------------------------------|
| Prevention          | [Training] | [Coding/process standards] | [Design review]   |
|                     | [Checklist creation] | [Supplier pre-qualification]         |
| Appraisal           | [Peer code review] | [Test case execution]                 |
|                     | [Load/stress testing] | [Inspection/dry run]               |
| Internal Failure    | [Bug fix before release] | [Rework of rejected design]     |
|                     | [Regression testing after patches]                          |
| External Failure    | [Negative user reviews] | [Post-launch hotfixes]            |
| (← Most expensive!) | [Customer complaints] | [Safety incidents / legal action]  |
|                     | ← INVEST IN PREVENTION TO AVOID THESE                      |

─── QA ACTIVITIES BY PHASE ─────────────────────────────────
| Phase / Week   | QA Activity                              | Owner         |
|----------------|------------------------------------------|---------------|
| Planning       | Create QA plan & test plan               | PM / QA Lead  |
|                | Define acceptance criteria per feature   | BA / QA       |
| Design         | Prototype review / design walkthrough    | BA + QA       |
| Development    | Unit testing (automated, daily CI/CD)    | Dev           |
| Pre-launch     | Integration & system testing             | QA            |
| UAT phase      | [Beta test / Dry run / Rehearsal]        | QA + Users    |
| Post-launch    | Monitor [Crashlytics / reviews / survey] | QA Lead       |

* IT:     Unit → Integration → System → UAT → Post-launch monitoring
* Non-IT: Supplier check → Equipment inspection → Dry run → Event day → Survey
```

---
---

# 🚀 QUICK REFERENCE: ĐỀ NÓI GÌ → VIẾT GÌ Ở ĐÂU

| Đề nói... | Requirement liên quan | Viết gì |
|-----------|----------------------|---------|
| "build / develop app" | Charter, WBS, User Stories | Platform (iOS/Android), SSO login, offline mode |
| "organize / plan event" | Charter, Deliverables, Risk | Permits, safety plan, volunteer plan, weather risk |
| "$X budget" | Charter, EVM | BAC = $X; 10% buffer risk |
| "X months / weeks" | Charter, Gantt, CPM, EVM | BDAC = X; timeline in Gantt |
| "Y% satisfaction/rating" | Charter, SMART Goals, QA | Quality metric across all 3 |
| "students / participants use it" | Stakeholders, User Stories | End Users = Low power, High interest → Keep Informed |
| "existing system / current LMS" | Charter Assumptions, Risk | "API access by Week X" + "API delay" risk |
| "free software only" | Charter Constraints | Cost: "all software must be free/open-source" |
| "secure permits" | WBS (1.3.1), Deliverables, Risk | Permit milestone + "permit denial" risk |
| "train staff / volunteers" | WBS, RACI, User Stories | Training as deliverable + role in RACI |
| "sponsor / funding" | Stakeholders, Risk, CommPlan | Sponsor = High power + "sponsor withdrawal" risk |
| "quality / no error / zero complaints" | SMART Goals, QA, Risk | Quality metric + QA prevention + risk |

---

*PMG201c – 14 Requirements Complete Template*
*Dùng cho mọi đề IT và Non-IT | FPT University*
*For study purposes only*
