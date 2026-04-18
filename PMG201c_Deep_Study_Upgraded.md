 # 📘 PMG201c – Project Management (Deep Study Note)

> [!info]
> **DE CUONG ON THI CUOI KY**  
> 8 dang de thuong gap: Stakeholders | RACI | SMART | Risk | WBS | Critical Path | EVM

---

## 🚀 1. TONG QUAN - 8 DANG DE THUONG GAP

> [!tip]
> ❗ **Khong copy-paste template - tu viet tay, bam sat scenario cu the trong de bai!**

**PMG201c -- Project Management**

**DE CUONG ON THI CUOI KY**

*8 dang de thuong gap \| Stakeholders \| RACI \| SMART \| Risk \| WBS \|
Critical Path \| EVM*

**1. TONG QUAN - 8 DANG DE THUONG GAP**


| **Request** | **Nội dung yêu cầu** |
|------------|---------------------|
| **Req 1 - Stakeholders** | Xác định >=5 stakeholders với vai trò và mô tả chi tiết (liên quan dự án cụ thể) |
| **Req 2 - RACI Matrix** | Lập bảng RACI: >=10 tasks, phân công vai trò R/A/C/I cho từng thành viên |
| **Req 3 - SMART Goals** | Viết 3-4 mục tiêu SMART (Specific, Measurable, Attainable, Relevant, Time-bound) |
| **Req 4 - Risk** | Xác định >=3 rủi ro: mô tả, xác suất, mức độ, Mitigation & Contingency Plan |
| **Req 5 - User Stories** | Liệt kê User Stories: Title + 'As a... I want... So that...' + >=2 Acceptance Criteria |
| **Req 6 - WBS** | Tạo WBS đến Level 3-4: Level1=Project, Level2=Phases, Level3=Tasks, Level4=Sub-tasks |
| **Req 7 - Deliverables** | Xác định milestones và deliverables theo từng giai đoạn dự án |
| **Req 8 - Schedule & EVM** | Vẽ Network Diagram, Critical Path, ES/EF/LS/LF/Float; EVM: CPI, SPI, EAC, ETC |
  ------------------- ---------------------------------------------------

**LUU Y: Khong copy-paste template - tu viet tay, bam sat scenario cu
the trong de bai!**

**2. STAKEHOLDERS & RACI MATRIX**

**2.1 Cac loai Stakeholder pho bien**

| **Stakeholder/Role**           | **Mô tả và đặc điểm**                                                                  |
| ------------------------------ | -------------------------------------------------------------------------------------- |
| Project Sponsor                | Người tài trợ ngân sách; External; High power, High interest; Strategy: Manage Closely |
| Project Manager / Scrum Master | Quản lý tiến độ, nguồn lực, rủi ro; Internal; đảm bảo team tuân theo quy trình         |
| Business Analyst (BA)          | Chuyển yêu cầu khách hàng thành tài liệu kỹ thuật; Internal stakeholder                |
| Developer Team                 | Thực hiện code, unit test; Internal; làm việc theo BA & PM                             |
| Tester / QA                    | Tạo test plan, test case, tìm bug; Internal stakeholder                                |
| Product Owner                  | Đại diện khách hàng; cung cấp requirements; review output mỗi sprint; External         |
| End Users / Students           | Người dùng cuối; Low power, High interest; Strategy: Keep Informed                     |
| System Administrators          | Quản lý hệ thống; High power, High interest; Strategy: Manage Closely                  |
  ---------------------- ------------------------------------------------

**2.2 Power/Interest Grid - Chien luoc quan ly**

