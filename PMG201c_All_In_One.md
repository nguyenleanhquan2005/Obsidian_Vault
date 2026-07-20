# 📘 PMG201c – Project Management (Tài liệu ôn thi tổng hợp)

> [!note]
> This is a consolidated file merging previous separate notes to reduce redundancy. No information was removed.

## 📌 Table of Contents
1. [📚 I. Lý thuyết & Kiến thức nền](#-i-lý-thuyết--kiến-thức-nền)
2. [📝 II. Template đầy đủ (14 Requirements)](#-ii-template-đầy-đủ-14-requirements)
3. [🖥️ III. Đề thi đầy đủ (với đáp án chi tiết)](#-iii-đề-thi-đầy-đủ-với-đáp-án-chi-tiết)
4. [🎯 IV. 5 Đề thực hành (với đáp án)](#-iv-5-đề-thực-hành-với-đáp-án)

---

## 📚 I. Lý thuyết & Kiến thức nền

### 📘 PMG201c – Project Management (Deep Study Note)

> [!info]
> **DE CUONG ON THI CUOI KY**  
> 8 dang de thuong gap: Stakeholders | RACI | SMART | Risk | WBS | Critical Path | EVM

---

### 🚀 1. TONG QUAN - 8 DANG DE THUONG GAP

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

**2.2 Power/Interest Grid - Chien luoc quan ly**

| **Power \ Interest** | **High Interest**                                                                                                                                 | **Low Interest**                                                |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| **High Power**       | (Manage Closely – **Quản lý chặt chẽ):** Ví dụ như Project Sponsor, System Administrators.  cập nhật thường xuyên, tham gia quyết định quan trọng | (Keep Satisfied – Giữ hài lòng: báo cáo ngắn gọn, tránh bất ngờ |
| **Low Power**        | Keep Informed – newsletter, demo, training                                                                                                        | Monitor – theo dõi, ít tương tác                                |

**2.3 RACI Matrix - Cach dien**

| **Ký hiệu**     | **Nghĩa**                                              |
| --------------- | ------------------------------------------------------ |
| R - Responsible | Người thực hiện công việc (có thể nhiều người)         |
| A - Accountable | Người chịu trách nhiệm cuối cùng; mỗi task chỉ 1 người |
| C - Consult     | Người được tham khảo trước khi quyết định              |
| I - Inform      | Người được thông báo kết quả                           |

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

---

### 2.4 RACI cho Dự Án KHÔNG PHẢI PHẦN MỀM

> [!important]
> ❗ **Vấn đề hay gặp:** Khi đề bài KHÔNG phải là app/website (ví dụ: pop-up store, podcast, sự kiện...), nhiều sinh viên không biết task là gì vì không có "Develop module" hay "Deploy system".

---

#### 🧠 Tư duy chìa khóa: Task = CÁC BƯỚC ĐỂ HOÀN THÀNH DỰ ÁN ĐÓ

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

#### 🛒 VÍ DỤ 1: Pop-up Retail Validation (Fall 2025 Exam)

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

#### 🎙️ VÍ DỤ 2: Digital Podcast / Media Channel (Fall 2025 Exam)

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

#### 🎯 CÔNG THỨC TÌM TASK CHO MỌI ĐỀ BÀI

**Bước 1:** Đọc đề, tìm **GÌ** cần làm ra (deliverable) → đó là task thực hiện chính (nhóm ③)

**Bước 2:** Hỏi: *"Trước khi làm ③, cần chuẩn bị gì?"* → nhóm ①②

**Bước 3:** Hỏi: *"Sau khi làm ③, cần kiểm tra/kết thúc gì?"* → nhóm ④⑤

**Bước 4:** Thêm **2 task quản lý** là: `Monitor progress & budget` và `Create final report`

→ **Tổng = 10-12 tasks**, đủ điều kiện! ✅

---

#### 📊 Bảng so sánh Task theo loại đề bài

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

**6.3 Schedule Crashing & Fast Tracking**

| Phuong phap               | Cach lam                                                                            | Tac dong                                           |
| ------------------------- | ----------------------------------------------------------------------------------- | -------------------------------------------------- |
| Crashing (Don nen)        | Them nguon luc (nhan su, overtime) vao task tren Critical Path co duration dai nhat | Rut ngan thoi gian NHUNG TANG chi phi              |
| Fast Tracking (Song song) | Lam song song 2 tasks von FS (task sau bat dau truoc khi task truoc ket thuc)       | Rut ngan thoi gian, KHONG tang budget, tang rui ro |

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

**8. CAC CHU DE KHAC**

**8.1 Types of Organization**

| Đặc điểm              | Functional             | Matrix (Strong)   | Projectized                     |
| --------------------- | ---------------------- | ----------------- | ------------------------------- |
| PM Authority          | Little/None            | Moderate to High  | High to Almost Total            |
| Resource Availability | Little/None            | Moderate to High  | High to Almost Total            |
| Manages Budget        | Functional Manager     | Mixed             | Project Manager                 |
| PM Role               | Part-time              | Full-time         | Full-time                       |
| Tốt khi nào           | Công việc lặp, ổn định | Chia sẻ nguồn lực | Dự án ngắn, scope rõ, cần focus |

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

**8.3 Quality Costs**

| Loại                                  | Ví dụ                                                          |
| ------------------------------------- | -------------------------------------------------------------- |
| Prevention Costs (Phòng ngừa)         | Quality training, coding standards, process documentation      |
| Appraisal Costs (Thẩm định)           | Peer code review, test case development, inspections           |
| Internal Failure (Thất bại nội bộ)    | Rework, scrap - phát hiện TRƯỚC khi release cho khách hàng     |
| External Failure (Thất bại bên ngoài) | Fix bugs sau release, warranty work, lost business - Đắt nhất! |

**8.4 Estimation Techniques**

| Kỹ thuật             | Khi nào dùng                                                             |
| -------------------- | ------------------------------------------------------------------------ |
| Analogous (Tương tự) | Dựa trên dự án tương tự trước đó. Nhanh nhưng ít chính xác.              |
| Parametric (Tham số) | Tính từng đơn vị rồi cộng lại. VD: số giờ x rate. Chính xác hơn.         |
| Bottom-up            | Ước tính từng task nhỏ rồi cộng lên. Chính xác nhất, tốn thời gian nhất. |
| 3-Point (PERT)       | E = (O + 4M + P) / 6. Tính đến cả trường hợp tốt nhất và xấu nhất.       |
| Expert Judgment      | Tin vào ý kiến chuyên gia. Dùng khi thiếu dữ liệu lịch sử                |

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

#### Mẹo ghi nhớ nhanh cho bài thi:

1. **Chữ "S" (Schedule)** luôn đi với **PV**.
2. **Chữ "C" (Cost)** luôn đi với **AC**.
3. **EV** luôn nằm ở **vế trước** trong các công thức tính sai lệch (CV, SV) và chỉ số hiệu suất (CPI, SPI).
4. **Hiệu suất (Index):** Chia. **Sai lệch (Variance):** Trừ.
5. Để tính toán về thời gian, chỉ cần thay biến số chi phí bằng biến số thời gian (ví dụ: EDAC dùng SPI thay vì CPI).

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

### 🧠 QUICK MEMORY ZONE

> [!important]
> 🔥 **Critical Path = tat ca tasks co Float = 0**

> [!important]
> 💰 **CPI < 1 = Over Budget | CPI > 1 = Under Budget**

> [!important]
> ⏱️ **SPI < 1 = Behind Schedule | SPI > 1 = Ahead**

---

### ✅ CHECKLIST BEFORE SUBMISSION

- [ ] Stakeholders >= 5 (internal + external)
- [ ] RACI >= 10 tasks, moi task chi 1 A
- [ ] SMART >= 3 goals, du S-M-A-R-T
- [ ] Risk >= 3 (Probability + Impact + Mitigation + Contingency)
- [ ] WBS dung Level 1-4
- [ ] Deliverables du milestones
- [ ] Network diagram + Critical Path
- [ ] EVM tinh dung CPI, SPI, EAC, ETC

---

### 🧩 STUDY STRATEGY

> [!note]
> - Hoc theo **pattern de** (8 dang)
> - Nho cong thuc EVM truoc (de an diem nhanh)
> - Ve nhanh Critical Path = loi the lon

---

✨ *Optimized for Obsidian – Deep Learning Style*

#### **Topic:** _Should university students be required to participate in environmental protection projects?_

In the present day, the climate crisis has triggered discussions on the role of youth in sustainable development. Some people believe that environmental  participation should be a requirement for all university students during their free time. In my opinion, I strongly agree with this statement. I believe that such a great offers for both benefit. It serves as personal development for students while also generating significant long-term advantages for society.

Firstly, environmental project help student invaluable in hands-on experience. From a management perspective, organizing recycling campaigns or reforestation efforts requires strategic planning and effective communication - soft skills that are highly value for employers . Furthermore, by taking meaningful action, student gain a sense of agency and purpose, leading to a healthier mental state and more impressive portfolio.

Beyond individual gains, the collective impact of student-led environmental work is significant. Students represent a massive demographic of intellectual labor. When mobilized, they increase a nation's social capital. From an economic lens, community-driven initiatives are the most-effective than large scale government projects. Student programs in waste management or urban gardening can reduce costs. More importantly, this policy creates "Green Citizens" who will carry sustainable value into their future careers as leaders and innovators

Critics often argue that students are already overwhelmed with academic pressures. They claim compulsory service infringes upon limited free time. However this overlooks the concept of meaningful leisure. Much free time is currently spent on passive digital consumption, which can lead to burnout. Integrating environmental work into the curriculum perhaps through academic credits. It teaches vital time management skills and social responsibility.

In conclusion, requiring students to participate in environmental is a visionary policy. It bridges the gap between theory and practice, equipping students with life skills while addressing urgent ecological issues. Although it requires administrative planning, the rewards for the individual and the global community far outweigh the challenges. Environmental stewardship should be a fundamental pillar of modern higher education.

#### The Synergy of Human Writing and AI

In the modern days, Artificial Intelligence, such as ChatGPT or Gemini has become more and more 






Dưới đây là bảng tổng hợp và giải thích hệ thống công thức **Earned Value Management (EVM)** dựa trên tài liệu môn học **PMG201c**. Việc nắm vững các nhóm chỉ số này sẽ giúp bạn kiểm soát hoàn toàn tiến độ và chi phí của dự án.

#### 1. Nhóm chỉ số nền tảng (Cái lõi của EVM)

Đây là các giá trị đầu vào để tính toán mọi công thức khác:

- **PV (Planned Value):** Giá trị kế hoạch. Là số tiền đáng lẽ phải chi ra cho công việc dự kiến hoàn thành tính đến thời điểm hiện tại.
- **AC (Actual Cost):** Chi phí thực tế. Số tiền thực tế đã chi ra để làm được khối lượng công việc hiện tại.
- **EV (Earned Value):** Giá trị đạt được. Giá trị của khối lượng công việc thực tế đã hoàn thành, tính theo đơn giá dự tính ban đầu.
- **BAC (Budget at Completion):** Tổng ngân sách dự án. Tổng tất cả các PV của dự án.
- **BDAC (Budgeted Duration at Completion):** Tổng thời gian kế hoạch của dự án.

#### 2. Nhóm chỉ số sai lệch (Dự án đang ở đâu?)

Dùng phép tính **Trừ (-)**. Kết quả **> 0** luôn là tốt.

- **CV (Cost Variance) = EV - AC:** Sai lệch chi phí.
    - _CV > 0:_ Dưới ngân sách (Tốt).
    - _CV < 0:_ Vượt ngân sách (Xấu).
- **SV (Schedule Variance) = EV - PV:** Sai lệch tiến độ.
    - _SV > 0:_ Vượt tiến độ/Nhanh hơn dự kiến (Tốt).
    - _SV < 0:_ Chậm tiến độ (Xấu).
- **VAC (Variance at Completion) = BAC - EAC:** Sai lệch khi hoàn thành. Dự báo khi kết thúc dự án ta sẽ dư hay thiếu bao nhiêu tiền.

#### 3. Nhóm chỉ số hiệu suất (Dự án chạy hiệu quả thế nào?)

Dùng phép tính **Chia (÷)**. Kết quả **> 1** luôn là tốt.

- **CPI (Cost Performance Index) = EV / AC:** Hiệu suất chi phí.
    - _Ví dụ:_ CPI = 1.2 nghĩa là chi 1 đồng nhưng làm ra được 1.2 đồng giá trị.
- **SPI (Schedule Performance Index) = EV / PV:** Hiệu suất tiến độ.
    - _Ví dụ:_ SPI = 0.8 nghĩa là dự án mới chỉ chạy được 80% tốc độ cần thiết.

#### 4. Nhóm chỉ số dự báo (Tương lai sẽ thế nào?)

Dùng để ước tính các con số khi dự án kết thúc:

- **EAC (Estimate at Completion):** Tổng chi phí ước tính khi dự án kết thúc.
    - Công thức phổ biến nhất: **EAC = BAC / CPI**.
- **ETC (Estimate to Complete):** Cần thêm bao nhiêu tiền nữa để hoàn thành phần việc còn lại.
    - **ETC = EAC - AC** hoặc **ETC = (BAC - EV) / CPI**.
- **EDAC (Estimated Duration at Completion):** Tổng thời gian ước tính khi dự án kết thúc.
    - **EDAC = BDAC / SPI**.
- **TCPI (To-Complete Performance Index):** Hiệu suất cần đạt được trong phần việc còn lại để về đích đúng ngân sách.
    - **TCPI = (BAC - EV) / (BAC - AC)**.


### PMG201c – Practical Exam 1 (Fall 2025) – QUESTION + FULL ANSWER

**Scenario:** You have developed a unique, niche consumer product. Your project is to validate its market viability through a temporary pop-up retail operation. Requirements: securing permits, designing and building the display, managing inventory, training student sales staff. Revenue target: **$15,000 gross revenue**. Operation period: **2 consecutive weeks**. Budget (setup + ops, excluding manufacturing cost): **$1,500**. Inventory shrinkage/loss must be kept **< 2%** of total inventory value. Customer satisfaction survey must exceed **> 90% positive**.

---

#### ✅ Request 1 (20%) – Project Charter Statement

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

#### ✅ Request 2 (20%) – Cost/Budget Items (≥5 items, total ≤ $1,500)

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

#### ✅ Request 3 (30%) – Communication Plan

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

#### ✅ Request 4 (30%) – Risk Register (≥3 Risks)

> [!note]
> This exam requires: Risk Title, Description, **Possible Impacts** (scope/quality, time, cost), Mitigation Plan & Contingency Plan.

| # | Risk Name & Description | Impact on Scope/Quality | Impact on Time | Impact on Cost | Mitigation Plan | Contingency Plan |
|---|------------------------|------------------------|----------------|----------------|-----------------|-----------------|
| 1 | **Low Foot Traffic / Sales Underperformance Risk:** The volume of customers visiting the booth is lower than projected, resulting in total revenue falling short of the $15,000 target over the 2-week operation. | **Quality:** Insufficient sales data undermines the statistical validity of the market validation conclusion. | **Time:** Cannot extend the operation period — the venue is booked for a fixed 2-week period only. | **Cost:** Revenue falls below $15,000, producing a negative ROI on the $1,500 investment; the business case for scaling fails. | Select a venue with consistently high foot traffic (weekend peak hours). Launch a marketing campaign at least 1 week before opening: social media posts, flyers distributed across campus. Position the booth near the main entrance of the venue for maximum visibility. | If revenue < $5,000 after Week 1 → PM immediately activates: (1) increased social media advertising using remaining budget, (2) a limited-time flash sale or promotional discount to urgently drive purchases, (3) an escalation report to management to reassess the strategy. |
| 2 | **Inventory Shrinkage Exceeding 2%:** Products are lost, damaged, or stolen, pushing the shrinkage/loss rate above 2% of total inventory value, violating the stated budget constraint. | **Quality:** Violates the <2% shrinkage KPI — constitutes a direct financial quality failure of the project. | **Time:** Requires a partial inventory halt for emergency counting and reconciliation, disrupting sales operations. | **Cost:** Every additional 1% of shrinkage on a $10,000 inventory = $100 in direct losses beyond the allowed threshold. | Implement a mandatory daily inventory count by Sales Staff at the end of each day. Keep high-value products in a locked display case or behind the counter. Install a small portable security camera or ensure merchandise is always within line-of-sight of staff. Require staff to sign a responsibility sheet for the products assigned to their shift. | If shrinkage exceeds 1% after Week 1 → increase surveillance, move sensitive items to a secured back area, and issue an immediate report to management with the updated shrinkage figure and recovery plan. |
| 3 | **Customer Satisfaction Below 90%:** Post-purchase survey results show < 90% positive feedback related to product quality or the retail experience, failing the primary quality KPI. | **Quality:** The most critical quality KPI is failed — the validation may produce a "Do Not Scale" recommendation due to poor customer reception, regardless of sales performance. | **Time:** Complaint investigation and repeat testing require time within the fixed 2-week window, which cannot be extended. | **Cost:** May result in product refunds, exchanges, and potential reputational costs that reduce net revenue. | Conduct intensive staff training on product knowledge and customer service techniques before opening day. Run an internal mystery shopper test on Day 1 to identify service gaps before they affect real customers. Administer satisfaction surveys immediately after each purchase (paper or QR code → Google Form). | If Week 1 survey results show < 85% satisfaction → PM holds an immediate emergency team meeting to diagnose the root cause (product issue? staff behavior? pricing?), and executes corrective actions in Week 2: staff re-training, improved product presentation and signage, or a clearly communicated exchange/return policy. |

---
---

### PMG201c – Practical Exam 2 (Summer 2025) – QUESTION + FULL ANSWER

**Prompt:** Select a project from a university course, campus activity, or a relevant project from someone you know. Answer the following requests based on your understanding and reasonable assumptions.

> [!note]
> **Project Selected:** Building the **FPT University Course Registration System (CRS)** — a web-based platform allowing students to register for courses online, view their timetable, and track their academic records.

---

#### ✅ Request 1 (20%) – Project Charter Statement

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

#### ✅ Request 2 (20%) – Cost/Budget Items (≥5)

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

#### ✅ Request 3 (30%) – Communication Plan

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

#### ✅ Request 4 (30%) – Milestones & Activity Sequence

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

### PMG201c – Practical Exam 2 (Fall 2025) – QUESTION + FULL ANSWER

**Scenario:** Local media lacks adequate coverage of events relevant to the university community. Your project is to establish a digital news channel (e.g., a weekly podcast or video series) focused exclusively on this niche. Requirements: produce and distribute at least one high-quality piece of content per week; reach **500 unique subscribers/followers**. Maintain a continuous production cycle for **3 months**. Total budget for promotional boosting and equipment: **$500**. All editing and production software must be **free or open-source**. Quality standard: **zero verifiable complaints of factual inaccuracy** and a **95% content completion rate** (low drop-off from viewers/listeners).

---

#### ✅ Request 1 (20%) – Project Charter Statement

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

#### ✅ Request 2 (20%) – Measurable Project Objectives (≥2)

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

#### ✅ Request 3 (30%) – RACI Chart

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

#### ✅ Request 4 (30%) – Milestones & Activity Sequence

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

#### ✅ Request 1 (20%) – Project Charter Statement

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

#### ✅ Request 2 (20%) – Cost/Budget Items (≥5 items, total ≤ $1,500)

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

#### ✅ Request 3 (30%) – Communication Plan

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

#### ✅ Request 4 (30%) – Risk Register (≥3 Risks)

> [!note]
> Đề bài yêu cầu: Risk Title, Description, **Possible Impacts** (scope/quality, time, cost), Mitigation & Contingency Plan.

| # | Risk Name & Description | Impact on Scope/Quality | Impact on Time | Impact on Cost | Mitigation Plan | Contingency Plan |
|---|------------------------|------------------------|----------------|----------------|-----------------|-----------------|
| 1 | **Low Foot Traffic / Sales Underperformance:** Lượng khách đến gian hàng thấp hơn dự kiến, dẫn đến doanh thu không đạt $15,000 trong 2 tuần. | **Quality:** Dữ liệu validation không đủ ý nghĩa thống kê → kết luận kém tin cậy. | **Time:** Không thể gia hạn vì venue đã đặt cố định 2 tuần. | **Cost:** Không đạt $15,000 → ROI âm so với $1,500 đã đầu tư. | Chọn địa điểm có lưu lượng người cao (cuối tuần cao điểm). Lên chiến dịch marketing trước 1 tuần: social media, flyers tại trường. Đặt gian hàng gần lối vào chính của venue. | Nếu hết tuần 1 doanh thu < $5,000 → PM kích hoạt: (1) tăng cường quảng cáo social media trong ngân sách còn lại, (2) tổ chức flash sale / giảm giá khuyến mãi đặc biệt, (3) báo cáo ngay cho management để xem xét điều chỉnh strategy. |
| 2 | **Inventory Shrinkage Exceeding 2%:** Hàng hóa bị mất, hư hỏng hoặc bị lấy trộm vượt quá 2% tổng giá trị hàng tồn kho, vi phạm budget constraint. | **Quality:** Vi phạm KPI shrinkage → thất bại về chỉ tiêu chất lượng tài chính. | **Time:** Phải dừng bán một số SKU để kiểm kê, gây gián đoạn hoạt động. | **Cost:** Mỗi % shrinkage thêm = mất thêm tiền hàng. Ví dụ: nếu inventory $10,000 thì 2% = $200 giới hạn. | Thiết lập hệ thống kiểm kê cuối ngày (daily inventory count) với Sales Staff. Lắp camera an ninh nhỏ hoặc đặt hàng trong tầm nhìn nhân viên. Sử dụng display locked case cho hàng có giá trị cao. Nhân viên ký nhận trách nhiệm hàng hóa mỗi ca. | Nếu phát hiện shrinkage vượt 1% sau tuần 1 → tăng cường giám sát, chuyển hàng nhạy cảm vào kho hàng phía sau, và PM báo cáo ngay cho management về tình trạng thực tế. |
| 3 | **Customer Satisfaction Falling Below 90%:** Phản hồi khách hàng qua survey cho thấy < 90% positive về chất lượng sản phẩm hoặc trải nghiệm mua sắm. | **Quality:** Không đạt KPI chính về satisfaction → dự án fail về mục tiêu validation. Kết quả có thể khuyên nghị ngược lại (không nên expand). | **Time:** Cần thêm thời gian xử lý khiếu nại và re-test – nhưng dự án chỉ có 2 tuần cố định. | **Cost:** Có thể phải refund hoặc exchange hàng, tăng chi phí phát sinh. | Huấn luyện nhân viên kỹ về product knowledge và customer service trước khi khai trương. Thực hiện mystery shopper test trong ngày đầu để phát hiện gap. Thiết lập quick feedback loop: thu thập survey ngay sau mỗi giao dịch (paper or QR code). | Nếu survey kết quả tuần 1 < 85% → PM ngay lập tức họp team, xác định nguyên nhân cụ thể (sản phẩm? nhân viên? giá?), thực hiện corrective action trong tuần 2: huấn luyện lại nhân viên, adjust product presentation, hoặc offer exchange policy rõ ràng hơn. |

---
---

### **PMG201c - Practical Exam 2 (Summer 2025) – ĐỀ BÀI + ĐÁP ÁN**

**Đề bài:** Chọn một dự án từ môn học tại trường ĐH hoặc hoạt động trường ĐH mà bạn đang/đã tham gia (hoặc của bạn bè/người thân). Trả lời các câu hỏi dựa trên hiểu biết và giả định của bạn.

> [!note]
> **Dự án được chọn:** Xây dựng **Hệ thống Quản lý Học phần (Course Registration System)** cho FPT University – một hệ thống web cho phép sinh viên đăng ký môn học online, xem thời khóa biểu và theo dõi kết quả học tập.

---

#### ✅ Request 1 (20%) – Project Charter Statement

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

#### ✅ Request 2 (20%) – Cost/Budget Items (≥5)

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

#### ✅ Request 3 (30%) – Communication Plan

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

#### ✅ Request 4 (30%) – Milestones & Activity Sequence

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

### **PMG201c - Practical Exam 2 (Fall 2025) – ĐỀ BÀI + ĐÁP ÁN**

**Scenario:** Media địa phương thiếu coverage về sự kiện liên quan cộng đồng trường ĐH. Dự án: lập kênh tin tức số (weekly podcast hoặc video series) tập trung vào niche này. Yêu cầu: ≥1 content/tuần, đạt 500 unique subscribers. Duy trì sản xuất liên tục **3 tháng**. Budget: **$500** (boosting + equipment). Phần mềm: **phải miễn phí hoặc open-source**. Quality: **zero verifiable complaints** về factual inaccuracy; **95% completion rate** (low drop-off).

---

#### ✅ Request 1 (20%) – Project Charter Statement

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

#### ✅ Request 2 (20%) – Measurable Project Objectives (≥2)

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

#### ✅ Request 3 (30%) – RACI Chart

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

#### ✅ Request 4 (30%) – Milestones & Activity Sequence

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

### **PMG201c - Practical Exam 2 (Summer 2025)**

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

### **PMG201c - Practical Exam 2 (Fall 2025)**

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

---

## 📝 II. Template đầy đủ (14 Requirements)

### 📋 PMG201c – SỞ DÀN Ý & TEMPLATE ĐẦY ĐỦ (14 REQUIREMENTS)
### Fill-in-the-blank cho mọi đề IT và Non-IT

> [!important]
> **Cách dùng:** Đọc đề → highlight thông tin → điền vào `[...]`
> Chỗ có `* Tip:` là gợi ý cách nghĩ, **KHÔNG chép vào bài thi**
> Chỗ có `* IT:` / `* Non-IT:` = gợi ý riêng cho từng loại đề

---

### ⚡ BƯỚC ĐẦU TIÊN: ĐỌC ĐỀ VÀ TÁCH 5 NHÓM THÔNG TIN

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

### 1️⃣ PROJECT CHARTER

### 🧠 Nguyên tắc vàng: Bạn TỰ SÁNG TẠO có căn cứ

```
❌ Suy nghĩ sai: "Đề không nói thì mình không biết, không viết được"
✅ Suy nghĩ đúng: "Đề cho scenario → mình đóng vai PM →
                   tự đặt chi tiết HỢP LÝ dựa trên thực tế"
```

---

### 🧩 BƯỚC 2: HỎI 5 CÂU NÀY TRƯỚC KHI VIẾT

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

### 🖥️ TEMPLATE A – DỰ ÁN IT / APP / SOFTWARE

#### 🔍 Cách đọc đề IT nhanh:
- Đề nói "build / develop / create" → đây là dự án làm ra sản phẩm phần mềm
- Tìm: ai dùng? (students, customers, staff) → đó là End User
- Tìm: làm được gì? (submit, track, pay, communicate) → High-Level Requirements
- Nếu đề nói "mobile app" → tự thêm: iOS + Android, offline mode, app store submission

#### ✏️ Fill-in Template:

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

### 🌿 TEMPLATE B – DỰ ÁN NON-IT (EVENT / CONSTRUCTION / SERVICE)

#### 🔍 Cách đọc đề Non-IT nhanh:
- Đề nói "organize / plan / set up / establish / build" một thứ vật lý hoặc sự kiện
- Tìm: ai tham gia? (participants, visitors, customers) → End User
- Tìm: mục tiêu số học? (100 people, $30,000 revenue, 90% satisfaction) → Success Metrics
- Tìm: điều kiện đặc biệt? (permits, weather, safety, compliance) → Constraints/Risks

#### ✏️ Fill-in Template:

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

### 📌 BẢNG TRA NHANH: "ĐỀ NÓI GÌ → CHARTER VIẾT GÌ"

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

### 🎓 VÍ DỤ ÁP DỤNG VỚI ĐỀ THẬT

#### Đề gốc (Practical Exam – Fall 2025):
> *"You have developed a unique consumer product. Your project is to validate market viability through a temporary pop-up retail operation. Requires securing permits, designing display, managing inventory, training student sales staff, achieving $15,000 gross revenue. Operation must run for two consecutive weeks. Setup costs limited to $1,500. Inventory shrinkage below 2%. Customer satisfaction must exceed 90% positive feedback."*

#### Áp dụng từng bước:

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

### 2️⃣ WBS (Work Breakdown Structure)

#### 🧠 Hiểu đúng: Cây phân rã công việc, bắt buộc đến Level 3
```
Level 1 = Tên project
Level 2 = Các PHASE (luôn đủ 5: Initiating / Planning / Executing / M&C / Closing)
Level 3 = Tasks trong mỗi phase
Level 4 = Sub-tasks (càng chi tiết càng tốt điểm)
```

#### ✏️ TEMPLATE:

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

### 3️⃣ DELIVERABLES & MILESTONES

#### 🧠 Hiểu đúng:
```
Milestone  = Cột mốc quan trọng (checkpoint)
Deliverable = Sản phẩm bàn giao tại mốc đó
Completion Criteria = Điều kiện để coi milestone là "xong" (ai ký? tỉ lệ bao nhiêu?)
Luôn có: Initiating → Planning → [Mid milestone] → Pre-launch/Pre-event → Closing
```

#### ✏️ TEMPLATE:

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

### 4️⃣ RACI MATRIX

#### 🧠 Quy tắc bắt buộc:
```
✅ Mỗi task có đúng 1 chữ A (không được 2 A)
✅ Mỗi task có ít nhất 1 chữ R
✅ Dùng đủ cả 4 ký hiệu R / A / C / I
✅ Ít nhất 10 tasks
```

#### ✏️ XÁC ĐỊNH ROLES TRƯỚC:
```
IT Roles:     PM | BA | Dev | QA | PO (Product Owner)
Non-IT Roles: PM | Coordinator | Marketing | [Domain expert] | Sponsor rep

* PM thường A hoặc C, hiếm khi R (PM quản lý, không làm trực tiếp)
* PO/Sponsor thường A ở tasks liên quan yêu cầu, C hoặc I ở kỹ thuật
```

#### ✏️ TEMPLATE:

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

### 5️⃣ SMART GOALS

#### 🧠 Quy tắc:
```
Phân tích RIÊNG TỪNG TIÊU CHÍ S-M-A-R-T, KHÔNG gộp chung
Ít nhất 3 goals, liên quan 3 khía cạnh: User / Quality / Business/Revenue
```

#### ✏️ TEMPLATE (lặp lại cho mỗi goal):

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

### 6️⃣ RISK MANAGEMENT

#### 🧠 Phân biệt:
```
Mitigation  = Làm TRƯỚC khi rủi ro xảy ra → giảm khả năng / tác động
Contingency = Làm SAU khi rủi ro đã xảy ra → khắc phục hậu quả

Ít nhất 3 risks, mỗi risk 1 domain:
  Risk 1: Về chi phí / ngân sách
  Risk 2: Về tiến độ / nhân sự
  Risk 3: Về kỹ thuật / logistics / bên ngoài
```

#### ✏️ TEMPLATE:

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

### 7️⃣ STAKEHOLDERS & ROLES

#### 📊 Power/Interest Grid (thuộc lòng):
```
              HIGH INTEREST         LOW INTEREST
HIGH POWER  | Manage Closely   |  Keep Satisfied  |
LOW POWER   | Keep Informed    |  Monitor         |
```

#### ✏️ TEMPLATE:

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

### 8️⃣ USER STORIES

#### 🧠 Format chuẩn:
```
"As a [role], I want [feature/action] so that [benefit/reason]."
+ ≥ 2 Acceptance Criteria (AC): điều kiện để story là "done"
  AC hay bắt đầu bằng: "The system displays..." / "User receives..." / "The [feature] allows..."
```

#### ✏️ TEMPLATE (lặp lại cho mỗi story):

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

### 9️⃣ ORGANIZATIONAL STRUCTURE

#### 🧠 Chọn 1 trong 3 và GIẢI THÍCH tại sao PHÙ HỢP với project này:
```
Functional   → Công việc routine, ổn định, nhân viên thuộc phòng ban cố định
Matrix       → Dự án cần chia sẻ nguồn lực từ nhiều phòng ban
Projectized  → Dự án ngắn hạn, scope rõ, PM cần toàn quyền
```

#### ✏️ TEMPLATE:

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

### 🔟 COMMUNICATION PLAN

#### 🧠 Cần đủ 5 cột:
```
Information | Purpose | Frequency | Method/Format | Responsible
Luôn có: Internal (PM ↔ team) | Executive (PM → Sponsor) | External (PM → End users)
```

#### ✏️ TEMPLATE:

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

### 1️⃣1️⃣ GANTT CHART

#### 🧠 Trong bài thi viết tay:
```
Vẽ bảng: cột = tuần/tháng | hàng = activities
Điền ██ hoặc X vào ô tương ứng
"Monitoring & Control" kéo suốt dự án
```

#### ✏️ TEMPLATE:

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

### 1️⃣2️⃣ CRITICAL PATH ⭐ PHẢI LẤY TRỌN ĐIỂM

#### 📐 CÔNG THỨC (thuộc lòng):

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

#### ✏️ TEMPLATE GIẢI (4 bước):

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

### 1️⃣3️⃣ EVM ⭐ PHẢI LẤY TRỌN ĐIỂM

#### 📐 TOÀN BỘ CÔNG THỨC:

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

#### ✏️ TEMPLATE GIẢI:

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

### 1️⃣4️⃣ QA/QC PLAN

#### 🧠 4 loại chi phí chất lượng:
```
Prevention  = Đầu tư TRƯỚC để tránh lỗi (training, standards, process docs)
Appraisal   = Kiểm tra TRONG khi làm (review, testing, audit)
Int. Failure = Lỗi phát hiện TRƯỚC bàn giao (rework, bug fix pre-launch)
Ext. Failure = Lỗi SAU bàn giao (warranty, hotfix, complaint) ← TỐN NHẤT, tránh tối đa
```

#### ✏️ TEMPLATE:

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

### 🚀 QUICK REFERENCE: ĐỀ NÓI GÌ → VIẾT GÌ Ở ĐÂU

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


---

## 🖥️ III. Đề thi đầy đủ (với đáp án chi tiết)

### 📘 PMG201c – 2 FULL PRACTICE EXAMS (14 Requirements Each)
### With Step-by-Step Guidance & Complete Model Answers

> [!important]
> These two exams cover **all 14 topic areas** examined in PMG201c.
> **Critical Path** and **EVM** sections include fully worked numerical solutions.
> Scoring guide per section is indicated. Total = 100 points each exam.

---

### 🖥️ EXAM 1 – IT / APP TOPIC
### Project: "FPT EduGo" – University Mobile E-Learning App

**Scenario:**
FPT University wants to develop a mobile application called **"FPT EduGo"** to improve the learning experience for students. The app allows students to access lecture videos, submit assignments, take online quizzes, track their academic progress, and communicate with instructors via in-app messaging. The app must be available on both iOS and Android platforms.

**Key constraints:**
- **Duration:** 6 months (24 weeks)
- **Budget (BAC):** $80,000
- **Quality:** Minimum 4.0/5.0 star rating on app stores within the first 3 months; 99% uptime; response time < 2 seconds
- **Scope:** Mobile app only (iOS + Android); excludes web version in this phase

---

### ✅ REQUIREMENT 1 – PROJECT CHARTER (5 pts)

#### 📋 What to write:
A Project Charter is the formal document that **authorizes the project**. It must include: project name, purpose/justification, high-level requirements, constraints, assumptions, and key stakeholders.

#### 🧭 Guidance:
- Keep it narrative (paragraph + bullet), not just a list
- Justification = WHY the project exists (problem it solves)
- Constraints = time, cost, scope, quality limits
- Assumptions = things you assume to be true without proof

#### ✅ Model Answer:

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

### ✅ REQUIREMENT 2 – WBS (Work Breakdown Structure) (8 pts)

#### 📋 What to write:
A hierarchical decomposition of all project work. Must reach Level 3 minimum (Level 4 preferred).

#### 🧭 Guidance:
- Level 1 = Project Name
- Level 2 = Phases (Initiating, Planning, Executing, Monitoring & Controlling, Closing)
- Level 3 = Major tasks per phase
- Level 4 = Sub-tasks (specific, assignable units of work)

#### ✅ Model Answer:

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

### ✅ REQUIREMENT 3 – DELIVERABLES & MILESTONES (5 pts)

#### 📋 What to write:
Identify key milestones (major checkpoints) and the deliverables produced at each. Include completion criteria.

#### ✅ Model Answer:

| # | Milestone | Deliverables | Completion Criteria |
|---|-----------|--------------|---------------------|
| 1 | Project Initiated (Week 1) | Approved Project Charter, Stakeholder Register, Kick-off minutes | Charter signed by Sponsor; all key stakeholders identified |
| 2 | Planning Complete (Week 3) | Project Management Plan (all sub-plans) | PMP reviewed & approved by sponsor; team briefed |
| 3 | Design Approved (Week 8) | SRS document, System architecture, UI/UX wireframes, DB schema | Product Owner approves design; no open critical issues |
| 4 | Development Complete (Week 18) | Functional backend APIs, iOS & Android app builds | All modules developed; code reviewed & merged to main branch |
| 5 | UAT Passed (Week 22) | UAT report, bug-fix log, performance test report | 95% of test cases pass; 0 critical/high-severity bugs open |
| 6 | Project Closed (Week 24) | Live app on stores, final report, lessons learned | App published; sign-off from all stakeholders |

---

### ✅ REQUIREMENT 4 – RACI MATRIX (8 pts)

#### 📋 What to write:
A responsibility assignment matrix with ≥ 10 tasks. Roles: PM, BA, Dev, QA, PO.

#### 🧭 Guidance:
- Each task: exactly **1 A** (accountable)
- Each task: at least **1 R** (responsible, does the work)
- C = consulted before decisions; I = informed of outcome

#### ✅ Model Answer:

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

### ✅ REQUIREMENT 5 – SMART GOALS (8 pts)

#### 📋 What to write:
Write 3 SMART goals. Each must have all 5 criteria (S, M, A, R, T) analyzed individually.

#### ✅ Model Answer:

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

### ✅ REQUIREMENT 6 – RISK MANAGEMENT (8 pts)

#### ✅ Model Answer:

| # | Risk Name | Description | Probability | Impact | Mitigation Plan | Contingency Plan |
|---|-----------|-------------|-------------|--------|-----------------|------------------|
| 1 | API Integration Delay | FPT IT department delays providing LMS API access past Week 2 | Medium | High | Formally request API access in Week 1 with signed SLA; assign BA as liaison | Use mock APIs for development; negotiate extended timeline with sponsor |
| 2 | Key Developer Resignation | Lead developer leaves mid-project, causing knowledge loss | Low | High | Document all code with wikis; conduct weekly knowledge-sharing sessions | Cross-train backup developer; hire freelancer via Upwork with 1-week onboarding |
| 3 | App Store Rejection | Apple or Google rejects app submission due to policy violations | Low | High | Review App Store guidelines before development starts; conduct compliance checklist in QA phase | Revise submission based on rejection reasons; allocate 1-week buffer at end of schedule |
| 4 | Scope Creep | Stakeholders request additional features (web version, AI tutor) mid-project | High | Medium | Implement formal change request process from Week 1; PM must approve all scope changes | Defer new features to Phase 2; document them in Product Backlog |
| 5 | Performance Issues Under Load | App crashes when >500 users login simultaneously | Medium | High | Conduct load testing in Week 21 using JMeter; design for horizontal scaling on AWS | Activate auto-scaling groups on AWS; schedule off-peak maintenance window |

---

### ✅ REQUIREMENT 7 – STAKEHOLDERS & ROLES (5 pts)

#### 📋 What to write:
Identify ≥ 5 stakeholders. Include: role, type (internal/external), Power/Interest position, management strategy.

#### ✅ Model Answer:

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

### ✅ REQUIREMENT 8 – USER STORIES (8 pts)

#### 📋 What to write:
At least 5 User Stories in the format: **"As a [role], I want [feature] so that [benefit]."**
Each story needs ≥ 2 Acceptance Criteria.

#### ✅ Model Answer:

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

### ✅ REQUIREMENT 9 – ORGANIZATIONAL STRUCTURE (3 pts)

#### 📋 What to write:
Choose and justify the organizational structure type (Functional / Matrix / Projectized).

#### ✅ Model Answer:

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

### ✅ REQUIREMENT 10 – COMMUNICATION PLAN (8 pts)

#### ✅ Model Answer:

| Stakeholder | Information | Purpose | Frequency | Method/Format | Responsible |
|-------------|-------------|---------|-----------|---------------|-------------|
| University Dean (Sponsor) | Project status, budget vs. actual, milestones achieved | Maintain executive awareness & decision support | Bi-weekly | Formal PDF status report + 30-min meeting | PM |
| Development Team | Sprint goals, task assignments, blockers | Coordinate daily work, remove impediments | Daily | Standup meeting (15 min) via Google Meet + Jira updates | Scrum Master / PM |
| Business Analyst | Requirements updates, design change requests | Ensure alignment between requirements and development | Weekly | Sprint review + shared Google Docs | PM |
| QA Team | Test results, bug reports, UAT schedule | Track quality metrics, assign bug fixes | Weekly | Jira bug tracker + weekly QA report | QA Lead |
| Students (Beta Testers) | App download link, feedback forms, issue reporting | Collect real-user feedback pre-launch | Once (UAT phase, Week 20–22) | Email + in-app feedback form | BA |
| FPT IT Department | API access requests, infrastructure specs | Coordinate technical integrations | As needed | Email + technical documentation | Dev Lead |

---

### ✅ REQUIREMENT 11 – GANTT CHART (5 pts)

#### 📋 What to write:
Show all main activities on a timeline. In markdown, use a table with weeks.

#### ✅ Model Answer:

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

### ✅ REQUIREMENT 12 – CRITICAL PATH METHOD (15 pts) ⭐ MUST SCORE FULL MARKS

#### 📋 What to write:
Given a network diagram, calculate ES, EF, LS, LF, Float for all activities. Identify the Critical Path and total project duration.

#### 🔢 Network Diagram (Activity-on-Node):

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

#### 🧭 Step-by-Step Guidance:

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

#### ✅ Model Answer:

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

### ✅ REQUIREMENT 13 – EVM (Earned Value Management) (15 pts) ⭐ MUST SCORE FULL MARKS

#### 🔢 Given Data:
- **BAC** (Budget at Completion) = **$80,000**
- **BDAC** (Planned Duration) = **24 weeks**
- **Status Date:** End of Week **10**
- **AC** (Actual Cost at Week 10) = **$38,000**
- **% Work Completed** = **45%**

#### 🧭 Step-by-Step Guidance:

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

#### ✅ Model Answer:

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

### ✅ REQUIREMENT 14 – QA/QC PLAN (5 pts)

#### 📋 What to write:
Describe the quality management approach including prevention, appraisal, and failure costs + specific QA activities.

#### ✅ Model Answer:

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

### 🌽 EXAM 2 – NON-IT TOPIC
### Project: "City Marathon 2026" – Annual 10K City Running Event

**Scenario:**
The City Sports Department wants to organize the **"City Marathon 2026"** — an annual running event open to all citizens. The event features a **10K race** and **5K fun run**, targeting **2,000 registered participants**. The event will be held on a single day (Race Day). The project involves securing city permits, attracting corporate sponsors, marketing the event, recruiting volunteers, procuring equipment and medals, setting up a medical safety team, and managing event-day operations.

**Key constraints:**
- **Duration:** 8 months of planning (32 weeks); Race Day = end of Week 32
- **Budget (BAC):** $150,000
- **Quality:** ≥ 90% participant satisfaction score; 0 serious medical incidents; 95% content completion by viewers/listeners (for online streaming)
- **Scope:** Physical race event + live social media stream; excludes any virtual/remote participation mode

---

### ✅ REQUIREMENT 1 – PROJECT CHARTER (5 pts)

#### ✅ Model Answer:

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

### ✅ REQUIREMENT 2 – WBS (8 pts)

#### ✅ Model Answer:

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

### ✅ REQUIREMENT 3 – DELIVERABLES & MILESTONES (5 pts)

#### ✅ Model Answer:

| # | Milestone | Deliverables | Completion Criteria |
|---|-----------|--------------|---------------------|
| 1 | Project Initiated (Week 2) | Approved Project Charter, Stakeholder Register | Charter signed by City Sports Director |
| 2 | City Permits Secured (Week 6) | Signed traffic permit, police coordination agreement, road closure plan | All required permits received from city government |
| 3 | Sponsorship Closed (Week 12) | ≥ 5 signed sponsorship agreements; at least $40,000 sponsor income confirmed | All agreements signed; invoices issued |
| 4 | Registration & Marketing Complete (Week 20) | 2,000 registered participants; completed marketing campaign | Registration target met; all bibs & race kits dispatched |
| 5 | Logistics Ready (Week 28) | Medals, timing chips, tents, restrooms, medical teams, volunteers all confirmed | Race-day readiness checklist 100% complete |
| 6 | Event Complete & Project Closed (Week 34) | Post-race satisfaction survey report, final budget report, lessons learned | Survey score ≥ 90%; all payments settled; archive complete |

---

### ✅ REQUIREMENT 4 – RACI MATRIX (8 pts)

#### ✅ Model Answer:

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

### ✅ REQUIREMENT 5 – SMART GOALS (8 pts)

#### ✅ Model Answer:

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

### ✅ REQUIREMENT 6 – RISK MANAGEMENT (8 pts)

#### ✅ Model Answer:

| # | Risk Name | Description | Probability | Impact | Mitigation Plan | Contingency Plan |
|---|-----------|-------------|-------------|--------|-----------------|------------------|
| 1 | Permit Rejection / Delay | City government delays or denies traffic permit for the race route | Medium | High | Submit permit applications in Week 2 (12 weeks before needed); engage city sports liaison officer early | Propose an alternative route with shorter road closure; negotiate a revised event date |
| 2 | Insufficient Participant Registration | Registration falls below 2,000 by Week 18 | Medium | High | Launch Early Bird discount pricing; run targeted social media ads; partner with running clubs and gyms | Add a corporate team relay category; offer last-minute group discounts to companies |
| 3 | Sponsor Withdrawal | A major sponsor cancels their deal after signing | Low | High | Include penalty clauses in sponsorship contracts; secure 2 backup sponsors in pipeline | Activate backup sponsors immediately; reduce non-critical event expenses (e.g., smaller prize pool) |
| 4 | Bad Weather on Race Day | Heavy rain, extreme heat, or storm creates safety hazard | Medium | High | Include weather clause in city permit; monitor weather forecasts from Week 30; develop rain contingency plan | Delay race start by 2 hours; activate indoor shelter points along route; issue refunds if force majeure declared |
| 5 | Medical Emergency During Race | Participant suffers cardiac arrest or serious injury | Low | Very High | Station AED devices and trained paramedics every 2km; all volunteers trained in basic first aid | Full emergency response protocol activated; ambulance on standby; direct hospital coordination |

---

### ✅ REQUIREMENT 7 – STAKEHOLDERS & ROLES (5 pts)

#### ✅ Model Answer:

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

### ✅ REQUIREMENT 8 – USER STORIES (8 pts)

#### ✅ Model Answer:

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

### ✅ REQUIREMENT 9 – ORGANIZATIONAL STRUCTURE (3 pts)

#### ✅ Model Answer:

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

### ✅ REQUIREMENT 10 – COMMUNICATION PLAN (8 pts)

#### ✅ Model Answer:

| Stakeholder | Information | Purpose | Frequency | Method/Format | Responsible |
|-------------|-------------|---------|-----------|---------------|-------------|
| City Sports Director | Budget status, milestone completion, risk flags | Executive oversight & approval of key decisions | Monthly | Formal PDF report + 30-min briefing | PM |
| Corporate Sponsors | Brand placement updates, registration count, event media coverage preview | Maintain sponsor confidence & relationship | Bi-weekly | Email brief + sponsor portal dashboard | Sponsor Relations Officer |
| Registered Participants | Race schedule, route map, weather updates, bib numbers | Keep participants informed and engaged | Weekly (from Week 20 onward) | Email newsletter + Facebook/Instagram updates | Marketing Team |
| Volunteers | Training schedule, role assignments, race day reporting points | Coordinate Race Day volunteer operations | Bi-weekly (from Week 18); daily in Race Week | WhatsApp group + printed briefing packs | Volunteer Coordinator |
| Police & Traffic Authority | Road closure timeline, emergency contact list, route layout | Ensure legal compliance and safety coordination | Monthly + 1 week before Race Day | Formal meetings + shared documentation | PM + WC |
| Local Media | Press releases, event highlights, interview scheduling | Drive public awareness and media coverage | At key milestones (launch, Week 20, Race Week) | Press releases via email; press conference in Race Week | Marketing Team |

---

### ✅ REQUIREMENT 11 – GANTT CHART (5 pts)

#### ✅ Model Answer:

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

### ✅ REQUIREMENT 12 – CRITICAL PATH METHOD (15 pts) ⭐ MUST SCORE FULL MARKS

#### 🔢 Network Diagram:

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

#### ✅ FORWARD PASS:

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

#### ✅ BACKWARD PASS:

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

#### ✅ FULL TABLE WITH FLOAT:

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

### ✅ REQUIREMENT 13 – EVM (Earned Value Management) (15 pts) ⭐ MUST SCORE FULL MARKS

#### 🔢 Given Data:
- **BAC** = **$150,000**
- **BDAC** = **32 weeks**
- **Status Date:** End of Week **12**
- **AC** (Actual Cost at Week 12) = **$65,000**
- **% Work Completed** = **38%**

#### ✅ Model Answer:

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

### ✅ REQUIREMENT 14 – QA/QC PLAN (5 pts)

#### ✅ Model Answer:

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


---

## 🎯 IV. 5 Đề thực hành (với đáp án)

### 📝 PMG201c – ANSWER KEY (All 5 Practice Exam Sets)

> [!important]
> ❗ This is a reference answer for study purposes. In your real exam, always rephrase in your own words and stay closely tied to the specific scenario given!

---

### 🏫 EXAM 1 – STUDENT CLUB MANAGEMENT SYSTEM – ANSWERS

**Scenario Summary:** Build an online Club Management System (CMS) for FPT University | 4 months | $12,000 | ≥200 active student users in Month 1 | System uptime ≥99.5% | Response time <2s

---

#### Request 1 (20%) – Stakeholders

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

#### Request 2 (20%) – RACI Matrix

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

#### Request 3 (30%) – 3 SMART Goals

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

#### Request 4 (30%) – Risk Register

| # | Risk Name & Description | Probability | Impact | Mitigation Plan | Contingency Plan |
|---|------------------------|-------------|--------|-----------------|-----------------|
| 1 | **Low User Adoption Risk:** Students are unaware of or uninterested in the new CMS, resulting in fewer than 200 active users in the first month. | Medium | High | Partner with club administrators and the IT Portal team to promote the system at least 2 weeks before launch. Conduct demo/workshop sessions for Club Admins prior to go-live. | If fewer than 100 users are active after the first 2 weeks → PM triggers an emergency email blast to all students and negotiates a 2-week target extension with the Sponsor. |
| 2 | **Technical Performance Risk:** The system fails to meet uptime ≥99.5% or response time <2s due to server overload or unoptimized code. | Medium | High | Conduct load testing from Week 10 of the project using 300 VUs (50% above target). Implement a Redis caching layer. Select a cloud provider with an SLA of ≥99.9%. | If downtime occurs → switch to backup server immediately. PM notifies the Sponsor within 1 hour. Dev team hotfixes within 4 hours. |
| 3 | **Budget Overrun Risk:** Development and infrastructure costs exceed $12,000 due to scope creep or inaccurate labor estimates. | Low | High | Build a detailed budget breakdown from Day 1 with a 10% contingency reserve ($1,200). Enforce a formal Change Control Process: all scope changes require PM + Sponsor approval before implementation. Track EVM weekly. | If costs exceed budget by >10% → PM calls an emergency meeting with the Sponsor to cut scope (e.g., defer advanced reporting module to Phase 2) or request a budget increase. |
| 4 | **Key Staff Departure Risk:** A lead developer or BA resigns or is reassigned during the project, disrupting schedule and knowledge continuity. | Low | High | Enforce regular knowledge sharing and documentation. Every module must have at least 2 developers who understand how to maintain it (no single point of failure). | If it occurs → PM immediately escalates to the Sponsor to request a replacement resource. Uses the 2-week contingency buffer built into the schedule to absorb the impact. |

---
---

### 📱 EXAM 2 – FOOD DELIVERY APP FOR CAMPUS – ANSWERS

**Scenario Summary:** Campus Food Delivery App (CampusEats) | 6 months | $20,000 | $30,000 revenue target in first 6 months of operation | User satisfaction ≥85%

---

#### Request 1 (20%) – Project Charter Statement

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

#### Request 2 (20%) – Cost/Budget Items

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

#### Request 3 (30%) – Communication Plan

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

#### Request 4 (30%) – Milestones & Activity Sequence

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

### 🏥 EXAM 3 – ONLINE HEALTH TRACKING PLATFORM – ANSWERS

**Scenario Summary:** HealthTrack Pro – daily health data logging + AI recommendations + sharing with doctors | 8 months | $50,000 | HIPAA compliant | 500 active users in first 3 months post-launch

---

#### Request 1 (20%) – Stakeholders

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

#### Request 2 (20%) – 3 SMART Goals

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

#### Request 3 (30%) – Work Breakdown Structure (WBS)

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

#### Request 4 (30%) – Network Diagram Calculation

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

### 🎬 EXAM 4 – UNIVERSITY DIGITAL MEDIA CHANNEL – ANSWERS

**Scenario Summary:** FPT University Digital Media Channel (YouTube + Podcast + Newsletter) | 3 months | $500 (equipment & boosting only) | All software must be free/open-source | Target: 500 YouTube subscribers | Zero factual inaccuracy complaints

---

#### Request 1 (20%) – Project Charter Statement

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

#### Request 2 (20%) – Measurable Project Objectives

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

#### Request 3 (30%) – RACI Chart

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

#### Request 4 (30%) – Milestones & Activity Sequence

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

### 💰 EXAM 5 – EVM COMPREHENSIVE SCENARIO – ANSWERS

**Given:** BAC = $120,000 | BDAC = 12 months | Evaluation at Month 6 | AC = $55,000 | Actual % complete = 40%

---

#### Request 1 (20%) – EVM Calculations

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

#### Request 2 (20%) – Overall Assessment & Corrective Actions

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

#### Request 3 (30%) – Risk Register

| # | Risk Name & Description | Probability | Impact | Mitigation Plan | Contingency Plan |
|---|------------------------|-------------|--------|-----------------|------------------|
| 1 | **Scope Creep Risk:** Stakeholders continuously add new requirements or change existing ones outside the agreed scope baseline, causing the team to spend time and money that doesn't register as project progress in the EVM. This is the most common cause of a negative CV. | Medium | High | Enforce a **Formal Change Control Process** from Day 1: all scope changes must be documented, impact-assessed (cost and schedule), and approved by both PM and Sponsor before implementation. Conduct bi-weekly scope review meetings with the Sponsor. | If scope creep has already occurred → PM collects all undocumented changes, quantifies the additional cost and schedule impact, and submits a formal Change Request for Sponsor approval to either increase the BAC or remove an equivalent amount of existing scope. |
| 2 | **Technical Rework / Inefficiency Risk:** The development team encounters unanticipated technical problems (e.g., wrong architecture choice, high technical debt), requiring significant rework. This causes Actual Cost (AC) to rise without a corresponding increase in Earned Value (EV). | Medium | High | Conduct **technical spikes and proof-of-concept** for complex modules before committing to full development. Enforce mandatory code reviews before merging. Schedule an architectural review by a senior developer or architect every 2 sprints to catch technical debt early. | If significant rework is confirmed → PM identifies the affected module, brings in a senior contractor to accelerate fixes, re-estimates the remaining work (new ETC), updates the EAC, and presents a revised schedule to the Sponsor with a recovery plan. |
| 3 | **Inaccurate Initial Estimation Risk:** The original task-level estimates for the ERP system were overly optimistic and did not account for the actual complexity of enterprise integration, causing the CPI to be below 1.0 from the very beginning of the project. | High | High | Use **3-Point Estimation (PERT: (O + 4M + P) / 6)** for all future estimates instead of single-point estimates. Require expert review of all estimates before baselining. Add a **10–15% contingency reserve** to the overall budget. Reference analogous ERP project data to sanity-check estimates. | If fundamentally wrong estimates are confirmed → PM conducts a complete Bottom-up re-estimation of all remaining work packages, presents the revised EAC and ETC to the Sponsor, and works with the Sponsor to decide whether to fund the gap or cut scope to fit the original BAC. |

---

#### Request 4 (30%) – Critical Path Method & Schedule Crashing

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

### 📌 QUICK REFERENCE – PMG201c ANSWER FRAMEWORK

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


---

