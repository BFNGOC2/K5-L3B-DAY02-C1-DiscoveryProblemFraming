# Báo cáo nhóm — Day 02 Discovery & Problem Framing

> Bản chung của nhóm, viết trên repo do nhóm trưởng fork. Không copy file này sang repo cá nhân.
> Template chi tiết và prompt mẫu: [docs/01-worksheet.md](../../docs/01-worksheet.md). Bài mẫu: [docs/02-deliverable-example.md](../../docs/02-deliverable-example.md).

## 1. Thông tin nhóm

- Tên nhóm: C1
- Thành viên: xem `TEAM.md`
- Candidate problem được chọn (1 câu): Khi developer gặp lỗi trong quá trình phát triển, họ muốn lần ra nguyên nhân từ log/traceback và code liên quan để xử lý lỗi mà không tạo thêm lỗi mới.
- Quyết định cuối: **Not Yet**

---

## 2. Hội tụ nhóm (CP3)

### 2.1. Pitch

|   # | Người đưa ra       | Candidate (Job Story ngắn)                                                                                                                                                | Actor                                          | Bottleneck                                                                                                      | Câu hỏi phản biện nhận được (ai hỏi) |
| --: | ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | ------------------------------------ |
|   1 | Thiều Thế Ngọc     | Khi nhận ticket mới từ khách hàng hoặc BA, tôi muốn hiểu yêu cầu và các task kỹ thuật cần làm, để lập kế hoạch phát triển phù hợp                                         | Developer; BA/khách hàng cung cấp yêu cầu      | Phân tích ticket: 20–30 phút/ticket (15–20 ticket/tuần)                                                         |                                      |
|   2 | Thiều Thế Ngọc     | Khi gặp lỗi trong quá trình phát triển, tôi muốn tìm nguyên nhân và hướng khắc phục, để giảm thời gian debug                                                              | Developer                                      | Debug lỗi: 20–45 phút/lỗi (3–5 lỗi/ngày)                                                                        |                                      |
|   3 | Thiều Thế Ngọc     | Khi cân nhắc mua sản phẩm có nhiều đánh giá, tôi muốn tổng hợp ưu/nhược điểm và độ tin cậy, để quyết định mua tốt hơn                                                     | Người mua hàng                                 | Đọc và tổng hợp 500–1.000 đánh giá mất 20–30 phút/sản phẩm                                                      |                                      |
|   4 | Trần Trọng Đức Tài | Khi bắt đầu lab hoặc bài tập lớn mới, tôi muốn kiểm tra nhanh checklist cấu trúc repo và format nộp bài, để tránh bị trừ điểm vì lỗi quy cách cơ bản                      | Sinh viên trong nhóm (3–4 bạn)                 | Đối chiếu rubric thủ công mất 30–40 phút/bài; có 1–7 bài lab mỗi tuần                                           |                                      |
|   5 | Trần Trọng Đức Tài | Khi đến hạn họp tiến độ nhóm hằng tuần, tôi muốn biết ai đã hoàn thành phần nào và ai đang bị kẹt, để kịp thời phân chia lại công việc trước deadline                     | Trưởng nhóm và các thành viên                  | Họp 1–2 lần/tuần; mất 20–25 phút hỏi từng người do tin nhắn Discord bị trôi                                     |                                      |
|   6 | Trần Trọng Đức Tài | Khi chuẩn bị đến giờ học, tôi muốn xem lịch học, tiến độ và thời hạn ngay trên Phoenix, để không phải tìm qua email, file HTML và tra cứu lại trên web                    | Sinh viên khóa AI thực chiến (hơn 6.000 người) | Mỗi tuần 3–4 buổi; mỗi lần tra cứu mất 1,5–2 phút qua nhiều bước; từng có người vào lớp trễ do tìm nhầm link cũ |                                      |
|   7 | Vũ Tuấn Đạt        | Khi cần dùng tài nguyên chung như thiết bị, robot thử nghiệm, nhân sự hoặc pin, tôi muốn biết lịch và mức ưu tiên rõ ràng, để tránh xung đột hoặc chờ đợi không cần thiết | Các phòng, PMO                                 | Nhiều lần xung đột lịch/tài nguyên trong một tháng; có thể đối chiếu tin nhắn và lịch đặt                       |
|   8 | Vũ Tuấn Đạt        | Khi dự án cần phối hợp giữa hai phòng trở lên, tôi muốn biết việc nào đang chờ phòng nào, để xử lý điểm nghẽn trước khi trễ mốc                                           | PMO, các phòng liên quan                       | 20 dự án phụ thuộc chéo phòng; 7 lần trễ mốc trong một tháng do chờ phòng khác                                  |
|   9 | Vũ Tuấn Đạt        | Khi họp review dự án, tôi muốn nắm nhanh rủi ro và blocker từ báo cáo, tin nhắn và biên bản của nhiều phòng, để đưa đúng vấn đề lên bàn họp                               | PMO, trưởng phòng                              | Mỗi kỳ review phải đọc khoảng 50 tài liệu/kênh; mất 1–2 giờ chuẩn bị                                            |

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

|   # | Giả định                                                                                                                               | Loại (Value / Usability / Feasibility / Viability) | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
| --: | -------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------- | ---------------: | ---------------------: | ----------------- |
|   1 | Developer gặp 3–5 lỗi cần debug mỗi ngày và mất 20–45 phút cho mỗi lỗi như ước tính ban đầu.                                           | Value                                              |                5 |                      2 | Có                |
|   2 | Đọc log, khoanh vùng nguyên nhân và tìm hướng xử lý là phần tốn thời gian đáng kể trong quy trình debug.                               | Value                                              |                5 |                      1 | Có                |
|   3 | Gợi ý dựa trên error log và một phần context liên quan của dự án có thể hữu ích hơn việc dev tự đưa traceback vào công cụ LLM hiện có. | Value                                              |                5 |                      1 | Có                |
|   4 | Có thể cung cấp đủ context liên quan để đưa ra giả thuyết nguyên nhân mà không cần gửi toàn bộ mã nguồn hoặc vượt giới hạn context.    | Feasibility                                        |                5 |                      1 | Có                |
|   5 | Developer có thể hiểu căn cứ của gợi ý, xác minh nó và dùng kết quả mà không làm tăng sửa sai hoặc lỗi tái phát.                       | Usability                                          |                5 |                      1 | Có                |
|   6 | Log và context mã nguồn có thể được xử lý theo chính sách bảo mật dự án, với chi phí và độ trễ chấp nhận được.                         | Viability                                          |                5 |                      1 | Có                |

_Điền 4–6 giả định; xóa dòng thừa._

