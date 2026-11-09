# Báo cáo nhóm — Day 02 Discovery & Problem Framing

> Bản chung của nhóm, viết trên repo do nhóm trưởng fork. Không copy file này sang repo cá nhân.
> Template chi tiết và prompt mẫu: [docs/01-worksheet.md](../../docs/01-worksheet.md). Bài mẫu: [docs/02-deliverable-example.md](../../docs/02-deliverable-example.md).

## 1. Thông tin nhóm

- Tên nhóm:
- Thành viên: xem `TEAM.md`
- Candidate problem được chọn (1 câu):
- Quyết định cuối: Go / Not Yet / No-Go

---

## 2. Hội tụ nhóm (CP3)

### 2.1. Pitch

|   # | Người đưa ra       | Candidate (Job Story ngắn)                                                                                                                                                | Actor                                          | Bottleneck                                                                                                      | Câu hỏi phản biện nhận được (ai hỏi) |
| --: | ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | ------------------------------------ |
|   1 | Thiều Thế Ngọc     | Khi nhận ticket mới từ khách hàng hoặc BA, tôi muốn hiểu yêu cầu và các task kỹ thuật cần làm, để lập kế hoạch phát triển phù hợp                                         | Developer; BA/khách hàng cung cấp yêu cầu      | Phân tích ticket: 20–30 phút/ticket (15–20 ticket/tuần)                                                         |                                      |
|   2 | Thiều Thế Ngọc     | Khi gặp lỗi trong quá trình phát triển, tôi muốn tìm nguyên nhân và hướng khắc phục, để giảm thời gian debug                                                              | Developer                                      | Debug lỗi: 20–45 phút/lỗi (3–5 lỗi/ngày)                                                                        |                                      |
|   3 | Thiều Thế Ngọc     | Khi cân nhắc mua sản phẩm có nhiều đánh giá, tôi muốn tổng hợp ưu/nhược điểm và độ tin cậy, để quyết định mua tốt hơn                                                     | Người mua hàng                                 | Đọc và tổng hợp 500–1.000 đánh giá mất 20–30 phút/sản phẩm                                                      |                                      |
|   4 | Trần Trọng Đứa Tài | Khi bắt đầu lab hoặc bài tập lớn mới, tôi muốn kiểm tra nhanh checklist cấu trúc repo và format nộp bài, để tránh bị trừ điểm vì lỗi quy cách cơ bản                      | Sinh viên trong nhóm (3–4 bạn)                 | Đối chiếu rubric thủ công mất 30–40 phút/bài; có 1–7 bài lab mỗi tuần                                           |                                      |
|   5 | Trần Trọng Đứa Tài | Khi đến hạn họp tiến độ nhóm hằng tuần, tôi muốn biết ai đã hoàn thành phần nào và ai đang bị kẹt, để kịp thời phân chia lại công việc trước deadline                     | Trưởng nhóm và các thành viên                  | Họp 1–2 lần/tuần; mất 20–25 phút hỏi từng người do tin nhắn Discord bị trôi                                     |                                      |
|   6 | Trần Trọng Đứa Tài | Khi chuẩn bị đến giờ học, tôi muốn xem lịch học, tiến độ và thời hạn ngay trên Phoenix, để không phải tìm qua email, file HTML và tra cứu lại trên web                    | Sinh viên khóa AI thực chiến (hơn 6.000 người) | Mỗi tuần 3–4 buổi; mỗi lần tra cứu mất 1,5–2 phút qua nhiều bước; từng có người vào lớp trễ do tìm nhầm link cũ |                                      |
|   7 | Vũ Tấn Đạt         | Khi cần dùng tài nguyên chung như thiết bị, robot thử nghiệm, nhân sự hoặc pin, tôi muốn biết lịch và mức ưu tiên rõ ràng, để tránh xung đột hoặc chờ đợi không cần thiết | Các phòng, PMO                                 | Nhiều lần xung đột lịch/tài nguyên trong một tháng; có thể đối chiếu tin nhắn và lịch đặt                       |
|   8 | Vũ Tấn Đạt         | Khi dự án cần phối hợp giữa hai phòng trở lên, tôi muốn biết việc nào đang chờ phòng nào, để xử lý điểm nghẽn trước khi trễ mốc                                           | PMO, các phòng liên quan                       | 20 dự án phụ thuộc chéo phòng; 7 lần trễ mốc trong một tháng do chờ phòng khác                                  |
|   9 | Vũ Tấn Đạt         | Khi họp review dự án, tôi muốn nắm nhanh rủi ro và blocker từ báo cáo, tin nhắn và biên bản của nhiều phòng, để đưa đúng vấn đề lên bàn họp                               | PMO, trưởng phòng                              | Mỗi kỳ review phải đọc khoảng 50 tài liệu/kênh; mất 1–2 giờ chuẩn bị                                            |

