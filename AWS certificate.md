
Trong quá trình thiết kế và xây dựng hệ thống AWS, để 1 hệ thống chạy hiệu quả thì có nhiều yếu tố
## **Thiết kế kiến trúc bảo mật (Secure Architectures):**

#### <span style="color:rgb(0, 176, 240)"><span style="color:rgb(0, 112, 192)"><span style="color:rgb(0, 32, 96)">IAM (Identity and Access Managment</span><span style="color:rgb(0, 32, 96)">)</span></span></span>

**Định nghĩa:** Quản lý quyền truy cập dịch vụ AWS. Bạn có thể sử dụng IAM để kiểm soát truy cập vào các tài nguyên AWS thông qua users, roles và policies. Quản lý actions the users hoặc service có thể thực hiện.
<span style="color:rgb(192, 0, 0)">Đ<span style="color:rgb(192, 0, 0)">ặc điể</span>m</span>:
- <span style="color:rgb(192, 0, 0)">kiểm</span> soát truy cập an ninh mạnh mẽ một cách tập trung và có khả năng mở rộng(enforce robust security access controls in a ==centralized and scalable manner==).
- Cung cấp những quyền tối thiểu nhằm bảo mật tốt nhất để giảm thiểu rủi ro ( ==Least Privilege==).
- Kiểm soát Truy cập Chi tiết Dịch vụ này cho phép bạn xác định chính xác ai (danh tính nào) có thể thực hiện hành động nào trên tài nguyên nào (==Granular Control==).
<span style="color:rgb(192, 0, 0)">2 chức năng chính là</span>: 
- **Xác thực (Authentication)** (kiểm soát quá trình đăng nhập và xác minh danh tính)
- **Ủy quyền (Authorization)** (quản lý quyền truy cập đến các tài nguyên AWS)
#### <span style="color:rgb(0, 176, 240)"><span style="color:rgb(0, 32, 96)">MFA: Multi-Factor Authentication</span></span>
Bảo mật đa lớp giúp tăng mức độ bảo mật khi đăng nhập vào AWS, giúp ngăn chặn người lạ lỡ khi có biết mật khẩu.
#### <span style="color:rgb(0, 176, 240)"><span style="color:rgb(0, 32, 96)"><span style="color:rgb(0, 32, 96)">SCP: Service Control Policies - Chính <span style="color:rgb(0, 32, 96)">sách</span> Kiểm soát Dịch vụ</span></span></span>:
-Giúp doanh nghiệp duy trì **compliance (tuân thủ)** và **an toàn hệ thống** ở quy mô lớn.
- Là **lớp kiểm soát quyền lực cao nhất (Governance layer)** trong hệ thống **AWS Organizations**.
- `AWS Organizations`: quản lý tập trung(Centralized control) các quyền truy cập tối đa (`Maximum available permissions`) trong tổ chức mà các **account con** trong **AWS Organization** có thể có
- Dùng để **quản lý tuân thủ, bảo mật và kiểm soát truy cập ở cấp tổ chức (organization level)**
- `Guardrails` (Rào cản/Lan can bảo vệ): Đảm bảo các tài khoản tuân thủ các nguyên tắc 
- `Principle of least privilege` (Nguyên tắc đặc quyền tối thiểu)
- Áp dụng **chính sách kiểu JSON**, tương tự như IAM policy, nhưng:
    
    - Không cấp quyền trực tiếp.
        
    - Chỉ **giới hạn** quyền có thể được cấp bởi IAM policies.
        
- Có thể gán SCP cho:
    
    - **Root Organization**
        
    - **Organizational Unit (OU)**
        
    - **Tài khoản AWS con (member account)**
        
- SCP chỉ có tác dụng với **IAM users và roles trong tài khoản đó**, **không** ảnh hưởng đến **root user**.
- Ví dụ:
    - Chặn tất cả tài khoản con tạo tài nguyên ở ngoài vùng “ap-southeast-1 (Singapore)”.
        
    - Cấm xóa log của CloudTrail hoặc S3 bucket log
#### <span style="color:rgb(0, 32, 96)">Encryption (KMS, TLS/ACM),</span>
##### 1. **KMS (AWS Key Management Service)**
- **Mục đích:** Dịch vụ quản lý khóa mã hóa Data at rest (encryption keys) tập trung của AWS.  

- **Chức năng chính:**
    
    - Tạo, lưu trữ, và kiểm soát việc sử dụng **keys** dùng để mã hóa dữ liệu (ví dụ: trong S3, EBS, RDS…).
        
    - Hỗ trợ **envelope encryption** (mã hóa nhiều lớp).
        
- **Ví dụ:** Khi bạn bật “Encrypt data at rest” trên S3, thường là dùng KMS key (AWS-managed key hoặc customer-managed key).
##### 2. **TLS (Transport Layer Security)**

- **Mục đích:** Mã hóa **dữ liệu trong quá trình truyền (data in transit)**.
    
- **Hoạt động:** Dùng **HTTPS** (TLS/SSL) để bảo vệ dữ liệu giữa client ↔ server khỏi nghe lén hoặc sửa đổi.
    
##### 3. **ACM (AWS Certificate Manager)**

- **Mục đích:** Cung cấp, quản lý, và tự động gia hạn **TLS/SSL certificates** cho các dịch vụ AWS như CloudFront, ALB, API Gateway…
    
- **Tác dụng:** Bảo mật kết nối HTTPS mà không cần cài đặt chứng chỉ thủ công.
#### <span style="color:rgb(0, 32, 96)">Security Groups,</span>
để quản lý truy cập mạng tới các tài nguyên AWS Cloud, đặc biệt là các **EC2 instances**, thi hành bảo mật mạng ở tầng L3/4 đối với các **EC2 interfaces**. Security Groups đóng vai trò như một **Host-based Firewall** khi liên kết với một EC2 instance.
• Có hai loại quy định là **inbound** và **outbound** :
- **Stateful:** Nếu bạn cho phép traffic vào (inbound), phản hồi tự động được phép ra (outbound).
- Mặc định không có bất kỳ **inbound rules** nào cho phép truy cập.
- Tất cả outbound được phép

• Nguồn xuất phát của một quy định có thể là IP Address, VPC Subnets CIDR, hoặc Security Group ID.