| **Power \ Interest** | **High Interest**                                                                                                                                 | **Low Interest**                                                |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| **High Power**       | (Manage Closely – **Quản lý chặt chẽ):** Ví dụ như Project Sponsor, System Administrators.  cập nhật thường xuyên, tham gia quyết định quan trọng | (Keep Satisfied – Giữ hài lòng: báo cáo ngắn gọn, tránh bất ngờ |
| **Low Power**        | Keep Informed – newsletter, demo, training                                                                                                        | Monitor – theo dõi, ít tương tác                                |
  ------------------------- ---------------------------------------------

**2.3 RACI Matrix - Cach dien**

| **Ký hiệu**     | **Nghĩa**                                              |
| --------------- | ------------------------------------------------------ |
| R - Responsible | Người thực hiện công việc (có thể nhiều người)         |
| A - Accountable | Người chịu trách nhiệm cuối cùng; mỗi task chỉ 1 người |
| C - Consult     | Người được tham khảo trước khi quyết định              |
| I - Inform      | Người được thông báo kết quả                           |
  ------------------- ---------------------------------------------------

**Vi du RACI cho LMS Project:**

| **Task**                     | **SM** | **BA** | **Dev** | **Tester** | **PO** |
| ---------------------------- | ------ | ------ | ------- | ---------- | ------ |
| Define system requirements   | I      | R      | I       | I          | A      |
| Design system architecture   | C      | C      | A/R     | I          | C      |
| Set up database schema       | C      | C      | A/R     | I          | I      |
| Develop backend              | I      | I      | A/R     | I          | C      |
| Develop frontend UI          | I      | I      | A/R     | I          | C      |
| Integrate frontend & backend | I      | C      | R       | I          | A      |
| Test system                  | C      | C      | I       | A/R        | C      |
| Prepare deployment           | A      | C      | R       | C          | I      |
| Deploy system                | A      | I      | R       | C          | I      |
| Develop docs                 | I      | A/R    | C       | I          | C      |
  ------------------------ -------- -------- --------- ------------ ------------

---

## 2.4 RACI cho Dự Án KHÔNG PHẢI PHẦN MỀM

> [!important]
> ❗ **Vấn đề hay gặp:** Khi đề bài KHÔNG phải là app/website (ví dụ: pop-up store, podcast, sự kiện...), nhiều sinh viên không biết task là gì vì không có "Develop module" hay "Deploy system".

---

### 🧠 Tư duy chìa khóa: Task = CÁC BƯỚC ĐỂ HOÀN THÀNH DỰ ÁN ĐÓ

Dù là phần mềm hay vật lý, mọi dự án đều đi qua **5 nhóm bước**:

| Nhóm | Phần mềm | Pop-up Retail | Podcast / Media |
|------|----------|---------------|-----------------|
| **① Lập kế hoạch** | Define requirements | Secure permits & location | Define content strategy |
| **② Thiết kế / Chuẩn bị** | Design architecture | Design & build display | Set up recording equipment & platforms |
| **③ Thực hiện chính** | Develop modules | Manage inventory & staff | Record & edit episodes |
| **④ Kiểm soát chất lượng** | Test system | Sales monitoring & stock check | Fact-check & review content |
| **⑤ Kết thúc / Đánh giá** | Deploy & close | Close operation & report | Publish & analyze metrics |

> **Nguyên tắc:** Hãy tưởng tượng bạn **thực sự đang làm dự án đó** — bạn phải làm gì từ ngày 1 đến ngày cuối? Mỗi việc đó = 1 task!

---

### 🛒 VÍ DỤ 1: Pop-up Retail Validation (Fall 2025 Exam)

**Scenario:** Bạn bán sản phẩm tại một gian hàng tạm thời trong 2 tuần. Budget $1,500. Target: $15,000 doanh thu, satisfaction >90%.

**Roles được chọn:** PM (Project Manager) | OC (Operations Coordinator) | SA (Sales Associate / Student Staff) | MK (Marketing Lead)

**Cách nghĩ ra tasks:** *"Để mở một pop-up shop, tôi cần làm gì?"*

1. Xin giấy phép → **Secure venue permits & licenses**
2. Chọn địa điểm → **Select & confirm pop-up location**
3. Thiết kế gian hàng → **Design & build display setup**
4. Mua/nhận hàng → **Manage & receive inventory**
5. Tuyển/huấn luyện nhân viên → **Recruit & train student sales staff**
6. Quảng bá → **Execute pre-launch marketing campaign**
7. Mở cửa bán → **Conduct daily sales operations (Week 1 & 2)**
8. Kiểm kê hàng ngày → **Daily inventory tracking & shrinkage monitoring**
9. Khảo sát khách → **Collect customer satisfaction surveys**
10. Báo cáo cuối → **Compile sales & satisfaction final report**
11. Đóng gian hàng → **Dismantle display & close operation**

**RACI Matrix – Pop-up Retail:**

| # | Task | PM | OC | SA | MK |
|---|------|----|----|----|----|
| 1 | Secure venue permits & licenses | A | R | I | I |
| 2 | Select & confirm pop-up location | A | R | I | C |
| 3 | Design & build display setup | C | A/R | R | C |
| 4 | Manage & receive inventory | A | R | C | I |
| 5 | Recruit & train student sales staff | A | R | C | I |
| 6 | Execute pre-launch marketing campaign | C | I | I | A/R |
| 7 | Conduct daily sales operations | C | A | R | I |
| 8 | Daily inventory tracking & shrinkage monitoring | A | R | C | I |
| 9 | Collect customer satisfaction surveys | C | A | R | I |
| 10 | Compile sales & satisfaction final report | A | R | I | C |
| 11 | Dismantle display & close operation | A | R | R | I |

> [!tip]
> ✅ Với đề pop-up retail: OC (Operations) thường là **R** cho hầu hết task vật lý. PM **A** cho các task cần chịu trách nhiệm tổng thể. SA (nhân viên) **R** cho tasks bán hàng trực tiếp.

---

### 🎙️ VÍ DỤ 2: Digital Podcast / Media Channel (Fall 2025 Exam)

**Scenario:** Tạo kênh tin tức số cho sinh viên (YouTube + Podcast). 3 tháng, $500, phần mềm miễn phí. Target: 500 subscribers, 0 factual complaints.

**Roles được chọn:** PM (Project Manager) | CC (Content Creator) | TE (Technical Editor) | PH (Podcast Host / Presenter)

**Cách nghĩ ra tasks:** *"Để ra được 1 episode podcast/video hàng tuần, tôi cần làm gì?"*

1. Lên chiến lược nội dung → **Define content strategy & 12-week editorial calendar**
2. Setup kênh/nền tảng → **Set up YouTube channel (branding, banner)**
3. Setup podcast → **Set up podcast hosting platform (Anchor/Spotify)**
4. Setup newsletter → **Set up newsletter platform (Mailchimp free)**
5. Mua thiết bị → **Procure equipment within $500 budget**
6. Nghiên cứu topic → **Research & select weekly topics**
7. Viết script → **Write episode script & talking points**
8. Ghi âm/quay → **Record video & audio episode**
9. Dựng phim/âm thanh → **Edit video (DaVinci) & audio (Audacity)**
10. Kiểm tra thông tin → **Fact-check all content before publication**
11. Upload & publish → **Upload to YouTube + distribute podcast & newsletter**
12. Theo dõi KPI → **Monitor analytics (subscribers, views) & weekly report**

**RACI Matrix – Podcast / Media Channel:**

| # | Task | PM | CC | TE | PH |
|---|------|----|----|----|----|
| 1 | Define content strategy & editorial calendar | A | R | C | C |
| 2 | Set up YouTube channel | A | C | R | I |
| 3 | Set up podcast hosting platform | A | I | R | I |
| 4 | Set up newsletter platform | A | I | R | I |
| 5 | Procure equipment within budget | A | C | R | I |
| 6 | Research & select weekly topics | C | A/R | C | C |
| 7 | Write episode script & talking points | I | A/R | C | C |
| 8 | Record video & audio episode | I | C | C | A/R |
| 9 | Edit video & audio | C | I | A/R | I |
| 10 | Fact-check all content before publication | A | I | R | C |
| 11 | Upload to YouTube + distribute podcast/newsletter | A | I | R | I |
| 12 | Monitor analytics & weekly report | A/R | I | C | I |

> [!tip]
> ✅ Với đề media/podcast: TE (Technical Editor) thường **R** cho các task kỹ thuật (setup, edit, upload). CC **R** cho research & script. PH (host/presenter) **R** khi đứng trước mic/camera.

---

### 🎯 CÔNG THỨC TÌM TASK CHO MỌI ĐỀ BÀI

**Bước 1:** Đọc đề, tìm **GÌ** cần làm ra (deliverable) → đó là task thực hiện chính (nhóm ③)

**Bước 2:** Hỏi: *"Trước khi làm ③, cần chuẩn bị gì?"* → nhóm ①②

**Bước 3:** Hỏi: *"Sau khi làm ③, cần kiểm tra/kết thúc gì?"* → nhóm ④⑤

**Bước 4:** Thêm **2 task quản lý** là: `Monitor progress & budget` và `Create final report`

→ **Tổng = 10-12 tasks**, đủ điều kiện! ✅

---

### 📊 Bảng so sánh Task theo loại đề bài

| Loại đề | Task đặc thù nhất | Role thường là R |
|---------|------------------|-----------------|
| **App / Software** | Develop modules, Test system, Deploy | Developer, QA |
| **Pop-up / Event** | Secure permits, Build display, Manage inventory, Run daily ops | Operations Coordinator |
| **Podcast / Media** | Record episodes, Edit content, Publish, Fact-check | Content Creator, Technical Editor |
| **Food & Beverage** | Source ingredients, Prepare menu, Train staff, Manage orders | Operations Manager |
| **Marketing Campaign** | Create assets, Run ads, Track metrics | Marketing Lead |

---

**3. SMART GOALS**

**3.1 Framework SMART**

| **Tiêu chí** | **Giải thích**                                            |
| ------------ | --------------------------------------------------------- |
| S_Specific   | Mục tiêu rõ ràng: Ai, làm gì, ở đâu, tại sao?             |
| M_Measurable | Đo được bằng số: Bao nhiêu, khi nào xong?                 |
| A_Attainable | Có thể đạt được với nguồn lực hiện tại: Có khả thi không? |
| R_Relevant   | Liên quan mục tiêu dự án: Có quan trọng không?            |
| T_Time-bound | Có thời hạn cụ thể: Deadline là khi nào?                  |
  ------------------ ----------------------------------------------------

**3.2 Vi du SMART Goals (LMS Project)**

**Goal 1: Đạt 250 học viên đăng ký trong 3 tháng đầu ra mắt.**

-   Specific: Tang so luong hoc vien dang ky cho cac khoa hoc tren nen
    tang LMS

-   Measurable: Dat con so 250 nguoi dang ky trong 3 thang

-   Attainable: Kha thi voi chien luoc marketing va chat luong khoa hoc
    hien tai

-   Relevant: Tang nguoi dung truc tiep dong gop vao tang truong nen
    tang

-   Time-bound: Dat duoc trong vong 3 thang ke tu ngay ra mat

**Goal 2: Điểm đánh giá trung bình của các khóa học \>= 3.8/5 sao trong năm đầu tiên.**

-   Specific: Duy tri chat luong khoa hoc theo phan hoi hoc vien

-   Measurable: Diem trung binh \>= 3.8/5 tu reviews

-   Attainable: Dat duoc bang cach lien tuc cai thien noi dung theo
    feedback

-   Relevant: Chat luong khoa hoc anh huong truc tiep den retention rate

-   Time-bound: Dat duoc truoc cuoi nam thu nhat

**Goal 3: Đảm bảo tất cả các function được test 100% trong giai đoạn phát triển.**

-   Specific: Kiem thu toan bo chuc nang trong phase development

-   Measurable: 100% critical test cases phai pass truoc khi release

-   Attainable: Kha thi voi QA team co nang luc va testing strategy ro
    rang

-   Relevant: Testing dam bao san pham on dinh, tang su hai long

-   Time-bound: Hoan thanh trong scheduled development timeline

**4. RISK MANAGEMENT**

**4.1 Chiến lược đối phó với rủi ro**

| **Chiến lược**       | **Mô tả**                                                                         |
| -------------------- | --------------------------------------------------------------------------------- |
| Avoid-Tránh né       | Tránh hoàn toàn bằng cách đổi kế hoạch<br>- Dung tech quen thuoc thay vi đổi moi  |
| Transfer-Chuyển giao | Chuyển giao (outsource, bảo hiểm)<br>- Thue cloud provider de tranh rui ro server |
| Mitigate-Giảm thiểu  | Giảm xác suất hoặc tác động<br>- Training team de giam loi ky thuat               |
| Accept-Chấp nhận     | Chấp nhận và chuẩn bị plan dự phòng<br>- Lập contingency budget 10%               |

  ------------------- ---------------------------------------------------

**4.2 Risk Register - 5 rui ro tieu bieu**

| **Risk Name**                     | **Probability** | **Impact** | **Mitigation Plan**                                                                                                          | **Contingency Plan**                                                                                 |
| --------------------------------- | --------------- | ---------- | ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| Budget overrun                    | Medium          | High       | Add 10% buffer, estimate carefully<br>- Dự toán cẩn thận, thêm quỹ dự phòng (buffer) khoảng 10% ngân sách                    | Cut scope, renegotiate<br>- Nếu xảy ra, thương lượng lại với Sponsor để cắt giảm phạm vi dự án       |
| Schedule tight                    | High            | High       | Prioritize tasks, add buffer<br>- Đặt độ ưu tiên (priority) cho từng task, sử dụng kỹ thuật time-boxing, bổ sung buffer time | Reschedule<br>- Yêu cầu team làm thêm giờ (overtime/crashing), hoặc đàm phán dời lịch với khách hàng |
| Staff attrition_Chảy máu chất xám | Medium          | High       | Training, mentoring                                                                                                          | Hire backup                                                                                          |
| Sprint not met                    | Medium          | High       | Clear goals, daily standup                                                                                                   | Reprioritize                                                                                         |
| Feedback delay                    | Medium          | Medium     | Weekly check-in                                                                                                              | Fix next sprint                                                                                      |

--------------- ----------------- ------------ ------------------ ------------------

**5. WORK BREAKDOWN STRUCTURE (WBS)**

**5.1 Cau truc WBS chuan**

| **Level** | **Nội dung**                                                                     |
| --------- | -------------------------------------------------------------------------------- |
| Level 1   | Project name                                                                     |
| Level 2   | Phases (Initiating, Planning, Executing, Monitoring & Controlling, Closing etc.) |
| Level 3   | Tasks trong moi phase (e.g., Analysis, Design, Testing)                          |
| Level 4   | Sub-tasks (e.g., Create use-case for Module 1, Implement Module 2)               |
| Level 5   | Work packages                                                                    |

------------- ---------------------------------------------------------

**5.2 Template WBS - Software Project (LMS)**

**1. \[Project Name\] - Level 1**

-   1.1. Initiating

    -   1.1.1. Create project charter

    -   1.1.2. Kick-off meeting

    -   1.1.3. Identify stakeholders & create register

    -   1.1.4. Get project charter approval

-   1.2. Planning

    -   1.2.1. Create Scope Management Plan (SMP)

    -   1.2.2. Create Time Management Plan (TMP)

    -   1.2.3. Create Cost Management Plan (CMP)

    -   1.2.4. Create Risk Management Plan (RMP)

    -   1.2.5. Create Resource Management Plan (ReMP)

    -   1.2.6. Deliver Project Management Plan

-   1.3. Executing

    -   1.3.1. Analysis - Feasibility report, Use-case diagram, SRS
        document

    -   1.3.2. Design - Overall architecture + Module 1..N designs

    -   1.3.3. Prototyping - Create & review prototypes with customer
        per module

    -   1.3.4. Implementing - Common functions + Module 1..N

    -   1.3.5. Testing - Unit, Integration, System, Acceptance testing

    -   1.3.6. Support - Training, Documentation, User Support,
        Enhancements

-   1.4. Monitoring & Controlling

    -   1.4.1. Control scope \| 1.4.2. Track progress \| 1.4.3. Cost
        control \| 1.4.4. Risk monitoring

-   1.5. Closing

    -   1.5.1. Create lesson learn \| 1.5.2. Final report \| 1.5.3.
        Archive \| 1.5.4. Ceremony

**5.3 Milestones & Deliverables**

| #   | Milestone  | Deliverables                                                     | Completion Criteria                   |
| --- | ---------- | ---------------------------------------------------------------- | ------------------------------------- |
| 1   | Initiating | Approved project charter, Kick-off minutes, Stakeholder register | All docs signed off by sponsor        |
| 2   | Planning   | Project Management Plan (all sub-plans)                          | PMP approved, team briefed            |
| 3   | Analysis   | SRS, Feasibility Report, Use-case diagram & specs                | All requirements validated            |
| 4   | Design     | Architecture doc, Module 1-N designs, Prototypes                 | Design reviewed & approved            |
| 5   | Closing    | Lesson Learn, Final Report, Project Archive                      | Formal sign-off from all stakeholders |

  


**6. PROJECT SCHEDULING - NETWORK DIAGRAM & CRITICAL PATH**

**6.1 Cong thuc tinh ES, EF, LS, LF, Float**


| Chỉ số | Công thức              | Ghi chú                             |     |
| ------ | ---------------------- | ----------------------------------- | --- |
| ES     | = EF của task trước    | Nếu nhiều predecessors: lấy MAX(EF) |     |
| EF     | = ES + Duration        | Forward pass: Start → End           |     |
| LF     | = LS của task sau      | Backward pass                       |     |
| LS     | = LF - Duration        | Nếu nhiều successors: lấy MIN(LS)   |     |
| Float  | = LF - EF hoặc LS - ES | Float = 0 → Critical                |     |
  ---------------- ------------------------- ----------------------------

**📌 Quy tắc 

> [!info]  
> - Forward Pass: tinh ES va EF tu Start den End (dung MAX khi co nhieu predecessors)
> - Backward Pass: tinh LS va LF tu End ve Start (dung MIN khi co nhieu successors)
> - Critical Path = Float = 0 duong di qua cac tasks co Float = 0
> - Project Duration = EF của End

**6.2 Vi du - SamplePE Network Diagram**

Activities: Start-\>A(3)-\>B(2), A-\>C(3), A-\>D(2), C,B-\>E(9),
B-\>F(10), D-\>G(3), E,F,G-\>H(6), G-\>I(2), H,I-\>J(8)-\>End

| Path   | Tasks                                           | Duration          |     |
| ------ | ----------------------------------------------- | ----------------- | --- |
| Path 1 | Start → A(3) → B(2) → F(10) → H(6) → J(8) → End | **29 (Critical)** |     |
| Path 2 | Start → A(3) → C(3) → E(9) → H(6) → J(8) → End  | **29 (Critical)** |     |
| Path 3 | Start → A(3) → B(2) → E(9) → H(6) → J(8) → End  | 28                |     |
| Path 4 | Start → A(3) → D(2) → G(3) → H(6) → J(8) → End  | 22                |     |
| Path 5 | Start → A(3) → D(2) → G(3) → I(2) → J(8) → End  | 18                |     |
  ---------- ------------------------------------------ ---------------------

**6.3 Schedule Crashing & Fast Tracking**

| Phuong phap               | Cach lam                                                                            | Tac dong                                           |
| ------------------------- | ----------------------------------------------------------------------------------- | -------------------------------------------------- |
| Crashing (Don nen)        | Them nguon luc (nhan su, overtime) vao task tren Critical Path co duration dai nhat | Rut ngan thoi gian NHUNG TANG chi phi              |
| Fast Tracking (Song song) | Lam song song 2 tasks von FS (task sau bat dau truoc khi task truoc ket thuc)       | Rut ngan thoi gian, KHONG tang budget, tang rui ro |
  ------------------ ---------------------------- -----------------------

**Quy tac vang khi chon task de rut ngan:**

-   Chi duoc rut ngan task nam tren Critical Path (Float = 0)

-   Uu tien task co Duration DAI NHAT de giam nhieu nhat

-   Sau khi rut ngan 1 path, kiem tra tat ca path khac xem co path nao
    vuot target khong

**7. EARNED VALUE MANAGEMENT (EVM)**

**7.1 Bang tat ca cong thuc EVM**

| Ký hiệu | Tên                         | Công thức                         | Ý nghĩa                                    |
| ------- | --------------------------- | --------------------------------- | ------------------------------------------ |
| PV      | Planned Value               | BAC x (elapsed_time / total_time) | Giá trị công việc dự kiến tại thời điểm đó |
| EV      | Earned Value                | BAC x % complete OR CPI x AC      | Giá trị công việc đã hoàn thành thực tế    |
| AC      | Actual Cost                 | Đề cho sẵn                        | Chi phí thực tế đã chi đến thời điểm đó    |
| BAC     | Budget at Completion        | Đề cho sẵn                        | Tổng ngân sách dự án ban đầu               |
| CPI     | Cost Performance Index      | EV / AC                           | >1: under budget \| <1: over budget        |
| SPI     | Schedule Performance Index  | EV / PV                           | >1: ahead of schedule \| <1: behind        |
| CV      | Cost Variance               | EV - AC                           | >0: under budget \| <0: over budget        |
| SV      | Schedule Variance           | EV - PV                           | >0: ahead \| <0: behind schedule           |
| EAC     | Estimate at Completion      | BAC / CPI                         | Ước tính tổng chi phí khi hoàn thành       |
| ETC     | Estimate to Complete        | (BAC - EV) / CPI                  | Chi phí còn lại để hoàn thành dự án        |
| VAC     | Variance at Completion      | BAC - EAC                         | Chênh lệch ngân sách khi hoàn thành        |
| EDAC    | Est. Duration at Completion | DAC / SPI                         | Ước tính thời gian thực tế hoàn thành      |
  ---------- ------------------ ------------------- ----------------------

**7.2 Vi du giai EVM (SamplePE)**

**De bai: BAC=\$8,400,000 \| Duration=5 nam=60 thang \| Do tai thang 15
\| AC=\$2,650,000 \| CPI=0.95**

-   PV = 15/60 x \$8,400,000 = \$2,100,000

-   EV = CPI x AC = 0.95 x \$2,650,000 = \$2,517,500

-   SPI = EV/PV = \$2,517,500 / \$2,100,000 = 1.2 -\> AHEAD OF SCHEDULE

-   CPI = 0.95 \< 1 -\> OVER BUDGET

-   EAC = BAC/CPI = \$8,400,000 / 0.95 = \$8,842,105 (vuot ngan sach goc
    \$442,105)

-   EDAC = 60 / 1.2 = 50 months -\> Hoan thanh som hon 10 thang

-   ETC = EAC - AC = \$8,842,105 - \$2,650,000 = \$6,192,105

| Chỉ số         | Kết luận                                                     |
| -------------- | ------------------------------------------------------------ |
| CPI = 0.95 < 1 | Dự án OVER BUDGET - Mỗi $1 chi ra chỉ mang lại $0.95 giá trị |
| SPI = 1.2 > 1  | Dự án AHEAD OF SCHEDULE - Hoàn thành 120% so với kế hoạch    |
| EAC > BAC      | Chi phí cuối cùng sẽ vượt ngân sách ban đầu                  |
| EDAC < DAC     | Sẽ hoàn thành sớm hơn dự kiến (vì SPI > 1)                   |
  ------------------ ----------------------------------------------------

**8. CAC CHU DE KHAC**

**8.1 Types of Organization**

| Đặc điểm              | Functional             | Matrix (Strong)   | Projectized                     |
| --------------------- | ---------------------- | ----------------- | ------------------------------- |
| PM Authority          | Little/None            | Moderate to High  | High to Almost Total            |
| Resource Availability | Little/None            | Moderate to High  | High to Almost Total            |
| Manages Budget        | Functional Manager     | Mixed             | Project Manager                 |
| PM Role               | Part-time              | Full-time         | Full-time                       |
| Tốt khi nào           | Công việc lặp, ổn định | Chia sẻ nguồn lực | Dự án ngắn, scope rõ, cần focus |
  ------------------ ----------------- ----------------- -----------------

**Vi sao chon Projectized cho du an LMS (4 thang):**

-   Thoi gian ngan can tap trung toan luc; Scope ro rang, deliverables
    cu the

-   Team nho, PM co full authority; Agile/Scrum hoat dong tot trong moi
    truong projectized

**8.2 Activity Relationships (FS, SS, FF, SF)**

| Quan hệ               | Giải thích                                                              |
| --------------------- | ----------------------------------------------------------------------- |
| FS - Finish to Start  | Task sau CHỈ BẮT ĐẦU khi task trước HOÀN THÀNH. (Phổ biến nhất)         |
| SS - Start to Start   | Task sau có thể BẮT ĐẦU CÙNG LÚC với task trước.                        |
| FF - Finish to Finish | Task sau không thể HOÀN THÀNH trễ hơn task trước.                       |
| SF - Start to Finish  | Task sau không thể hoàn thành cho đến khi task trước bắt đầu. (Ít dùng) |
  ------------------- ---------------------------------------------------

**8.3 Quality Costs**

| Loại                                  | Ví dụ                                                          |
| ------------------------------------- | -------------------------------------------------------------- |
| Prevention Costs (Phòng ngừa)         | Quality training, coding standards, process documentation      |
| Appraisal Costs (Thẩm định)           | Peer code review, test case development, inspections           |
| Internal Failure (Thất bại nội bộ)    | Rework, scrap - phát hiện TRƯỚC khi release cho khách hàng     |
| External Failure (Thất bại bên ngoài) | Fix bugs sau release, warranty work, lost business - Đắt nhất! |
  ------------------------ ----------------------------------------------

**8.4 Estimation Techniques**

| Kỹ thuật             | Khi nào dùng                                                             |
| -------------------- | ------------------------------------------------------------------------ |
| Analogous (Tương tự) | Dựa trên dự án tương tự trước đó. Nhanh nhưng ít chính xác.              |
| Parametric (Tham số) | Tính từng đơn vị rồi cộng lại. VD: số giờ x rate. Chính xác hơn.         |
| Bottom-up            | Ước tính từng task nhỏ rồi cộng lên. Chính xác nhất, tốn thời gian nhất. |
| 3-Point (PERT)       | E = (O + 4M + P) / 6. Tính đến cả trường hợp tốt nhất và xấu nhất.       |
| Expert Judgment      | Tin vào ý kiến chuyên gia. Dùng khi thiếu dữ liệu lịch sử                |
  ------------------- ---------------------------------------------------

**9. BANG TRA NHANH & CHECKLIST**

**9.1 Tat ca cong thuc EVM - Quick Reference**

| Chỉ số | Công thức               | Cách đọc kết quả                         |
| ------ | ----------------------- | ---------------------------------------- |
| PV     | BAC x (elapsed / total) | Không so sánh đơn giản, dùng để tính SPI |
| EV     | BAC x %done OR CPI x AC | Giá trị thực sự đã tạo ra                |
| CPI    | EV / AC                 | <1: Xấu (over budget) \| >1: Tốt         |
| SPI    | EV / PV                 | <1: Xấu (behind) \| >1: Tốt (ahead)      |
| CV     | EV - AC                 | <0: Over budget                          |
| SV     | EV - PV                 | <0: Behind schedule                      |
| EAC    | BAC / CPI               | Tổng chi phí dự đoán khi xong            |
| ETC    | (BAC - EV) / CPI        | Cần thêm bao nhiêu tiền để xong          |
| VAC    | BAC - EAC               | <0: Dự kiến vượt ngân sách               |
| EDAC   | DAC / SPI               | Mất bao lâu để xong (dự đoán)            |

### Mẹo ghi nhớ nhanh cho bài thi:

1. **Chữ "S" (Schedule)** luôn đi với **PV**.
    
2. **Chữ "C" (Cost)** luôn đi với **AC**.
    
3. **EV** luôn nằm ở **vế trước** trong các công thức tính sai lệch (CV, SV) và chỉ số hiệu suất (CPI, SPI).
    
4. **Hiệu suất (Index):** Chia. **Sai lệch (Variance):** Trừ.
    
5. Để tính toán về thời gian, chỉ cần thay biến số chi phí bằng biến số thời gian (ví dụ: EDAC dùng SPI thay vì CPI).
  ------------ --------------------------- -------------------------------

**9.2 Checklist truoc khi nop bai**

| Requirement | Nội dung                                                                                 |
| ----------- | ---------------------------------------------------------------------------------------- |
| Req 1       | >= 5 stakeholders, mô tả cụ thể theo dự án trong đề, có cả external & internal           |
| Req 2       | >= 10 tasks, đủ 4 ký hiệu R/A/C/I, mỗi task có đúng 1 chữ A                              |
| Req 3       | >= 3 goals, phân tích đầy đủ S-M-A-R-T cho từng goal, có số cụ thể                       |
| Req 4       | >= 3 risks, có Probability + Impact + Mitigation AND Contingency Plan                    |
| Req 6       | WBS: Level 1=tên dự án, Level 2=phases (đến Closing), đánh số đúng 1.1.1, 1.1.2...       |
| Req 7       | Deliverables: Đủ 5 milestones, có deliverables và completion criteria rõ ràng            |
| Req 8       | Network: Vẽ sơ đồ rõ ràng, tính đúng ES/EF/LS/LF/Float, xác định Critical Path (Float=0) |
| Req 8       | EVM: Tính đúng PV, EV, CPI, SPI, EAC, EDAC, ETC; comment tình trạng dự án                |

-   KHONG copy-paste template - tu viet tay, bam sat vao scenario cua de
    bai!

**CHUC THI TOT - PMG201c**

*De cuong tong hop tu cac tai lieu mau PMG201c - FPT University*


---

## 🧠 QUICK MEMORY ZONE

> [!important]
> 🔥 **Critical Path = tat ca tasks co Float = 0**

> [!important]
> 💰 **CPI < 1 = Over Budget | CPI > 1 = Under Budget**

> [!important]
> ⏱️ **SPI < 1 = Behind Schedule | SPI > 1 = Ahead**

---

## ✅ CHECKLIST BEFORE SUBMISSION

- [ ] Stakeholders >= 5 (internal + external)
- [ ] RACI >= 10 tasks, moi task chi 1 A
- [ ] SMART >= 3 goals, du S-M-A-R-T
- [ ] Risk >= 3 (Probability + Impact + Mitigation + Contingency)
- [ ] WBS dung Level 1-4
- [ ] Deliverables du milestones
- [ ] Network diagram + Critical Path
- [ ] EVM tinh dung CPI, SPI, EAC, ETC

---

## 🧩 STUDY STRATEGY

> [!note]
> - Hoc theo **pattern de** (8 dang)
> - Nho cong thuc EVM truoc (de an diem nhanh)
> - Ve nhanh Critical Path = loi the lon

---

✨ *Optimized for Obsidian – Deep Learning Style*

### **Topic:** _Should university students be required to participate in environmental protection projects?_

In the present day, the climate crisis has triggered discussions on the role of youth in sustainable development. Some people believe that environmental  participation should be a requirement for all university students during their free time. In my opinion, I strongly agree with this statement. I believe that such a great offers for both benefit. It serves as personal development for students while also generating significant long-term advantages for society.

Firstly, environmental project help student invaluable in hands-on experience. From a management perspective, organizing recycling campaigns or reforestation efforts requires strategic planning and effective communication - soft skills that are highly value for employers . Furthermore, by taking meaningful action, student gain a sense of agency and purpose, leading to a healthier mental state and more impressive portfolio.

Beyond individual gains, the collective impact of student-led environmental work is significant. Students represent a massive demographic of intellectual labor. When mobilized, they increase a nation's social capital. From an economic lens, community-driven initiatives are the most-effective than large scale government projects. Student programs in waste management or urban gardening can reduce costs. More importantly, this policy creates "Green Citizens" who will carry sustainable value into their future careers as leaders and innovators

Critics often argue that students are already overwhelmed with academic pressures. They claim compulsory service infringes upon limited free time. However this overlooks the concept of meaningful leisure. Much free time is currently spent on passive digital consumption, which can lead to burnout. Integrating environmental work into the curriculum perhaps through academic credits. It teaches vital time management skills and social responsibility.

In conclusion, requiring students to participate in environmental is a visionary policy. It bridges the gap between theory and practice, equipping students with life skills while addressing urgent ecological issues. Although it requires administrative planning, the rewards for the individual and the global community far outweigh the challenges. Environmental stewardship should be a fundamental pillar of modern higher education.

### The Synergy of Human Writing and AI

In the modern days, Artificial Intelligence, such as ChatGPT or Gemini has become more and more 






Dưới đây là bảng tổng hợp và giải thích hệ thống công thức **Earned Value Management (EVM)** dựa trên tài liệu môn học **PMG201c**. Việc nắm vững các nhóm chỉ số này sẽ giúp bạn kiểm soát hoàn toàn tiến độ và chi phí của dự án.

### 1. Nhóm chỉ số nền tảng (Cái lõi của EVM)

Đây là các giá trị đầu vào để tính toán mọi công thức khác:

- **PV (Planned Value):** Giá trị kế hoạch. Là số tiền đáng lẽ phải chi ra cho công việc dự kiến hoàn thành tính đến thời điểm hiện tại.
    
- **AC (Actual Cost):** Chi phí thực tế. Số tiền thực tế đã chi ra để làm được khối lượng công việc hiện tại.
    
- **EV (Earned Value):** Giá trị đạt được. Giá trị của khối lượng công việc thực tế đã hoàn thành, tính theo đơn giá dự tính ban đầu.
    
- **BAC (Budget at Completion):** Tổng ngân sách dự án. Tổng tất cả các PV của dự án.
    
- **BDAC (Budgeted Duration at Completion):** Tổng thời gian kế hoạch của dự án.
    

### 2. Nhóm chỉ số sai lệch (Dự án đang ở đâu?)

Dùng phép tính **Trừ (-)**. Kết quả **> 0** luôn là tốt.

- **CV (Cost Variance) = EV - AC:** Sai lệch chi phí.
    
    - _CV > 0:_ Dưới ngân sách (Tốt).
        
    - _CV < 0:_ Vượt ngân sách (Xấu).
        
- **SV (Schedule Variance) = EV - PV:** Sai lệch tiến độ.
    
    - _SV > 0:_ Vượt tiến độ/Nhanh hơn dự kiến (Tốt).
        
    - _SV < 0:_ Chậm tiến độ (Xấu).
        
- **VAC (Variance at Completion) = BAC - EAC:** Sai lệch khi hoàn thành. Dự báo khi kết thúc dự án ta sẽ dư hay thiếu bao nhiêu tiền.
    

### 3. Nhóm chỉ số hiệu suất (Dự án chạy hiệu quả thế nào?)

Dùng phép tính **Chia (÷)**. Kết quả **> 1** luôn là tốt.

- **CPI (Cost Performance Index) = EV / AC:** Hiệu suất chi phí.
    
    - _Ví dụ:_ CPI = 1.2 nghĩa là chi 1 đồng nhưng làm ra được 1.2 đồng giá trị.
        
- **SPI (Schedule Performance Index) = EV / PV:** Hiệu suất tiến độ.
    
    - _Ví dụ:_ SPI = 0.8 nghĩa là dự án mới chỉ chạy được 80% tốc độ cần thiết.
        

### 4. Nhóm chỉ số dự báo (Tương lai sẽ thế nào?)

Dùng để ước tính các con số khi dự án kết thúc:

- **EAC (Estimate at Completion):** Tổng chi phí ước tính khi dự án kết thúc.
    
    - Công thức phổ biến nhất: **EAC = BAC / CPI**.
        
- **ETC (Estimate to Complete):** Cần thêm bao nhiêu tiền nữa để hoàn thành phần việc còn lại.
    
    - **ETC = EAC - AC** hoặc **ETC = (BAC - EV) / CPI**.
        
- **EDAC (Estimated Duration at Completion):** Tổng thời gian ước tính khi dự án kết thúc.
    
    - **EDAC = BDAC / SPI**.
        
- **TCPI (To-Complete Performance Index):** Hiệu suất cần đạt được trong phần việc còn lại để về đích đúng ngân sách.
    
    - **TCPI = (BAC - EV) / (BAC - AC)**.
        


# PMG201c – Practical Exam 1 (Fall 2025) – QUESTION + FULL ANSWER

**Scenario:** You have developed a unique, niche consumer product. Your project is to validate its market viability through a temporary pop-up retail operation. Requirements: securing permits, designing and building the display, managing inventory, training student sales staff. Revenue target: **$15,000 gross revenue**. Operation period: **2 consecutive weeks**. Budget (setup + ops, excluding manufacturing cost): **$1,500**. Inventory shrinkage/loss must be kept **< 2%** of total inventory value. Customer satisfaction survey must exceed **> 90% positive**.

---

### ✅ Request 1 (20%) – Project Charter Statement

**1. Project Name:** Pop-Up Retail Market Validation

**2. Project Justification (Purpose & Reasons):**
The product has been developed but has no real-world evidence of market demand. The project is undertaken to:
- **Validate product-market fit** before committing to large-scale manufacturing and distribution investments.
- **Gather real-world data** (sales figures, customer feedback) through direct interaction with the target consumer base.
- **Minimize financial risk** by stress-testing market response with a minimal budget ($1,500) before any major capital commitment.
- The data collected will objectively justify or refute plans to scale up production and marketing.

**3. Project Constraints:**

| Constraint | Description |
|-----------|-------------|
| **Scope** | Includes: obtaining venue permits, designing and constructing the display booth, receiving and managing inventory, recruiting and training student sales staff, and collecting post-purchase customer surveys. Excludes: product manufacturing (manufacturing cost is explicitly out of scope). |
| **Time** | The pop-up operation must run for exactly **2 consecutive weeks** — no shorter, no extension permitted. |
| **Cost/Budget** | Setup and operational costs are capped at **$1,500** (excluding product cost). Total inventory shrinkage/loss must remain below **2%** of total inventory value. Revenue target: **$15,000 in gross revenue** over 2 weeks. |
| **Quality** | Customer satisfaction, measured by a post-purchase survey administered to all buyers, must exceed **> 90% positive feedback** regarding both product quality and the overall retail experience. |

---

### ✅ Request 2 (20%) – Cost/Budget Items (≥5 items, total ≤ $1,500)

| # | Cost Item | Description | Estimated Amount | Estimation Method & Person in Charge |
|---|-----------|-------------|-----------------|--------------------------------------|
| 1 | **Location & Venue Rental Fee** | Cost to rent the pop-up space at a shopping mall or campus venue for 2 weeks, including any security deposit and daily operating fees. | $500 | **Analogous Estimation:** Based on rental rates from a similar event booth organized previously. Person in charge: **Operations Coordinator**. |
| 2 | **Permits & Licenses** | Government or building management permit fees for a temporary retail operation at the chosen venue. | $100 | **Expert Judgment:** Consulted with someone experienced in obtaining temporary vendor permits. Person in charge: **PM**. |
| 3 | **Display & Booth Setup Materials** | Materials to build and decorate the retail booth: shelving units, signage, lighting, tables, and floor mat. | $450 | **Bottom-Up:** Itemized estimate – Shelving: $150, Signage: $100, Lighting: $80, Table: $70, Miscellaneous: $50. Person in charge: **Operations Coordinator**. |
| 4 | **Marketing & Promotional Materials** | Design and printing of flyers and posters for pre-event promotion; small social media advertising campaign to drive foot traffic. | $250 | **Parametric:** Design ($50) + Printing ($100) + Social Ads ($100). Person in charge: **Marketing Lead**. |
| 5 | **Staff Supplies & Training Materials** | Branded t-shirts/uniforms for student sales staff, printed training guides, clipboards, and printed customer survey forms. | $100 | **Bottom-Up:** Uniforms ($40 × 2 = $80) + Training materials ($20). Person in charge: **PM**. |
| 6 | **Contingency Reserve** | Emergency buffer for unexpected costs (e.g., rain → need a canvas awning, broken shelving → replacement). | $100 | **6.7% of total estimated budget**. Person in charge: **PM**. |

**Estimated Total: $1,500** ✅

---

### ✅ Request 3 (30%) – Communication Plan

**3 Stakeholders:**

| # | Stakeholder | Type |
|---|-------------|------|
| 1 | **Project Team** (Operations Coordinator + Sales Staff + Marketing Lead) | Project-Internal |
| 2 | **Company / Organization Management** (product owner / investor / founder funding the product) | Organization-Internal |
| 3 | **Venue / Mall Management** (the property manager of the pop-up location) | External |

---

**Stakeholder 1: Project Team (Project-Internal)**

| Information | Purpose | Frequency | Method/Format | Responsible |
|-------------|---------|-----------|---------------|-------------|
| Daily sales totals, inventory levels, and any incidents that occurred | Synchronize team on daily performance, identify issues immediately | **Daily** (end of each selling day) | 15-minute end-of-day debrief at the booth + WhatsApp group update | PM |
| Weekly summary: total revenue, aggregated customer feedback, and open issues | Evaluate Week 1 progress and adjust strategy for Week 2 | **Weekly** (end of Week 1) | Team meeting + shared Google Sheet dashboard | PM |
| Task assignments & shift schedule for all team members | Ensure correct staffing at all times, prevent coverage gaps | **Once** (before opening day) | Email + printed shift schedule posted at the booth | PM |

---

**Stakeholder 2: Company Management (Organization-Internal)**

| Information | Purpose | Frequency | Method/Format | Responsible |
|-------------|---------|-----------|---------------|-------------|
| Mid-point report: Week 1 revenue, initial survey results, and budget spending vs. plan | Keep management informed of progress toward the $15,000 goal; allow intervention if off-track | **Once** (end of Week 1) | Formal written report (PDF) via email | PM |
| Final project report: total gross revenue, customer satisfaction %, shrinkage %, and a Go/No-Go recommendation for scaling | Provide the data management needs to decide whether to invest in large-scale production | **Once** (after operation closes) | PowerPoint presentation + PDF report | PM |
| Urgent escalations (budget breach, major incident) | Obtain approval to take corrective action or spend contingency funds | **As needed** | Immediate phone call | PM |

---

**Stakeholder 3: Venue/Mall Management (External)**

| Information | Purpose | Frequency | Method/Format | Responsible |
|-------------|---------|-----------|---------------|-------------|
| Setup timeline (booth construction date, daily operating hours, teardown date) | Ensure venue staff are prepared; prevent conflicts with other events | **Once** (1 week before opening) | Formal email + signed operating agreement | Operations Coordinator |
| Daily check-in (confirm no issues with the space, utilities, or access) | Maintain good relationship; resolve any facility issues quickly | **Daily** (start of each day) | Brief verbal check-in at the venue management counter | Operations Coordinator |
| End-of-operation notice & booth dismantling plan | Return the space in proper condition; avoid penalty fees | **Once** (2 days before final day) | Formal email confirming teardown schedule | PM |

---

### ✅ Request 4 (30%) – Risk Register (≥3 Risks)

> [!note]
> This exam requires: Risk Title, Description, **Possible Impacts** (scope/quality, time, cost), Mitigation Plan & Contingency Plan.

| # | Risk Name & Description | Impact on Scope/Quality | Impact on Time | Impact on Cost | Mitigation Plan | Contingency Plan |
|---|------------------------|------------------------|----------------|----------------|-----------------|-----------------|
| 1 | **Low Foot Traffic / Sales Underperformance Risk:** The volume of customers visiting the booth is lower than projected, resulting in total revenue falling short of the $15,000 target over the 2-week operation. | **Quality:** Insufficient sales data undermines the statistical validity of the market validation conclusion. | **Time:** Cannot extend the operation period — the venue is booked for a fixed 2-week period only. | **Cost:** Revenue falls below $15,000, producing a negative ROI on the $1,500 investment; the business case for scaling fails. | Select a venue with consistently high foot traffic (weekend peak hours). Launch a marketing campaign at least 1 week before opening: social media posts, flyers distributed across campus. Position the booth near the main entrance of the venue for maximum visibility. | If revenue < $5,000 after Week 1 → PM immediately activates: (1) increased social media advertising using remaining budget, (2) a limited-time flash sale or promotional discount to urgently drive purchases, (3) an escalation report to management to reassess the strategy. |
| 2 | **Inventory Shrinkage Exceeding 2%:** Products are lost, damaged, or stolen, pushing the shrinkage/loss rate above 2% of total inventory value, violating the stated budget constraint. | **Quality:** Violates the <2% shrinkage KPI — constitutes a direct financial quality failure of the project. | **Time:** Requires a partial inventory halt for emergency counting and reconciliation, disrupting sales operations. | **Cost:** Every additional 1% of shrinkage on a $10,000 inventory = $100 in direct losses beyond the allowed threshold. | Implement a mandatory daily inventory count by Sales Staff at the end of each day. Keep high-value products in a locked display case or behind the counter. Install a small portable security camera or ensure merchandise is always within line-of-sight of staff. Require staff to sign a responsibility sheet for the products assigned to their shift. | If shrinkage exceeds 1% after Week 1 → increase surveillance, move sensitive items to a secured back area, and issue an immediate report to management with the updated shrinkage figure and recovery plan. |
| 3 | **Customer Satisfaction Below 90%:** Post-purchase survey results show < 90% positive feedback related to product quality or the retail experience, failing the primary quality KPI. | **Quality:** The most critical quality KPI is failed — the validation may produce a "Do Not Scale" recommendation due to poor customer reception, regardless of sales performance. | **Time:** Complaint investigation and repeat testing require time within the fixed 2-week window, which cannot be extended. | **Cost:** May result in product refunds, exchanges, and potential reputational costs that reduce net revenue. | Conduct intensive staff training on product knowledge and customer service techniques before opening day. Run an internal mystery shopper test on Day 1 to identify service gaps before they affect real customers. Administer satisfaction surveys immediately after each purchase (paper or QR code → Google Form). | If Week 1 survey results show < 85% satisfaction → PM holds an immediate emergency team meeting to diagnose the root cause (product issue? staff behavior? pricing?), and executes corrective actions in Week 2: staff re-training, improved product presentation and signage, or a clearly communicated exchange/return policy. |

---
---

# PMG201c – Practical Exam 2 (Summer 2025) – QUESTION + FULL ANSWER

**Prompt:** Select a project from a university course, campus activity, or a relevant project from someone you know. Answer the following requests based on your understanding and reasonable assumptions.

> [!note]
> **Project Selected:** Building the **FPT University Course Registration System (CRS)** — a web-based platform allowing students to register for courses online, view their timetable, and track their academic records.

---

### ✅ Request 1 (20%) – Project Charter Statement

**1. Project Name:** FPT University Course Registration System (CRS)

**2. Project Purpose / Justification:**
Currently, FPT University students must register for courses manually via email or in-person visits to the Academic Affairs Department, creating staff overload, information errors, and a lack of transparency in course slot allocation. The CRS project is undertaken to:
- Digitize and automate the entire course registration process, reducing the workload on administrative staff.
- Provide students with a self-service platform for fast, accurate, and transparent course registration available 24/7.
- Generate structured data to help the Academic Affairs Department plan class sizes, allocate lecturers, and forecast enrollment trends.

**3. High-Level Requirements (≥2):**

| # | High-Level Requirement |
|---|----------------------|
| 1 | **Student Self-Service Portal:** The system must allow students to log in using their student ID, browse the list of available courses, register for and cancel course enrollments, and receive an email confirmation of their enrollment within 5 minutes of completing the action. |
| 2 | **Admin Dashboard for Academic Affairs:** The Administrative Department must have a management interface to view total student registrations per course, open/close enrollment for specific courses, export class lists to Excel/PDF, and receive an automated alert when a class exceeds 80% capacity. |
| 3 | **Automated Conflict & Prerequisite Validation:** The system must automatically detect and reject registrations where a student selects a course that conflicts with their current timetable (time overlap) or for which they have not yet completed the prerequisite, displaying a clear and specific error message explaining the rejection. |

---

### ✅ Request 2 (20%) – Cost/Budget Items (≥5)

| # | Cost Item | Description | Estimated Amount | Estimation Method & Person in Charge |
|---|-----------|-------------|-----------------|--------------------------------------|
| 1 | **Backend Development** | Server-side API development: course registration logic, conflict and prerequisite check engine, student authentication, and database integration. | $6,000 | **Bottom-Up:** 2 backend developers × 3 months × $1,000/month. Person in charge: **Lead Developer**. |
| 2 | **Frontend Development** | Building the web UI for the Student Portal and Admin Dashboard using React/Vue.js, including responsive mobile design. | $4,000 | **Parametric:** 1 frontend developer × 4 months × $1,000/month. Person in charge: **Frontend Developer**. |
| 3 | **Database Design & Cloud Infrastructure** | Database schema design, cloud server setup (AWS/Azure), security configuration, and automated daily backup setup. | $2,000 | **Analogous:** Based on the infrastructure costs of the university's internal ERP project from the previous year (~$1,800). Person in charge: **System Admin + PM**. |
| 4 | **UI/UX Design** | Wireframing, prototyping, and full visual design of all interfaces. Includes user persona research sessions with real students. | $1,500 | **Expert Judgment:** Estimated by an experienced UX Designer — Research ($300) + Wireframes ($500) + Visual Design ($700). Person in charge: **UX Designer**. |
| 5 | **Testing & QA** | Full testing cycle: functional testing (all modules), integration testing, UAT with 50 real students, and performance testing at 500 concurrent users. | $1,500 | **Parametric:** 1 QA engineer × 1.5 months × $1,000/month. Person in charge: **QA Lead**. |
| 6 | **Training & Documentation** | Writing the user manual (student + admin versions), organizing 2 training workshops for administrative staff, and supporting system onboarding. | $500 | **Bottom-Up:** Manual writing ($200) + Training workshops ($300). Person in charge: **Business Analyst**. |
| 7 | **Contingency Reserve** | 10% budget buffer for unforeseen risks (scope changes, technical blockers, additional testing cycles). | $1,500 | **Percentage of Total:** 10% × $15,000 (Items 1–6). Person in charge: **PM**. |

**Estimated Total: ~$17,000** (within the assumed project budget)

---

### ✅ Request 3 (30%) – Communication Plan

**3 Stakeholders:**

| # | Stakeholder | Type |
|---|-------------|------|
| 1 | **Development Team** (Developers + QA + UX Designer) | Project-Internal |
| 2 | **FPT University Academic Affairs Department** | Organization-Internal |
| 3 | **Students** (Beta Testers & End Users) | External |

---

**Stakeholder 1: Development Team (Project-Internal)**

| Information | Purpose | Frequency | Method/Format | Responsible |
|-------------|---------|-----------|---------------|-------------|
| Sprint goals, task assignments for the week, and current blockers | Synchronize daily progress, surface and resolve blockers quickly | **Daily** | 15-minute Daily Standup – Google Meet | PM |
| Sprint review: tasks completed, bugs found, team velocity | Evaluate sprint output, gather team feedback, improve process | **Bi-weekly** (every 2 weeks) | Sprint Review Meeting on Jira board | PM + Team |
| Technical architectural decisions | Align the team on technical direction, prevent costly rework | **As needed** | Slack #tech channel + ad hoc meeting | Lead Developer |

---

**Stakeholder 2: Academic Affairs Department (Organization-Internal)**

| Information | Purpose | Frequency | Method/Format | Responsible |
|-------------|---------|-----------|---------------|-------------|
| Monthly project status report: features delivered, budget spent, upcoming milestones | Keep the department informed and aligned; ensure the system scope still meets their operational needs | **Monthly** | Formal PDF status report via email + follow-up meeting | PM |
| End-of-phase feature demo on the staging environment | Gather early real-user feedback from admins to course-correct before features are fully finalized | **Every 6 weeks** | Live demo session on the staging server | PM + BA |
| UAT invitation and training session schedule | Prepare administrative staff to participate in User Acceptance Testing and use the system at launch | **Once** (final month of project) | Formal email invitation + printed schedule | PM |

---

**Stakeholder 3: Students (External)**

| Information | Purpose | Frequency | Method/Format | Responsible |
|-------------|---------|-----------|---------------|-------------|
| Beta testing invitation with participation instructions | Collect real end-user feedback before the official launch to identify UX and functional issues | **Once** (2 weeks before launch) | Email via the FPT student portal + campus posters | BA + PM |
| System launch announcement and quick-start user guide | Ensure every student knows the system is live and understands how to use it | **Once** (on go-live day) | Mass email to all students + FAQ page on the FPT website | PM |
| Post-launch satisfaction survey | Measure user satisfaction and identify improvement opportunities for Phase 2 | **Once** (2 weeks after launch) | Google Form link sent via email | BA |

---

### ✅ Request 4 (30%) – Milestones & Activity Sequence

**3 Main Project Milestones:**

| # | Milestone | Deliverable | Target Date |
|---|-----------|-------------|-------------|
| M1 | **Requirements & Design Complete** | Approved SRS document; UI/UX prototype reviewed and approved by Academic Affairs | End of Month 2 |
| M2 | **Development & Testing Complete** | Fully functional system (all 3 modules); QA report confirming zero critical open bugs | End of Month 5 |
| M3 | **System Go-Live & Handover** | Live system accessible to all students; trained admin staff; published user manual | End of Month 6 |

**Selected Milestone: M2 – Development & Testing Complete**

**≥10 Activities & Dependency Sequence:**

| # | Activity | Duration | Predecessor | Relationship |
|---|----------|----------|-------------|--------------|
| 1 | Set up development environment & Git repository | 2 days | – | – |
| 2 | Implement database schema (students, courses, enrollment tables) | 4 days | 1 | FS |
| 3 | Develop Authentication module (student login, session management) | 5 days | 2 | FS |
| 4 | Develop Course Listing & Search module (Student Portal) | 8 days | 3 | FS |
| 5 | Develop Course Registration & Cancellation module | 10 days | 4 | FS |
| 6 | Develop Conflict & Prerequisite Validation engine | 7 days | 5 | SS (can start in parallel with Activity 5) |
| 7 | Develop Admin Dashboard (view registrations, manage course capacity) | 10 days | 3 | SS (can start in parallel with Activity 4) |
| 8 | Develop Email Notification system (enrollment confirmations) | 4 days | 5 | SS (starts in parallel with Activity 5) |
| 9 | Integration testing (all modules combined) | 6 days | 5, 6, 7, 8 | FS (all modules must be complete first) |
| 10 | Performance testing (500 concurrent users simulation) | 4 days | 9 | SS (can begin alongside integration testing) |
| 11 | User Acceptance Testing (UAT) with 50 students & admin staff | 7 days | 10 | FS |
| 12 | Bug fixing & regression testing | 5 days | 11 | FS |

> **Dependency Notes:**
> - A6 **SS** A5: Validation engine starts in parallel with Registration module development.
> - A7 **SS** A4: Admin Dashboard development starts in parallel with the student-facing Course Listing module.
> - A8 **SS** A5: Email notifications start in parallel with Registration module.
> - A10 **SS** A9: Performance testing begins alongside Integration testing's first phase.

---
---

# PMG201c – Practical Exam 2 (Fall 2025) – QUESTION + FULL ANSWER

**Scenario:** Local media lacks adequate coverage of events relevant to the university community. Your project is to establish a digital news channel (e.g., a weekly podcast or video series) focused exclusively on this niche. Requirements: produce and distribute at least one high-quality piece of content per week; reach **500 unique subscribers/followers**. Maintain a continuous production cycle for **3 months**. Total budget for promotional boosting and equipment: **$500**. All editing and production software must be **free or open-source**. Quality standard: **zero verifiable complaints of factual inaccuracy** and a **95% content completion rate** (low drop-off from viewers/listeners).

---

### ✅ Request 1 (20%) – Project Charter Statement

**1. Project Name:** FPT Campus Digital News Channel (CampusVoice)

**2. Justification (Purpose & Reasons):**
Local and mainstream media channels currently lack sufficient, timely, and relevant coverage of events within the FPT University community — including campus events, student achievements, research milestones, and career opportunities. The CampusVoice project is undertaken to:
- **Bridge the information gap:** Provide a reliable, student-centric source of credible news and stories about the FPT University community.
- **Build campus community:** Create a shared platform that connects students, faculty, and alumni through valuable and relevant content.
- **Develop real-world student skills:** Give student content creators hands-on experience in journalism, video production, audio engineering, and digital content marketing.
- **Strengthen FPT University's brand:** Promote the university's image to a wider external audience through professional, fact-based storytelling.

**3. Project Constraints:**

| Constraint | Description |
|-----------|-------------|
| **Scope** | Includes: setting up and operating 1 YouTube channel, 1 weekly podcast episode, and 1 weekly newsletter. Content topics: campus events, research achievements, and career opportunities. Excludes: live event streaming, other social media (TikTok, Facebook, Instagram), and long-form video documentary production. |
| **Time** | A continuous production cycle must be maintained for exactly **3 months (12 weeks)**, with a minimum of **1 content piece published per week**. |
| **Cost/Budget** | Total budget is **$500**, reserved exclusively for promotional boosting and physical equipment. All software used for editing and production **must be free or open-source** (examples: DaVinci Resolve for video, Audacity for audio, OBS for recording, Canva free tier for design, Mailchimp free tier for newsletters). |
| **Quality** | (1) **Zero verifiable complaints** of factual inaccuracy received throughout all 12 weeks of operation. (2) **≥95% content completion rate** — viewers must watch/listen to the content to the end (low audience drop-off), measured via platform analytics. |

---

### ✅ Request 2 (20%) – Measurable Project Objectives (≥2)

**Objective 1: Reach 500 unique YouTube subscribers by the end of Week 12 (end of the 3-month production cycle).**

**How it will be measured:**
- **Metric:** YouTube Studio Analytics → "Subscribers" total count (unique accounts).
- **Target:** ≥ 500 subscribers by **the last day of Week 12**.
- **Measurement tool:** YouTube Studio dashboard, reviewed by the PM every Friday.
- **Intermediate milestones:**
  - End of Week 4 (Month 1): ≥ 100 subscribers
  - End of Week 8 (Month 2): ≥ 300 subscribers
  - End of Week 12 (Month 3): ≥ 500 subscribers ← **Final success criterion**
- **Result classification:** ≥ 500 = SUCCESS | < 400 = FAIL → mandatory post-mortem and strategy revision required.

---

**Objective 2: Maintain a ≥ 95% content completion rate (percentage of viewers/listeners who reach the end of each episode) consistently throughout all 12 weeks of production.**

**How it will be measured:**
- **YouTube Metric:** YouTube Analytics → "Average Percentage Viewed" per video. Target: ≥ 95%.
- **Podcast Metric:** Anchor/Spotify for Podcasters Analytics → "Average Listen-Through Rate." Target: ≥ 95%.
- **Measurement frequency:** Measured after each episode is published; aggregated and reported every 4 weeks (3 reports total).
- **Measurement owner:** Technical Editor collects the data and reports to PM weekly.
- **Action trigger:** If 2 consecutive episodes have a completion rate < 90% → The team holds an immediate content review meeting to identify the cause (episodes too long? topic not engaging? audio quality issues?) and implements a corrective format change.
- **Success:** Average completion rate ≥ 95% across all 12 published episodes.

---

### ✅ Request 3 (30%) – RACI Chart

**3 Project Roles:**

| Role | Description |
|------|-------------|
| **PM (Project Manager)** | Plans the 12-week production calendar, manages the $500 budget, tracks KPIs weekly (subscribers, completion rate, complaints), approves all content before publication, and escalates issues. |
| **CC (Content Creator / Reporter)** | Researches weekly topics, contacts and interviews sources, writes the script and talking points for each episode, and drafts the newsletter content. First point of accountability for factual accuracy at the initial writing stage. |
| **TE (Technical Editor / Producer)** | Independently fact-checks all content before publication, edits the video (DaVinci Resolve) and audio (Audacity), uploads content to all platforms, manages technical platform operations, and compiles analytics reports. |

**RACI Matrix (≥10 Tasks):**

| # | Task / Activity / Deliverable | PM | CC | TE |
|---|-------------------------------|----|----|-----|
| 1 | Define 12-week content strategy & editorial calendar | A | R | C |
| 2 | Set up YouTube channel (branding, banner, description, links) | A | C | R |
| 3 | Set up podcast hosting platform (Anchor / Spotify for Podcasters) | A | I | R |
| 4 | Set up newsletter platform (Mailchimp free tier) | A | I | R |
| 5 | Procure physical equipment within $500 budget (mic, ring light) | A | C | R |
| 6 | Research weekly topic & identify credible, verifiable sources | C | A/R | C |
| 7 | Write the episode script & newsletter draft | I | A/R | C |
| 8 | Record video & audio episode | I | C | A/R |
| 9 | Edit video (DaVinci Resolve) & audio (Audacity) | C | I | A/R |
| 10 | Fact-check all content (verify every fact, quote & statistic) | A | C | R |
| 11 | Upload video to YouTube (optimize title, description, tags, thumbnail) | A | I | R |
| 12 | Distribute podcast episode & send weekly newsletter | A | I | R |
| 13 | Monitor platform analytics (subscribers, views, completion rate) & report | A/R | I | C |
| 14 | Manage the $500 promotional budget (YouTube Ads boosting campaigns) | A | I | C |

> [!tip]
> ✅ Verification: Each task has exactly **1 "A"**. All four symbols R, A, C, I appear in the table. ✅

---

### ✅ Request 4 (30%) – Milestones & Activity Sequence

**3 Main Project Milestones:**

| # | Milestone | Deliverable | Target Date |
|---|-----------|-------------|-------------|
| M1 | **Pre-Production Complete** – All platforms live; Episode 1 published | YouTube channel live, podcast feed active, first newsletter sent, Episode 1 published on all platforms | End of Week 2 |
| M2 | **Mid-Production Checkpoint** – 300 subscribers; content rhythm stable | 8 episodes published, Month 1–2 analytics report, 300 subscribers verified | End of Week 8 |
| M3 | **Project Closeout** – 500 subscribers, 0 complaints, final report submitted | All 12 episodes published, 500+ subscribers, final analytics & project closure report | End of Week 12 |

**Selected Milestone: M1 – Pre-Production Complete (End of Week 2)**

*Why M1 was selected:* M1 is the most critical milestone because any mistakes made here (wrong platform choice, poor branding, inadequate equipment) will compound and negatively affect all 12 subsequent weeks of production.

**≥10 Activities & Dependency Sequence:**

| # | Activity | Duration | Predecessor | Relationship |
|---|----------|----------|-------------|--------------|
| 1 | Conduct kick-off meeting & assign team roles | 1 day | – | – |
| 2 | Define target audience & 3 content pillars (campus events, research, careers) | 2 days | 1 | FS |
| 3 | Create 12-week editorial calendar (one topic per week scheduled in advance) | 2 days | 2 | FS |
| 4 | Design channel branding: name, logo, color palette using Canva free | 2 days | 2 | SS (starts in parallel with Activity 3) |
| 5 | Set up YouTube channel (upload branding, write channel description, add links) | 1 day | 4 | FS |
| 6 | Set up podcast hosting platform (Anchor free) | 1 day | 4 | SS (starts in parallel with Activity 5) |
| 7 | Set up newsletter on Mailchimp free (create template + subscriber sign-up form) | 1 day | 4 | SS (starts in parallel with Activity 5) |
| 8 | Procure equipment within budget (USB microphone, ring light, webcam) | 3 days | 1 | FS |
| 9 | Install & test free editing software (DaVinci Resolve, Audacity, OBS) | 2 days | 8 | SS (can begin installing software while awaiting equipment delivery) |
| 10 | Research and write the script for Episode 1 | 3 days | 3 | FS (requires the editorial calendar to be finalized) |
| 11 | Record Episode 1 (both video and audio) | 1 day | 8, 9, 10 | FS (all three — equipment, software, and script — must be ready) |
| 12 | Edit Episode 1: video (DaVinci Resolve) + audio (Audacity) | 2 days | 11 | FS |
| 13 | Fact-check all content in Episode 1 | 1 day | 12 | FS |
| 14 | Publish Episode 1 to YouTube + podcast platform; send first newsletter | 1 day | 5, 6, 7, 13 | FS (all platforms must be live AND content must be fact-checked and approved) |

**Key Dependency Highlights:**
- A4 **SS** A3: Channel branding design starts in parallel with building the editorial calendar.
- A6 **SS** A5 and A7 **SS** A5: Podcast and newsletter platform setup run simultaneously after branding is complete.
- A9 **SS** A8: Software installation begins while waiting for the physical equipment to arrive (separate contractors).
- A14 **FS** (A5 + A6 + A7 + A13): Publication can only happen once ALL platforms are live AND the content has passed fact-checking — this is a hard dependency with no exceptions.

---

*PMG201c – Real Past Exam Model Answers – FPT University*
*Note: These are model answers for study purposes. In your actual exam, always rewrite in your own words and stay closely tied to the specific scenario given in the question.*

**Scenario:** Bạn đã phát triển một sản phẩm tiêu dùng độc đáo. Dự án là validate sức hút thị trường qua một pop-up retail tạm thời. Yêu cầu: xin giấy phép, thiết kế gian hàng, quản lý hàng tồn kho, huấn luyện nhân viên sinh viên. Mục tiêu: $15,000 doanh thu. Thời gian vận hành: **2 tuần liên tiếp**. Budget (setup + ops, không tính giá vốn hàng): **$1,500**. Shrinkage/loss < 2% giá trị hàng tồn. Customer satisfaction survey: **> 90% positive**.

---

### ✅ Request 1 (20%) – Project Charter Statement

**1. Project Name:** Pop-Up Retail Market Validation

**2. Project Justification (Purpose & Reasons):**
Sản phẩm hiện chỉ mới được phát triển và chưa có bằng chứng thực tế về nhu cầu thị trường. Dự án được thực hiện nhằm:
- **Validate product-market fit** trước khi đầu tư vào sản xuất và phân phối quy mô lớn.
- **Thu thập dữ liệu thực tế** (sales data, customer feedback) từ việc tương tác trực tiếp với người mua hàng mục tiêu.
- **Giảm thiểu rủi ro tài chính** bằng cách kiểm tra phản ứng thị trường với chi phí tối thiểu ($1,500) trước khi commit ngân sách lớn hơn.
- Dữ liệu thu được sẽ justify hoặc bác bỏ kế hoạch mở rộng sản xuất và marketing quy mô lớn.

**3. Project Constraints:**

| Constraint | Description |
|-----------|-------------|
| **Scope** | Dự án bao gồm: xin giấy phép tổ chức, thiết kế và xây dựng gian hàng trưng bày, quản lý hàng tồn kho, tuyển dụng và huấn luyện nhân viên sinh viên bán hàng, thu thập phản hồi khách hàng. Không bao gồm: sản xuất sản phẩm (manufacturing cost bị loại trừ). |
| **Time** | Pop-up operation phải vận hành đúng **2 tuần liên tiếp** – không ngắn hơn, không kéo dài thêm. |
| **Cost/Budget** | Setup và operational costs tối đa **$1,500** (không gồm giá vốn hàng). Inventory shrinkage/loss phải dưới **2%** tổng giá trị hàng tồn kho. Mục tiêu doanh thu: **$15,000 gross revenue** trong 2 tuần. |
| **Quality** | Điểm hài lòng khách hàng đo bằng post-purchase survey phải đạt **> 90% positive feedback** về chất lượng sản phẩm và trải nghiệm mua sắm. |

---

### ✅ Request 2 (20%) – Cost/Budget Items (≥5 items, total ≤ $1,500)

| # | Cost Item | Description | Estimated Amount | Estimation Method & Person in Charge |
|---|-----------|-------------|-----------------|--------------------------------------|
| 1 | **Location & Venue Fee** | Chi phí thuê không gian pop-up tại trung tâm thương mại / khuôn viên trường trong 2 tuần, bao gồm tiền đặt cọc và phí vận hành mặt bằng. | $500 | **Analogous:** Dựa trên giá thuê gian hàng sự kiện tương tự đã tổ chức trước đó. Người phụ trách: **Operations Coordinator**. |
| 2 | **Permits & Licenses** | Lệ phí xin giấy phép bán hàng tạm thời từ chính quyền địa phương / ban quản lý tòa nhà. | $100 | **Expert Judgment:** Tham khảo luật sư hoặc người có kinh nghiệm xin phép trước đó. Người phụ trách: **PM**. |
| 3 | **Display & Booth Setup Materials** | Vật liệu xây dựng và trang trí gian hàng: kệ trưng bày, biển hiệu, đèn, bàn, thảm. | $450 | **Bottom-up:** Liệt kê từng hạng mục (kệ $150, biển $100, đèn $80, bàn $70, misc $50). Người phụ trách: **Operations Coordinator**. |
| 4 | **Marketing & Promotional Materials** | In ấn tờ rơi, banner, thiết kế poster quảng bá trước sự kiện. Chạy quảng cáo mạng xã hội nhỏ để thu hút khách. | $250 | **Parametric:** Chi phí thiết kế ($50) + in ấn ($100) + social ads ($100). Người phụ trách: **Marketing Lead**. |
| 5 | **Staff Supplies & Training Materials** | Đồng phục / áo thun nhận diện cho nhân viên sinh viên, tài liệu training, clipboard và survey forms. | $100 | **Bottom-up:** Áo ($40×2=$80) + materials ($20). Người phụ trách: **PM**. |
| 6 | **Contingency Reserve** | Dự phòng cho chi phí phát sinh không lường trước (mưa → cần mái che, hỏng kệ → thay thế...). | $100 | **6.7% of total budget** dự phòng. Người phụ trách: **PM**. |

**Tổng ước tính: $1,500** ✅

---

### ✅ Request 3 (30%) – Communication Plan

**3 Stakeholders:**

| # | Stakeholder | Type |
|---|-------------|------|
| 1 | **Project Team** (Operations Coordinator + Sales Staff + Marketing Lead) | Project-Internal |
| 2 | **Company/Organization Management** (người đứng sau sản phẩm – nhà đầu tư / founder) | Organization-Internal |
| 3 | **Venue/Mall Management** (ban quản lý địa điểm tổ chức pop-up) | External |

---

**Stakeholder 1: Project Team (Project-Internal)**

| Information | Purpose | Frequency | Method/Format | Responsible |
|-------------|---------|-----------|---------------|-------------|
| Daily sales figures, inventory levels, incidents | Đồng bộ tiến độ, phát hiện vấn đề tức thì | **Daily** (cuối mỗi ngày bán) | Daily briefing 15 phút tại gian hàng + WhatsApp group | PM |
| Weekly summary: doanh thu, customer feedback tổng hợp, issues | Đánh giá tiến độ cuối tuần 1, chuẩn bị cho tuần 2 | **Weekly** (cuối tuần 1) | Team meeting + Google Sheet dashboard | PM |
| Task assignments & shift schedule | Đảm bảo đủ người đúng ca, không bị thiếu nhân lực | **Once** (trước ngày khai trương) | Email + printed schedule | PM |

---

**Stakeholder 2: Company Management (Organization-Internal)**

| Information | Purpose | Frequency | Method/Format | Responsible |
|-------------|---------|-----------|---------------|-------------|
| Mid-point report: doanh thu tuần 1, survey results sơ bộ, spending vs. budget | Cập nhật cho management về tiến độ đạt mục tiêu $15,000 và xử lý nếu cần can thiệp | **Once** (hết tuần 1) | Formal written report (PDF) qua email | PM |
| Final project report: tổng doanh thu, customer satisfaction %, shrinkage %, Go/No-Go recommendation | Cung cấp data để management quyết định có expand production không | **Once** (sau khi kết thúc) | Presentation + PDF report | PM |
| Urgent escalation (vượt budget, sự cố lớn) | Xin phê duyệt chi thêm hoặc can thiệp kịp thời | **As needed** | Phone call ngay lập tức | PM |

---

**Stakeholder 3: Venue/Mall Management (External)**

| Information | Purpose | Frequency | Method/Format | Responsible |
|-------------|---------|-----------|---------------|-------------|
| Setup schedule & timeline (ngày dựng gian hàng, giờ vận hành, ngày tháo dỡ) | Đảm bảo venue chuẩn bị sẵn sàng, không xung đột với events khác | **Once** (1 tuần trước khai trương) | Formal email + signed agreement | Operations Coordinator |
| Daily check-in (xác nhận không có vấn đề về mặt bằng, điện, nước) | Duy trì quan hệ tốt, giải quyết sự cố cơ sở vật chất nhanh | **Daily** (đầu mỗi ngày) | Verbal check-in tại quầy quản lý | Operations Coordinator |
| End-of-operation notice & booth dismantling plan | Trả lại mặt bằng đúng quy định, tránh phát sinh phí phạt | **Once** (trước ngày cuối 2 ngày) | Formal email | PM |

---

### ✅ Request 4 (30%) – Risk Register (≥3 Risks)

> [!note]
> Đề bài yêu cầu: Risk Title, Description, **Possible Impacts** (scope/quality, time, cost), Mitigation & Contingency Plan.

| # | Risk Name & Description | Impact on Scope/Quality | Impact on Time | Impact on Cost | Mitigation Plan | Contingency Plan |
|---|------------------------|------------------------|----------------|----------------|-----------------|-----------------|
| 1 | **Low Foot Traffic / Sales Underperformance:** Lượng khách đến gian hàng thấp hơn dự kiến, dẫn đến doanh thu không đạt $15,000 trong 2 tuần. | **Quality:** Dữ liệu validation không đủ ý nghĩa thống kê → kết luận kém tin cậy. | **Time:** Không thể gia hạn vì venue đã đặt cố định 2 tuần. | **Cost:** Không đạt $15,000 → ROI âm so với $1,500 đã đầu tư. | Chọn địa điểm có lưu lượng người cao (cuối tuần cao điểm). Lên chiến dịch marketing trước 1 tuần: social media, flyers tại trường. Đặt gian hàng gần lối vào chính của venue. | Nếu hết tuần 1 doanh thu < $5,000 → PM kích hoạt: (1) tăng cường quảng cáo social media trong ngân sách còn lại, (2) tổ chức flash sale / giảm giá khuyến mãi đặc biệt, (3) báo cáo ngay cho management để xem xét điều chỉnh strategy. |
| 2 | **Inventory Shrinkage Exceeding 2%:** Hàng hóa bị mất, hư hỏng hoặc bị lấy trộm vượt quá 2% tổng giá trị hàng tồn kho, vi phạm budget constraint. | **Quality:** Vi phạm KPI shrinkage → thất bại về chỉ tiêu chất lượng tài chính. | **Time:** Phải dừng bán một số SKU để kiểm kê, gây gián đoạn hoạt động. | **Cost:** Mỗi % shrinkage thêm = mất thêm tiền hàng. Ví dụ: nếu inventory $10,000 thì 2% = $200 giới hạn. | Thiết lập hệ thống kiểm kê cuối ngày (daily inventory count) với Sales Staff. Lắp camera an ninh nhỏ hoặc đặt hàng trong tầm nhìn nhân viên. Sử dụng display locked case cho hàng có giá trị cao. Nhân viên ký nhận trách nhiệm hàng hóa mỗi ca. | Nếu phát hiện shrinkage vượt 1% sau tuần 1 → tăng cường giám sát, chuyển hàng nhạy cảm vào kho hàng phía sau, và PM báo cáo ngay cho management về tình trạng thực tế. |
| 3 | **Customer Satisfaction Falling Below 90%:** Phản hồi khách hàng qua survey cho thấy < 90% positive về chất lượng sản phẩm hoặc trải nghiệm mua sắm. | **Quality:** Không đạt KPI chính về satisfaction → dự án fail về mục tiêu validation. Kết quả có thể khuyên nghị ngược lại (không nên expand). | **Time:** Cần thêm thời gian xử lý khiếu nại và re-test – nhưng dự án chỉ có 2 tuần cố định. | **Cost:** Có thể phải refund hoặc exchange hàng, tăng chi phí phát sinh. | Huấn luyện nhân viên kỹ về product knowledge và customer service trước khi khai trương. Thực hiện mystery shopper test trong ngày đầu để phát hiện gap. Thiết lập quick feedback loop: thu thập survey ngay sau mỗi giao dịch (paper or QR code). | Nếu survey kết quả tuần 1 < 85% → PM ngay lập tức họp team, xác định nguyên nhân cụ thể (sản phẩm? nhân viên? giá?), thực hiện corrective action trong tuần 2: huấn luyện lại nhân viên, adjust product presentation, hoặc offer exchange policy rõ ràng hơn. |

---
---

# **PMG201c - Practical Exam 2 (Summer 2025) – ĐỀ BÀI + ĐÁP ÁN**

**Đề bài:** Chọn một dự án từ môn học tại trường ĐH hoặc hoạt động trường ĐH mà bạn đang/đã tham gia (hoặc của bạn bè/người thân). Trả lời các câu hỏi dựa trên hiểu biết và giả định của bạn.

> [!note]
> **Dự án được chọn:** Xây dựng **Hệ thống Quản lý Học phần (Course Registration System)** cho FPT University – một hệ thống web cho phép sinh viên đăng ký môn học online, xem thời khóa biểu và theo dõi kết quả học tập.

---

### ✅ Request 1 (20%) – Project Charter Statement

**1. Project Name:** FPT University Course Registration System (CRS)

**2. Project Purpose / Justification:**
Hiện tại, sinh viên FPT University phải đăng ký học phần thủ công qua email hoặc gặp trực tiếp phòng đào tạo, gây ra tình trạng quá tải nhân sự, nhầm lẫn thông tin và không minh bạch trong quá trình phân bổ chỗ học. Dự án CRS được thực hiện nhằm:
- Số hóa toàn bộ quy trình đăng ký học phần, giảm tải cho phòng đào tạo.
- Cung cấp cho sinh viên trải nghiệm đăng ký môn học nhanh chóng, minh bạch và chính xác 24/7.
- Tạo nền tảng dữ liệu để phòng đào tạo lập kế hoạch lớp học và phân bổ giảng viên hiệu quả hơn.

**3. High-Level Requirements (≥2):**

| # | High-Level Requirement |
|---|----------------------|
| 1 | **Student Self-Service Portal:** Hệ thống phải cho phép sinh viên đăng nhập bằng mã số sinh viên, xem danh sách môn học mở, đăng ký và hủy đăng ký môn học, và nhận xác nhận đăng ký qua email trong vòng 5 phút. |
| 2 | **Admin Dashboard for Academic Department:** Phòng đào tạo phải có giao diện quản lý để xem tổng số sinh viên đăng ký từng môn, đóng/mở đăng ký theo môn, export danh sách lớp học ra file Excel/PDF, và nhận cảnh báo khi lớp sắp đầy (>80% capacity). |
| 3 | **Automated Conflict & Prerequisite Check:** Hệ thống tự động kiểm tra và từ chối đăng ký nếu sinh viên chọn môn có trùng giờ hoặc chưa qua môn tiên quyết (prerequisite), đồng thời hiển thị thông báo lỗi rõ ràng. |

---

### ✅ Request 2 (20%) – Cost/Budget Items (≥5)

| # | Cost Item | Description | Estimated Amount | Estimation Method & Person in Charge |
|---|-----------|-------------|-----------------|--------------------------------------|
| 1 | **Backend Development** | Phát triển server-side: API đăng ký môn học, business logic (conflict check, prerequisite), authentication, database integration. | $6,000 | **Bottom-up:** 2 backend devs × 3 tháng × $1,000/tháng. Người phụ trách: **Lead Developer**. |
| 2 | **Frontend Development** | Xây dựng giao diện web (Student Portal + Admin Dashboard) bằng React/Vue. Bao gồm responsive design cho mobile. | $4,000 | **Parametric:** 1 frontend dev × 4 tháng × $1,000/tháng. Người phụ trách: **Frontend Developer**. |
| 3 | **Database Design & Server Infrastructure** | Thiết kế schema, setup cloud server (AWS/Azure), configuration security và backup tự động hàng ngày. | $2,000 | **Analogous:** Dựa trên chi phí infrastructure của dự án ERP nội bộ năm trước ($1,800). Người phụ trách: **System Admin + PM**. |
| 4 | **UI/UX Design** | Thiết kế wireframe, prototype và design assets cho toàn bộ giao diện. Persona research với sinh viên thật. | $1,500 | **Expert Judgment:** Ước tính từ UX Designer có kinh nghiệm. Bao gồm: research ($300), wireframe ($500), design ($700). Người phụ trách: **UX Designer**. |
| 5 | **Testing & QA** | Kiểm thử toàn diện: functional, integration, UAT với 50 sinh viên thật, performance test (500 concurrent users). | $1,500 | **Parametric:** 1 QA × 1.5 tháng × $1,000/tháng. Người phụ trách: **QA Lead**. |
| 6 | **Training & Documentation** | Viết user manual, tổ chức training session cho phòng đào tạo (2 buổi), hỗ trợ onboarding. | $500 | **Bottom-up:** Manual writing ($200) + training sessions ($300). Người phụ trách: **BA**. |
| 7 | **Contingency Reserve** | Dự phòng 10% ngân sách cho rủi ro phát sinh. | $1,500 | **10% of estimated total** ($15,000). Người phụ trách: **PM**. |

**Tổng ước tính: ~$17,000** (nằm trong phạm vi ngân sách dự án giả định)

---

### ✅ Request 3 (30%) – Communication Plan

**3 Stakeholders:**

| # | Stakeholder | Type |
|---|-------------|------|
| 1 | **Development Team** (Dev + QA + UX Designer) | Project-Internal |
| 2 | **FPT University Academic Department** (Phòng đào tạo) | Organization-Internal |
| 3 | **Students (Beta Testers & End Users)** | External |

---

**Stakeholder 1: Development Team (Project-Internal)**

| Information | Purpose | Frequency | Method/Format | Responsible |
|-------------|---------|-----------|---------------|-------------|
| Sprint goals, task assignments, blockers | Đồng bộ tiến độ hàng ngày, giải quyết vướng mắc sớm | **Daily** | Daily Standup 15 phút – Google Meet | PM |
| Sprint review: tasks completed, bugs found, velocity | Đánh giá sprint, nhận feedback, cải tiến quy trình | **Bi-weekly** (2 tuần/lần) | Sprint Review Meeting – Jira board | PM + Team |
| Technical architecture decisions | Thống nhất về technical direction và avoid rework | **As needed** | Slack #tech channel + informal meeting | Lead Developer |

---

**Stakeholder 2: Academic Department (Organization-Internal)**

| Information | Purpose | Frequency | Method/Format | Responsible |
|-------------|---------|-----------|---------------|-------------|
| Monthly project status: features delivered, budget spent, upcoming milestones | Đảm bảo dự án đang đi đúng hướng, scope phù hợp với yêu cầu phòng đào tạo | **Monthly** | Formal status report (PDF) + meeting | PM |
| Feature demo at end of each phase | Lấy feedback từ người dùng thực (admin) để điều chỉnh sớm | **Every 6 weeks** | Live demo trên staging environment | PM + BA |
| UAT invitation & training schedule | Chuẩn bị phòng đào tạo sẵn sàng tham gia test và sử dụng hệ thống | **Once** (tháng cuối dự án) | Email formal invitation + schedule | PM |

---

**Stakeholder 3: Students (External)**

| Information | Purpose | Frequency | Method/Format | Responsible |
|-------------|---------|-----------|---------------|-------------|
| Beta testing invitation & instructions | Thu thập feedback thực từ người dùng cuối trước go-live | **Once** (2 tuần trước launch) | Email qua student portal FPT + Poster trên campus | BA + PM |
| System launch announcement & user guide | Thông báo hệ thống đã sẵn sàng, hướng dẫn cách đăng ký | **Once** (ngày go-live) | Email toàn sinh viên + FAQ page trên website | PM |
| Post-launch survey (satisfaction feedback) | Đo lường user satisfaction, tìm cải tiến cho Phase 2 | **Once** (2 tuần sau launch) | Google Form qua email | BA |

---

### ✅ Request 4 (30%) – Milestones & Activity Sequence

**3 Main Project Milestones:**

| # | Milestone | Deliverable | Target Date |
|---|-----------|-------------|-------------|
| M1 | **Requirements & Design Complete** | Approved SRS document, UI/UX prototype reviewed by Academic Dept | End of Month 2 |
| M2 | **Development & Testing Complete** | Working system (all 3 modules), QA test report with 0 critical bugs | End of Month 5 |
| M3 | **Go-Live & Handover** | Live system accessible to all students, trained admin staff, user manual | End of Month 6 |

**Selected Milestone: M2 – Development & Testing Complete**

**≥ 10 Activities & Sequence:**

| # | Activity | Duration | Predecessor | Relationship |
|---|----------|----------|-------------|--------------|
| 1 | Set up development environment & Git repository | 2 days | – | – |
| 2 | Implement database schema (students, courses, enrollment) | 4 days | 1 | FS |
| 3 | Develop Authentication module (login, session management) | 5 days | 2 | FS |
| 4 | Develop Course Listing & Search module (Student Portal) | 8 days | 3 | FS |
| 5 | Develop Course Registration & Cancellation module | 10 days | 4 | FS |
| 6 | Develop Conflict & Prerequisite Check engine | 7 days | 5 | SS (starts with Activity 5) |
| 7 | Develop Admin Dashboard (view registrations, manage courses) | 10 days | 3 | SS (starts with Activity 4) |
| 8 | Develop Email Notification system (confirmation emails) | 4 days | 5 | SS (starts with Activity 5) |
| 9 | Integration testing (all modules together) | 6 days | 5, 6, 7, 8 | FS (after all modules done) |
| 10 | Performance testing (500 concurrent users simulation) | 4 days | 9 | SS (starts with Activity 9) |
| 11 | UAT with 50 real students & Academic Dept staff | 7 days | 10 | FS |
| 12 | Bug fixing & regression testing | 5 days | 11 | FS |

> **Activity Notes:**
> - A6 **SS** A5: Conflict check engine có thể bắt đầu develop song song với Registration module.
> - A7 **SS** A4: Admin Dashboard dev có thể bắt đầu song song với Course Listing.
> - A8 **SS** A5: Email system dev song song với Registration module.
> - A10 **SS** A9: Performance test bắt đầu song song khi Integration test đang chạy phase đầu.

---
---

# **PMG201c - Practical Exam 2 (Fall 2025) – ĐỀ BÀI + ĐÁP ÁN**

**Scenario:** Media địa phương thiếu coverage về sự kiện liên quan cộng đồng trường ĐH. Dự án: lập kênh tin tức số (weekly podcast hoặc video series) tập trung vào niche này. Yêu cầu: ≥1 content/tuần, đạt 500 unique subscribers. Duy trì sản xuất liên tục **3 tháng**. Budget: **$500** (boosting + equipment). Phần mềm: **phải miễn phí hoặc open-source**. Quality: **zero verifiable complaints** về factual inaccuracy; **95% completion rate** (low drop-off).

---

### ✅ Request 1 (20%) – Project Charter Statement

**1. Project Name:** FPT Campus Digital News Channel (CampusVoice)

**2. Justification (Purpose & Reasons):**
Media địa phương và các kênh truyền thông phổ thông hiện không có đủ nội dung phù hợp và kịp thời về các sự kiện trong cộng đồng FPT University (sự kiện campus, thành tựu sinh viên, cơ hội việc làm và nghiên cứu). Dự án CampusVoice được thực hiện nhằm:
- **Lấp đầy khoảng trống thông tin:** Cung cấp nguồn tin tức đáng tin cậy, chuyên sâu về cộng đồng FPT University từ góc nhìn sinh viên.
- **Xây dựng cộng đồng:** Tạo ra nơi tập hợp sinh viên, giảng viên và alumni qua nội dung có giá trị và liên quan.
- **Phát triển kỹ năng thực tế cho sinh viên:** Cho phép sinh viên thực hành journalism, video production, và content marketing trong môi trường thực tế.
- **Tăng nhận diện thương hiệu FPT:** Quảng bá hình ảnh trường ra bên ngoài thông qua nội dung chuyên nghiệp, minh bạch.

**3. Project Constraints:**

| Constraint | Description |
|-----------|-------------|
| **Scope** | Dự án bao gồm: thiết lập và vận hành 1 YouTube channel, 1 podcast feed hàng tuần, 1 newsletter hàng tuần. Nội dung: sự kiện campus, thành tựu nghiên cứu, cơ hội nghề nghiệp. Không bao gồm: live streaming, social media khác (TikTok, Facebook), sản xuất phim dài. |
| **Time** | Chu kỳ sản xuất liên tục phải được duy trì đúng **3 tháng** (12 tuần), xuất bản ít nhất **1 nội dung/tuần**. |
| **Cost/Budget** | Tổng budget: **$500** (chỉ dành cho promotional boosting và thiết bị vật lý). Tất cả phần mềm editing và production **phải hoàn toàn miễn phí hoặc open-source** (VD: DaVinci Resolve, Audacity, OBS, Mailchimp free, Canva free). |
| **Quality** | (1) **Zero verifiable complaints** về factual inaccuracy trong toàn bộ 12 tuần vận hành. (2) **≥95% content completion rate** (khán giả xem/nghe đến hết nội dung – low drop-off rate). |

---

### ✅ Request 2 (20%) – Measurable Project Objectives (≥2)

**Objective 1: Đạt 500 unique subscribers/followers trên nền tảng chính (YouTube channel) vào cuối tuần thứ 12.**

**How it will be measured:**
- **Metric:** YouTube Studio Analytics → "Subscribers" count (unique accounts subscribed).
- **Target value:** ≥ 500 subscribers vào ngày cuối cùng của tháng thứ 3 (cuối tuần 12).
- **Measurement tool:** YouTube Studio dashboard, kiểm tra bởi PM mỗi thứ Sáu hàng tuần.
- **Intermediate milestones để track:**
  - Cuối tuần 4 (tháng 1): ≥ 100 subscribers
  - Cuối tuần 8 (tháng 2): ≥ 300 subscribers
  - Cuối tuần 12 (tháng 3): ≥ 500 subscribers ← **Success criterion**
- **Success = PASS** nếu ≥500 vào deadline. **FAIL** nếu < 400 → cần post-mortem và strategy revision.

---

**Objective 2: Duy trì ≥ 95% content completion rate (tỷ lệ người xem/nghe xong nội dung) trong suốt 12 tuần sản xuất.**

**How it will be measured:**
- **Metric (YouTube):** YouTube Analytics → "Average percentage viewed" per video. Target: ≥ 95% average.
- **Metric (Podcast):** Anchor/Spotify Analytics → "Average listen-through rate". Target: ≥ 95%.
- **Measurement frequency:** Đo sau mỗi episode publish, báo cáo tổng hợp mỗi 4 tuần.
- **Measurement owner:** Technical Editor thu thập số liệu và báo cáo cho PM.
- **Action trigger:** Nếu 2 episodes liên tiếp có completion rate < 90% → Team họp ngay để review nội dung, xem xét rút ngắn độ dài episode hoặc thay đổi format.
- **Success = PASS** nếu average completion rate ≥ 95% trên tổng 12 episodes.

---

### ✅ Request 3 (30%) – RACI Chart

**3 Project Roles:**

| Role | Description |
|------|-------------|
| **PM (Project Manager)** | Lập editorial calendar 12 tuần, quản lý budget $500, theo dõi KPIs hàng tuần (subscribers, completion rate, complaints), phê duyệt content trước publication, escalate vấn đề. |
| **CC (Content Creator / Reporter)** | Nghiên cứu đề tài hàng tuần, phỏng vấn nguồn tin, viết script/kịch bản, soạn bản thảo newsletter. Chịu trách nhiệm tính chính xác thông tin ở bước đầu. |
| **TE (Technical Editor / Producer)** | Fact-check thông tin trước khi publish, edit video (DaVinci Resolve) và audio (Audacity), upload lên YouTube/podcast, quản lý kỹ thuật các nền tảng, theo dõi và báo cáo analytics. |

**RACI Matrix (≥10 tasks):**

| # | Task / Activity / Deliverable | PM | CC | TE |
|---|-------------------------------|----|----|-----|
| 1 | Define 12-week content strategy & editorial calendar | **A** | **R** | C |
| 2 | Set up YouTube channel (banner, description, branding) | **A** | C | **R** |
| 3 | Set up podcast hosting (Anchor/Spotify for Podcasters) | **A** | I | **R** |
| 4 | Set up newsletter platform (Mailchimp free) | **A** | I | **R** |
| 5 | Procure equipment within $500 budget (mic, ring light) | **A** | C | **R** |
| 6 | Research weekly topic & identify credible sources | C | **A/R** | C |
| 7 | Write video/podcast script & newsletter draft | I | **A/R** | C |
| 8 | Record video & audio episode | I | C | **A/R** |
| 9 | Edit video (DaVinci Resolve) & audio (Audacity) | C | I | **A/R** |
| 10 | Fact-check all content (verify all facts & quotes) | **A** | C | **R** |
| 11 | Upload video to YouTube (optimize title, description, tags) | **A** | I | **R** |
| 12 | Distribute podcast episode & send weekly newsletter | **A** | I | **R** |
| 13 | Monitor analytics (subscribers, views, completion rate) & weekly report | **A/R** | I | C |
| 14 | Manage $500 promotional budget (YouTube Ads boosting) | **A** | I | C |

> [!tip]
> ✅ Kiểm tra: Mỗi task có đúng **1 chữ A**. Cả bảng có đủ **R, A, C, I**. ✅

---

### ✅ Request 4 (30%) – Milestones & Activity Sequence

**3 Main Project Milestones:**

| # | Milestone | Deliverable | Target |
|---|-----------|-------------|--------|
| M1 | **Pre-Production Complete** – Toàn bộ setup xong, Episode 1 đã publish | YouTube channel live, Podcast feed active, Newsletter sent, Ep.1 published | End of Week 2 |
| M2 | **Mid-Production Check** – Đạt 300 subscribers, content rhythm ổn định | 8 episodes published, analytics report Month 1-2, 300 subscribers | End of Week 8 |
| M3 | **Project Closeout** – Đạt 500 subscribers, 0 complaints, final report | All 12 episodes published, 500+ subscribers, final analytics report | End of Week 12 |

**Selected Milestone: M1 – Pre-Production Complete (End of Week 2)**

*Lý do chọn:* M1 là milestone quan trọng nhất vì nếu setup sai ngay từ đầu (chọn sai platform, không có branding, thiết bị kém) thì toàn bộ 12 tuần sau đều bị ảnh hưởng.

**≥ 10 Activities & Sequence:**

| # | Activity | Duration | Predecessor | Relationship |
|---|----------|----------|-------------|--------------|
| 1 | Conduct kick-off meeting & assign roles | 1 day | – | – |
| 2 | Define target audience & content pillars (3 pillars: events, research, careers) | 2 days | 1 | FS |
| 3 | Create 12-week editorial calendar (topic per week) | 2 days | 2 | FS |
| 4 | Design channel branding: name, logo, color palette (Canva free) | 2 days | 2 | SS (starts with Activity 3) |
| 5 | Set up YouTube channel (upload banner, write description, add links) | 1 day | 4 | FS |
| 6 | Set up podcast hosting platform (Anchor free) | 1 day | 4 | SS (starts with Activity 5) |
| 7 | Set up newsletter on Mailchimp free (template + subscriber list) | 1 day | 4 | SS (starts with Activity 5) |
| 8 | Procure equipment within budget (USB mic, ring light, webcam) | 3 days | 1 | FS |
| 9 | Install & test free editing software (DaVinci Resolve, Audacity, OBS) | 2 days | 8 | SS (can start while waiting for delivery) |
| 10 | Research & write script for Episode 1 | 3 days | 3 | FS (needs editorial calendar) |
| 11 | Record Episode 1 (video + audio) | 1 day | 8, 9, 10 | FS (need equipment + script ready) |
| 12 | Edit Episode 1: video (DaVinci) + audio (Audacity) | 2 days | 11 | FS |
| 13 | Fact-check Episode 1 content | 1 day | 12 | FS |
| 14 | Publish Episode 1 to YouTube + podcast + send newsletter | 1 day | 5, 6, 7, 13 | FS (platforms ready + content approved) |

**Dependency highlights:**
- A4 **SS** A3: Thiết kế branding bắt đầu ngay khi đang lên editorial calendar (song song).
- A6 **SS** A5: Setup podcast và YouTube bắt đầu cùng thời điểm sau khi có branding.
- A7 **SS** A5: Setup Mailchimp song song với YouTube setup.
- A9 **SS** A8: Cài phần mềm ngay trong lúc đợi thiết bị về.
- A14 **FS** (A5 + A6 + A7 + A13): Chỉ publish khi TẤT CẢ platforms đã sẵn sàng VÀ content đã qua fact-check.

---

*PMG201c – Practical Exam Answers (Real Past Exams) – FPT University*  
*Ghi chú: Đây là đáp án mẫu để học. Trong bài thi thật, hãy tự viết lại theo cách hiểu của bạn và bám sát scenario đề cho!*


Dưới đây là nội dung đề bài được chép lại từ các tệp bạn đã cung cấp (tổng hợp từ phiên bản **Summer 2025** đầy đủ nhất, bao gồm cả yêu cầu về trình tự hoạt động ở Request 4):

---

# **PMG201c - Practical Exam 2 (Summer 2025)**

Select a project from the university training subjects or university activities that you are currently working on, have worked on in the past or a relevant project from your friend/relative that you know, give the solutions or answers for following requests based on your understanding about the project and assumptions.

**Request 1 (20%):** develop a narrative charter statement that includes the following details  
1. Project name,  
2. Project purpose or justification (reasons to implement this project),  
3. High level requirements: this describes in broad terms what you want the project to do or to provide - you need to provide at least two of these.  

**Request 2 (20%):** provide at least five main cost/budget items. Each cost/budget item, you need to provide the following details: name, description, estimation along with the way to estimate (how to estimate, person in charged,…)  

**Request 3 (30%):** develop communication plan for the project where you:  
1. Define at least three project stakeholders (project-internal, organization-internal, external)  
2. Create a communication plan for each of those stakeholders and the communications you believe they should receive. Each communication needs to include the following details: information, purpose, frequency, method or format, responsible.  

**Request 4 (30%):** provide at least three main project milestones that will be used to mark project progress. Select one project milestone that you know the best then determine at least ten activities and determine their sequences with relevant relationships (FS, SS, SF, FF) among them to complete that milestone.

---

**ANALYSIS SHEET**

SECTION 1 (Questions 1-1)

1)

