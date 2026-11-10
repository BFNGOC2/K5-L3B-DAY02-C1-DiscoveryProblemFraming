# Báo cáo cá nhân — Thiều Thế Ngọc

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Thiều Thế Ngọc
- MSSV: 2A202603788
- Email trường (không bắt buộc, repo có thể để public): 26ai.ngoctt@vinuni.edu.vn
- Tên nhóm: C1
- Link repo nhóm: [BFNGOC2/K5-L3B-DAY02-C1-DiscoveryProblemFraming](https://github.com/BFNGOC2/K5-L3B-DAY02-C1-DiscoveryProblemFraming)

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

|   # | Lăng kính                                              | Job Story: Khi… tôi muốn… để…                                                                                                                          | Ai chịu ảnh hưởng?                          | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng)                                        |
| --: | ------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------- | ------------------------------------------------------------------------------------------------ |
|   1 | Tốn thời gian · Cần đọc, tổng hợp nhiều thông tin      | Khi nhận ticket mới từ khách hàng hoặc BA, tôi muốn hiểu rõ yêu cầu và các đầu việc kỹ thuật cần thực hiện, để lập kế hoạch phát triển phù hợp         | Developer, BA, khách hàng                   | 15–20 ticket/tuần; phân tích mỗi ticket mất 20–30 phút, tương đương khoảng 5–10 giờ/tuần         |
|   2 | Tốn thời gian · Cần đọc, tổng hợp nhiều thông tin      | Khi gặp lỗi trong quá trình phát triển, tôi muốn xác định nguyên nhân có khả năng xảy ra và hướng khắc phục, để giảm thời gian debug                   | Developer                                   | 3–5 lỗi cần debug/ngày; mỗi lỗi mất 20–45 phút, tương đương khoảng 1–3,75 giờ/ngày               |
|   3 | Cần đọc, tổng hợp nhiều thông tin · Pain từ người khác | Khi QA gửi báo cáo bug, tôi muốn nhận ra các bug có chung nguyên nhân hoặc liên quan cùng chức năng, để team ưu tiên xử lý lỗi gốc                     | QA, developer, team phát triển              | 20–30 bug report/tuần; phân loại mỗi bug mất 5–10 phút, tương đương khoảng 1,7–5 giờ/tuần        |
|   4 | Lặp lại · Cần đọc, tổng hợp nhiều thông tin            | Khi hệ thống sử dụng nhiều dịch vụ bên thứ ba, tôi muốn biết API nào có request bất thường hoặc lãng phí, để tối ưu chi phí vận hành                   | Developer, đội vận hành, bên chịu ngân sách | 10.000–20.000 API request/ngày; ước tính 5–10% request trùng lặp hoặc không cần thiết (giả định) |
|   5 | Tốn thời gian · Cần đọc, tổng hợp nhiều thông tin      | Khi cần tìm lại đoạn code hoặc giải pháp đã dùng trước đây, tôi muốn tìm theo mô tả vấn đề, để nhanh chóng tái sử dụng kiến thức                       | Developer, team phát triển                  | Tìm kiếm 3–5 lần/tuần; mỗi lần mất 10–20 phút, tương đương khoảng 30–100 phút/tuần               |
|   6 | Cần đọc, tổng hợp nhiều thông tin                      | Khi cân nhắc mua một sản phẩm có nhiều đánh giá, tôi muốn nắm được các ưu nhược điểm và độ tin cậy của đánh giá, để đưa ra quyết định mua hàng tốt hơn | Người mua hàng                              | Mỗi sản phẩm có 500–1.000 đánh giá; đọc và tổng hợp trước khi mua mất khoảng 20–30 phút          |

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem                                             | Vì sao chọn                                                                        | Điều còn chưa chắc                                                                                          |
| ---: | --------------------------------------------------- | ---------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
|    1 | CP1 #1 — Phân tích ticket và xác định task kỹ thuật | Tần suất cao (15–20 ticket/tuần), tốn 5–10 giờ/tuần; đầu ra và thời gian có thể đo | Quy trình phân tích hiện tại gồm những bước nào; chất lượng task đề xuất cần đạt mức nào                    |
|    2 | CP1 #2 — Debug lỗi từ error log                     | Xảy ra thường xuyên (3–5 lỗi/ngày), tốn khoảng 1–3,75 giờ/ngày                     | Thời gian 20–45 phút là toàn bộ debug hay riêng đọc log/tìm nguyên nhân; nhóm lỗi nào chiếm nhiều thời gian |
|    3 | CP1 #6 — Tổng hợp đánh giá sản phẩm                 | Mỗi sản phẩm có 500–1.000 đánh giá; đọc và tổng hợp mất 20–30 phút/lần             | Tần suất mua sắm; cách đánh giá độ tin cậy của review và mức độ chính xác cần thiết                         |

### Problem Card #1

| Trường                                    | Nội dung                                                                                                                                                                             |
| ----------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Job Story                                 | Khi nhận ticket mới từ khách hàng hoặc BA, tôi muốn hiểu rõ yêu cầu và các đầu việc kỹ thuật cần thực hiện, để lập kế hoạch phát triển phù hợp                                       |
| Actor                                     | Developer nhận và phân tích ticket; BA hoặc khách hàng cung cấp yêu cầu                                                                                                              |
| Thời điểm / bối cảnh                      | Khi có ticket mới cần làm rõ và đưa vào kế hoạch phát triển                                                                                                                          |
| Quy trình hiện tại (3–7 bước)             | Bản nháp cần xác nhận: 1. Đọc ticket và tài liệu liên quan · 2. Làm rõ yêu cầu/điều kiện còn thiếu · 3. Tách yêu cầu thành task kỹ thuật · 4. Ước lượng và sắp xếp task vào kế hoạch |
| Bottleneck (bước nào, mất bao nhiêu phút) | Phân tích ticket và chuyển yêu cầu thành task: tổng thời gian hiện được ghi nhận là 20–30 phút/ticket; chưa có thời gian riêng cho từng bước                                         |
| Impact (nếu không giải thì sao)           | 15–20 ticket/tuần tiêu tốn khoảng 5–10 giờ/tuần; thời gian phân tích kéo dài có thể làm chậm việc lập kế hoạch                                                                       |
| Success metric (baseline → target)        | Baseline: 20–30 phút/ticket. Mục tiêu đề xuất để kiểm chứng: giảm còn tối đa 10–15 phút/ticket, không làm tăng task thiếu yêu cầu hoặc phải làm lại                                  |
| Phương án không dùng AI                   | Dùng mẫu phân tích ticket, checklist yêu cầu/tiêu chí chấp nhận và quy tắc tách task theo loại công việc                                                                             |
| Giả thuyết về AI (nếu có)                 | Hệ thống tóm tắt yêu cầu, nêu điểm chưa rõ và đề xuất task kỹ thuật kèm căn cứ từ ticket; developer rà soát, chỉnh sửa và quyết định trước khi đưa vào kế hoạch                      |
| Cảm nhận nhanh                            | Workflow                                                                                                                                                                             |

Quy trình nháp hiện tại:

```text
BẢN NHÁP — baseline 20–30 phút/ticket (thời gian từng bước chưa đo)
[Đọc ticket/tài liệu] → [Làm rõ yêu cầu] → [Tách thành task kỹ thuật] → [Ước lượng, lập kế hoạch]
                              Toàn bộ quy trình phân tích: 20–30 phút/ticket
```

### Problem Card #2

| Trường                                    | Nội dung                                                                                                                                                                                                    |
| ----------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Job Story                                 | Khi gặp lỗi trong quá trình phát triển, tôi muốn xác định nguyên nhân có khả năng xảy ra và hướng khắc phục, để giảm thời gian debug                                                                        |
| Actor                                     | Developer đang xử lý lỗi                                                                                                                                                                                    |
| Thời điểm / bối cảnh                      | Khi ứng dụng phát sinh lỗi trong quá trình phát triển và có error log để điều tra                                                                                                                           |
| Quy trình hiện tại (3–7 bước)             | Bản nháp cần xác nhận: 1. Tái hiện lỗi/ghi nhận hiện tượng · 2. Đọc error log và xác định đoạn liên quan · 3. Tìm kiếm nguyên nhân khả dĩ · 4. Thử hướng khắc phục · 5. Kiểm tra lại và xác nhận lỗi đã hết |
| Bottleneck (bước nào, mất bao nhiêu phút) | Đọc log, khoanh vùng nguyên nhân và tìm hướng xử lý; toàn bộ quá trình hiện mất 20–45 phút/lỗi, chưa đo riêng từng bước                                                                                     |
| Impact (nếu không giải thì sao)           | 3–5 lỗi/ngày tiêu tốn khoảng 1–3,75 giờ/ngày cho debug; lỗi chưa được xử lý có thể cản trở tiến độ phát triển                                                                                               |
| Success metric (baseline → target)        | Baseline: 20–45 phút/lỗi. Mục tiêu đề xuất để kiểm chứng: giảm còn tối đa 10–20 phút/lỗi, không làm tăng tỷ lệ sửa sai hoặc lỗi tái phát                                                                    |
| Phương án không dùng AI                   | Chuẩn hóa log, dùng checklist debug và tra cứu runbook/các lỗi đã biết theo mã lỗi                                                                                                                          |
| Giả thuyết về AI (nếu có)                 | Hệ thống tóm tắt log, nêu nguyên nhân khả dĩ kèm dấu hiệu liên quan và hướng kiểm tra; đây chỉ là gợi ý, developer xác minh log và kiểm tra hướng sửa trước khi áp dụng                                     |
| Cảm nhận nhanh                            | Workflow                                                                                                                                                                                                    |

Quy trình nháp hiện tại:

```text
BẢN NHÁP — baseline 20–45 phút/lỗi (thời gian từng bước chưa đo)
[Tái hiện/ghi nhận lỗi] → [Đọc và khoanh vùng log] → [Tìm nguyên nhân] → [Thử sửa] → [Kiểm tra lại]
                                         Toàn bộ quá trình debug: 20–45 phút/lỗi
```

### Problem Card #3

| Trường                                    | Nội dung                                                                                                                                                                                                     |
| ----------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Job Story                                 | Khi cân nhắc mua một sản phẩm có nhiều đánh giá, tôi muốn nắm được các ưu nhược điểm và độ tin cậy của đánh giá, để đưa ra quyết định mua hàng tốt hơn                                                       |
| Actor                                     | Người mua hàng                                                                                                                                                                                               |
| Thời điểm / bối cảnh                      | Trước khi quyết định mua sản phẩm có nhiều đánh giá trực tuyến                                                                                                                                               |
| Quy trình hiện tại (3–7 bước)             | Bản nháp cần xác nhận: 1. Mở trang sản phẩm và xem đánh giá · 2. Đọc các nhận xét để tìm ưu/nhược điểm · 3. So sánh các nhận xét và để ý dấu hiệu bất thường · 4. Tự tổng hợp thông tin trước khi quyết định |
| Bottleneck (bước nào, mất bao nhiêu phút) | Đọc và tổng hợp số lượng lớn đánh giá; mỗi sản phẩm mất 20–30 phút, chưa đo thời gian riêng cho từng bước                                                                                                    |
| Impact (nếu không giải thì sao)           | Cần xem xét 500–1.000 đánh giá/sản phẩm; việc tổng hợp tốn thời gian và người mua có thể khó nhận ra ý kiến lặp lại hoặc dấu hiệu bất thường                                                                 |
| Success metric (baseline → target)        | Baseline: 20–30 phút/sản phẩm. Mục tiêu đề xuất để kiểm chứng: giảm còn tối đa 10–15 phút, vẫn nêu được ưu/nhược điểm chính và để người mua tự kiểm tra review gốc                                           |
| Phương án không dùng AI                   | Lọc theo điểm đánh giá/thời gian, đọc các review mới nhất và hữu ích nhất, rồi dùng checklist ghi nhận ưu/nhược điểm                                                                                         |
| Giả thuyết về AI (nếu có)                 | Hệ thống nhóm các chủ đề ưu/nhược điểm, tóm tắt ý kiến trái chiều và đánh dấu review có dấu hiệu bất thường kèm lý do; đây không phải kết luận review giả, người mua cần kiểm tra review gốc                 |
| Cảm nhận nhanh                            | Workflow                                                                                                                                                                                                     |

Quy trình nháp hiện tại:

```text
BẢN NHÁP — baseline 20–30 phút/sản phẩm (thời gian từng bước chưa đo)
[Mở danh sách 500–1.000 review] → [Đọc/lọc review] → [So sánh ý kiến và tìm dấu hiệu bất thường] → [Tổng hợp ưu/nhược điểm]
                                                     Toàn bộ quá trình: 20–30 phút/sản phẩm
```

### Card muốn pitch nhất

- Card số: #2 — Debug lỗi từ error log
- Vì sao: Lỗi xảy ra thường xuyên (3–5 lỗi/ngày), mỗi lỗi mất 20–45 phút debug, tương đương khoảng 1–3,75 giờ/ngày. Đây là vấn đề có thể đo thời gian trước/sau và ảnh hưởng trực tiếp đến tiến độ phát triển.
- Câu hỏi muốn nhóm phản biện: Bottleneck có thực sự nằm ở đọc log và tìm nguyên nhân, hay ở bước tái hiện/kiểm chứng lỗi? Error log có đủ ngữ cảnh để đề xuất hướng xử lý đáng tin cậy không, và cần tiêu chí nào để bảo đảm giảm thời gian mà không làm tăng sửa sai hoặc lỗi tái phát?

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra                                                                                                                                                                                         | Đồng ý? | Đã sửa gì                                                                                                                                                                              |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Card #1: “Task kỹ thuật cần thực hiện” còn rộng; các task do hệ thống đề xuất có thể thiếu điều kiện chấp nhận hoặc không bám yêu cầu gốc. Mục tiêu giảm thời gian cũng cần được kiểm tra cùng chất lượng. | Đồng ý  | Làm rõ trong giả thuyết AI rằng đề xuất phải kèm căn cứ từ ticket và developer rà soát/chỉnh sửa; giữ điều kiện không tăng task thiếu yêu cầu hoặc phải làm lại khi đánh giá mục tiêu. |
| Card #2: Error log có thể chưa đủ ngữ cảnh để xác định nguyên nhân; nếu coi gợi ý là kết luận hoặc áp dụng sửa tự động có thể dẫn đến sửa sai.                                                             | Đồng ý  | Ghi rõ nguyên nhân chỉ là giả thuyết, cần developer đối chiếu log và kiểm tra hướng sửa trước khi áp dụng.                                                                             |
| Card #3: 500–1.000 review là quy mô lớn nhưng chưa rõ người mua thực sự đọc bao nhiêu; dấu hiệu bất thường không đủ để kết luận review giả.                                                                | Đồng ý  | Giới hạn giả thuyết ở việc nêu dấu hiệu kèm lý do, không kết luận review giả; yêu cầu người mua kiểm tra review gốc.                                                                   |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động                  | Tôi đã làm gì?                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Kết quả / ảnh hưởng tới bài nhóm                                                                                                                                                                                                                                                          |
| -------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Pitch Problem Card         | Pitch 3 candidate: #1 phân tích ticket mới; #2 tìm nguyên nhân và hướng khắc phục lỗi; #6 tổng hợp đánh giá sản phẩm để hỗ trợ quyết định mua hàng.                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Đưa ra các candidate kèm actor và bottleneck định lượng để nhóm thảo luận, phản biện và chọn vấn đề phù hợp.                                                                                                                                                                              |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: (1) Candidate #6: Mỗi lần kiểm tra chỉ mất 1–2 phút; liệu có cần tạo giải pháp mới không, nếu giải pháp cũng tốn thời gian và người dùng vẫn mất khoảng 1 phút để xem lịch học? (2) Candidate #9: Vì mỗi cuộc họp thường bàn về công việc nội bộ quan trọng, việc tổng hợp hàng loạt dữ liệu có thể tạo ra những rủi ro gì? (3) Candidate #4: Vì sao chỉ kiểm tra checklist khi bắt đầu làm, thay vì kiểm tra kỹ lại sau khi hoàn thành?                                                                                                                                                   | Các câu hỏi gợi ý nhóm cần cân nhắc lợi ích thời gian thực tế của candidate #6, rủi ro bảo mật khi tổng hợp dữ liệu nội bộ ở #9, và bổ sung bước kiểm tra sau khi hoàn thành ở #4.                                                                                                        |
| Nhận phản biện             | Câu hỏi tôi nhận được: (1) Candidate #1: Thời gian 20–30 phút/ticket là do mô tả yêu cầu ban đầu thiếu/mơ hồ hay do độ phức tạp kỹ thuật của hệ thống? (2) Candidate #3: Người mua thực sự đọc lướt hàng trăm đánh giá hay chủ yếu tìm từ khóa/tiêu chí cụ thể như độ bền, kích thước và lỗi thường gặp? (3) Candidate #2: Với lỗi phổ biến, công cụ hiện có như Copilot, ChatGPT, Antigravity hoặc Cursor đã hỗ trợ rất nhanh; giải pháp này tạo giá trị khác biệt gì so với việc dev tự đưa traceback vào LLM, làm sao hiểu đủ context mã nguồn trong giới hạn token, và làm thế nào hạn chế rò rỉ mã nguồn? | Tôi ghi nhận cần phân biệt nguyên nhân gây tốn thời gian phân tích ticket (#1), kiểm chứng cách người mua tìm thông tin review (#3), và làm rõ giá trị khác biệt, giới hạn context cùng biện pháp bảo vệ mã nguồn của candidate debug (#2) trước khi chốt giải pháp.                      |
| Gom cluster / cây OST      | Không tham gia gom cluster hoặc xây dựng cây OST; có tham gia lập bảng chấm điểm các candidate theo tiêu chí của nhóm.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | Bảng điểm giúp nhóm so sánh các candidate có hệ thống trước khi chọn vấn đề ưu tiên.                                                                                                                                                                                                      |
| Chọn candidate problem     | Dựa trên bảng chấm điểm, cùng nhóm chọn #2 — Debug lỗi (30/35 điểm sơ bộ).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Ưu tiên vấn đề có actor rõ, pain định lượng (3–5 lỗi/ngày; 20–45 phút/lỗi) để tiếp tục kiểm chứng; điểm số cần được nhóm xác nhận.                                                                                                                                                        |
| Kiểm chứng / research      | Tổng hợp 3 phỏng vấn sâu và 5 câu hỏi nhanh; ghi snapshot developer và sinh viên CNTT. Research GitHub Copilot từ tài liệu chính thức và bổ sung Sentry theo nguồn nhóm cung cấp.                                                                                                                                                                                                                                                                                                                                                                                                                              | Ghi nhận cả tín hiệu xác nhận (3/3 người phỏng vấn mất thời gian tìm nguyên nhân; 4/5 người hỏi nhanh từng mất hơn 30 phút) lẫn phản bác (2/3 không muốn AI tự sửa; 1/5 không cần công cụ mới). Nêu rõ mẫu nhỏ và thời gian tự ước lượng; không kết luận đại diện cho toàn bộ người dùng. |
| Quy trình nhóm             | Cùng nhóm mô tả các bước debug hiện tại/tương lai và hoàn thiện bảng before/after; phân biệt bước có hỗ trợ Rule/AI với bước còn cần người.                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Xác định lần theo log và code liên quan là bottleneck cần đo; ghi rõ thời lượng tương lai 7–10 phút chỉ là ước tính chưa kiểm chứng, không gộp baseline khác nhau giữa developer và sinh viên.                                                                                            |
| Problem Statement          | Làm rõ actor, luồng xử lý lỗi, bottleneck, impact và metric dự kiến dựa trên bằng chứng kiểm chứng; ghi boundary về dữ liệu và quyền quyết định của người dùng.                                                                                                                                                                                                                                                                                                                                                                                                                                                | Bản v0 nêu được khác biệt baseline giữa developer và sinh viên, đề xuất đo riêng theo nhóm và không để AI tự sửa/commit hoặc xử lý dữ liệu chưa được phép.                                                                                                                                |
| Mức can thiệp AI           | Cùng nhóm xác định Workflow: Rule tiền xử lý traceback/context, AI giải thích và đưa giả thuyết, người dùng kiểm chứng và tự sửa/test; điền AI Canvas.                                                                                                                                                                                                                                                                                                                                                                                                                                                         | AI chỉ đưa giả thuyết có căn cứ, input là traceback/log và snippet code đã được phép chia sẻ; người dùng giữ quyền quyết định, phản hồi lấy từ kết quả kiểm thử và mức hữu ích.                                                                                                           |
| Quyết định                 | Đối chiếu 4 rủi ro với kết quả kiểm chứng; đề xuất điều kiện cần làm rõ trước pilot và ngưỡng dừng.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Chọn Not Yet vì chính sách dùng log/mã nguồn với AI chưa xác nhận và chưa có đánh giá trên lỗi thực tế; đề xuất đánh giá ngoại tuyến sau khi được phép, dừng nếu lộ dữ liệu hoặc gợi ý nguy hiểm.                                                                                         |

---

## 5. Dùng AI

| Checkpoint                     | Tôi dùng AI để làm gì?                                                       | AI hữu ích ở đâu?                                                                               | AI sai hoặc hời hợt ở đâu?                                                                                                                | Tôi sửa gì bằng nhận định của mình?                                                                                                                                |
| ------------------------------ | ---------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| CP1 Scan                       | Dùng AI để gợi ý thêm các hướng candidate, sau đó chọn lọc và hoàn thiện Job Story trong báo cáo. | Hỗ trợ mở rộng các hướng để cân nhắc, thay vì chỉ tập trung vào một loại vấn đề. | Gợi ý AI không xác nhận được tính đúng đắn của số liệu hay mức độ thường gặp; một số số liệu vẫn là ước lượng hoặc giả định, như tỷ lệ request ở candidate #4. | Tự chọn và diễn đạt lại các candidate phù hợp; không xem gợi ý AI là bằng chứng, đồng thời đánh dấu rõ số liệu giả định/chưa kiểm chứng. |
| CP2 Problem Card               | Dùng AI phản biện ba Problem Card: phân tích ticket, debug lỗi từ error log và tổng hợp đánh giá sản phẩm. | Nêu các điểm cần làm rõ: task kỹ thuật cần bám yêu cầu và có điều kiện chấp nhận; error log có thể chưa đủ context; quy mô review chưa chứng minh người mua đọc hết và dấu hiệu bất thường không đủ kết luận review giả. | Phản biện chỉ dựa trên nội dung card, không xác minh baseline/thời lượng với người dùng thực tế; gợi ý không thay thế kiểm chứng. | Giữ các giới hạn trong giả thuyết: task có căn cứ từ ticket và developer rà soát; nguyên nhân lỗi là giả thuyết cần kiểm tra; review bất thường chỉ được nêu dấu hiệu kèm lý do, người mua cần xem review gốc. |
| CP4 Research                   | Hỗ trợ sắp xếp nội dung kiểm chứng và research thành bảng trong báo cáo.     | Giúp hệ thống hóa snapshot, tín hiệu xác nhận/phản bác và bài học từ công cụ.                   | Ban đầu đưa thêm các công cụ research ngoài nguồn người dùng cung cấp, khiến phạm vi bảng không còn đúng với bằng chứng nhóm đã thu thập. | Giữ Sentry là nguồn do nhóm cung cấp và chỉ giữ GitHub Copilot khi có tài liệu chính thức đã mở; không trình bày gợi ý thêm của AI như research nhóm đã thực hiện. |
| CP5 Quy trình                  | Hỗ trợ trình bày quy trình hiện tại/tương lai và bảng before/after.          | Giúp thể hiện các bước, vai trò con người/Rule/AI và phương án quay về.                         | Các thời lượng tương lai dễ bị hiểu nhầm là kết quả đã đo; các nhóm người dùng cũng có baseline khác nhau.                                | Ghi thời lượng 7–10 phút là ước tính chưa thử nghiệm, không gộp số liệu developer và sinh viên.                                                                    |
| CP5–6 Problem Statement        | Hỗ trợ tổ chức các trường problem statement và diễn đạt metric/boundary.     | Giúp kết nối bottleneck, metric, boundary và dữ liệu kiểm chứng.                                | Có nguy cơ khái quát quá mức từ mẫu nhỏ hoặc biến mục tiêu dự kiến thành baseline thực tế.                                                | Nêu rõ thời gian là tự ước lượng, yêu cầu đo riêng theo nhóm và giữ các tuyên bố chưa kiểm chứng ở dạng giả thuyết.                                                |
| CP6 Mức can thiệp / quyết định | Hỗ trợ cấu trúc AI Canvas, so sánh mức can thiệp và trình bày lý do Not Yet. | Làm rõ AI chỉ đưa giả thuyết, người dùng kiểm tra và quyết định; nêu điều kiện trước khi pilot. | Không thể xác nhận thay nhóm về chính sách bảo mật, chi phí hoặc công cụ được phép dùng.                                                  | Giữ quyết định Not Yet cho đến khi xác nhận chính sách dữ liệu và kiểm thử trên lỗi thực tế; không coi nhận định của AI là bằng chứng.                             |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

Khi nghe top 3 problems của các bạn khác, tôi học được thêm những góc nhìn về các vấn đề có thể gặp. Điều đó giúp tôi chú ý hơn đến việc tìm điểm nghẽn thực sự, thay vì chỉ nhìn vào biểu hiện bên ngoài của vấn đề.

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**
Nhóm bắt đầu nghĩ đến AI/công cụ debug trước khi xác nhận phần nào của quy trình tốn thời gian. Sau khi kiểm chứng, hãy nói nhóm đã tập trung lại vào việc tìm nguyên nhân từ log và code liên quan.

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**
Tôi thấy các phản biện có ý đúng nhưng chưa đủ để thay đổi ý.
**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

Kết quả kiểm chứng không làm tôi bất ngờ, vì theo tôi debug là vấn đề thường xuyên gặp ở developer.

**6.5. Điều khó nhất khi viết Problem Statement là gì?**
Tách vấn đề khỏi giải pháp, xác định bottleneck cụ thể, và chọn metric khi số liệu thời gian giữa developer với sinh viên khác nhau, lại chủ yếu là tự ước lượng.
**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**
Nếu làm lại, tôi sẽ hỏi thêm developer/sinh viên, bấm giờ nhiều lỗi theo từng bước và hỏi sớm về chính sách chia sẻ log/mã nguồn. Có thể phản biện mạnh hơn xem AI có tạo thêm giá trị so với công cụ hiện có không.
**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi _problem → quy trình → metric → boundary → mức can thiệp AI → quyết định_ của bài nhóm mình.
Đầu tiên là liệt kê các candidate để lựa chọn, sau đó chấm điểm theo nhiều tiêu chí để quyết định vấn đề nhóm cần giải quyết. Sau đó đi kiểm chứng bằng cách phỏng vấn các bạn trong lớp về vấn đề và thấy có nhiều bạn cùng gặp vấn đề tương tự. Sau đó dùng AI kiểm chứng xem vấn đề còn thiếu sót hay bất hợp lý không.

---

## 7. Tài liệu tham khảo

- GitHub Docs, [Asking GitHub Copilot questions in your IDE](https://docs.github.com/en/copilot/how-tos/copilot-in-your-ide/chat-with-copilot/chat-in-ide).
- Sentry, [Sentry](https://sentry.io/welcome/).