• Không thể tạo quy định với quy luật phủ nhận và không thể liên kết trực tiếp với VPC hay VPC Subnet.

#### <span style="color:rgb(0, 32, 96)">NACLs,</span>
NACLs được sử dụng để **quản lý và kiểm soát truy cập mạng** đến các tài nguyên trong **AWS Cloud**, đặc biệt là các **EC2 instances** nằm trong các **subnets** của VPC.  
Chúng thi hành cơ chế **bảo mật mạng ở tầng L3/L4 (Network và Transport layer)**, nơi các gói tin được lọc dựa trên **IP address, port, và protocol**
#### <span style="color:rgb(0, 32, 96)">GuardDuty,</span>

#### <span style="color:rgb(0, 32, 96)">Shield,</span>

#### <span style="color:rgb(0, 32, 96)">WAF </span>

#### <span style="color:rgb(0, 32, 96)">Secrets Manager</span>

Amazon GuardDuty is primarily a threat detection service that <span style="color:rgb(192, 0, 0)">continuously monitors for malicious activity</span> and <span style="color:rgb(192, 0, 0)">unauthorized behavior</span> within your AWS environment. It helps to <span style="color:rgb(192, 0, 0)">identify threats</span> related to AWS accounts, access keys, and network traffic. While GuardDuty is a valuable service for monitoring and detecting security threats, it is not specifically designed for assessing application vulnerabilities or identifying infrastructure deployments that do not meet best practices. To meet the requirements of assessing application vulnerabilities and ensuring infrastructure deployments align with best practices, the company could use AWS Config.

CloudTrail: to monitor and log API calls in AWS accounts. CloudTrail records contain the API event, the user who made the API call, and the time that the call was made

<span style="color:rgb(192, 0, 0)">Amazon Inspector</span> is an <span style="color:rgb(192, 0, 0)"><span style="color:rgb(192, 0, 0)">a</span>utomated security assessment service</span> that helps improve the security and compliance of applications deployed on Amazon EC2 instances. It <span style="color:rgb(192, 0, 0)">assesses applications for vulnerabilities, deviations</span> from <span style="color:rgb(192, 0, 0)">best practices, and compliance with security <span style="color:rgb(0, 0, 0)">standards</span>.</span> By using Amazon Inspector, the company can <span style="color:rgb(192, 0, 0)">identify security issues and potential vulnerabilities</span> in their infrastructure deployments and take necessary actions to address them. This service can help the company ensure that their applications are following best practices and are secure from potential threats.

## **2. Thiết kế kiến trúc linh hoạt và bền vững (Resilient Architectures)**

Multi-AZ,

Multi-Region,

DR Strategies,

Auto Scaling,

Route 53,

Load Balancing,

Backup & Restore
Chào bạn,

Thật tuyệt vời! Yêu cầu của bạn đã cung cấp một cấu trúc cực kỳ chi tiết, cho phép tôi tổng hợp các khái niệm quan trọng về kiến trúc bảo mật và linh hoạt của AWS. Với vai trò chuyên gia, tôi sẽ trình bày thông tin chi tiết và được trích dẫn đầy đủ từ các nguồn tài liệu của chúng ta.

---

## 1️⃣ Thiết Kế Kiến Trúc Bảo Mật (Secure Architectures)

Kiến trúc bảo mật trên AWS được xây dựng dựa trên nguyên tắc **Phòng thủ theo Chiều sâu (Defense-In-Depth)** và sự hiểu biết rõ ràng về Mô hình Trách nhiệm Chia sẻ (Shared Responsibility Model).

### 🧩 Mô hình Trách nhiệm Chia sẻ (AWS Shared Responsibility Model)

Đây là khung bảo mật xác định nghĩa vụ bảo mật giữa AWS và khách hàng.

- **Trách nhiệm của AWS (Security _of_ the Cloud):** AWS chịu trách nhiệm bảo mật **cơ sở hạ tầng toàn cầu** (regions, availability zones, edge locations), phần cứng, phần mềm, mạng và các dịch vụ cốt lõi (compute, storage, database, networking). Nếu bạn thiết lập một dịch vụ (ví dụ: S3) mà nó không hoạt động, đó là trách nhiệm của AWS.
- **Trách nhiệm của Khách hàng (Security _in_ the Cloud):** Khách hàng chịu trách nhiệm về **dữ liệu và cấu hình**. Điều này bao gồm:
    - **Cấu hình hệ điều hành khách (Guest OS)** và các ứng dụng.
    - **Quản lý truy cập** (IAM).
    - **Mã hóa dữ liệu** (cả client-side và server-side).
    - Cấu hình các thành phần mạng ảo (như Security Groups và Network ACLs).
- **Trách nhiệm đối với Dịch vụ Máy tính (Shared Responsibility for Compute):** Trách nhiệm thay đổi tùy thuộc vào loại dịch vụ:
    - **Infrastructure as a Service (IaaS)** (ví dụ: EC2): Khách hàng có trách nhiệm cao đối với Guest OS, runtime, và ứng dụng.
    - **Functions as a Service (FaaS)** (ví dụ: Lambda): AWS quản lý máy chủ, OS, và runtime. Khách hàng chỉ chịu trách nhiệm về code/chức năng của mình.

### 🔐 Quản lý Danh tính và Truy cập (Identity & Access Management - IAM)