### 2.2. Cluster

| Cluster | Các candidate | Pattern chung                                                                                                                                                                                                        |
| ------- | ------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| A       | #7, #8, #9    | Quản lý quy trình và phối hợp liên phòng ban (PMO/quản trị dự án): tối ưu phân bổ tài nguyên dùng chung, theo dõi phụ thuộc chéo giữa các phòng ban, tổng hợp rủi ro và blocker để chuẩn bị họp review dự án.        |
| B       | #1, #2, #4    | Tối ưu quy trình kỹ thuật và đảm bảo chất lượng (developer/sinh viên kỹ thuật): giảm thời gian phân tích ticket/yêu cầu, tăng tốc debug lỗi kỹ thuật, tự động hóa kiểm tra checklist/rubric về quy cách repo.        |
| C       | #3, #5, #6    | Tổng hợp thông tin và theo dõi tiến độ cá nhân/nhóm (người dùng cuối/trưởng nhóm/sinh viên): tóm tắt đánh giá sản phẩm, cập nhật tiến độ công việc hằng tuần để tránh trôi tin nhắn, tra cứu nhanh lịch học/Phoenix. |

### 2.3. Opportunity Solution Tree rút gọn

Gốc là **1 outcome**. Nhánh là **opportunity** (nhu cầu, pain), không phải tính năng hay công cụ.

```text
OUTCOME: Cắt giảm tối đa thời gian lãng phí vào các tác vụ tra cứu, rà soát thủ công và chờ đợi thông tin, giúp cá nhân và đội ngũ tập trung vào công việc cốt lõi.
├── Opportunity A (Cluster A — Quản lý quy trình và PMO):
│   Thiếu thông tin kịp thời về phụ thuộc chéo giữa các bên và xung đột lịch tài nguyên dùng chung, dẫn đến chờ đợi và trễ mốc dự án.
├── Opportunity B (Cluster B — Quy trình kỹ thuật và đảm bảo chất lượng):
│   Developer và sinh viên kỹ thuật mất nhiều thời gian cho các công đoạn rà soát cơ học lặp lại như phân tích ticket chưa rõ, đối chiếu checklist/rubric thủ công và tìm nguyên nhân lỗi trong log.
└── Opportunity C (Cluster C — Tổng hợp thông tin và theo dõi tiến độ):
    Người dùng và thành viên nhóm phải tự tổng hợp thông tin từ nhiều nguồn rời rạc, như đánh giá sản phẩm, tin nhắn Discord và lịch học trên HTML/Phoenix.
```

Những ý đã gạch bỏ vì là solution đội lốt opportunity:

- ✗ “Xây dựng hệ thống Calendar/Booking tự động phân quyền tài nguyên” — opportunity thật là tránh xung đột lịch và giảm thời gian chờ thiết bị.
- ✗ “Dùng Copilot/Cursor tự động sửa code và đọc traceback” — opportunity thật là giảm thời gian tìm đúng nguyên nhân gây lỗi kỹ thuật.
- ✗ “Xây dựng chatbot AI tự động tóm tắt đánh giá sản phẩm” — opportunity thật là nắm nhanh ưu/nhược điểm chính để ra quyết định mua hàng.
- ✗ “Viết bot nhắc lịch học và tự động đồng bộ lịch” — opportunity thật là tra cứu lịch học và thông tin liên quan thuận tiện, không phải tìm qua nhiều nguồn.