Giả định nhóm kiểm chứng trong buổi này: Trước tiên xác nhận #1–#2 bằng trao đổi với developer và xem lại các lần debug gần đây; kiểm tra #3–#5 bằng một số lỗi đã xử lý và so sánh với quy trình/công cụ hiện tại. Chỉ thử với log và mã nguồn sau khi xác nhận #6 về bảo mật, chi phí và độ trễ. Điểm bằng chứng là ước lượng sơ bộ, cần cập nhật sau kiểm chứng.

### 3.2. Kiểm chứng

**Cách đã dùng:** Phỏng vấn sâu 3 người và hỏi nhanh 5 sinh viên trong lớp. Ba snapshot phỏng vấn được ghi bên dưới; cỡ mẫu nhỏ, kết quả chỉ là tín hiệu ban đầu.

Interview snapshot #1:

| Trường                                            | Nội dung                                                                                                                                                                                                                                 |
| ------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Người được hỏi (vai trò, không ghi tên thật)      | Developer (Dev); phỏng vấn ngày 09/11/2026.                                                                                                                                                                                              |
| Câu nói đáng nhớ nhất (nguyên văn)                | “Không tìm đúng lỗi để sửa nó sẽ phát sinh lỗi chồng lỗi.”                                                                                                                                                                               |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | Ngày 09/11/2026, Dev gặp một bug và phải lần theo log cùng các file liên quan để tìm nguyên nhân.                                                                                                                                        |
| Hiện đang xử lý bằng cách nào (workaround)?       | Tìm nguyên nhân bug theo từng log và truy vấn các file tham chiếu.                                                                                                                                                                       |
| Mất bao lâu, bao lần?                             | Ước lượng của người được hỏi: 10–20 phút cho bug nhỏ, 1–2 giờ cho bug lớn; chưa có nhật ký bấm giờ để đối chiếu.                                                                                                                         |
| Insight / opportunity rút ra                      | Developer mất nhiều thời gian xác định đúng nguyên nhân; sửa sai có thể gây lỗi chồng lỗi. Cơ hội là hỗ trợ phân tích log, tìm code liên quan và đề xuất hướng xử lý kèm bước xác minh, nhưng developer vẫn phải kiểm tra trước khi sửa. |

Interview snapshot #2 (sinh viên CNTT):

| Trường                                            | Nội dung                                                                                                                                                                                                                                                                        |
| ------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Người được hỏi (vai trò, không ghi tên thật)      | Sinh viên ngành CNTT, đang làm bài tập lớn môn Lập trình Web; năm học chưa được ghi rõ.                                                                                                                                                                                         |
| Câu nói đáng nhớ nhất (nguyên văn)                | “Traceback báo lỗi đỏ lòm cả trang toàn tiếng Anh chuyên ngành, em nhìn hoa cả mắt không biết bắt đầu sửa từ dòng nào, đành bấm Ctrl+Z quay về từ đầu.”                                                                                                                         |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | Tối hôm kia, khi làm đồ án môn Web bằng NodeJS, submit form thì server báo `UnhandledPromiseRejection`. Người được hỏi mất hơn một tiếng tra Google từng dòng lỗi; thử dán code tìm được trên mạng làm hỏng cả trang.                                                           |
| Hiện đang xử lý bằng cách nào (workaround)?       | Hỏi bạn cùng bàn hoặc chụp màn hình gửi vào nhóm môn học để nhờ trợ giảng xem.                                                                                                                                                                                                  |
| Mất bao lâu, bao lần?                             | Theo người được hỏi, lỗi xảy ra liên tục mỗi đợt làm bài tập lớn; khoảng 30–45 phút/lỗi. Đây là tự ước lượng, chưa có nhật ký bấm giờ.                                                                                                                                          |
| Insight / opportunity rút ra                      | Với người mới, traceback dài và thuật ngữ chuyên ngành gây khó khăn khi xác định điểm bắt đầu. Cơ hội là giải thích lỗi bằng tiếng Việt, chỉ đến code liên quan trong project (không nhầm sang `node_modules`) và hướng dẫn bước kiểm chứng; không tự chèn code lạ vào project. |

Interview snapshot #3 (backend developer):

| Trường                                            | Nội dung |
| ------------------------------------------------- | -------- |
| Người được hỏi (vai trò, không ghi tên thật)      | Backend developer tại công ty phần mềm khoảng 30 người. |
| Tín hiệu đáng chú ý (diễn giải, không phải nguyên văn) | Người được hỏi cho biết suy luận lỗi bắt nguồn từ đâu tốn thời gian hơn việc đọc log để định vị lỗi. |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | Tuần trước gặp lỗi timeout ở một API; mất khoảng 40 phút mới khoanh được vùng nguyên nhân. |
| Hiện đang xử lý bằng cách nào (workaround)?       | Tìm lỗi tương tự trong Slack/Google, đưa traceback vào một công cụ LLM rồi tự kiểm tra. |
| Mất bao lâu, bao lần?                             | Người được hỏi ước lượng khoảng 3 lỗi/ngày, 20–40 phút/lỗi; thời gian từng bước chưa được bấm giờ. |
| Insight / opportunity rút ra                      | Điểm nghẽn không chỉ là đọc log mà là suy luận lỗi bắt nguồn từ đâu; developer đã có workaround dùng LLM nên giá trị bổ sung cần được chứng minh. |

Tổng hợp:

| Nguồn               | Số người / số mẫu | Tín hiệu xác nhận                                                                                                                                                                                                                            | Tín hiệu phản bác                                                                                                                                                                                                                                                                                                                                |
| ------------------- | ----------------: | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Phỏng vấn sâu       |                 3 | Cả 3 người xác nhận phần tốn thời gian nhất là lần tìm nguyên nhân, không phải gõ code sửa. Hai snapshot cho thấy cách tìm nguyên nhân gồm lần theo log và truy vấn các file liên quan (developer) hoặc tra từng dòng traceback (sinh viên). | 2/3 người, đặc biệt developer đi làm, không muốn AI tự sửa file vì lo hỏng chuẩn dự án; sinh viên lo code do AI tạo dùng thư viện lạ, không phù hợp yêu cầu bài. Một người cho rằng debug bằng breakpoint quen tay nên không cần thêm công cụ. Thời gian được tự ước lượng và khác theo loại/độ lớn bug; chưa đủ để xác nhận một baseline chung. |
| Hỏi nhanh trong lớp |                 5 | 4/5 người trả lời từng mất hơn 30 phút xử lý một lỗi logic chưa rõ nguyên nhân.                                                                                                                                                              | 1/5 cho biết đã quen tự debug bằng breakpoint và không cần thêm công cụ. Mẫu nhỏ, chưa đại diện cho sinh viên nói chung.                                                                                                                                                                                                                         |

**Nhóm đã sửa problem thế nào sau kiểm chứng:**