- **AWS IAM:** Là dịch vụ cốt lõi để quản lý người dùng và quyền truy cập. IAM là một **dịch vụ toàn cầu (Global Service)**.
- **Nguyên tắc Đặc quyền Tối thiểu (Principle of Least Privilege - PoLP):** Chỉ cấp cho người dùng hoặc tài nguyên đủ quyền cần thiết để thực hiện công việc. Việc cấp quyền quá mức (ví dụ: cấp quyền admin cho mọi người) là một ý tưởng tồi.
- **Người dùng Root (AWS Account Root User):** Là tài khoản được tạo khi tài khoản AWS được tạo. Nó có **toàn quyền truy cập vào mọi thứ**. Nó không nên được sử dụng cho các tác vụ hàng ngày và phải được bảo mật nghiêm ngặt bằng MFA.
- **Xác thực Đa yếu tố (Multi-Factor Authentication - MFA):** Thêm một lớp bảo mật bổ sung.
- **Cấu trúc Policy IAM (Anatomy of an IAM Policy):** Policy được viết bằng tài liệu JSON và xác định các quyền được `Allow` hoặc `Deny`. Các thành phần bao gồm `Statement ID`, `Effect`, `Action` và `Resource`.
- **Mô hình Zero-Trust:** Hoạt động trên nguyên tắc **"Không tin tưởng ai cả, xác minh mọi thứ"**. Trong mô hình này, danh tính (Identity) trở thành ranh giới bảo mật chính.
- **Zero-Trust trên AWS:** AWS cung cấp các công cụ như IAM, CloudTrail và GuardDuty để phát hiện các mối đe dọa dựa trên danh tính. Tuy nhiên, việc triển khai các biện pháp kiểm soát theo thời gian thực (như dựa trên thiết bị hoặc vị trí) thường đòi hỏi kiến thức chuyên môn sâu hoặc sử dụng giải pháp bên thứ ba.
- **Directory Service / Active Directory / Identity Providers / SSO:** Các dịch vụ thư mục (Directory Service) giúp quản lý danh tính tập trung. AWS hỗ trợ kết hợp với các dịch vụ bên ngoài như Active Directory (AD). **Single Sign-On (SSO)** và **Identity Providers** như Amazon Cognito giúp xử lý danh tính liên kết (Federated Identity), cho phép người dùng bên thứ ba truy cập các dịch vụ AWS bằng thông tin xác thực tạm thời.

### 🛡️ Bảo mật (Security)

#### Khái niệm Cơ bản

- **Bộ ba CIA (CIA Triad):** Mô hình nền tảng bao gồm **Confidentiality** (Bảo mật dữ liệu khỏi truy cập trái phép), **Integrity** (Đảm bảo tính chính xác), và **Availability** (Đảm bảo truy cập khi cần).
- **Phòng thủ theo Chiều sâu (Defense-In-Depth):** Áp dụng bảo mật ở tất cả các lớp, từ mạng biên (perimeter) đến ứng dụng và dữ liệu.
- **Lỗ hổng (Vulnerabilities):** Là điểm yếu trong ứng dụng có thể bị kẻ tấn công lợi dụng.

#### Mã hóa (Encryption)

- **Mã hóa khi Truyền (In-Transit Encryption):** Bảo vệ dữ liệu đang di chuyển. Thường sử dụng SSL/TLS.
- **Mã hóa khi Lưu trữ (At-Rest Encryption):** Bảo vệ dữ liệu tĩnh. Thường được thực hiện bằng mã hóa phía máy chủ (ví dụ: S3 server-side encryption).
- **Khóa Mật mã (Cryptographic Keys):** Được sử dụng cùng với thuật toán để mã hóa/giải mã dữ liệu. Mã hóa **đối xứng (Symmetric)** sử dụng cùng một khóa (ví dụ: AES), trong khi mã hóa **bất đối xứng (Asymmetric)** sử dụng hai khóa (ví dụ: RSA).
- **AWS KMS (Key Management Service):** Dịch vụ được quản lý để tạo và kiểm soát khóa mã hóa. KMS là **HSM đa người thuê (multi-tenant HSM)**.
- **CloudHSM:** Cung cấp **HSM đơn người thuê (single-tenant HSM)**. Được xây dựng trên phần cứng được xác thực **FIPS 140-2 level 3**, lý tưởng cho các yêu cầu tuân thủ nghiêm ngặt.
- **AWS Secrets Manager:** Dịch vụ quản lý vòng đời của bí mật (secrets) như mật khẩu CSDL và khóa API, giúp tránh mã hóa cứng bí mật trong mã nguồn.

#### Giảm thiểu Mối đe dọa và Tuân thủ (Threat Mitigation and Compliance)

- **DDoS (Distributed Denial of Service):** Tấn công nhằm làm quá tải hệ thống bằng một lượng lớn yêu cầu.
- **AWS Shield:** Dịch vụ quản lý bảo vệ chống DDoS.
    - **Shield Standard:** Miễn phí, tự động bật, bảo vệ chống lại các cuộc tấn công DDoS phổ biến ở Lớp 3 và Lớp 4.
    - **Shield Advanced:** Bảo vệ nâng cao, cung cấp quyền truy cập vào Đội Phản ứng DDoS (DRT) 24x7 và bảo vệ chi phí trong các đợt tấn công lớn.
- **AWS WAF (Web Application Firewall):** Tường lửa cấp ứng dụng (Layer 7). Bảo vệ các ứng dụng web khỏi các khai thác phổ biến như **SQL injection và cross-site scripting (XSS)**.
- **AWS GuardDuty:** Dịch vụ phát hiện mối đe dọa thông minh (IDs/IPS) liên tục giám sát CloudTrail logs, VPC Flow Logs và DNS logs để phát hiện các hoạt động độc hại.
- **AWS Inspector:** Công cụ chạy các đánh giá bảo mật (security benchmark) và tuân thủ trên các **instance EC2 cụ thể**. Nó tạo ra báo cáo PDF.
- **AWS Artifact:** Cung cấp quyền truy cập vào các báo cáo tuân thủ của AWS (ví dụ: SOC, PCI).
- **Chương trình Tuân thủ (Compliance Programs):** AWS giúp khách hàng đáp ứng các yêu cầu như **GDPR**, **HIPAA**, **FedRAMP**, và **PCI DSS**.

### 🌐 Mạng (Bảo mật mạng)

- **VPC (Virtual Private Cloud) & Subnets:** VPC là một khu vực mạng được cách ly logic (logically isolated section). Các Subnets là các phân vùng logic của mạng, thường nằm trong một AZ. Bảo mật mạng đòi hỏi kiểm soát truy cập ở nhiều lớp (Defense-In-Depth).
- **Security Groups (SG) vs NACLs (Network Access Control Lists):**
    - **Security Groups:** Tường lửa cấp **instance** (chính xác hơn là Elastic Network Interface). SG là **có trạng thái (stateful)**, nghĩa là lưu lượng trả về cho một yêu cầu được cho phép sẽ tự động được cho phép đi ra. Nó chỉ hỗ trợ quy tắc **allow** (allow rules).
    - **NACLs:** Tường lửa cấp **subnet**. NACLs là **không trạng thái (stateless)**, nghĩa là lưu lượng trả về phải được cho phép rõ ràng bởi một quy tắc đi ra. Nó hỗ trợ cả quy tắc **allow** và **deny** và các quy tắc được xử lý theo thứ tự số. NACLs hữu ích để chặn các dải IP độc hại ở cấp độ mạng biên.
