# Team

> Điền file này trên repo chung do nhóm trưởng fork. Nhóm điền phần **Thông tin nhóm** và **Thành viên**. Mỗi người tự điền phần của mình trong **Cá nhân**. Không copy file này sang repo khác.

## Thông tin nhóm

- Tên nhóm: C1
- Candidate problem nhóm chọn (1 câu): Debug lỗi: khi gặp lỗi trong quá trình phát triển, developer muốn xác định nguyên nhân và hướng khắc phục để giảm thời gian debug.
- Quyết định cuối (Go / Not Yet / No-Go): Not Yet

## Thành viên

| STT | Họ và tên      | MSSV        | Vai trò trong nhóm                                                       | Tài khoản GitHub |
| --: | -------------- | ----------- | ------------------------------------------------------------------------ | ---------------- |
|   1 | Thiều Thế Ngọc     | 2A202603788 | Ghi chép, Phản biện, Phỏng vấn kiểm chứng, research, phân công công việc                                            | BFNGOC2          |
|   2 | Vũ Tuấn Đạt        | 2A202603744 | Vẽ quy trình, viết Problem Statement, phản biện, phụ giúp nhóm trưởng các task khác                                 | datkunal         |
|   3 | Trần Trọng Đức Tài | 2A202603732 | Phản biện, Thiết kế quy trình tương lai (4.2), Phân tích mức can thiệp AI (6.2), Problem Statement v1 & Eval (7), Hạn chế & Hướng tiếp theo (9) | DucTai2804       |
|   4 |                    |             |                                                                                                                     |                  |

Không ghi email hay số điện thoại vào bảng này, vì repo có thể để public.

Gợi ý vai trò (một người có thể giữ nhiều vai): điều phối thời gian, ghi chép, người phản biện chính, phụ trách kiểm chứng (phỏng vấn/survey), phụ trách research, vẽ quy trình, viết Problem Statement.

## Phân công theo checkpoint

| Checkpoint                                 | Người chính | Người hỗ trợ | Sản phẩm                                       |
| ------------------------------------------ | ----------- | ------------ | ---------------------------------------------- |
| CP3 — Hội tụ nhóm                          | Thiều Thế Ngọc, Vũ Tuấn Đạt, Trần Trọng Đức Tài |              | Cluster, cây OST, bảng chấm điểm               |
| CP4 — Kiểm chứng                           | Thiều Thế Ngọc, Vũ Tuấn Đạt, Trần Trọng Đức Tài |              | Assumption map, snapshot hoặc survey           |
| CP4 — Research                             | Thiều Thế Ngọc, Vũ Tuấn Đạt, Trần Trọng Đức Tài |              | Bảng research có link                          |
| CP5 — Quy trình trước/sau                  | Thiều Thế Ngọc, Vũ Tuấn Đạt, Trần Trọng Đức Tài |              | Quy trình + bảng before/after                  |
| CP5 — Problem Statement v0                 | Thiều Thế Ngọc, Vũ Tuấn Đạt, Trần Trọng Đức Tài |              | Problem Statement v0                           |
| CP6 — Mức can thiệp + Problem Statement v1 | Thiều Thế Ngọc, Vũ Tuấn Đạt, Trần Trọng Đức Tài |              | Ma trận, AI Canvas, eval, Problem Statement v1 |
| CP6 — Quyết định                           | Thiều Thế Ngọc, Vũ Tuấn Đạt, Trần Trọng Đức Tài |              | 4 rủi ro + Go/Not Yet/No-Go                    |

## Cá nhân

Mỗi thành viên thêm một mục theo mẫu dưới đây, tiêu đề là `HoVaTen-MSSV`.

### Thiều Thế Ngọc-2A202603788

**Phần việc phụ trách:** Ghi chép, phản biện, tổng hợp kiểm chứng và research, lập bảng chấm điểm candidate, phối hợp phân công và hoàn thiện báo cáo nhóm.

- **Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):
  - Pitch ba candidate và tham gia chấm điểm để nhóm chọn bài debug lỗi.
  - Tổng hợp snapshot phỏng vấn developer/sinh viên và kết quả hỏi nhanh; hệ thống hóa tín hiệu xác nhận, phản bác và giới hạn mẫu.
  - Tổng hợp research GitHub Copilot và Sentry; hoàn thiện các phần before/after, Problem Statement v0, AI Canvas và quyết định Not Yet dựa trên nội dung/bằng chứng nhóm cung cấp.

- **Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):
  - `report/team/group_report.md`: mục 2.4, 3.2–3.3, 4.3, 5, 6.3, 8.2.
  - `report/individual/2A202603788_ThieuTheNgoc.md`: mục 4–5.

- **Điều mình học được từ phần nhóm:**

- Học cách trình bày vấn đề với nhóm, tìm điểm nghẽn thực sự và thống nhất ý kiến giữa các thành viên.