Kết quả 3 cuộc phỏng vấn và hỏi nhanh 5 sinh viên củng cố rằng khó khăn chính là lần tìm nguyên nhân; tuy nhiên, nhu cầu và khả năng chấp nhận tự động hóa khác nhau theo người dùng. Vì vậy, problem được làm rõ là hỗ trợ người dùng hiểu traceback, tìm code liên quan và kiểm chứng nguyên nhân, không phải để AI tự sửa file. Tín hiệu từ sinh viên nhấn mạnh cần giải thích dễ hiểu và chỉ đúng code trong project; developer vẫn cần kiểm soát thay đổi để giữ chuẩn dự án. Cỡ mẫu nhỏ và thời gian tự ước lượng nên chưa xác nhận baseline chung hoặc tần suất 3–5 lỗi/ngày; cần đo thêm trên nhiều lỗi và nhóm người dùng.

### 3.3. Research giải pháp đã có

| Công cụ / case / pattern | Link                                                                                                                          | Giải bước nào trong quy trình?                                                             | Điểm mạnh                                                                                                | Khoảng trống / rủi ro                                                                                                                               | Bài học cho nhóm                                                                                                                                            |
| ------------------------ | ----------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| GitHub Copilot           | [GitHub Copilot Chat trong IDE](https://docs.github.com/en/copilot/how-tos/copilot-in-your-ide/chat-with-copilot/chat-in-ide) | Phân tích lỗi, đọc code liên quan, xác định nguyên nhân và đề xuất hướng sửa.              | Tích hợp trong IDE, tận dụng repository context, hỗ trợ trực tiếp trong workflow của developer.          | Có thể thiếu context nên gợi ý vẫn cần developer kiểm chứng.                                                                                        | Cần kết hợp error log với code liên quan, không chỉ phân tích log độc lập.                                                                                  |
| Sentry                   | [Sentry](https://sentry.io/welcome/)                                                                                          | Bắt lỗi runtime, lưu stack trace và thông tin/lịch sử thao tác quanh thời điểm xảy ra lỗi. | Tự động gom lỗi và cung cấp ngữ cảnh runtime để developer biết lỗi xuất hiện ở đâu, trong điều kiện nào. | Theo ghi chú research của nhóm, công cụ giúp định vị và cung cấp ngữ cảnh nhưng không tự giải thích logic của ứng dụng hoặc đảm bảo hướng sửa đúng. | Ngữ cảnh runtime là input hữu ích để điều tra; giải pháp của nhóm cần kết hợp context này với code liên quan và vẫn yêu cầu developer xác minh nguyên nhân. |

---

## 4. Quy trình trước/sau (CP5)

### 4.1. Quy trình hiện tại

> Căn cứ: phỏng vấn sâu 3 người và hỏi nhanh 5 sinh viên. Backend developer ước lượng khoảng 3 lỗi/ngày và 20–40 phút/lỗi; một lỗi API timeout gần đây mất khoảng 40 phút để khoanh vùng. Snapshot developer khác ghi bug nhỏ 10–20 phút, bug lớn 1–2 giờ; sinh viên ước lượng 30–45 phút/lỗi và kể một lần gần đây mất hơn 1 giờ tra cứu. Đây là các tự ước lượng khác nhau, không gộp thành baseline chung. Thời gian từng bước chưa được đo riêng.

Sơ đồ (ASCII, Mermaid hoặc link ảnh trong `report/assets/`):

```text
HIỆN TẠI — thời gian tổng ước lượng khác nhau theo người và độ lớn lỗi

[1 Nhận thấy lỗi + lấy log/traceback: chưa đo riêng] → [2 Đọc log, xác định điểm lỗi: chưa đo riêng]
→ [3 Truy code liên quan, khoanh vùng nguyên nhân: thời gian chưa đo riêng; một lỗi timeout mất khoảng 40' để khoanh vùng] ← BOTTLENECK
→ [4 Đưa ra giả thuyết nguyên nhân + hướng xử lý: chưa đo riêng]
→ [5 Sửa + kiểm tra lại: chưa đo riêng]
(nếu giả thuyết sai → quay lại bước 3; sửa sai có thể gây "lỗi chồng lỗi")
```

| Bước | Actor     | Input                                              | Output                                               | Thời gian / tần suất                                                                   | Ghi chú                                 |
| ---: | --------- | -------------------------------------------------- | ---------------------------------------------------- | -------------------------------------------------------------------------------------- | --------------------------------------- |
|    1 | Developer | Lỗi khi chạy/phát triển (thông báo lỗi, test fail) | Log hoặc traceback của lỗi                           | Chưa đo riêng; backend developer ước lượng tổng cộng khoảng 3 lỗi/ngày                 | Cần xác nhận cách lấy log               |
|    2 | Developer | Log, traceback                                     | Điểm lỗi nghi ngờ (file, dòng, thông báo)            | Chưa đo riêng                                                                         |                                         |
|    3 | Developer | Điểm lỗi, các file tham chiếu liên quan            | Hiểu luồng chạy dẫn tới lỗi, khoanh vùng nguyên nhân | Chưa đo riêng; một lỗi API timeout mất khoảng 40 phút để khoanh vùng, không tách theo bước | Lần theo từng log và truy vấn từng file |
|    4 | Developer | Kết quả khoanh vùng                                | Giả thuyết nguyên nhân và hướng xử lý                | Chưa đo riêng                                                                         | Sai ở bước này dễ dẫn tới lỗi chồng lỗi |
|    5 | Developer | Hướng xử lý đã chọn                                | Bản sửa đã kiểm tra                                  | Chưa đo riêng                                                                         | Nếu không hết lỗi thì quay lại bước 3   |

**Bottleneck chính:** Bước 3, suy luận lỗi bắt nguồn từ đâu và lần theo code liên quan; backend developer cho biết đọc log để định vị lỗi nhanh hơn việc đoán nguồn gốc, và một lỗi API timeout gần đây mất khoảng 40 phút để khoanh vùng. Cả 3 người phỏng vấn nói tìm nguyên nhân là phần tốn thời gian nhất. Tuy nhiên, số phút từng bước chưa được bấm giờ và mẫu nhỏ; cần ghi thời gian theo từng bước trên các lỗi tiếp theo để xác nhận.

### 4.2. Quy trình tương lai

Ghi rõ bước nào **Rule**, bước nào **AI**, bước nào **con người**, **boundary** ở đâu, **phương án quay về** khi AI sai.

```text
TƯƠNG LAI — Kỳ vọng giảm 50–70% thời gian tìm nguyên nhân

[1 Lấy log/traceback khi gặp lỗi] (CON NGƯỜI kích hoạt / RULE bắt lỗi: 10s)
  ↓
[2 Đọc log, tự động bóc tách điểm lỗi: file, dòng, exception] (RULE: 5s)
  ↓
[3 Tự động trích xuất các file tham chiếu liên quan + AI khoanh vùng nguyên nhân] (RULE + AI: 30s)
  ↓
[4 AI đề xuất giả thuyết nguyên nhân & hướng xử lý → Dev thẩm định, chọn hướng] (AI + CON NGƯỜI: 5–7') ← BOUNDARY
  ↓
[5 Áp dụng bản sửa + Rule chạy test kiểm tra lại] (CON NGƯỜI + RULE: 1–2')
  ├── Nếu test pass: Hoàn thành
  └── Nếu test fail / AI đoán sai: Kích hoạt [PHƯƠNG ÁN QUAY VỀ] (Rollback về bước 3 thủ công)
```

**Phân định vai trò chi tiết:**

- **Bước 1 — Con người / Rule:** Developer gặp lỗi khi chạy/test và kích hoạt công cụ hỗ trợ debug (hoặc plugin tự động bắt lỗi từ console).
- **Bước 2 — Rule:** Script/Regex tự động bóc tách traceback sạch: xác định tên exception, file và số dòng nghi ngờ trong mã nguồn dự án, loại bỏ các dòng log rác từ thư viện bên ngoài.
- **Bước 3 — Rule + AI (Giải quyết Bottleneck chính):**
    - _Rule:_ Tự động quét call stack và nhặt đúng nội dung các hàm/file tham chiếu liên quan trong dự án (che các thông tin nhạy cảm như API key/password).
    - _AI:_ Đọc traceback kết hợp với context các file tham chiếu do Rule cung cấp để tái hiện luồng chạy và chỉ ra nguyên nhân gốc.
- **Bước 4 — AI + Con người (Human-in-the-loop — HITL):**
    - _AI:_ Sinh ra giả thuyết nguyên nhân bằng tiếng Việt ngắn gọn và đề xuất 1–2 hướng xử lý cụ thể (kèm code diff minh họa).
    - _Developer:_ Đọc giải thích, đối chiếu với logic nghiệp vụ thực tế để thẩm định giả thuyết của AI và chọn hướng xử lý phù hợp.
- **Bước 5 — Con người + Rule:** Developer áp dụng code sửa; Rule tự động kích hoạt test runner (unit test/linter) để xác nhận lỗi đã được khắc phục hoàn toàn.

**Boundary (Ranh giới an toàn):**

1. AI **tuyệt đối không được tự ý ghi đè file mã nguồn hay tự động commit git**; mọi thay đổi code bắt buộc phải qua bước Developer thẩm định và chấp thuận (Bước 4).
2. AI **chỉ được cung cấp các đoạn code trong các file tham chiếu liên quan trực tiếp đến traceback**, không được nạp toàn bộ mã nguồn dự án để đảm bảo bảo mật và không vượt context window.
3. Gợi ý của AI **chỉ được coi là giả thuyết tham khảo**, không được coi là kết luận tuyệt đối.

**Phương án quay về (Rollback / Fallback):**

- Nếu giả thuyết của AI sai lệch hoặc code sửa làm phát sinh lỗi mới (lỗi chồng lỗi / test fail): Developer bấm nút Rollback để hủy bỏ toàn bộ thay đổi, khôi phục mã nguồn về trạng thái ban đầu, tạm dừng gợi ý của AI và quay lại Bước 3 của quy trình thủ công (tự đặt log/breakpoint để lần theo file như ở 4.1).

### 4.3. Before / after

| Chỉ số               |                                                                                  Trước |                                                                                 Sau (kỳ vọng) | Ghi chú                                                                                                                                                          |
| -------------------- | -------------------------------------------------------------------------------------: | --------------------------------------------------------------------------------------------: | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Số bước              |                                                                                      5 |                                                                                             5 | Cùng số bước theo sơ đồ; thay đổi ở cách Rule/AI hỗ trợ các bước 2–4.                                                                                            |
| Tổng thời gian       | Developer: bug nhỏ 10–20 phút, bug lớn 1–2 giờ; sinh viên: 30–45 phút/lỗi tự ước lượng |                             Khoảng 7–10 phút theo ước tính các bước trong quy trình tương lai | Con số sau cộng từ thời lượng giả định ở mục 4.2, chưa được đo hay thử nghiệm; nhóm người dùng có baseline khác nhau nên không so sánh/gộp trực tiếp.            |
| Số bước thủ công     |                                                                                    5/5 |                                                                 3/5 có thao tác của con người | Tương lai: người dùng kích hoạt, developer thẩm định giả thuyết và tự áp dụng bản sửa; các bước khác có Rule/AI hỗ trợ.                                          |
| Bottleneck chính     |                    Lần theo traceback/log và file liên quan để khoanh vùng nguyên nhân |                                            Developer thẩm định giả thuyết và xác minh sửa lỗi | Phỏng vấn gợi ý đây là phần tốn thời gian; chưa có bấm giờ theo từng bước để xác nhận.                                                                           |
| Rủi ro mới phát sinh |                                                                                      — | AI đoán sai, lộ mã nguồn/log, đề xuất thay đổi không phù hợp chuẩn dự án hoặc yêu cầu bài tập | Chỉ dùng context tối thiểu đã được phép và khử bí mật; AI không sửa file/commit; người dùng kiểm tra và chạy test; nếu không an toàn thì quay về debug thủ công. |

---

## 5. Problem Statement v0 (CP5)

| Trường                                                                     | Nội dung                                                                                                                                                                                                                                                                                                                                                                         |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Actor**                                                                  | Developer và sinh viên CNTT đang tự xử lý lỗi runtime/logic trong project, đặc biệt khi chưa biết bắt đầu lần theo traceback hoặc code liên quan từ đâu. Nhu cầu của hai nhóm cần được đo riêng.                                                                                                                                                                                 |
| **Quy trình**                                                              | Khi gặp lỗi, người dùng đọc thông báo/traceback, tìm log và file liên quan để khoanh vùng nguyên nhân, chọn cách sửa rồi chạy lại để kiểm tra.                                                                                                                                                                                                                                   |
| **Bottleneck**                                                             | Xác định nguyên nhân từ traceback/log và lần theo code liên quan; cả 3 người phỏng vấn cho biết việc tìm nguyên nhân tốn thời gian nhất, nhưng thời lượng từng bước chưa được bấm giờ.                                                                                                                                                                                           |
| **Impact**                                                                 | Thời gian xử lý bị kéo dài và người dùng có thể thử cách sửa không phù hợp, làm phát sinh lỗi khác. Số liệu hiện có là tự ước lượng, khác nhau theo nhóm: developer báo 10–20 phút/bug nhỏ và 1–2 giờ/bug lớn; sinh viên báo 30–45 phút/lỗi, đồng thời kể một lần gần đây mất hơn 1 giờ tra cứu.                                                                                 |
| **Success Metric** (baseline → target, cách đo)                            | Baseline sơ bộ: các mốc tự ước lượng nêu trên; chưa có baseline bấm giờ chung. Mục tiêu đề xuất: giảm ít nhất 30% thời gian trung vị để khoanh vùng nguyên nhân trong từng nhóm người dùng, không tăng lỗi tái phát sau khi sửa. Đo riêng theo developer/sinh viên trên 15–20 lỗi tương đương; ghi thời gian bắt đầu/kết thúc tìm nguyên nhân, kết quả kiểm thử và lỗi tái phát. |
| **Boundary** (AI không được làm gì; khi nào cần con người kiểm tra — HITL) | Không tự ghi/sửa file, chạy lệnh, commit hoặc triển khai. Không đưa mã nguồn, log có dữ liệu nhạy cảm vào công cụ chưa được tổ chức/giảng viên cho phép; chỉ dùng context tối thiểu đã khử bí mật. Người dùng phải kiểm tra giả thuyết và tự quyết định sửa; sinh viên cần bảo đảm cách sửa phù hợp yêu cầu môn học.                                                             |

Phản biện nhận được (từ AI hoặc nhóm khác) và nhóm có đồng ý không:

- Tín hiệu phản bác từ kiểm chứng: 2/3 người phỏng vấn không muốn AI tự sửa file; sinh viên lo code lạ không phù hợp yêu cầu bài, và 1/5 người hỏi nhanh đã quen dùng breakpoint nên không cần công cụ mới. Nhóm đồng ý giữ người dùng ở bước quyết định/sửa, coi AI chỉ là gợi ý cần kiểm chứng. Kết quả cũng cho thấy không nên dùng một mức thời gian chung cho developer và sinh viên.

## 6. Mức can thiệp AI (CP6)

### 6.1. Ma trận độ mơ hồ × độ phức tạp

Bài của nhóm nằm ở ô: **Độ mơ hồ trung bình đến khá × Độ phức tạp khá đến cao**. Ma trận chỉ có 2 mức (thấp/cao), nên nhóm đặt bài ở vùng nghiêng về phía **độ phức tạp cao**, với độ mơ hồ nằm giữa hai cột, không cực đoan.

Vì sao:

- **Độ mơ hồ trung bình đến khá:** một lỗi thường có vài nguyên nhân khả dĩ và hướng xử lý chấp nhận được khác nhau, nên không có đáp án cố định như phân loại vào nhóm có sẵn. Tuy vậy, lỗi có log/traceback, file tham chiếu và có thể kiểm chứng bằng cách chạy lại, nên kết quả đúng/sai vẫn xác minh được. Người được phỏng vấn cũng cho thấy sửa sai thì gây "lỗi chồng lỗi", tức là cần kiểm tra chứ không thể chọn tùy ý.
- **Độ phức tạp khá đến cao:** quy trình hiện tại có từ 3 bước nối tiếp trở lên (lấy log → đọc log → truy file tham chiếu → giả thuyết → sửa/kiểm tra), dùng nhiều nguồn (log/traceback, các file tham chiếu, mã nguồn liên quan) và bước sau phụ thuộc kết quả bước trước (giả thuyết sai thì quay lại bước 3).
- **Hàm ý theo ma trận:** độ phức tạp cao với độ mơ hồ không quá cao gợi ý **Workflow nhiều bước rõ ràng, chưa chắc cần Agent**. Nếu độ mơ hồ thực tế cao hơn thì mới cân nhắc Agent, kèm boundary, người kiểm tra và phương án quay về rất rõ.

### 6.2. So sánh 4 mức

| Mức                       | Phương án cho bài của nhóm                                                                                                                             | Đủ khi nào                                                                                                                                          | Rủi ro                                                                                                                                           | Chọn?                               |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------- |
| **No AI** (sửa quy trình) | Bắt buộc viết tài liệu quy chuẩn code nghiêm ngặt, quy định viết Unit Test 100% và review chéo trước khi merge                                         | Đủ với các dự án nhỏ, cấu trúc đơn giản, ít phụ thuộc bên ngoài và team tuân thủ chặt chẽ TDD                                                       | Không ngăn được các bug logic runtime phát sinh do dữ liệu thực tế biến thiên; làm chậm tiến độ release sản phẩm                                 | Không                               |
| **Rule**                  | Dùng Linter (ESLint, Flake8), Static Code Analysis (SonarQube) và Regex bóc tách traceback                                                             | Đủ với các lỗi cú pháp (syntax error), vi phạm quy chuẩn format hoặc biến chưa khai báo                                                             | Bất lực hoàn toàn trước lỗi logic luồng dữ liệu nghiệp vụ (ví dụ: hàm A trả về dữ liệu sai cấu trúc ở bước 1 làm hàm B crash ở bước 4)           | Chỉ dùng ở khâu tiền xử lý (bước 2) |
| **Workflow**              | **Rule** lọc traceback sạch & trích xuất code liên quan → **AI** phân tích luồng chạy & gợi ý code diff → **Dev** thẩm định duyệt → **Rule** chạy test | Đủ khi quy trình gồm các bước tuần tự cố định; AI chỉ làm khâu "suy luận nguyên nhân" và "đề xuất giải pháp", con người giữ quyền quyết định (HITL) | AI có thể sinh ảo giác (hallucination) hoặc gợi ý chưa tối ưu; kiểm soát chặt bằng bước Dev review và Test runner tự động                        | **CÓ (CHỌN)**                       |
| **Agent**                 | AI tự đọc lỗi, tự duyệt toàn bộ repo, tự sửa file mã nguồn, tự chạy test và tự commit git                                                              | Đủ khi hệ thống có bộ test suite bao phủ 100% và môi trường sandbox cô lập hoàn hảo, cho phép agent chạy thử - sai tự do                            | Rất dễ rò rỉ mã nguồn; chi phí token cực lớn; AI có thể "sửa lụi" bằng cách xóa bỏ assertion của test để test pass; dev mất quyền kiểm soát code | Không                               |

**Mức chọn:** **Workflow (Quy trình bán tự động có con người kiểm duyệt — Human-in-the-loop)**.

**Vì sao không chọn mức đơn giản hơn:**
Vì No AI hay Rule thuần túy chỉ bắt được lỗi tĩnh (static pattern) đã biết trước. Những bug ngốn 20–45 phút (hoặc 1–2 giờ) của dev là lỗi runtime và luồng dữ liệu biến thiên, bắt buộc cần năng lực suy luận ngữ cảnh (contextual reasoning) của mô hình ngôn ngữ lớn (LLM).

**Vì sao không chọn mức phức tạp hơn:**
Vì Agent quá rủi ro về mặt an toàn mã nguồn, chi phí token cao và độ trễ lớn khi phải duyệt qua nhiều file. Hơn nữa, kết quả phỏng vấn developer cho thấy người dùng muốn giữ quyền kiểm soát để tránh "lỗi chồng lỗi", từ chối việc để AI tự ý can thiệp mã nguồn dự án mà không có sự kiểm duyệt của con người.

### 6.3. AI Canvas rút gọn

| Thành phần                                                        | Nội dung                                                                                                                                                                                                                                                                               |
| ----------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Prediction** — AI dự đoán / tạo ra gì?                          | Giải thích traceback bằng ngôn ngữ dễ hiểu (tiếng Việt khi phù hợp), nêu các giả thuyết nguyên nhân có căn cứ vào log/code được cung cấp, chỉ vị trí project liên quan và đề xuất bước kiểm tra tiếp theo. Nếu thiếu dữ liệu, cần nói chưa đủ căn cứ.                                  |
| **Judgment** — con người cân nhắc, quyết định gì?                 | Developer/sinh viên đối chiếu file, dòng lỗi, bước tái hiện và yêu cầu project/bài tập; đánh giá giả thuyết có hợp lý và an toàn không, rồi quyết định có tự áp dụng hướng sửa hay quay lại debug thủ công.                                                                            |
| **Action** — hành động cuối cùng là gì, ai làm?                   | Người dùng tự sửa hoặc chọn cách xử lý, chạy test/tái hiện lỗi và xác nhận kết quả. AI chỉ gợi ý; không tự ghi file, chạy lệnh, commit hay triển khai.                                                                                                                                 |
| **Outcome** — đo kết quả bằng gì?                                 | Thời gian trung vị khoanh vùng nguyên nhân theo từng nhóm người dùng; tỷ lệ lỗi được xác minh/khắc phục; lỗi tái phát hoặc lỗi mới sau khi sửa; mức độ người dùng hiểu được giải thích.                                                                                                |
| **Input** — AI cần dữ liệu đầu vào gì mỗi lần chạy? Có sẵn không? | Traceback/log, mô tả bước tái hiện, runtime/framework/phiên bản và snippet code/file liên quan tối thiểu. Log/traceback thường có khi gặp lỗi; context code và quyền chia sẻ không phải lúc nào cũng sẵn có, cần chọn đúng phần, khử secrets/PII và xác nhận chính sách trước khi gửi. |
| **Feedback** — lấy phản hồi ở đâu để cải thiện?                   | Sau khi người dùng kiểm chứng, ghi nhận giả thuyết đúng/sai/chưa đủ căn cứ, bước nào hữu ích, thời gian xử lý, kết quả test và lỗi tái phát. Chỉ lưu/chia sẻ log hoặc mã nguồn nếu được phép; nếu không, ghi phản hồi đã khử thông tin nhạy cảm.                                       |

### 6.4. Hai câu hỏi của Google PAIR

- Người dùng muốn **được hỗ trợ (augment)** hay **giao hẳn việc (automate)**? Bằng chứng hiện nghiêng về **Augment**: 2/3 người phỏng vấn không muốn AI tự sửa file; developer lo hỏng chuẩn dự án, sinh viên lo code lạ không phù hợp yêu cầu bài. Một người quen debug bằng breakpoint và không cần công cụ mới; 4/5 người hỏi nhanh từng mất hơn 30 phút với lỗi logic chưa rõ nguyên nhân. Đây là tín hiệu ủng hộ hỗ trợ tìm nguyên nhân nhưng vẫn để người dùng kiểm soát, không phải bằng chứng rằng mọi người sẽ dùng công cụ. Chưa hỏi trực tiếp cả 3 người về lựa chọn augment/automate; cần kiểm chứng thêm.
- AI sai kiểu nào tệ hơn, **báo nhầm** hay **bỏ sót**? Vì sao, và thiết kế đã xử lý thế nào: **Báo nhầm tệ hơn.** Nếu AI đưa ra nguyên nhân sai với vẻ chắc chắn (báo nhầm), developer có thể sửa sai chỗ và gây ra "lỗi chồng lỗi" như người được hỏi lo ngại, mất thêm thời gian so với tự debug. Nếu AI bỏ sót (không chỉ ra được nguyên nhân thật), developer chỉ quay về cách làm hiện tại, không mất thêm so với baseline. Thiết kế nghiêng về tránh báo nhầm: (1) đưa ra giả thuyết kèm căn cứ (dòng log, file liên quan) để developer tự đối chiếu; (2) đề xuất bước xác minh trước khi sửa; (3) cho phép AI trả lời "chưa đủ căn cứ" thay vì đoán; (4) AI không tự sửa code, developer quyết định. Mức độ tin cậy cụ thể của gợi ý cần được đánh giá bằng tiêu chí ở mục 7.

---

## 7. Problem Statement v1 + tiêu chí đánh giá (CP6)

| Trường                                          | Nội dung                                                                                                                                                                                                                                                                   |
| ----------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Actor**                                       | Developer (đặc biệt là junior và mid-level) đang phát triển hoặc bảo trì mã nguồn trong các dự án có cấu trúc nhiều module/file phụ thuộc.                                                                                                                                 |
| **Quy trình**                                   | Khi gặp lỗi runtime: Kích hoạt tool → Rule lọc traceback sạch → Rule trích xuất các hàm/file tham chiếu liên quan + AI phân tích luồng chạy và gợi ý giả thuyết nguyên nhân & code diff → Developer thẩm định (HITL) → Rule chạy test kiểm tra.                            |
| **Bottleneck**                                  | Lần mò stack trace và mở từng file tham chiếu trong call stack để truy ngược luồng dữ liệu lỗi (Call Stack Navigation): mất 5–15 phút (với bug nhỏ) và 30–60+ phút (với bug lớn/nhiều tầng gọi).                                                                           |
| **Impact**                                      | Tốn 10–20 phút/bug nhỏ, 1–2 giờ/bug lớn (tần suất 3–5 bug/ngày); làm gián đoạn luồng tư duy (flow state); nguy cơ "lỗi chồng lỗi" làm vỡ logic hệ thống nếu chẩn đoán sai bản chất.                                                                                        |
| **Success Metric** (baseline → target, cách đo) | (1) Giảm 50–70% thời gian ở bước khoanh vùng nguyên nhân (từ 10–20' xuống <5–7' với bug nhỏ; từ 1–2h xuống <20–25' với bug lớn); (2) Tỷ lệ dev chấp thuận giả thuyết của AI ≥ 70%; (3) 0% lỗi mới phát sinh (test runner pass 100%). Đo trên 15–20 bug trong 1 tuần pilot. |
| **Boundary**                                    | AI **tuyệt đối không tự ý sửa file hay commit git**; AI **chỉ nhận snippet code liên quan trực tiếp đã mask secret** (không gửi cả repo); gợi ý của AI **chỉ là giả thuyết tham khảo** (bắt buộc Developer thẩm định HITL).                                                |
| **AI intervention point**                       | Ở Bước 3 và Bước 4: Sau khi Rule đã tiền xử lý traceback và gom context các file tham chiếu liên quan; trước khi Developer quyết định sửa code.                                                                                                                            |
| **Mức chọn**                                    | **Workflow** (Quy trình bán tự động có con người kiểm duyệt — Human-in-the-loop).                                                                                                                                                                                          |
| **Rủi ro & người kiểm tra**                     | AI ảo giác/suy luận sai logic gây "lỗi chồng lỗi", rò rỉ mã nguồn nhạy cảm → Developer thẩm định logic nghiệp vụ (Bước 4); Test runner tự động xác minh code (Bước 5); Rule tiền xử lý lọc mask secrets trước khi gửi AI (Bước 3).                                         |

**Thay đổi so với v0 và lý do:**

| Trường             | v0 (Dự thảo ban đầu từ Problem Card)           | v1 (Sau phỏng vấn & thiết kế Workflow)                                                                                                    | Vì sao đổi                                                                                                                                     |
| ------------------ | ---------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| **Actor**          | Developer chung chung gặp lỗi khi code         | Developer làm việc trong dự án có nhiều module/file phụ thuộc                                                                             | Phỏng vấn cho thấy lỗi cú pháp/đơn giản thì compiler/linter bắt ngay (Rule là đủ), pain chỉ xuất hiện khi lỗi liên quan nhiều file tham chiếu. |
| **Bottleneck**     | "Không biết cách sửa lỗi"                      | "Tốn nhiều thời gian đọc log và lần mò các file tham chiếu trong stack trace để khoanh vùng nguyên nhân"                                  | Phỏng vấn chỉ rõ dev biết cách sửa nhưng mất nhiều thời gian nhất ở khâu đọc trace và mở từng file liên quan để truy ngược luồng dữ liệu.      |
| **Success Metric** | Chỉ đo chung chung: "Giảm 50% thời gian debug" | Đo 3 tiêu chí: (1) Giảm 50–70% thời gian tìm nguyên nhân; (2) Tỷ lệ chấp thuận giả thuyết ≥ 70%; (3) 0% lỗi chồng lỗi (test pass 100%)    | Nhanh hơn nhưng sửa sai gây "lỗi chồng lỗi" thì còn tệ hơn baseline; cần kiểm soát cả độ chính xác và an toàn code.                            |
| **Boundary**       | AI không tự commit code lên git                | Bổ sung: AI không tự ghi đè file, không nạp toàn bộ repo (chỉ gửi context liên quan đã mask secret), gợi ý chỉ là giả thuyết có dẫn chứng | Phân tích câu hỏi Google PAIR: Developer coi trọng tính an toàn, tránh báo nhầm và cần bảo mật mã nguồn dự án.                                 |
| **Mức can thiệp**  | Chưa xác định rõ (cân nhắc Tool hoặc Agent)    | Chốt mức **Workflow** (Human-in-the-loop)                                                                                                 | Rule không đủ cho logic runtime; Agent quá rủi ro về bảo mật, chi phí và nguy cơ "sửa lụi" làm hỏng codebase.                                  |

**Tiêu chí đánh giá đầu ra của AI (3–5 tiêu chí):**

|   # | Tiêu chí                                                           | Đạt khi                                                                                                                                 | Không đạt khi                                                                                                          |
| --: | ------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
|   1 | **Tính có căn cứ (Groundedness / Căn cứ dòng lỗi)**                | Mọi giả thuyết nguyên nhân đều trích dẫn chính xác dòng code, tên biến, hàm có thật trong traceback và context file tham chiếu.         | Đưa ra nhận định suy đoán chung chung, bịa ra tên biến/hàm hoặc file không hề tồn tại trong dự án (hallucination).     |
|   2 | **Tránh báo nhầm (Precision / Thận trọng khi thiếu dữ kiện)**      | Khi context chưa đủ hoặc lỗi mơ hồ, AI nêu rõ "chưa đủ căn cứ" và đề xuất dev kiểm tra thêm log/biến cụ thể thay vì đoán mò.            | Khẳng định chắc chắn một nguyên nhân sai, khiến dev sửa lệch hướng dẫn tới "lỗi chồng lỗi".                            |
|   3 | **Tính hành động được & Dễ hiểu (Actionability & Explainability)** | Giải thích ngắn gọn luồng chạy gây lỗi bằng tiếng Việt (dưới 200 từ) và đề xuất 1–2 code diff cụ thể, đọc hiểu và áp dụng được ngay.    | Giải thích lan man, lý thuyết hàn lâm, không có code diff minh họa hoặc code diff sai cú pháp.                         |
|   4 | **Tính an toàn & Bảo mật context (Safety & Privacy)**              | Không yêu cầu hoặc xử lý các chuỗi nhạy cảm (API key, token, mật khẩu, PII); code diff không xóa bỏ test assertions để "vượt qua test". | Gợi ý sửa code bằng cách xóa assert/bỏ qua exception; hoặc đòi hỏi nạp toàn bộ mã nguồn/thông tin nhạy cảm lên prompt. |

---

## 8. Quyết định (CP6)

### 8.1. Bốn rủi ro

| Rủi ro          | Câu hỏi                                                           | Mức độ rủi ro (Thấp = an toàn / TB / Cao = nguy hiểm) | Lý do / bằng chứng                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| --------------- | ----------------------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Value**       | Người dùng có thật sự cần và sẽ dùng không?                       | TB                                                    | Có tín hiệu pain: 3/3 người phỏng vấn nói phần tốn thời gian nhất là lần tìm nguyên nhân; 4/5 người hỏi nhanh từng mất hơn 30 phút với lỗi logic chưa rõ nguyên nhân. Đồng thời, 1/5 không cần công cụ mới và 2/3 người phỏng vấn không muốn AI tự sửa file. Tần suất 3–5 lỗi/ngày chưa được xác nhận; các mốc thời gian là tự ước lượng, khác nhau theo người dùng/độ lớn bug; chưa so sánh có kiểm soát với việc dán traceback vào LLM sẵn có (giả định #1–#3). |
| **Usability**   | Người dùng có dùng được, có hiểu và sửa được đầu ra của AI không? | TB                                                    | Thiết kế theo hướng augment: gợi ý kèm căn cứ (dòng log, file liên quan) và bước xác minh, developer quyết định, AI không tự sửa (mục 6.4). Rủi ro còn lại là developer tin gợi ý sai hoặc phải mất thêm thời gian kiểm tra; chưa thử với người dùng thật (giả định #5).                                                                                                                                                                                          |
| **Feasibility** | Có đủ dữ liệu, công cụ, kỹ năng để làm không?                     | TB                                                    | Log/traceback và file liên quan có trong quy trình debug; research ban đầu về GitHub Copilot và Sentry cho thấy có công cụ hỗ trợ code context hoặc thu thập runtime context. Tuy nhiên, nhóm chưa thử nghiệm công cụ, chưa chứng minh cách chọn đủ context mà không gửi toàn bộ mã nguồn, và chưa đánh giá độ chính xác/hữu ích trên bộ lỗi thực tế (giả định #4).                                                                                               |
| **Viability**   | Có hợp chi phí, pháp lý, quy định tổ chức không? Ai vận hành?     | Cao                                                   | Cần đưa log và một phần mã nguồn vào công cụ AI; chưa có bằng chứng về chính sách bảo mật của dự án, chi phí và độ trễ chấp nhận được (giả định #6, bằng chứng 1/5, mức quan trọng 5/5). Không ai được hỏi trực tiếp về vấn đề này trong phỏng vấn. Mức Cao vì chưa biết, không phải vì đã biết là vi phạm; có thể hạ xuống sau khi hỏi chính sách của dự án.                                                                                                     |

### 8.2. Kết luận

**Quyết định:** **Not Yet**

**Lý do:** Có tín hiệu pain ban đầu từ 3 cuộc phỏng vấn và 5 câu hỏi nhanh, nhưng mẫu nhỏ, thời gian tự ước lượng và có người không cần công cụ mới. Chưa thử nghiệm AI trên lỗi thực tế để biết gợi ý có tốt hơn cách dùng LLM hiện tại hay không. Quan trọng hơn, rủi ro Viability đang ở mức Cao vì chưa xác nhận chính sách chia sẻ mã nguồn/log, chi phí và công cụ được phép dùng. Chưa nên pilot trên mã nguồn hoặc dữ liệu thật trước khi làm rõ điều này.

**Nếu Go — pilot nhỏ nhất:** Chỉ sau khi được phép dùng dữ liệu/công cụ: đánh giá ngoại tuyến trên 15–20 lỗi đã xử lý, tách kết quả developer và sinh viên. Dùng log/context đã khử bí mật, không cho AI ghi file hoặc chạy lệnh; so sánh thời gian khoanh vùng với cách debug hiện tại và chấm gợi ý theo tiêu chí mục 7. Chỉ cân nhắc pilot giới hạn nếu thời gian trung vị giảm ít nhất 30% trong nhóm được thử, ít nhất 70% giả thuyết được developer xác nhận là hữu ích/có căn cứ và không có đề xuất nguy hiểm được áp dụng.

**Nếu Not Yet — cần kiểm chứng gì trước:** (1) Xin xác nhận từ Tech Lead/giảng viên hoặc bộ phận phụ trách rằng có thể dùng công cụ AI với log/snippet đã khử bí mật; (2) ghi baseline bấm giờ theo loại lỗi và nhóm người dùng, không gộp bug nhỏ/lớn hoặc developer/sinh viên; (3) thử ngoại tuyến trên lỗi đã giải quyết, so sánh với workaround hiện tại gồm tìm kiếm và LLM; (4) đánh giá mức dễ hiểu, độ chính xác/căn cứ và lỗi tái phát.

**Nếu No-Go — nên làm gì thay AI:** Dùng debugger/breakpoint, chuẩn hóa log và hướng dẫn đọc traceback; tạo checklist/runbook lỗi phổ biến, nhờ peer review/trợ giảng khi cần. Không gửi code/log ra dịch vụ AI không được phép.

**Ngưỡng dừng** (nếu sau … mà … thì quay về …): Dừng đánh giá ngay nếu phát hiện secret/PII hoặc mã nguồn bị gửi tới dịch vụ chưa được phép, hay có gợi ý nguy hiểm được áp dụng. Sau 15–20 lỗi, nếu thời gian trung vị không giảm ít nhất 30%, dưới 70% gợi ý được người dùng xác nhận là hữu ích/có căn cứ, hoặc lỗi tái phát tăng so với baseline thì không mở rộng; quay lại debugger, breakpoint và runbook thủ công.

---

## 9. Hạn chế và hướng tiếp theo

### 9.1. Hạn chế của nghiên cứu hiện tại

- **Mẫu dữ liệu thực nghiệm còn nhỏ:** Có 3 phỏng vấn sâu và 5 câu trả lời hỏi nhanh; snapshot cho thấy thời gian tự ước lượng khác nhau giữa developer (10–20 phút/bug nhỏ, 1–2 giờ/bug lớn) và sinh viên (30–45 phút/lỗi). Chưa có số liệu bấm giờ thực tế, chưa xác nhận tần suất 3–5 bug/ngày, và chưa có đủ mẫu đa dạng ngôn ngữ/framework để khái quát (giả định #1, #2 trong Assumption Map).
- **Rủi ro Viability còn ở mức Cao:** Chưa kiểm chứng chính thức chính sách bảo mật thông tin (Security & IP Policy) của các tổ chức/doanh nghiệp về việc đưa log và các đoạn mã nguồn lên các mô hình LLM thương mại bên ngoài qua Cloud API (giả định #6).
- **Giới hạn phạm vi bài toán:** Thiết kế hiện tại mới giải quyết tối ưu cho các lỗi runtime cục bộ trong cùng một repository (monolith / single service), chưa xử lý được các hệ thống phân tán phức tạp (microservices, lỗi mạng bất đồng bộ, race condition đa luồng giữa nhiều dịch vụ).

### 9.2. Hướng triển khai tiếp theo (Next Steps)

- **Kiểm chứng chính sách bảo mật (Ưu tiên số 1):** Làm việc với Tech Lead / bộ phận Security để làm rõ ranh giới chia sẻ dữ liệu mã nguồn. Nếu tổ chức cấm đưa code ra ngoài, nghiên cứu phương án tích hợp mô hình ngôn ngữ mã nguồn mở chạy local (như Qwen2.5-Coder hoặc DeepSeek-Coder chạy qua Ollama/vLLM tại máy dev).
- **Đo lường baseline chuẩn xác qua Pilot 1 tuần:** Tổ chức ghi chép và bấm giờ thực tế trên 15–20 bug liên tiếp của nhóm phát triển để có số liệu baseline đáng tin cậy thay vì số ước lượng từ trí nhớ.
- **Xây dựng bản thử nghiệm tối thiểu (POC CLI Tool):**
    - Viết 1 script Python nhỏ gọn hoạt động tại terminal: nhận traceback → dùng Regex bóc tách danh sách file nội bộ trong call stack → tự động trích xuất 20–30 dòng code xung quanh vị trí lỗi (đã mask secret) → ghép prompt chuẩn gửi đến LLM.
    - Đánh giá chất lượng bản nháp giả thuyết và code diff dựa trên **4 tiêu chí đánh giá** đã thiết lập ở Mục 7 để đo tỷ lệ chấp thuận (Acceptance Rate) trước khi tích hợp sâu thành VS Code Extension.

## 10. Tài liệu tham khảo

-