- **AWS VPN (Virtual Private Network):** Thiết lập một đường hầm **an toàn và riêng tư (secure and private tunnel)** giữa mạng on-premise và VPC. VPN sử dụng giao thức bảo mật như **IPsec**.
- **AWS Direct Connect (DX):** Tạo một **kết nối vật lý trực tiếp** từ on-premise đến AWS, không đi qua internet công cộng. DX cung cấp băng thông cao nhưng **không tự động mã hóa** dữ liệu (unencrypted); thường cần VPN chạy trên DX để đảm bảo bảo mật.

---

## 2️⃣ Thiết Kế Kiến Trúc Linh hoạt và Bền vững (Resilient Architectures)

Phần này tập trung vào trụ cột **Reliability (Độ tin cậy)** của Khuôn khổ Well-Architected, cùng với các khái niệm về cơ sở hạ tầng toàn cầu.

### 🏗️ Kiến trúc Đám mây (Cloud Architecture)

- **Tính Sẵn sàng Cao (High Availability - HA):** Đảm bảo dịch vụ vẫn hoạt động bằng cách **loại bỏ các điểm lỗi đơn lẻ (SPoF)**. Điều này chủ yếu được thực hiện bằng cách chạy workload trên nhiều **Vùng sẵn sàng (AZs)**.
- **Khả năng chịu lỗi (Fault Tolerance):** Khả năng ngăn ngừa lỗi. HA và Fault Tolerance đảm bảo rằng nếu một thành phần bị lỗi (ví dụ: một máy chủ web), toàn bộ doanh nghiệp sẽ không bị sập.
- **Khả năng Mở rộng Cao (High Scalability):** Khả năng tăng hoặc giảm tài nguyên dựa trên nhu cầu.
- **Tính Đàn hồi Cao (High Elasticity):** Khả năng tự động **co/giãn** (shrink and grow) nhanh chóng để đáp ứng nhu cầu một cách tự động.
- **Độ bền Cao (High Durability):** Khả năng phục hồi sau lỗi theo cách mong đợi.

#### Phục hồi sau Thảm họa (Disaster Recovery - DR) và Kế hoạch Khởi động Kinh doanh (Business Continuity Plan)

DR tập trung vào việc phục hồi sau các sự kiện quy mô lớn ảnh hưởng đến toàn bộ khu vực (Multi-Region).

- **RTO (Recovery Time Objective):** **Thời gian ngừng hoạt động tối đa có thể chấp nhận** được để phục hồi dịch vụ.
- **RPO (Recovery Point Objective):** **Khoảng thời gian mất dữ liệu tối đa có thể chấp nhận** được.
- **Các Tùy chọn DR (Disaster Recovery Options):** Các chiến lược được chọn dựa trên các mục tiêu RTO/RPO do doanh nghiệp xác định.
    1. **Sao lưu và Khôi phục (Backup and Restore):** RTO/RPO cao nhất, chi phí thấp nhất.
    2. **Đèn hoa tiêu (Pilot Light):** Một phiên bản tối thiểu luôn chạy (ví dụ: chỉ CSDL cốt lõi).
    3. **Dự phòng ấm (Warm Standby):** Một bản sao thu nhỏ, đầy đủ chức năng luôn chạy.
    4. **Đa địa điểm Hoạt động-Hoạt động (Multi-Site Active-Active):** Workload chạy đồng thời ở nhiều khu vực, cung cấp RTO/RPO gần như bằng không, chi phí và độ phức tạp cao nhất.

### 🌐 Cơ sở hạ tầng Toàn cầu AWS (AWS Global Infrastructure)

- **Khu vực (Regions):** Các vị trí địa lý vật lý, được thiết kế để hoàn toàn tách biệt (isolated) khỏi các Khu vực khác để có khả năng chịu lỗi cao nhất.
- **Vùng sẵn sàng (Availability Zones - AZs):** Các trung tâm dữ liệu riêng biệt về mặt vật lý (independent failure zone) trong một Region. AZs được kết nối với nhau bằng liên kết mạng có độ trễ thấp, thông lượng cao. Việc triển khai trên nhiều AZ (Multi-AZ) là cơ chế chính cho Tính sẵn sàng cao.
- **Mạng lưới Toàn cầu AWS (AWS Global Network):** Mạng xương sống riêng tư, hiệu suất cao, kết nối các Regions và AZs.
- **Địa điểm Biên (Points of Presence - PoP) / Edge Locations:** Các trang web dữ liệu được sử dụng để **lưu trữ bản sao dữ liệu (cache copies of data)** cho việc phân phối nhanh nhất đến người dùng cuối, chủ yếu được sử dụng bởi **CloudFront**.
- **AWS Outposts:** Cung cấp một rack máy chủ vật lý chạy các dịch vụ AWS ngay tại trung tâm dữ liệu on-premise của khách hàng, cho phép mô hình hybrid nhất quán.
- **Nơi cư trú Dữ liệu (Data Residency):** Vị trí địa lý nơi tài nguyên đám mây cư trú, thường được quy định bởi các yêu cầu tuân thủ.
- **GovCloud:** Các Region đặc biệt của Mỹ được thiết kế để chứa các workload nhạy cảm, có quy định tuân thủ như **FedRAMP**.

### 🧱 Khuôn khổ Well-Architected (Well-Architected Framework)

Khuôn khổ này bao gồm sáu trụ cột, trong đó ba trụ cột sau liên quan trực tiếp đến tính linh hoạt và bảo mật:

- **Độ tin cậy (Reliability):** Đảm bảo workload thực hiện đúng chức năng và có khả năng phục hồi sau sự cố.
    - **Nguyên tắc thiết kế:** **Tự động phục hồi sau sự cố**; kiểm tra quy trình phục hồi (ví dụ: sử dụng **game days**); **mở rộng theo chiều ngang (scale horizontally)** để tăng tính sẵn sàng tổng thể.
    - Sự kết hợp giữa **Elastic Load Balancing (ELB)** và **Auto Scaling Groups (ASGs)** là mô hình cơ bản để đạt được tính linh hoạt.