### Vũ Tuấn Đạt-2A202603744

**Phần việc phụ trách:** Vẽ quy trình, viết Problem Statement, phản biện; gom cluster và cây OST ở CP3; phụ giúp nhóm trưởng các task khác.

- **Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):
  - Gom nhóm 9 candidate thành các cluster và dựng cây OST (CP3).
  - Đặt câu hỏi phản biện cho candidate #1, #3, #5 của các bạn; nhận và trả lời phản biện #7, #8, #9 cho candidate của mình.
  - Điền quy trình hiện tại của bài debug lỗi (mục 4.1): sơ đồ, bảng 5 bước, bottleneck.
  - Xác định ô của bài trong ma trận độ mơ hồ × độ phức tạp (mục 6.1).
  - Trả lời hai câu hỏi PAIR về augment/automate và báo nhầm/bỏ sót (mục 6.4).
  - Đánh giá bốn rủi ro Value / Usability / Feasibility / Viability (mục 8.1).

- **Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):
  - `group_report.md`: mục 2.2 và 2.3 (cluster, cây OST), 4.1, 6.1, 6.4, 8.1.
  - Commit `7ce87b4` ("docs: điền mục 4.1, 6.1, 6.4, 8.1 của báo cáo nhóm").
  - Báo cáo cá nhân: `report/individual/2A202603744_VuTuanDat.md`.

- **Điều mình học được từ phần nhóm:**

### Trần Trọng Đức Tài-2A202603732

**Phần việc phụ trách:** Thiết kế quy trình tương lai (mục 4.2), phân tích và so sánh 4 mức can thiệp AI (mục 6.2), hoàn thiện Problem Statement v1 kèm 4 tiêu chí đánh giá đầu ra AI (mục 7), tổng kết hạn chế và hướng phát triển tiếp theo (mục 9), tham gia phản biện ở CP3 và CP5.

- **Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):
  - Pitch 3 Problem Cards cá nhân (Checklist repo, Họp nhóm, Tra cứu lịch học) và đặt câu hỏi phản biện trọng tâm cho bài Candidate #2 (Ngọc) về bối cảnh mã nguồn / giới hạn token, Candidate #7 (Đạt) và #8 (Đạt), giúp nhóm hội tụ đúng vào Candidate #2.
  - Thiết kế quy trình tương lai 5 bước (mục 4.2): bóc tách rõ vai trò giữa Con người, Rule và AI; xác lập ranh giới an toàn (Boundary: AI không tự commit/ghi đè code, chỉ nhận context liên quan) và quy trình quay về (Rollback).
  - So sánh 4 mức can thiệp (No AI, Rule, Workflow, Agent) ở mục 6.2; lập luận chặt chẽ lý do chọn Workflow (HITL) và từ chối Rule hay Agent.
  - Xây dựng Problem Statement v1 với 9 trường hoàn chỉnh (mục 7), lập bảng giải thích 5 điểm thay đổi cốt lõi so với v0, thiết lập 4 tiêu chí đánh giá đầu ra của AI (Groundedness, Precision, Actionability, Safety).
  - Viết mục 9 (Hạn chế và hướng tiếp theo): chỉ rõ 3 hạn chế thực nghiệm và đề xuất 3 bước triển khai cụ thể (Viability check, Pilot 1 tuần, POC CLI Tool).

- **Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):
  - `group_report.md`: mục 4.2 (Quy trình tương lai), mục 6.2 (So sánh 4 mức can thiệp AI), mục 7 (Problem Statement v1 & tiêu chí đánh giá), mục 9 (Hạn chế và hướng tiếp theo).
  - Các commit trên GitHub repository:
    - Commit `7f56a28`: `docs(team): bo sung muc 4.2 quy trinh tuong lai vao group_report`
    - Commit `4a859c4`: `docs(team): hoan thien muc 6.2 so sanh 4 muc can thiep AI`
    - Commit `8d0165c`: `docs(team): hoan thien muc 7 problem statement v1 va muc 9 han che huong tiep theo`
  - Báo cáo cá nhân: `report/individual/2A202603732_TranTrongDucTai.md`.

- **Điều mình học được từ phần nhóm:**
  - Hiểu sâu sắc rằng ứng dụng AI không phải là thần thánh hóa giao toàn quyền cho Agent làm từ A-Z, mà giá trị thực tế nằm ở việc xác định đúng bottleneck và phân định ranh giới an toàn giữa Rule, AI và con người.
  - Nhận ra tầm quan trọng của việc phản biện: Ban đầu ai cũng nghĩ đến giải pháp của mình hoặc muốn xây dựng giải pháp lớn, nhưng qua phản biện và phỏng vấn thực tế, nhóm đã gọt giũa được một bài toán sắc bén, khả thi và có thể đo lường rõ ràng.