### 2.4. Chấm điểm shortlist (1–5)

| Candidate                               | Actor rõ | Quy trình rõ | Pain có bằng chứng | Impact đo được | Vừa sức lab | So sánh được No AI/Rule/Workflow/Agent | Nhóm hiểu domain | Tổng |
| --------------------------------------- | -------: | -----------: | -----------------: | -------------: | ----------: | -------------------------------------: | ---------------: | ---: |
| #1 Phân tích ticket mới                 |        4 |            4 |                  4 |              5 |           3 |                                      5 |                3 |   28 |
| #2 Debug lỗi                            |        5 |            4 |                  5 |              5 |           3 |                                      5 |                3 |   30 |
| #3 Tổng hợp đánh giá sản phẩm           |        4 |            3 |                  3 |              3 |           4 |                                      5 |                3 |   25 |
| #4 Checklist lab/rubric                 |        4 |            4 |                  4 |              4 |           5 |                                      4 |                3 |   28 |
| #5 Theo dõi tiến độ nhóm                |        4 |            4 |                  4 |              4 |           4 |                                      4 |                3 |   27 |
| #6 Tra cứu lịch học/Phoenix             |        4 |            3 |                  3 |              2 |           2 |                                      4 |                3 |   21 |
| #7 Phân bổ tài nguyên chung             |        3 |            3 |                  3 |              3 |           3 |                                      4 |                3 |   22 |
| #8 Theo dõi phụ thuộc liên phòng ban    |        4 |            4 |                  5 |              4 |           3 |                                      4 |                3 |   27 |
| #9 Tổng hợp rủi ro/blocker trước review |        4 |            4 |                  4 |              4 |           4 |                                      5 |                3 |   28 |

**Candidate được chọn:** #2 — Debug lỗi: khi gặp lỗi trong quá trình phát triển, developer muốn xác định nguyên nhân và hướng khắc phục để giảm thời gian debug.

**Vì sao chọn:** Đạt điểm cao nhất trong bảng sơ bộ (30/35); actor rõ, pain có bằng chứng định lượng (3–5 lỗi/ngày, 20–45 phút/lỗi), impact đo được và có thể so sánh phương án No AI/Rule/Workflow/Agent. Vấn đề cũng gắn trực tiếp với quy trình phát triển kỹ thuật.

**Vì sao loại các candidate còn lại:** Chọn #2 làm phạm vi ưu tiên cho vòng tiếp theo, không có nghĩa các vấn đề khác không quan trọng. Các candidate còn lại hiện có mức độ khả thi hoặc bằng chứng thấp hơn, phụ thuộc nhiều bên/dữ liệu hơn, hoặc cần thu hẹp quy trình và kiểm chứng thêm. Cụ thể, #6 mới mất khoảng 1–2 phút mỗi lần tra cứu; #7–#9 cần phối hợp liên phòng ban và có thể liên quan dữ liệu nội bộ; #3, #5 cần kiểm chứng thêm hành vi và tần suất người dùng. #1 và #4 vẫn là các lựa chọn gần điểm, nhưng nhóm ưu tiên pain debug có tần suất cao và thời gian baseline rõ hơn.

## **Xử lý bất đồng (nếu có):** Chưa ghi nhận bất đồng trong thông tin hiện có.

## 3. Kiểm chứng + research giải pháp đã có (CP4)

### 3.1. Assumption Map