- **Bảo mật (Security):** (Đã đề cập ở Phần 1).
- **Vận hành Xuất sắc (Operational Excellence):** Tập trung vào việc chạy và giám sát hệ thống.
    - **Nguyên tắc thiết kế:** **Thực hiện hoạt động dưới dạng mã (Perform operations as code)**; thực hiện các thay đổi nhỏ, thường xuyên, có thể đảo ngược; và **tinh chỉnh các quy trình vận hành thường xuyên**. Tự động hóa là yếu tố nền tảng để đạt được sự xuất sắc trong vận hành.

## **3. Thiết kế hệ thống hiệu năng cao (High-Performing Architectures)**

AWS bao gồm 3 loại services cơ bản:

## Compute

- Để chạy bất kì ứng dụng nào (to run any application)
- kiểm soát và quản lý các chức năng máy chủ như mở rộng quy mô và triển khai (control and manage server functions such as scaling and deployment)
- Chạy các ứng dụng phi trạng thái được kích hoạt bằng sự kiện (Run event-initiated stateless applications)

Compute scaling (EC2 Auto Scaling, Lambda, Fargate),

Elasticity in the AWS Cloud refers to 
- The ability to rightsize resources as demand shifts

- How easily resources can be procured when they are needed

 AWS. EC2 (Elastic Compute Cloud) là một dịch vụ cực kỳ linh hoạt, và AWS cung cấp nhiều cách để thanh toán cho các máy chủ ảo (instances) này.

Dưới đây là so sánh chi tiết giữa bốn mô hình chính: **On-Demand, Reserved Instance (RI), Spot Instance,** và **Dedicated Instance/Host**.

## So Sánh Các Mô Hình Định Giá và Thuê EC2

| Đặc điểm                        | On-Demand                                                                                | Reserved Instances (RI)                                                                                                        | Spot Instances                                                                                                                                     | Dedicated Instance / Host                                                                                                                                                   |
| :------------------------------ | :--------------------------------------------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Bản chất**                    | Mặc định. Trả theo mức sử dụng.                                                          | Cam kết sử dụng dài hạn.                                                                                                       | Đấu thầu dung lượng EC2 dự phòng.                                                                                                                  | Đảm bảo phần cứng vật lý dành riêng (Single-Tenant).                                                                                                                        |
| **Tiết kiệm chi phí**           | **0%** (Giá tiêu chuẩn).                                                                 | **Giảm giá đáng kể**, lên đến 75% (hoặc 72%).                                                                                  | **Giảm giá lớn nhất**, lên đến 90% so với On-Demand.                                                                                               | **Đắt nhất**. Chi phí cơ bản cao hơn, nhưng có thể giảm nếu kết hợp với RI/Spot.                                                                                            |
| **Cam kết**                     | **Không** có cam kết trả trước hoặc dài hạn.                                             | **1 hoặc 3 năm**.                                                                                                              | **Không** có cam kết thời gian cố định.                                                                                                            | Không phải mô hình định giá thuần túy, nhưng thường là cam kết dài hạn do yêu cầu về cấp phép/tuân thủ.                                                                     |
| **Đơn vị thanh toán**           | Tính theo giờ hoặc **theo giây** (tối thiểu 60 giây) đối với các hệ điều hành như Linux. | Trả trước toàn bộ, một phần, hoặc không trả trước.                                                                             | Tính theo giây.                                                                                                                                    | Tính theo giờ (tùy thuộc vào mô hình giá kết hợp).                                                                                                                          |
| **Tính linh hoạt**              | **Tối đa**. Có thể khởi chạy và chấm dứt bất cứ lúc nào.                                 | **Thấp**. Phải cam kết với loại instance cụ thể. RI Convertible linh hoạt hơn (có thể thay đổi thuộc tính) so với RI Standard. | Linh hoạt về thời điểm bắt đầu và kết thúc.                                                                                                        | Có thể sử dụng On-Demand, RI, hoặc Spot.                                                                                                                                    |
| **Nguy cơ gián đoạn**           | **Không**.                                                                               | **Không**.                                                                                                                     | **Cao**. AWS có thể thu hồi (terminate) instance bất cứ lúc nào với cảnh báo trước **hai phút** nếu dung lượng cần thiết cho khách hàng On-Demand. | Không có nguy cơ gián đoạn do thiếu dung lượng AWS.                                                                                                                         |
| **Mô hình thuê**                | **Chia sẻ** (Shared Tenancy) – nhiều tài khoản AWS sử dụng chung phần cứng vật lý.       | Chia sẻ (Mặc định).                                                                                                            | Chia sẻ.                                                                                                                                           | **Độc quyền** (Single-Tenant). Không chia sẻ phần cứng vật lý với khách hàng AWS khác.                                                                                      |
| **Trường hợp sử dụng lý tưởng** | Workload ngắn hạn, đột biến, **không thể dự đoán**. Ứng dụng mới để thử nghiệm.          | Workload có **mức sử dụng ổn định, có thể dự đoán** (Steady-state) trong 1 hoặc 3 năm.                                         | Workload **chịu lỗi** (fault-tolerant), **không trạng thái** (stateless), và có thể bị gián đoạn (ví dụ: xử lý hàng loạt, tính toán khoa học).     | Đáp ứng yêu cầu **tuân thủ nghiêm ngặt** (ví dụ: HIPAA, FedRAMP) hoặc để **Mang theo Giấy phép riêng (BYOL)** dựa trên đặc điểm của máy chủ vật lý (ví dụ: số core/socket). |

### Thông tin chi tiết bổ sung:

#### 1. Reserved Instances (RI) và Savings Plans

- RI (và Savings Plans, một giải pháp thay thế hiện đại) được thiết kế để mang lại **tiết kiệm dài hạn tốt nhất** cho việc sử dụng có thể dự đoán được.
- RI có thể được **chia sẻ** giữa nhiều tài khoản trong cùng một tổ chức.
- RI Tiêu chuẩn (Standard RI) có thể được bán trên AWS Marketplace nếu không được sử dụng hết. RI Chuyển đổi (Convertible RI) không thể bán hoặc mua trên Marketplace.

#### 2. Spot Instances