---

Bạn cần tôi hỗ trợ thêm phần trả lời cho các câu hỏi này không?


Dưới đây là nội dung đề bài được chép lại nguyên văn từ tệp `image.png`:

---

# **PMG201c - Practical Exam 2 (Fall 2025)**

The local media lacks coverage of events relevant to the university community. Your project is to establish a digital news channel (e.g., a weekly podcast or video series) focused exclusively on this niche. The project requires producing and distributing at least one high-quality piece of content per week and reaching a milestone of 500 unique subscribers/followers. The continuous production cycle must be maintained for a three-month period. The total budget for promotional boosting and equipment is strictly $500, with the budget constraint that all software used for editing and production must be free or open-source. For quality, the content must maintain a high level of journalistic integrity, defined by receiving zero verifiable complaints of factual inaccuracy and ensuring that 95% of viewers/listeners complete the content (low drop-off rate).

**Request 1 (20%):** develop a narrative charter statement that includes the following details

1. Project name,  
2. Justifications (purpose & reasons to implement this project),  
3. Project constraints, in terms of scope, time, cost/budget, and quality.  

**Request 2 (20%):** define measurable project objectives and related success criteria - list at least two project objectives and explain how each of that objective will be measured.

**Request 3 (30%):** describe the RACI chart where you:

1. Define at least three project roles  
2. List out at least ten tasks, activities, or deliverables.  
3. For each task/activity/deliverable, list out the responsibilities of the project roles.  

**Request 4 (30%):** provide at least three main project milestones that will be used to mark project progress. Select one project milestone that you know the best then determine at least ten activities and determine their sequences with relevant relationships (FS, SS, SF, FF) among them to complete that milestone.