|   # | Giả định | Loại (Value / Usability / Feasibility / Viability) | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
| --: | -------- | -------------------------------------------------- | ---------------: | ---------------------: | ----------------- |
|   1 | Developer gặp 3–5 lỗi cần debug mỗi ngày và mất 20–45 phút cho mỗi lỗi như ước tính ban đầu. | Value | 5 | 2 | Có |
|   2 | Đọc log, khoanh vùng nguyên nhân và tìm hướng xử lý là phần tốn thời gian đáng kể trong quy trình debug. | Value | 5 | 1 | Có |
|   3 | Gợi ý dựa trên error log và một phần context liên quan của dự án có thể hữu ích hơn việc dev tự đưa traceback vào công cụ LLM hiện có. | Value | 5 | 1 | Có |
|   4 | Có thể cung cấp đủ context liên quan để đưa ra giả thuyết nguyên nhân mà không cần gửi toàn bộ mã nguồn hoặc vượt giới hạn context. | Feasibility | 5 | 1 | Có |
|   5 | Developer có thể hiểu căn cứ của gợi ý, xác minh nó và dùng kết quả mà không làm tăng sửa sai hoặc lỗi tái phát. | Usability | 5 | 1 | Có |
|   6 | Log và context mã nguồn có thể được xử lý theo chính sách bảo mật dự án, với chi phí và độ trễ chấp nhận được. | Viability | 5 | 1 | Có |

_Điền 4–6 giả định; xóa dòng thừa._

Giả định nhóm kiểm chứng trong buổi này: Trước tiên xác nhận #1–#2 bằng trao đổi với developer và xem lại các lần debug gần đây; kiểm tra #3–#5 bằng một số lỗi đã xử lý và so sánh với quy trình/công cụ hiện tại. Chỉ thử với log và mã nguồn sau khi xác nhận #6 về bảo mật, chi phí và độ trễ. Điểm bằng chứng là ước lượng sơ bộ, cần cập nhật sau kiểm chứng.

### 3.2. Kiểm chứng

**Cách đã dùng:** Phỏng vấn nhanh 1 developer; snapshot dưới đây là một mẫu định tính, chưa đại diện cho toàn bộ developer.

Interview snapshot (mỗi buổi phỏng vấn một bảng, hoặc đặt file trong `report/assets/cp4-interview-snapshot-N.md`):

| Trường                                            | Nội dung |
| ------------------------------------------------- | -------- |
| Người được hỏi (vai trò, không ghi tên thật)      | Developer (Dev); phỏng vấn ngày 09/11/2026. |
| Câu nói đáng nhớ nhất (nguyên văn)                | “Không tìm đúng lỗi để sửa nó sẽ phát sinh lỗi chồng lỗi.” |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | Ngày 09/11/2026, Dev gặp một bug và phải lần theo log cùng các file liên quan để tìm nguyên nhân. |
| Hiện đang xử lý bằng cách nào (workaround)?       | Tìm nguyên nhân bug theo từng log và truy vấn các file tham chiếu. |
| Mất bao lâu, bao lần?                             | Ước lượng của người được hỏi: 10–20 phút cho bug nhỏ, 1–2 giờ cho bug lớn; chưa có nhật ký bấm giờ để đối chiếu. |
| Insight / opportunity rút ra                      | Developer mất nhiều thời gian xác định đúng nguyên nhân; sửa sai có thể gây lỗi chồng lỗi. Cơ hội là hỗ trợ phân tích log, tìm code liên quan và đề xuất hướng xử lý kèm bước xác minh, nhưng developer vẫn phải kiểm tra trước khi sửa. |

Tổng hợp:

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác |
| ----- | ----------------: | ----------------- | ----------------- |
| Phỏng vấn developer (snapshot 09/11/2026) | 1 | Việc tìm nguyên nhân hiện cần lần theo từng log và các file liên quan; người được hỏi nhận định sửa khi chưa tìm đúng lỗi có thể gây lỗi chồng lỗi. Điều này ủng hộ giả định rằng việc khoanh vùng nguyên nhân là một pain point đáng khảo sát. | Thời gian tự ước lượng là 10–20 phút/bug nhỏ và 1–2 giờ/bug lớn, không khớp với giả định ban đầu 20–45 phút cho mỗi lỗi nếu áp dụng chung cho mọi bug. Chưa có bằng chứng về tần suất 3–5 lỗi/ngày; một cuộc phỏng vấn không đủ đại diện để kết luận cho nhóm developer. |