- Spot Instances hoạt động trên cơ chế **đấu thầu** dung lượng máy tính không sử dụng của AWS.
- Chúng lý tưởng cho các workload mà việc gián đoạn **không gây ra hậu quả thảm khốc**.
- AWS Batch thường được sử dụng cùng với Spot Instances để tối ưu hóa chi phí cho các công việc xử lý hàng loạt.

#### 3. Dedicated Tenancy (Dedicated Instances và Dedicated Hosts)

Mô hình Dedicated là một sự lựa chọn về **sự thuê** (tenancy) và không phải là mô hình định giá thuần túy.

- **Dedicated Instance:** Instance chạy trên phần cứng vật lý **không được chia sẻ** với các khách hàng AWS khác, nhưng bạn không kiểm soát toàn bộ máy chủ vật lý đó.
- **Dedicated Host:** Khách hàng có quyền sử dụng toàn bộ máy chủ vật lý (giống như có máy chủ riêng). Đây là tùy chọn **đắt nhất** vì bạn thanh toán để sử dụng toàn bộ máy chủ. Dedicated Host rất quan trọng khi cần **khả năng hiển thị** các thuộc tính vật lý (như socket và core) để đáp ứng các yêu cầu cấp phép phần mềm nghiêm ngặt (BYOL).
## Storage

Storage (S3, EFS, EBS), Caching,

## Networking

