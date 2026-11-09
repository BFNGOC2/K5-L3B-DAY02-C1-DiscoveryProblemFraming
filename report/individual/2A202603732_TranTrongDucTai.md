# Báo cáo cá nhân — 2A202603732_TranTrongDucTai

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Trần Trọng Đức Tài
- MSSV: 2A202603732
- Email trường (không bắt buộc, repo có thể để public): 26ai.taittd@vinuni.edu.vn
- Tên nhóm: C1
- Link repo nhóm: https://github.com/BFNGOC2/K5-L3B-DAY02-C1-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Lặp lại | Khi bắt đầu một buổi lab hoặc bài tập lớn mới, tôi muốn kiểm tra nhanh checklist cấu trúc repo và format nộp bài, để không bị trừ điểm vì các lỗi quy cách cơ bản | Sinh viên trong nhóm (3–4 bạn) | Mỗi tuần 1–7 bài lab; mất khoảng 30–40 phút/bài đối chiếu rubric thủ công |
| 2 | Lặp lại | Khi đến hạn họp nhóm tiến độ hằng tuần, tôi muốn nắm được ai đã xong phần nào và ai đang bị kẹt, để phân chia lại công việc kịp deadline | Trưởng nhóm và các thành viên | Họp 1-2 lần/tuần; mất 20–25 phút hỏi từng người trong buổi họp vì tin nhắn trên Discord bị trôi |
| 3 | Lặp lại | Khi chuẩn bị đến giờ học, tôi muốn có thể xem ngay được lịch học mỗi buổi cùng tiến độ và thời hạn của mình trên trang Phoenix, để không tốn công tìm mail để vào file HTML của ban tổ chức, sau đó tìm lịch bằng MSSV rồi lại phải vào web Phoenix để xem các deadline. | Sinh viên theo khóa học AI thực chiến (khoảng hơn 6000) | Mỗi tuần 3–4 buổi học; mất khoảng 1'30s – 2'/lần tìm mail, mở file HTML rồi tra MSSV; thao tác lặp lại gây ức chế tâm lý và từng bị vào lớp trễ 1 buổi do tìm nhầm link cũ trong hộp thư |
| 4 | Tốn thời gian | Khi mở đề bài lab có nhiều file tài liệu dài (README, Rubric, Worksheet, Checklist), tôi muốn nắm nhanh các đầu việc bắt buộc phải nộp theo từng mốc thời gian, để kịp làm mà không bị ngợp hoặc bỏ sót yêu cầu | Sinh viên trong nhóm (3–4 bạn) | Mất 30–45 phút đọc lướt và lọc yêu cầu mỗi bài lab; từng bị sót mục checkpoint phụ ở bài lab trước |
| 5 | Cần đọc, tổng hợp nhiều thông tin | Khi chạy code thực hành gặp lỗi xung đột phiên bản thư viện (như CUDA, PyTorch, packages), tôi muốn tìm đúng nguyên nhân tương thích trong lịch sử log, để sửa ngay mà không phải gỡ cài đặt thử sai nhiều lần | Bản thân và bạn cùng nhóm phụ trách code | 2–3 lần/tuần; mất từ 45–60 phút tra cứu log lỗi trên StackOverflow và diễn đàn |
| 6 | Pain từ người khác | Khi phân chia viết báo cáo nhóm, các thành viên muốn nắm rõ rubric chấm điểm của từng mục cụ thể, để viết đúng yêu cầu mà không phải sửa lại nhiều lần trước deadline | Cả nhóm 4 người | Mất 2–3 lượt sửa lại bài viết trước giờ nộp; tốn hơn 1 tiếng cả nhóm ngồi họp lại để biên tập format chung |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.
  - Để có đủ các lăng kính còn lại theo yêu cầu đề bài, tôi nhờ AI gợi ý thêm và chọn bổ sung ý **#4 (lọc đầu việc từ tài liệu lab dài)**, ý **#5 (tìm nguyên nhân lỗi xung đột CUDA/PyTorch)** và ý **#6 (chuẩn hóa rubric báo cáo nhóm)**.

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Tra cứu lịch học & deadline (HTML vs Phoenix) (#3) | Nỗi đau thực tế chạm đến hơn 6000 học viên; tuy mất 1'30s–2'/lần nhưng thao tác phân mảnh gây ức chế tâm lý cao, tần suất lặp lại 3–4 buổi/tuần | Định dạng file HTML lịch học của BTC có giữ cấu trúc cố định qua các tuần không để parse tự động |
| 2 | Kiểm tra checklist cấu trúc repo và rubric nộp bài (#1) | Quy trình lặp lại mỗi bài lab, mất 30–40 phút/bài đối chiếu thủ công, dễ sót file dẫn đến rủi ro trừ điểm nặng | Mỗi bài lab rubric có thể thay đổi số lượng checkpoint khiến quy tắc kiểm tra phải cập nhật theo |
| 3 | Nắm tiến độ và người bị kẹt trong họp nhóm tuần (#2) | Pain thật trong phối hợp nhóm, giải quyết nạn trôi tin nhắn Discord, đo lường được thời gian họp | Các thành viên có chủ động cập nhật trạng thái công việc định kỳ hay không |

### Problem Card #1 — Checklist cấu trúc repo và rubric nộp bài (Problem #1)

| Trường | Nội dung |
|---|---|
| Job Story | Khi bắt đầu một buổi lab hoặc bài tập lớn mới, tôi muốn kiểm tra nhanh checklist cấu trúc repo và format nộp bài, để không bị trừ điểm vì các lỗi quy cách cơ bản |
| Actor | Sinh viên làm bài lab / Trưởng nhóm phụ trách nộp bài |
| Thời điểm / bối cảnh | Đầu buổi lab (setup repo) và 30 phút trước hạn chót nộp bài trên LMS |
| Quy trình hiện tại (3–7 bước) | 1. Đọc file README và SUBMISSION trên repo gốc · 2. Tạo fork và đổi tên repo theo cú pháp · 3. Soát từng file trong thư mục docs, report, assets · 4. Đối chiếu tên file báo cáo cá nhân `MSSV_HoTen.md` · 5. Kiểm tra link nộp bài trên LMS |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3 & 4: Mở từng file đối chiếu thủ công với Rubric và checklist (mất 15–20 phút, rất dễ sót file asset hoặc sai tên file) |
| Impact (nếu không giải thì sao) | Mất 30–40 phút/bài; rủi ro bị trừ 5 điểm do sai tên repo hoặc bị 0 điểm nếu thiếu file bắt buộc |
| Success metric (baseline → target) | Thời gian kiểm tra giảm từ 35 phút xuống dưới 3 phút; tỉ lệ lỗi quy cách cấu trúc giảm về 0% |
| Phương án không dùng AI | Dùng một script bash/powershell hoặc GitHub Action kiểm tra sự tồn tại của các file và regex kiểm tra tên file trước khi commit |
| Giả thuyết về AI (nếu có) | AI đọc qua toàn bộ rubric markdown và tự sinh ra script kiểm tra checklist tương ứng cho từng bài lab cụ thể |
| Cảm nhanh | Rule |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — ~35 phút

[1. Đọc README & SUBMISSION: 5'] → [2. Fork & đổi tên repo: 3']
→ [3. Mở rubric soát từng file: 15'] ← BOTTLENECK
→ [4. Đối chiếu cú pháp MSSV_HoTen: 7'] → [5. Check link LMS: 5']
```

### Problem Card #2 — Tra cứu lịch học & deadline (Problem #3)

| Trường | Nội dung |
|---|---|
| Job Story | Khi chuẩn bị đến giờ học, tôi muốn có thể xem ngay được lịch học mỗi buổi cùng tiến độ và thời hạn của mình trên trang Phoenix, để không tốn công tìm mail để vào file HTML của ban tổ chức, sau đó tìm lịch bằng MSSV rồi lại phải vào web Phoenix để xem các deadline |
| Actor | Học viên khóa học AI thực chiến (hơn 6000 học viên) |
| Thời điểm / bối cảnh | Trước mỗi buổi học khoảng 15–30 phút, hoặc khi cần lập kế hoạch làm bài tập trong tuần |
| Quy trình hiện tại (3–7 bước) | 1. Mở Gmail tìm mail thông báo của BTC · 2. Nhấp vào link mở file HTML lịch học · 3. Nhấn Ctrl+F gõ MSSV để tìm phòng và giờ học · 4. Mở tab mới truy cập trang Phoenix · 5. Đăng nhập và tìm mục bài tập để đối chiếu deadline · 6. Ghi chép thủ công vào lịch cá nhân |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 1 & Bước 3: Tìm mail và tra cứu MSSV trong file HTML lớn (mất khoảng 1' – 1'30s do nhiều mail trôi và phải gõ tìm MSSV, thao tác phân mảnh gây ức chế) |
| Impact (nếu không giải thì sao) | Mất 1'30s – 2' mỗi buổi học; tuần 3–4 buổi thao tác lặp lại gây ức chế tâm lý, dễ vào nhầm link cũ hoặc trễ giờ học |
| Success metric (baseline → target) | Thời gian tra cứu từ ~1'30s–2' xuống dưới 10 giây; 100% học viên xem được lịch học và deadline tại một nơi duy nhất |
| Phương án không dùng AI | Viết một extension trình duyệt hoặc script Google Sheet tự động đọc file HTML theo MSSV và sync thẳng vào Google Calendar |
| Giả thuyết về AI (nếu có) | AI đóng vai trò chatbot trên Discord/Telegram tự động nhận diện câu hỏi "Hôm nay tôi học gì?" dựa vào MSSV và trả về lịch + deadline |
| Cảm nhận nhanh | Rule / Workflow |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — ~1'30s – 2' (gây ức chế vì phân mảnh qua 2 nền tảng)

[1. Mở Gmail tìm mail BTC: 30s] → [2. Mở link file HTML: 15s]
→ [3. Ctrl+F gõ MSSV tìm lịch: 45s] ← BOTTLENECK (dễ ức chế)
→ [4. Mở web Phoenix: 15s] → [5. Tra deadline bài tập: 15s]
```

### Problem Card #3 — Nắm tiến độ và người bị kẹt trong họp nhóm (Problem #2)

| Trường | Nội dung |
|---|---|
| Job Story | Khi đến hạn họp nhóm tiến độ hằng tuần, tôi muốn nắm được ai đã xong phần nào và ai đang bị kẹt, để phân chia lại công việc kịp deadline |
| Actor | Trưởng nhóm và các thành viên nhóm làm bài lab (3–4 người) |
| Thời điểm / bối cảnh | Buổi họp online/offline định kỳ giữa tuần hoặc trước ngày nộp bài 1 ngày |
| Quy trình hiện tại (3–7 bước) | 1. Mở cuộc gọi họp nhóm trên Discord/Meet · 2. Trưởng nhóm hỏi từng thành viên về trạng thái task · 3. Thành viên tìm lại tin nhắn/file nháp để báo cáo · 4. Ghi nhận các điểm đang bị nghẽn (blocker) · 5. Thảo luận giải pháp gỡ nghẽn và phân công lại |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 2 & 3: Hỏi và chờ từng người lục lại tài liệu để báo cáo tiến độ (mất 10–15 phút, gây loãng buổi họp) |
| Impact (nếu không giải thì sao) | Buổi họp kéo dài 30–40 phút nhưng chỉ có 10 phút thảo luận thực chất; task bị chậm không được phát hiện sớm |
| Success metric (baseline → target) | Thời gian cập nhật tiến độ giảm từ 20 phút xuống dưới 5 phút; phát hiện blocker ngay trong ngày phát sinh |
| Phương án không dùng AI | Dùng bảng Trello / Notion Kanban cố định, mỗi bạn kéo thả card trước buổi họp 15 phút |
| Giả thuyết về AI (nếu có) | AI tổng hợp lịch sử commit/tin nhắn trên kênh thảo luận của nhóm và tạo bản tóm tắt tình trạng ai đang kẹt việc trước giờ họp |
| Cảm nhận nhanh | Workflow |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — ~25 phút

[1. Bắt đầu họp: 2'] → [2. Hỏi từng người tiến độ: 10'] ← BOTTLENECK
→ [3. Chờ lục tin nhắn/file nháp: 5'] → [4. Ghi nhận blocker: 3'] → [5. Phân công lại: 5']
```

### Card muốn pitch nhất

- Card số: **Card #2 (Problem #3 — Tra cứu lịch học & deadline HTML vs Phoenix)**
- Vì sao: Đây là bài toán có tác động thực tế rộng nhất (hơn 6000 học viên đều gặp). Tuy mỗi lần tra cứu chỉ mất khoảng 1'30s – 2', nhưng việc phải thao tác phân mảnh qua lại giữa Gmail, file HTML và web Phoenix 3–4 buổi/tuần gây ức chế tâm lý rất lớn và dễ vào nhầm link cũ. Bài toán có bottleneck rõ ràng, dễ đo lường thành công và giải quyết được triệt để bằng Rule/Workflow.
- Câu hỏi muốn nhóm phản biện: *"Nếu ban tổ chức thay đổi cấu trúc file HTML hoặc mã hóa lịch học theo từng lớp mà không dùng file chung nữa, giải pháp của nhóm có bị vô hiệu hóa không và làm sao để duy trì tính ổn định?"*

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Thời gian rà soát 1'30s – 2' là khá ngắn, liệu có đủ lớn để gọi là một 'nỗi đau' đáng giải quyết không? | Đồng ý một phần | Đã làm rõ trong phần Impact: Nỗi đau ở đây không chỉ là thời gian tuyệt đối, mà là **sự ức chế tâm lý và phân tâm** do quy trình phân mảnh qua 2 nền tảng lặp lại đều đặn 3–4 buổi/tuần ngay trước giờ vào lớp |
| Bài toán này thuần túy là đồng bộ dữ liệu (Calendar Sync), dùng AI có thể là 'dùng dao mổ trâu giết gà' | Hoàn toàn đồng ý | Đã xác định rõ phương án không dùng AI (Script/Extension) và ghi nhận cảm nhận nhanh là Rule / Workflow, không vội vàng áp đặt Agent phức tạp |
| Chưa có cơ chế xử lý khi sinh viên đổi lớp hoặc lịch học có thông báo bù đột xuất | Đồng ý | Đưa vào danh sách giả định cần kiểm chứng ở CP4 để hỏi người dùng về tần suất cập nhật lịch đột xuất của ban tổ chức |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Trình bày 3 Problem Cards cá nhân: Checklist repo (#4), Họp nhóm tiến độ (#5), Tra cứu lịch học & deadline (#6) | Nhóm chấm điểm toàn bộ 9 candidate; Candidate #2 (Debug lỗi của Ngọc) đạt điểm cao nhất (30/35) và được nhóm thống nhất chọn làm đề tài chính |
| Phản biện bài của bạn khác | **Câu hỏi tôi đã đặt:**<br>- **Cho Candidate #2 (Ngọc - Debug lỗi):** Với những lỗi phổ biến/cú pháp thì các công cụ sẵn có (như Copilot, ChatGPT hay chính Antigravity/Cursor) đã giải quyết trong vài giây, còn lỗi mất 20–45 phút thường phụ thuộc chặt chẽ vào context nghiệp vụ, luồng dữ liệu hoặc logic riêng của dự án. Giải pháp của bạn sẽ cung cấp thêm giá trị gì khác biệt so với việc dev tự copy traceback vào LLM, và làm sao để công cụ hiểu được toàn bộ context mã nguồn mà không gặp giới hạn token hay rò rỉ mã nguồn?<br>- **Cho Candidate #7 (Đạt - Phân bổ tài nguyên):** Nếu chỉ dùng một hệ thống Calendar/Booking thông thường kèm quy tắc ai đặt trước dùng trước (FIFO) hoặc phân quyền theo cấp bậc dự án thì đã đủ giải quyết chưa, hay hệ thống này bắt buộc phải giải quyết bài toán phân bổ động đa biến phức tạp nào khác?<br>- **Cho Candidate #8 (Đạt - Trễ mốc phụ thuộc chéo):** Nguyên nhân chính dẫn đến 7 lần trễ mốc là do thiếu công cụ theo dõi phụ thuộc chéo hay do văn hóa/SLA phản hồi giữa các phòng ban chưa được cam kết rõ ràng? Nếu các phòng ban vẫn không cập nhật trạng thái công việc lên hệ thống kịp thời thì công cụ giải quyết điểm nghẽn này như thế nào? | - Câu hỏi của tôi cho Candidate #2 được chọn làm điểm nghẽn trọng tâm cần giải quyết ở các bước sau: nhóm nhận ra giải pháp phải xử lý được context nghiệp vụ và luồng dữ liệu chứ không chỉ dừng ở việc đọc traceback đơn thuần.<br>- Giúp nhóm thấy rõ Candidate #7 chỉ cần Rule FIFO thông thường.<br>- Chỉ ra Candidate #8 phụ thuộc nặng nề vào văn hóa/SLA tổ chức và không vừa sức kiểm chứng trong 4 tiếng của buổi lab. |
| Nhận phản biện | **Câu hỏi tôi nhận được:**<br>1. *Từ Ngọc (về Card #6 - Tra cứu lịch học):* "Việc mỗi lần check chỉ mất 1-2p có thực sự cần thiết phải đưa ra giải pháp mới không vì nếu tạo ra giải pháp tốn thời gian và cũng mất 1p để phải xem lịch học?"<br>2. *Từ Ngọc (về Card #4 - Checklist repo):* "Tại sao lại chỉ kiểm tra nhanh checklist lúc đầu làm, mà không phải sau khi hoàn thành kiểm tra cho cẩn thận?"<br>3. *Từ Đạt (về Card #5 - Họp nhóm):* "Nguyên nhân chính khiến tin nhắn Discord bị trôi là do trao đổi tự do thiếu kênh/thread riêng, hay do thành viên không chủ động cập nhật tiến độ vào một nơi tập trung?" | **Tôi đã sửa gì:**<br>1. **Với Card #6:** Định hình lại giải pháp không phải là tạo ra thêm một trang web/app mới bắt người dùng phải mở vào xem mất thêm thời gian, mà là **cơ chế đẩy thông báo chủ động (Push Notification / Calendar Sync)**: tự động đồng bộ vào Google Calendar hoặc gửi tin nhắn Discord/Telegram trước 15–30 phút, người dùng **mất 0 giây tra cứu chủ động**. Tuy nhiên tôi đồng thuận với nhóm rằng impact của bài này (1.5–2 phút) nhỏ hơn nhiều so với bài debug lỗi (20–45 phút/lỗi, 3–5 lỗi/ngày) nên ủng hộ chọn bài của Ngọc.<br>2. **Với Card #4:** Bổ sung việc kiểm tra phải diễn ra ở **cả 2 thời điểm**: (1) Đầu buổi để setup đúng repo và cú pháp `MSSV_HoTen.md` ngay từ đầu; (2) Trước deadline 30 phút để rà soát toàn bộ file rubric cẩn thận.<br>3. **Với Card #5:** Bổ sung nhận định: Cần một **bảng trạng thái tập trung (Single Source of Truth như Trello/Notion)** để cập nhật trước buổi họp 15 phút, vì nếu chỉ chia thread thảo luận tự do thì tin nhắn vẫn bị trôi. |
| Gom cluster / cây OST | Cùng nhóm phân loại 9 candidate thành 3 cluster và xây dựng cây Opportunity Solution Tree rút gọn | Nhóm xác định đúng 1 Outcome chung, phân rã thành 3 nhánh Opportunity chuẩn xác và gạch bỏ các giải pháp công nghệ đội lốt cơ hội |
| Chọn candidate problem | Cùng nhóm chấm điểm shortlist trên 7 tiêu chí và thảo luận xử lý bất đồng | Thống nhất chọn Candidate #2 (Debug lỗi của Ngọc) vì đạt điểm cao nhất (30/35), actor rõ, pain có bằng chứng định lượng mạnh (3–5 lỗi/ngày, 20–45 phút/lỗi). Bài #6 của tôi đạt 21/35 điểm, được nhóm đánh giá là impact thời gian nhỏ hơn nên ưu tiên giải quyết bài #2. |
| Kiểm chứng / research | Đánh giá 6 giả định trong Assumption Map (mục 3.1) cùng nhóm; phân tích các rủi ro kỹ thuật về việc bóc tách call stack và bảo mật mã nguồn/API token khi gửi context ra bên ngoài | Nhóm xác định giả định #4 (chọn context) và #6 (chính sách bảo mật) là rủi ro trọng yếu, đưa vào làm tiêu chí thiết kế ranh giới ở mục 4.2 và 7 |
| Quy trình nhóm | Thiết kế Quy trình tương lai (mục 4.2) theo mô hình 5 bước: Rule bóc tách traceback → Rule + AI gom context và đề xuất giả thuyết & code diff → Developer HITL duyệt → Rule chạy test; thiết lập Boundary và phương án Rollback | Nhóm thống nhất dùng làm bản quy trình tương lai chính thức trong `group_report.md` (commit `7f56a28`) |
| Problem Statement | Hoàn thiện Problem Statement v1 gồm 9 trường (mục 7); đối chiếu và phân tích 5 điểm thay đổi cốt lõi so với v0; thiết lập 4 tiêu chí đánh giá đầu ra của AI (Groundedness, Precision, Actionability, Safety) | Định hình rõ ràng bài toán cho nhóm, gắn chặt tiêu chí đánh giá với rủi ro "lỗi chồng lỗi", được commit vào nhóm (`8d0165c`) |
| Mức can thiệp AI | So sánh chi tiết 4 mức can thiệp (No AI, Rule, Workflow, Agent) ở mục 6.2; lập luận chặt chẽ vì sao No AI/Rule không xử lý được logic runtime và vì sao Agent quá rủi ro về chi phí, rò rỉ mã nguồn và mất kiểm soát | Nhóm thống nhất chọn mức Workflow (Human-in-the-loop) làm giải pháp tối ưu cho đề tài (commit `4a859c4`) |
| Quyết định | Cùng nhóm thống nhất chốt quyết định **Not Yet** ở mục 8.2 (do rủi ro Viability ở mức Cao về bảo mật mã nguồn/log) và tổng kết Mục 9 (Hạn chế và hướng tiếp theo) gồm 3 hạn chế thực nghiệm và 3 bước triển khai cụ thể (Viability check, Pilot 1 tuần bấm giờ 15–20 bug, POC CLI Tool) | Giúp nhóm có căn cứ quyết định chuẩn xác, không vội pilot khi chưa rõ chính sách bảo mật và có ngưỡng dừng đo được |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Gợi ý mở rộng các góc nhìn để trải đủ 4 lăng kính (đặc biệt là lăng kính Tốn thời gian, Cần tổng hợp, Pain từ người khác) | Nhắc tôi nhớ đến các pain point thực tế khi cài đặt xung đột CUDA/PyTorch và duyệt qua các tài liệu lab dài | Gợi ý một số bài toán chung chung của ngành IT ("viết unit test", "tối ưu database") không gắn với trải nghiệm thật của sinh viên | Chọn lọc giữ lại 3 bài toán sát sườn sinh viên (#4, #5, #6) và tự viết lại Job Story kèm số liệu đo lường thật |
| CP2 Problem Card | Nhờ AI đóng vai người chấm lab khó tính để phản biện 3 Problem Cards (Checklist repo, Tra cứu lịch học, Họp nhóm) | Chỉ ra rằng thời gian tra cứu lịch học (1'30s–2') quá ngắn, có thể bị đánh giá là vụn vặt; đồng thời cảnh báo giải pháp Calendar Sync thuần túy không cần AI | Gợi ý biến bài toán thành "Chatbot trợ lý ảo đa năng tích hợp RAG" để hỏi đáp lịch học và bài tập (bị solution-first và phức tạp hóa) | Chấp nhận phản biện về thời gian để làm rõ nỗi đau tâm lý (phân mảnh nền tảng), giữ vững nhận định dùng Rule/Workflow thay vì Agent/Chatbot cồng kềnh |
| CP4 Research | Tra cứu các giải pháp debug lỗi tự động và cách các công cụ AI (như Cursor, GitHub Copilot Workspace, Sentry) thu thập context khi gặp lỗi | Tìm được pattern phổ biến là bóc tách Call Stack và lấy 20–30 dòng code quanh mỗi frame thay vì nạp cả repo | AI khẳng định "các LLM hiện đại có context 128k–1M token nên cứ nạp toàn bộ repo vào là AI tự hiểu hết" | Bác bỏ gợi ý nạp cả repo vì vi phạm nghiêm trọng bảo mật (Viability) và gây loãng context; quyết định thiết kế bộ lọc Regex/Rule để chỉ nhặt các file tham chiếu trực tiếp |
| CP5 Quy trình | Nhờ AI gợi ý cấu trúc quy trình tương lai và vẽ sơ đồ phân định vai trò | Gợi ý sơ đồ phân nhánh luồng kiểm tra kết quả test pass/fail trực quan | AI cho phép "AI tự áp dụng code diff và tự commit git nếu test pass" | Kiên quyết gạch bỏ hành động tự commit; đưa con người (Developer HITL) vào làm ranh giới an toàn bắt buộc (Boundary) trước khi áp dụng code diff |
| CP5–6 Problem Statement | Soạn thảo và chuẩn hóa 9 trường trong Problem Statement v1 và các tiêu chí đánh giá (eval) | Giúp định hình chuẩn cấu trúc so sánh thay đổi v0 → v1 và gợi ý các khía cạnh an toàn | Tiêu chí eval ban đầu AI gợi ý chung chung ("Code chạy đúng", "Giải thích hay") | Viết lại thành 4 tiêu chí đo được có điều kiện Đạt/Không đạt khắt khe: Groundedness (trích dẫn đúng dòng/biến), Precision (tránh báo nhầm gây lỗi chồng lỗi), Actionability (diff ngắn gọn <200 từ), Safety (mask secrets) |
| CP6 Mức can thiệp / quyết định | Phân tích ưu/nhược điểm giữa Workflow và Agent trong bài toán debug mã nguồn | Liệt kê các rủi ro kỹ thuật của Agent (chi phí token, latency khi duyệt repo) | AI vẫn nghiêng về việc khuyên nên thử nghiệm Agent vì "xu hướng công nghệ mới" | Giữ vững lập trường chọn Workflow (HITL) dựa trên nguyên tắc "bắt đầu từ mức đơn giản nhất" và bằng chứng phỏng vấn người dùng sợ "lỗi chồng lỗi" |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

Tôi nhận ra có những việc tuy nhiều người gặp nhưng không đáng để dùng AI giải quyết. Đề tài tra cứu lịch học của tôi chỉ mất tầm một hai phút, viết một đoạn script đồng bộ lịch là xong. Trong khi đó, bài debug lỗi của Ngọc giải quyết đúng vấn đề nhức nhối khi viết code: lập trình viên bị kẹt cả tiếng đồng hồ, mất tập trung và sợ nhất là sửa sai làm code phát sinh thêm lỗi mới. Vấn đề này phức tạp hơn nhiều và cần AI hỗ trợ suy luận ngữ cảnh thì mới hiệu quả.

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

Có, lúc đầu cả nhóm đều muốn làm một công cụ AI thật ngầu, có thể tự động đọc lỗi rồi tự sửa file và đẩy code lên git luôn. Nhóm chỉ nhận ra mình vội vàng khi ngồi vẽ lại các bước làm thực tế và tự hỏi: nếu AI sửa sai thì ai chịu trách nhiệm? Hóa ra người dùng rất sợ bị hỏng code dự án. Nhóm nhận ra điểm nghẽn thực sự là lúc tìm nguyên nhân qua các file liên quan chứ không phải lúc gõ code, nên quyết định chỉ để AI gợi ý cho con người xem và tự quyết định sửa.

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

Tôi đổi ý hai lần rõ rệt:
1. Khi Ngọc chỉ ra việc tra cứu lịch học chỉ mất một hai phút, tác động quá nhỏ, tôi thấy bạn nói đúng nên chủ động rút lui bài của mình để dồn sức làm bài debug lỗi.
2. Khi bàn về quy trình mới, ban đầu tôi muốn AI tự điền code sửa vào file luôn. Nhưng khi các bạn phản biện rằng làm thế rất dễ gây lỗi ngầm và lộ mã nguồn, tôi đã đổi ý sang phương án AI chỉ đưa ra gợi ý kèm dẫn chứng để người dùng tự duyệt, nếu không ưng thì bấm quay lại cách cũ.

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

Tôi khá bất ngờ khi kết quả phỏng vấn và khảo sát nhanh cho thấy lập trình viên không hề thiếu cách sửa lỗi. Phần khiến họ mệt mỏi nhất là phải mở từng file trong danh sách lỗi để lần xem dữ liệu sai từ đâu. Đa số người được hỏi đều không muốn AI tự động sửa file vì sợ làm phát sinh thêm lỗi khác, và có bạn đã quen dùng công cụ debug sẵn có nên không thấy cần công cụ mới. Điều này nhắc tôi rằng gợi ý của AI phải thật chắc chắn, thà nói chưa rõ còn hơn đoán bừa.

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

Khó nhất là không bị nhầm giữa vấn đề thực tế và giải pháp muốn làm, ví dụ viết nhầm vấn đề thành việc thiếu công cụ AI. Nhóm phải chỉnh sửa nhiều lần để nói rõ vấn đề là người lập trình mất từ mười phút đến cả tiếng đồng hồ chỉ để đọc log và mở các file liên quan. Ngoài ra, việc đặt ra mục tiêu đo lường cũng khó, nhóm phải thống nhất đo bằng việc giảm thời gian tìm lỗi và quan trọng nhất là sau khi sửa xong thì bộ kiểm thử phải chạy qua toàn bộ.

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

Nếu làm lại, tôi sẽ thay đổi hai việc:
1. Thúc đẩy nhóm bấm giờ thực tế cho cả hai nhóm là sinh viên và lập trình viên đi làm, vì thời gian làm bài tập và làm dự án thực tế rất khác nhau, không nên ước lượng chung chung từ trí nhớ.
2. Tôi sẽ phản biện mạnh hơn về chuyện bảo mật mã nguồn ngay từ đầu. Nhiều công ty cấm gửi mã nguồn lên các dịch vụ AI bên ngoài, nếu nhóm tính đến việc dùng các mô hình chạy trực tiếp trên máy sớm hơn thì đề tài sẽ thực tế hơn rất nhiều.

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

1. Vấn đề: Lập trình viên mất từ mười hai mươi phút với lỗi nhỏ đến cả tiếng với lỗi lớn chỉ để lần mò log và các file liên quan nhằm tìm nguyên nhân, vừa mất thời gian vừa dễ sửa sai.
2. Quy trình: Khi gặp lỗi, hệ thống lọc sạch thông báo lỗi, gom các đoạn mã liên quan để AI gợi ý nguyên nhân và hướng sửa, người dùng xem xét rồi quyết định áp dụng và chạy lại kiểm thử.
3. Chỉ số thành công: Giảm phân nửa thời gian tìm nguyên nhân lỗi, người dùng đồng ý với gợi ý của AI trên bảy mươi phần trăm và không làm phát sinh thêm lỗi mới sau khi sửa.
4. Ranh giới an toàn: AI tuyệt đối không tự ý sửa file hay đẩy code lên hệ thống, chỉ nhận những đoạn mã liên quan đã che thông tin nhạy cảm, và mọi kết quả chỉ mang tính tham khảo cho người dùng duyệt.
5. Mức can thiệp: Nhóm chọn hình thức quy trình từng bước có con người kiểm duyệt, vì bài toán cần AI đọc hiểu ngữ cảnh nhưng để AI tự làm hết thì quá rủi ro và dễ mất kiểm soát.
6. Quyết định: Nhóm quyết định chưa làm ngay vì rủi ro lộ mã nguồn còn cao và chưa rõ quy định bảo mật của tổ chức, cần thử nghiệm bấm giờ thực tế trước; nếu sau khoảng hai mươi lỗi mà không giảm được thời gian thì sẽ dừng lại và quay về cách làm thủ công.

---

## 7. Tài liệu tham khảo

-