**Nhóm đã sửa problem thế nào sau kiểm chứng:**

Thu hẹp problem từ giả định ban đầu “debug lỗi mất 20–45 phút/lỗi” thành vấn đề cần kiểm chứng cụ thể hơn: developer tốn thời gian lần theo log và code liên quan để tìm nguyên nhân; thời gian tự ước lượng khác nhau theo độ lớn của bug (10–20 phút với bug nhỏ, 1–2 giờ với bug lớn). Cập nhật hướng hỗ trợ thành phân tích log/context, truy tìm code liên quan và đề xuất bước kiểm tra; không coi gợi ý là kết luận hay để AI tự sửa. Chưa đủ dữ liệu để xác nhận tần suất lỗi, baseline đại diện, hoặc bottleneck luôn nằm ở phân tích log; cần ghi thời gian trên nhiều lỗi và hỏi thêm developer.

### 3.3. Research giải pháp đã có

| Công cụ / case / pattern | Link | Giải bước nào trong quy trình? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
| ------------------------ | ---- | ------------------------------ | --------- | --------------------- | ---------------- |
| GitHub Copilot | [GitHub Copilot Chat trong IDE](https://docs.github.com/en/copilot/how-tos/copilot-in-your-ide/chat-with-copilot/chat-in-ide) | Phân tích lỗi, đọc code liên quan, xác định nguyên nhân và đề xuất hướng sửa. | Tích hợp trong IDE, tận dụng repository context, hỗ trợ trực tiếp trong workflow của developer. | Có thể thiếu context nên gợi ý vẫn cần developer kiểm chứng. | Cần kết hợp error log với code liên quan, không chỉ phân tích log độc lập. |

---

## 4. Quy trình trước/sau (CP5)

### 4.1. Quy trình hiện tại

Sơ đồ (ASCII, Mermaid hoặc link ảnh trong `report/assets/`):

```text

```

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú |
| ---: | ----- | ----- | ------ | -------------------- | ------- |
|    1 |       |       |        |                      |         |
|    2 |       |       |        |                      |         |
|    3 |       |       |        |                      |         |
|    4 |       |       |        |                      |         |
|    5 |       |       |        |                      |         |

**Bottleneck chính:**

### 4.2. Quy trình tương lai

Ghi rõ bước nào **Rule**, bước nào **AI**, bước nào **con người**, **boundary** ở đâu, **phương án quay về** khi AI sai.

```text

```

### 4.3. Before / after

| Chỉ số               | Trước | Sau (kỳ vọng) | Ghi chú |
| -------------------- | ----: | ------------: | ------- |
| Số bước              |       |               |         |
| Tổng thời gian       |       |               |         |
| Số bước thủ công     |       |               |         |
| Bottleneck chính     |       |               |         |
| Rủi ro mới phát sinh |       |               |         |

---

## 5. Problem Statement v0 (CP5)

| Trường                                                                     | Nội dung |
| -------------------------------------------------------------------------- | -------- |
| **Actor**                                                                  |          |
| **Quy trình**                                                              |          |
| **Bottleneck**                                                             |          |
| **Impact**                                                                 |          |
| **Success Metric** (baseline → target, cách đo)                            |          |
| **Boundary** (AI không được làm gì; khi nào cần con người kiểm tra — HITL) |          |

Phản biện nhận được (từ AI hoặc nhóm khác) và nhóm có đồng ý không:

- ***

## 6. Mức can thiệp AI (CP6)

### 6.1. Ma trận độ mơ hồ × độ phức tạp

Bài của nhóm nằm ở ô:

Vì sao:

### 6.2. So sánh 4 mức

| Mức                       | Phương án cho bài của nhóm | Đủ khi nào | Rủi ro | Chọn? |
| ------------------------- | -------------------------- | ---------- | ------ | ----- |
| **No AI** (sửa quy trình) |                            |            |        |       |
| **Rule**                  |                            |            |        |       |
| **Workflow**              |                            |            |        |       |
| **Agent**                 |                            |            |        |       |

**Mức chọn:**

**Vì sao không chọn mức đơn giản hơn:**

### 6.3. AI Canvas rút gọn

| Thành phần                                                        | Nội dung |
| ----------------------------------------------------------------- | -------- |
| **Prediction** — AI dự đoán / tạo ra gì?                          |          |
| **Judgment** — con người cân nhắc, quyết định gì?                 |          |
| **Action** — hành động cuối cùng là gì, ai làm?                   |          |
| **Outcome** — đo kết quả bằng gì?                                 |          |
| **Input** — AI cần dữ liệu đầu vào gì mỗi lần chạy? Có sẵn không? |          |
| **Feedback** — lấy phản hồi ở đâu để cải thiện?                   |          |

### 6.4. Hai câu hỏi của Google PAIR

- Người dùng muốn **được hỗ trợ (augment)** hay **giao hẳn việc (automate)**? Bằng chứng:
- AI sai kiểu nào tệ hơn, **báo nhầm** hay **bỏ sót**? Vì sao, và thiết kế đã xử lý thế nào:

---

## 7. Problem Statement v1 + tiêu chí đánh giá (CP6)

| Trường                                          | Nội dung                        |
| ----------------------------------------------- | ------------------------------- |
| **Actor**                                       |                                 |
| **Quy trình**                                   |                                 |
| **Bottleneck**                                  |                                 |
| **Impact**                                      |                                 |
| **Success Metric** (baseline → target, cách đo) |                                 |
| **Boundary**                                    |                                 |
| **AI intervention point**                       |                                 |
| **Mức chọn**                                    | No AI / Rule / Workflow / Agent |
| **Rủi ro & người kiểm tra**                     |                                 |

**Thay đổi so với v0 và lý do:**

| Trường | v0  | v1  | Vì sao đổi |
| ------ | --- | --- | ---------- |
|        |     |     |            |

**Tiêu chí đánh giá đầu ra của AI (3–5 tiêu chí):**

|   # | Tiêu chí | Đạt khi | Không đạt khi |
| --: | -------- | ------- | ------------- |
|   1 |          |         |               |
|   2 |          |         |               |
|   3 |          |         |               |

---

## 8. Quyết định (CP6)

### 8.1. Bốn rủi ro

| Rủi ro          | Câu hỏi                                                           | Mức độ rủi ro (Thấp = an toàn / TB / Cao = nguy hiểm) | Lý do / bằng chứng |
| --------------- | ----------------------------------------------------------------- | ----------------------------------------------------- | ------------------ |
| **Value**       | Người dùng có thật sự cần và sẽ dùng không?                       |                                                       |                    |
| **Usability**   | Người dùng có dùng được, có hiểu và sửa được đầu ra của AI không? |                                                       |                    |
| **Feasibility** | Có đủ dữ liệu, công cụ, kỹ năng để làm không?                     |                                                       |                    |
| **Viability**   | Có hợp chi phí, pháp lý, quy định tổ chức không? Ai vận hành?     |                                                       |                    |

### 8.2. Kết luận

**Quyết định:** Go / Not Yet / No-Go

**Lý do:**

**Nếu Go — pilot nhỏ nhất:**

**Nếu Not Yet — cần kiểm chứng gì trước:**

**Nếu No-Go — nên làm gì thay AI:**

**Ngưỡng dừng** (nếu sau … mà … thì quay về …):

---

## 9. Hạn chế và hướng tiếp theo

-

## 10. Tài liệu tham khảo

-