Network Optimization (CloudFront, Global Accelerator)
[AWS Managed Services (AMS)](https://aws.amazon.com/managed-services/) helps you adopt AWS at ==scale and operate more efficiently and securely==. We leverage standard AWS services and offer guidance and execution of operational best practices with specialized automations, skills, and experience that are contextual to your environment and applications.

AMS provides ==proactive, preventative, and detective== capabilities that raise the operational bar and help reduce risk without constraining agility, allowing you to focus on innovation. AMS extends your team with operational capabilities including monitoring, incident management
## **4. Thiết kế tối ưu chi phí (Cost-Optimized Architectures)**

Cost Explorer,

Budgets,

Savings Plans,

Lifecycle Policies,

NAT Gateway Optimization,

Storage Tiering



AWS Config is a service that provides a detailed inventory of the AWS resources in your account and continuously tracks changes to these resources. It can help you assess compliance with best practices, identify deviations from desired configurations, and evaluate the security of your infrastructure deployments. By using AWS Config Rules, you can also define custom rules to check for specific configurations or vulnerabilities in your applications and infrastructure.

AWS direct connect create a private connection between an on-premises workload and an AWS Cloud workload.

Access Analyzer for S3 it provides detailed visibility into your S3 buckets, including information about access control lists (ACLs) and bucket policies. By using Access Analyzer for S3, the user can easily review all S3 buckets with ACLs and S3 bucket policies directly within the S3 console. This service helps ensure that your S3 buckets are properly secured and compliant with your organization's security requirements.

IAM Access Analyzer for S3 alerts you to S3 buckets that are configured to allow access to anyone on the internet or other AWS accounts, including AWS accounts outside of your organization

AWS Application composer Visually design and build modern applications quickly


benefits of using AWS Trusted Advisor are detecting underutilized resources to save costs and improving security by proactively monitoring the AWS environment
Chào bạn,

Thật vui khi được phân tích hai lĩnh vực cực kỳ quan trọng trong kiến trúc đám mây: **Hiệu năng cao** và **Tối ưu hóa chi phí**. Đây là hai trụ cột chính yếu (Performance Efficiency và Cost Optimization) trong Khuôn khổ Well-Architected.

Dưới đây là tổng hợp chi tiết dựa trên cấu trúc bạn đã cung cấp, tập trung vào việc tối ưu hóa kiến trúc để đạt được cả tốc độ và hiệu quả tài chính.

---

## 3️⃣ Thiết Kế Hiệu Năng Cao (High-Performing Architectures)

Trụ cột **Hiệu quả về Hiệu năng (Performance Efficiency)** tập trung vào việc sử dụng tài nguyên máy tính một cách hiệu quả để đáp ứng các yêu cầu hệ thống và duy trì hiệu quả đó khi nhu cầu thay đổi và công nghệ phát triển.

### 💻 Compute (Máy tính)

#### Tổng quan về EC2 và các loại Instance

- **EC2 Overview:** Amazon EC2 (Elastic Compute Cloud) là dịch vụ máy tính chủ lực của AWS, cho phép bạn khởi chạy các máy chủ ảo (VMs), mà AWS gọi là **instances**.
- **EC2 Instance Families & Types:** AWS cung cấp nhiều loại family instance được tối ưu hóa cho các nhu cầu cụ thể:
    - **General Purpose (M, T):** Cân bằng tốt giữa các tài nguyên, phù hợp cho hầu hết các trường hợp sử dụng, ví dụ: web servers, code repositories.
    - **Compute Optimized (C):** Lý tưởng cho các ứng dụng cần sức mạnh xử lý cao (High processing power), như mô hình hóa khoa học, game servers.
    - **Memory Optimized (R, X):** Tối ưu cho workload xử lý các tập dữ liệu lớn **trong bộ nhớ** (in-memory), ví dụ: in-memory databases, real-time big data analytics.
    - **Accelerated Optimized (P, G):** Sử dụng các bộ tăng tốc phần cứng (GPU/Co-processors), tuyệt vời cho Machine Learning, computational finance.
    - **Storage Optimized (I, D, H):** Cung cấp truy cập đọc/ghi tuần tự cao tới các tập dữ liệu lớn trên local storage, phù hợp cho CSDL NoSQL.
- **Dedicated Host vs. Instances:** Mặc định, các instance sử dụng **Shared Tenancy** (chia sẻ phần cứng vật lý với khách hàng khác).
    - **Dedicated Instances:** Instance chạy trên phần cứng đơn người thuê (single-tenant hardware) nhưng không kiểm soát toàn bộ máy chủ.
    - **Dedicated Host:** Khách hàng có quyền sử dụng toàn bộ máy chủ vật lý, thường được yêu cầu để đáp ứng các yêu cầu **tuân thủ nghiêm ngặt** hoặc cấp phép phần mềm (Bring Your Own License - BYOL).
- **EC2 Pricing Models:** Các mô hình này ảnh hưởng đến hiệu quả chi phí (xem Phần 4.2). **Spot Instances** được dùng cho workload chịu lỗi để tiết kiệm chi phí, nhưng có thể bị gián đoạn, trong khi **Reserved Instances** và **On-Demand** cung cấp tính sẵn sàng cao.
- **High Performance Computing (HPC):** Cung cấp khả năng tính toán cực lớn bằng cách gộp hàng trăm đến hàng nghìn máy chủ với kết nối nhanh. Dịch vụ **AWS Parallel Cluster** giúp triển khai và quản lý các cụm HPC trên AWS.
- **Edge and Hybrid Computing:**
    - **AWS Outposts:** Một rack máy chủ vật lý được đặt tại trung tâm dữ liệu on-premise của khách hàng, cho phép sử dụng API và dịch vụ AWS ngay tại chỗ, tạo trải nghiệm hybrid nhất quán.
    - **AWS Wavelength Zones:** Cho phép Edge Computing trên mạng 5G, giúp ứng dụng có độ trễ cực thấp (ultra low latency) bằng cách đặt chúng gần người dùng cuối nhất, thường dùng cho các ứng dụng nhạy cảm với độ trễ như gaming hoặc IoT.

#### So sánh Compute Serverless (Lambda vs. Fargate)

Để đạt hiệu năng cao với gánh nặng vận hành thấp, kiến trúc phi máy chủ (serverless) là nguyên tắc cốt lõi.

|Đặc điểm|AWS Lambda (FaaS)|Amazon Fargate (Serverless Containers)|
|:--|:--|:--|
|**Bản chất**|Chức năng (Function), dựa trên sự kiện|Công cụ máy tính phi máy chủ cho container|
|**Trừu tượng hóa**|**Tối đa** (Functions as a Service)|CaaS (Container as a Service)|
|**Thanh toán**|Theo mili giây (ms) và lời gọi|Theo giây (vCPU & Bộ nhớ)|
|**Khả năng mở rộng**|Rất nhanh, lý tưởng cho workload đột biến|Nhanh chóng, nhưng có thể chậm hơn Lambda|
|**Trường hợp sử dụng**|Tác vụ ngắn hạn, không trạng thái (stateless), xử lý sự kiện|Microservices, ứng dụng web container hóa chạy dài hạn|
|**Thời gian chạy tối đa**|15 phút|Không giới hạn|

### 🗄️ Storage (Lưu trữ)

Hiệu năng lưu trữ thường là sự đánh đổi giữa **độ trễ (latency)** và **khả năng mở rộng (scalability)**.

- **S3 (Simple Storage Service):** Là dịch vụ lưu trữ **đối tượng** (Object Storage) cung cấp khả năng mở rộng gần như **vô hạn**. Thích hợp cho dữ liệu phi cấu trúc, sao lưu, và phân tích dữ liệu lớn.
- **S3 Storage Classes:** Các lớp lưu trữ khác nhau cho phép tối ưu chi phí (Phần 4.2), nhưng cũng ảnh hưởng đến hiệu năng truy xuất: ví dụ, lớp **Standard** cung cấp hiệu năng truy xuất nhanh nhất và độ sẵn sàng cao nhất.
- **EBS (Elastic Block Store):** Cung cấp **lưu trữ khối** (Block Storage) có hiệu suất cao, **độ trễ thấp nhất** (low latency). Nó được gắn vào **một** instance EC2 duy nhất và cần thiết cho các ổ đĩa khởi động (boot drives) hoặc CSDL giao dịch.
- **EFS (Elastic File System):** Cung cấp **lưu trữ tệp** (File Storage) NFS có khả năng mở rộng, cho phép gắn đồng thời bởi **nhiều** instance EC2, lý tưởng cho các workload yêu cầu hệ thống tệp chia sẻ.
- **AWS Snow Family:** Các thiết bị vật lý (Snowcone, Snowball Edge, Snowmobile) được sử dụng để di chuyển lượng dữ liệu lớn (petabytes) vào AWS khi mạng chậm là rào cản.

### 🧮 Databases (Cơ sở dữ liệu)

Lựa chọn CSDL phù hợp là ứng dụng trực tiếp của nguyên tắc **"Mechanical Sympathy"** (hiểu cách các dịch vụ được tiêu thụ).

- **Amazon Aurora:** Engine CSDL quan hệ do AWS phát triển, tương thích với MySQL và PostgreSQL, nhưng cung cấp **hiệu năng và độ bền cao hơn** (PostgreSQL nhanh hơn 3 lần, MySQL nhanh hơn 5 lần).
- **DynamoDB (NoSQL Key-Value):** Cung cấp **hiệu suất cao** cho các ứng dụng có quy mô lớn (massively scalable) và **độ trễ một chữ số mili giây** (single-digit millisecond latency). Cung cấp chế độ **Provisioned** để đảm bảo hiệu suất (guarantee of performance) cho đọc/ghi.
- **ElastiCache:** Dịch vụ caching trong bộ nhớ được quản lý (Redis/Memcached). Việc thêm lớp caching này giúp **cải thiện hiệu suất ứng dụng** bằng cách giảm độ trễ truy cập dữ liệu thường xuyên.
- **Redshift (Data Warehouse):** Kho dữ liệu quy mô petabyte, tối ưu cho xử lý phân tích (OLAP), giúp tạo ra các báo cáo và phân tích phức tạp **rất nhanh** từ lượng lớn dữ liệu.
- **Database Migration Service (DMS):** Cho phép di chuyển CSDL nguồn (ví dụ: on-premise) sang CSDL đích trên AWS một cách an toàn và nhanh chóng.

### 🧠 ML, AI & Big Data

Các dịch vụ này giúp đạt hiệu năng cao bằng cách **dân chủ hóa các công nghệ tiên tiến (Democratize Advanced Technology)**, cho phép sử dụng các công cụ chuyên biệt thay vì tự xây dựng từ đầu.

- **AI and ML Services:** Amazon **SageMaker** là nền tảng flagship được quản lý hoàn toàn cho ML. AWS cũng cung cấp các dịch vụ chuyên biệt như **Amazon Lex** (chatbots), **Amazon Recognition** (nhận dạng hình ảnh), và **Amazon Comprehend** (Xử lý ngôn ngữ tự nhiên).
- **Big Data and Analytics:** **Amazon Athena** (query S3 bằng SQL) và **Amazon Kinesis** (xử lý dữ liệu streaming thời gian thực) giúp phân tích dữ liệu nhanh chóng mà không cần cung cấp máy chủ.
- **Amazon QuickSight:** Công cụ business intelligence (BI) để tạo dashboard và báo cáo, có thể kết nối với nhiều loại CSDL khác nhau.
- **Generative AI:** Các dịch vụ liên quan đến việc tạo ra nội dung mới như văn bản, hình ảnh, hoặc âm nhạc.

### 🌐 Networking (Hiệu năng)

- **CloudFront:** Mạng Phân phối Nội dung (CDN) toàn cầu. Cải thiện hiệu năng bằng cách lưu trữ nội dung tĩnh và động tại các **Địa điểm Biên (Edge Locations)** gần người dùng cuối nhất, giúp giảm độ trễ.
- **AWS Global Accelerator:** Cải thiện hiệu năng và tính sẵn sàng của ứng dụng bằng cách sử dụng **mạng toàn cầu của AWS** để định tuyến lưu lượng người dùng đến điểm cuối tối ưu. Nó sử dụng IP Anycast tĩnh.
- **AWS Global Network:** Mạng xương sống riêng tư, hiệu suất cao của AWS, kết nối các Regions và AZs với độ trễ thấp.
- **AWS Direct Connect (DX):** Thiết lập kết nối vật lý riêng tư giữa on-premise và AWS, đảm bảo băng thông cao và cung cấp trải nghiệm mạng nhất quán hơn so với kết nối internet thông thường.
- **Load Balancing (ELB Variants):** **Elastic Load Balancing** phân phối lưu lượng truy cập để đạt độ trễ tốt nhất. ELB đóng vai trò quan trọng trong việc đảm bảo tính sẵn sàng cao (HA) bằng cách phân phối tải trên nhiều AZ.

---

## 4️⃣ Thiết Kế Tối Ưu Chi Phí (Cost-Optimized Architectures)

Trụ cột **Tối ưu hóa Chi phí (Cost Optimization)** tập trung vào việc mang lại giá trị kinh doanh ở mức giá thấp nhất có thể, tránh các chi phí không cần thiết. Nguyên tắc chung là **chỉ trả tiền cho những gì bạn sử dụng** (Adopt a Consumption Model).

### 💵 Billing, Pricing & Support

- **AWS Pricing Calculator:** Công cụ **miễn phí** giúp ước tính chi phí cho hơn 100 dịch vụ AWS.
- **AWS Budgets:** Cho phép bạn đặt ngân sách **chủ động** cho chi phí và sử dụng, nhận cảnh báo khi vượt ngưỡng. Nó cho phép thực hiện các hành động tự động để phản ứng với cảnh báo ngân sách.
- **AWS Cost Explorer:** Công cụ **hồi cứu** (retrospective) trực quan hóa và phân tích chi phí và việc sử dụng AWS theo thời gian (hàng tháng hoặc hàng ngày), giúp xác định xu hướng và các yếu tố gây ra chi phí.
- **Consolidated Billing:** Tính năng của AWS Organizations gộp hóa đơn của nhiều tài khoản AWS thành một.
- **AWS Trusted Advisor:** Công cụ khuyến nghị giám sát tài khoản trong năm lĩnh vực, bao gồm **Cost Optimization** và **Performance**.
- **AWS Support Plans:** Gói **Basic** là miễn phí. Gói **Business** và **Enterprise** cung cấp tất cả các Trusted Advisor checks.
- **SLAs (Service Level Agreements):** AWS cung cấp cam kết về thời gian hoạt động; nếu không đạt được, khách hàng có thể nhận được các khoản tín dụng dịch vụ (service credits).

### 💰 TCO & Migration

- **Total Cost of Ownership (TCO):** Ước tính tài chính so sánh chi phí **trực tiếp và gián tiếp** của việc sở hữu cơ sở hạ tầng on-premise so với việc sử dụng AWS.
- **CAPEX vs OPEX:** Di chuyển sang đám mây cho phép các doanh nghiệp chuyển từ **Chi phí Vốn (CAPEX)** (chi tiêu trả trước cho phần cứng) sang **Chi phí Vận hành (OPEX)** (chi phí biến đổi, pay-as-you-go). Điều này cho phép tập trung vào kinh doanh thay vì hạ tầng.
- **Migration Evaluator:** Một công cụ được sử dụng để thu thập dữ liệu về cơ sở hạ tầng on-premise (agentless collector) nhằm ước tính chi phí so với AWS.
- **Cloud Adoption Framework (CAF):** Whitepaper cấp cao giúp tổ chức lập kế hoạch di chuyển.

### 🧱 AWS Well-Architected Framework (Tối ưu hóa Chi phí)

- **Ngừng chi tiền cho công việc nặng nhọc không tạo ra sự khác biệt (Stop Spending Money on Undifferentiated Heavy Lifting):** Hãy để AWS xử lý các hoạt động trung tâm dữ liệu (racking, cooling, patching).

### ⚙️ Management & Development Tools

Các công cụ này giúp giảm chi phí quản lý bằng cách tự động hóa và tăng hiệu quả vận hành:

- **Infrastructure as Code (IaC):** Viết code để định nghĩa và quản lý cơ sở hạ tầng đám mây. IaC là một nguyên tắc cơ bản cho **Operational Excellence** và Tối ưu hóa chi phí. Service Catalog
- **AWS CloudFormation (CFN):** Công cụ IaC **khai báo** (declarative) sử dụng template JSON/YAML để tự động hóa triển khai.
- **AWS CLI & CloudShell:** Cung cấp các giao diện hiệu quả để quản lý tài nguyên. **CloudShell** là giao diện shell dựa trên web, tiện lợi và miễn phí (1GB storage).
- **AWS Toolkit for VSCode:** Plugin giúp nhà phát triển làm việc với tài nguyên AWS một cách lập trình (programmatically) ngay trong IDE.


<div style="display: flex; gap: 10px; overflow-x: auto;">
  <img src="link_to_image1.jpg" style="height: 150px; object-fit: cover;">
  <img src="link_to_image2.jpg" style="height: 150px; object-fit: cover;">
  <img src="link_to_image3.jpg" style="height: 150px; object-fit: cover;">
</div>
