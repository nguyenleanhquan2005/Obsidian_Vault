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
        

### Mẹo ghi nhớ nhanh cho bài thi:

1. **Chữ "S" (Schedule)** luôn đi với **PV**.
    
2. **Chữ "C" (Cost)** luôn đi với **AC**.
    
3. **EV** luôn nằm ở **vế trước** trong các công thức tính sai lệch (CV, SV) và chỉ số hiệu suất (CPI, SPI).
    
4. **Hiệu suất (Index):** Chia. **Sai lệch (Variance):** Trừ.
    
5. Để tính toán về thời gian, chỉ cần thay biến số chi phí bằng biến số thời gian (ví dụ: EDAC dùng SPI thay vì CPI).
# PMG201c - Practical Exam 1 (Fall 2025)

You have developed a unique, niche consumer product, and your project is to validate its market viability through a temporary pop-up retail operation. The project requires securing permits, designing and building the display, managing inventory, training student sales staff, and achieving a sales goal of $15,000 in gross revenue. The pop-up operation must run for two consecutive weeks. The setup and operational costs (excluding product manufacturing cost) are strictly limited to $1500, and the budget constraint demands that the total inventory shrinkage/loss be kept below 2% of the total inventory value. For quality, the customer satisfaction rating, measured by post-purchase surveys, must exceed 90% positive feedback regarding product quality and the retail experience.

**Request 1 (20%):** develop a narrative charter statement that includes the following details

1. Project name: Pop-up retail validation
    
2. Justifications (purpose & reasons to implement this project),
    
3. Project constraints, in terms of scope, time, cost/budget, and quality.
    

**Request 2 (20%):** provide at least five main cost/budget items. Each cost/budget item, you need to provide following details: name, description, estimation along with the way to estimate (how to estimate, person in charged…)

**Request 3 (30%):** develop communication plan for the project where you:

1. Define at three project stakeholders (project-internal, organization-internal, external)
    
2. Create a communication plan for each of those stakeholders and the communications you believe they should receive. Each communication needs to include following details: information, purpose, frequency, method or format, responsible.
    

**Request 4 (30%):** identify three project risks by listing out the risk title/name, description, possible impacts (in term of scope or quality, time, and cost), and relevant risk response plans (mitigation, contingency).


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