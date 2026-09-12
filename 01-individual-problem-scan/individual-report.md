# 01 — Individual Problem Scan

> Điền theo Phase 1 + Phase 2 trong `01-worksheet.md`. Tự scan trước, dùng AI sau để phản biện. Không copy ví dụ Weekly Report.

## Thông tin cá nhân

- Họ và tên: Nguyễn Hải Đăng
- Mã học viên: 2A202602963
- Vai trò / bối cảnh (VD: sinh viên năm X, intern PM, ...): Intern AI Engineer tại một công ty chuyên cung cấp Saas và Paas
- Công việc hằng tuần (3-5 gạch đầu dòng để soi problem):
  - Nhận, kiểm tra và làm sạch (cleaning) các tập dữ liệu huấn luyện hoặc annotation<sup></sup>.
  - Chạy thử nghiệm benchmark, đánh giá hiệu năng mô hình (eval) và tổng hợp báo cáo chỉ số<sup></sup>.
  - Thử nghiệm, tinh chỉnh prompt (prompt engineering) và kiểm tra lỗi suy giảm chất lượng (regression testing)<sup></sup>.
  - Đọc tài liệu kỹ thuật, nghiên cứu và thử nghiệm tích hợp các mô hình AI API mới<sup></sup>.
  - Phân tích log hệ thống, lọc lỗi hallucination hoặc câu trả lời không đạt chất lượng trên môi trường thực tế<sup></sup>.
  - Tối ưu hóa chi phí token, thời gian phản hồi (latency) và phối hợp hỗ trợ đội ngũ lập trình backend<sup></sup>.
  - Viết tài liệu hướng dẫn tích hợp SDK/API và soạn thông tin cập nhật phiên bản (release notes) cho pipeline AI<sup></sup>.

---

## Phase 1 — Scan 5+ problems (tối thiểu 5, khuyến khích 8-10)

**Cách điền:** mỗi dòng = việc gì + ai chịu + đo bằng gì. Cột `Dấu hiệu thật` bắt buộc có số: mất bao lâu (bấm giờ mấy lần), mấy lần/tuần, bao nhiêu người gặp, log/ticket/quote nào.


| **#** | **Lăng kính (Lặp lại / Tốn thời gian / AI có thể tốt hơn / Pain từ người khác)** | **Problem quan sát được**                                                           | **Ai chịu ảnh hưởng?**   | **Dấu hiệu thật (số + bằng chứng)**                                       |
| ----- | ---------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | ---------------------------- | ------------------------------------------------------------------------------- |
| 1     | Lặp lại                                                                                      | Format và clean dataset từ nhiều JSON/CSV schema khác nhau                          | Intern AI Eng, Data Team     | Mất 2–3 giờ/tuần; làm thủ công bằng script đơn giản, hay lỗi parser |
| 2     | Lặp lại                                                                                      | Chạy benchmark eval và tổng hợp Accuracy/Latency/Token Cost vào Sheets             | AI Engineer, Tech Lead       | 90 phút/tuần; phải copy-paste log từ MLflow/W&B sang Sheets                 |
| 3     | Tốn thời gian                                                                                | Đọc và summarize API documentation của model mới (e.g., Anthropic, Gemini, OpenAI) | AI Engineer, Dev Team        | 2–3 giờ/lần; tốn công thử từng SDK, test rate-limits                     |
| 4     | Tốn thời gian                                                                                | Debug prompt regression khi update system prompt mới                                   | AI Engineer                  | 2 giờ/lần; test thủ công 20–30 edge-case input xem output có gãy không  |
| 5     | AI có thể tốt hơn                                                                          | Phân loại log lỗi API (Rate limit vs Context length vs Internal Server Error)        | AI Engineer, On-call Dev     | 1–2 giờ/tuần; log quá rác, phải filter grep thủ công                    |
| 6     | AI có thể tốt hơn                                                                          | Viết SDK integration docs + code snippet cho Devs dùng AI API của công ty           | Backend Dev, Integration Eng | Devs hỏi lại cùng 1 lỗi integration 3–4 lần/tuần                         |
| 7     | Pain từ người khác                                                                         | Backend Devs hỏi cách config API Key, Token Limit, Model parameters trong Slack       | Backend Dev, AI Eng          | AI Eng bị ngắt quãng 3–5 lần/tuần để trả lời cùng 1 câu             |
| 8     | Pain từ người khác                                                                         | Product Manager xin estimate token cost cho feature AI mới                             | PM, AI Engineer              | 45 phút/lần; phải tính toán thủ công dựa trên token input/output       |
| 9     | Lặp lại                                                                                      | Viết Release Notes/Changelog cho AI pipeline/API updates                               | AI Eng, Product Team         | 30 phút/tuần; phải xem lại PRs, git commit log                              |
| 10    | Tốn thời gian                                                                                | Review và lọc hallucination/bad outputs trong log sản xuất của user                | AI Engineer, Domain Expert   | 3–4 giờ/tuần; đọc hàng trăm log chat để gán tag ground-truth          |

> Gợi ý tự soi: tuần trước mất nhiều thời gian nhất vào việc gì? Việc gì hay trì hoãn? Người khác hay hỏi lại câu gì? Workflow nào ai cũng biết là chậm?

**AI đã dùng ở Phase 1 (nếu có):**

- Prompt đã hỏi:
  - System Prompt: Bạn là một coach tư duy "Problem first, not AI first" cho lab này (Tìm đúng bài toán cho AI). Bạn không được đề xuất giải pháp trước khi có problem, workflow và metric rõ. Bạn KHÔNG được khen, không được tâng bốc - chỉ phản biện thẳng.
  - Bối cảnh:
    - Tôi là một intern AI engineer tại một công ty Saas/Paas.
    - Tôi đã xác định được một số công việc như sau:
      - Mỗi tuần phải run, test, evaluate và tổng hợp kết quả vào Google Sheets
      - Log API, phân loại lỗi để debug
      - Clean dữ liệu từ nhiều nguồn khác nhau, nhiều schema khác nhau
      - Update changelog, notes
      - Lọc hallucination
      - Kiểm tra slack
      - Viết report
  - Bạn có bổ sung gì từ những đầu việc trên, có thể là những vấn đề khác của những người trong công ty VD như PM, Backend devs, techlead hay những người khác trong team.
- Ý dùng được:
- Ý bỏ vì không phải pain thật:

**Self-check Phase 1:**

- [X]  Đủ 5+ dòng, mỗi dòng có actor + số đo cụ thể
- [X]  Dùng ít nhất 3/4 lăng kính
- [X]  Không có dòng chung chung kiểu "mất nhiều thời gian"

---

## Phase 2 — Top 3 Problem Cards

### 2.1. Chọn top 3

Giữ bài nào: actor cụ thể, workflow vẽ được 3-7 bước, bottleneck ở 1 bước, impact đo được. Loại bài quá rộng.


| Rank | Problem (copy từ bảng scan)                     | Vì sao chọn (2-3 ý)                                                                                     | Điều còn chưa chắc                                                    |
| ---- | ------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| 1    | Debug Prompt Regression                           | Workflow rõ, bottleneck cụ thể, tốn nhiều công sức, impact lớn đến release stability<sup></sup>. | Đo lường độ "chính xác" của prompt regression coverage<sup></sup>. |
| 2    | Chạy Benchmark Eval & Aggregate Report           | Metric thời gian rõ ràng, lặp lại hàng tuần<sup></sup>.                                             | Cần xem có thể dùng Rule/Script thay vì AI không<sup></sup>.         |
| 3    | Lọc Hallucination/Bad Outputs từ Production Log | Bottleneck nặng nhất về mặt thời gian, pain thật<sup></sup>.                                         | Scope dữ liệu nhạy cảm (User Privacy)<sup></sup>.                      |

### 2.2. Problem Cards chi tiết (lặp lại cho cả 3 cards)

---

#### Problem Card #1 — [Debug Prompt Regression]

```text
Problem 1 câu:
Mỗi lần update System Prompt, AI Engineer mất khoảng 120 phút test và so sánh thủ công 30+ edge cases để phát hiện prompt regression trước khi release.

Actor:
Intern / AI Engineer.

Thời điểm / bối cảnh:
Trước mỗi phiên bản release hoặc khi cần refactor system prompt trên môi trường Staging.

Current workflow 3-7 bước:
1. Sửa code và thay đổi system prompt trong codebase.
2. Chạy batch script để gọi API sinh 30 outputs tương ứng với 30 golden test cases.
3. Đọc từng output bằng mắt để kiểm tra chất lượng.
4. So sánh ngữ nghĩa từng output mới với Ground Truth (đáp án chuẩn cũ).
5. Tổng hợp các case bị lỗi/gãy format vào log file để sửa prompt.

Bottleneck:
Bước 3 & 4 (Đọc & So sánh 30 outputs bằng mắt) tốn khoảng 90/120 phút, dễ bỏ sót lỗi do mỏi mắt và đánh giá không đồng nhất.

Impact:
Tốn 2 giờ/lần testing. Nếu lọt lỗi regression ra Production, team mất 4–5 giờ hotfix và lãng phí chi phí API token của user.

Success metric:
Giảm tổng thời gian regression test từ 120 phút xuống dưới 20 phút/lần. Số lỗi regression lọt ra Prod = 0.

Non-AI alternative:
Dùng Regex hoặc String Exact Match bằng Python script. (Hạn chế: Cực kỳ cứng nhắc, LLM chỉ cần thay đổi từ nối hoặc cấu trúc câu là script báo FAIL dù ý nghĩa vẫn đúng).

AI hypothesis:
Dùng LLM-as-a-Judge với prompt kiểm thử chuẩn hóa để so sánh ngữ nghĩa output mới vs Ground Truth, tự động xuất file diff phân loại PASS/FAIL.

Quick gut:
[ ] No AI / process fix
[ ] Rule
[X] Workflow
[ ] Agent
[ ] Chưa biết
```
**Draft workflow Card #1** (ASCII / Mermaid / ảnh đính kèm):

```text
CURRENT STATE — 120 phút

[1 Edit Prompt: 10'] → [2 Run Batch API: 10'] → [3 Đọc 30 Outputs: 50'] <-- bottleneck → [4 So sánh Ground Truth: 40'] <-- bottleneck → [5 Log bug: 10']

FUTURE STATE — 18 phút

[1 Edit Prompt: 10'] → [2 Run Batch API: 2'] → [3 LLM Evaluator Auto: 2'] → [4 Human Review (chỉ case FAIL): 4'] <-- human boundary → [5 Deploy/Fix: 2']

Fallback: nếu AI Evaluator đưa kết quả nghi ngờ hoặc bị sai, AI Engineer bỏ kết quả tự động và review lại 30 outputs thủ công.
```
File đính kèm (nếu vẽ riêng): `01-individual-problem-scan-workflow-card-1.png`

---

#### Problem Card #2 — [Chạy Benchmark Eval & Aggregate Report]

```text
Problem 1 câu:
AI Engineer mất khoảng 90 phút mỗi tuần copy-paste log kết quả benchmark (Accuracy, Latency, Token Cost) từ terminal/MLflow sang Google Sheets để làm báo cáo cho Tech Lead.

Actor:
AI Engineer.

Thời điểm / bối cảnh:
Thứ Sáu hằng tuần, trước buổi tuần review performance với Tech Lead.

Current workflow 3-7 bước:
1. Chạy script eval benchmark trên môi trường test.
2. Export log kết quả ra file JSON/Text từ MLflow hoặc W&B.
3. Mở Google Sheets báo cáo tuần của team.
4. Parse và copy-paste thủ công từng chỉ số Accuracy, Latency, Cost vào đúng cột.
5. Định dạng lại màu sắc, bảng biểu và gửi notification lên kênh Slack.

Bottleneck:
Bước 4 (Copy-paste và format chỉ số thủ công vào Sheets) tốn khoảng 45 phút, nhàm chán và dễ nhầm lẫn dòng/cột.

Impact:
Mất 90 phút/tuần của 1 AI Engineer (tương đương 6 giờ/tháng). Báo cáo dễ bị trễ nếu gặp lỗi format.

Success metric:
Giảm tổng thời gian tổng hợp báo cáo từ 90 phút xuống dưới 5 phút/tuần.

Non-AI alternative:
Viết Python script kết hợp Google Sheets API và Slack Webhook để tự động đẩy thẳng dữ liệu từ MLflow sang Sheets. (Hoàn toàn khả thi và tối ưu hơn dùng AI).

AI hypothesis:
Không cần dùng AI cho bài toán này, dùng Rule/Script tự động hóa hoàn toàn.

Quick gut:
[ ] No AI / process fix
[X] Rule
[ ] Workflow
[ ] Agent
[ ] Chưa biết
```
**Draft workflow Card #2:**

```text
CURRENT STATE — 90 phút

[1 Run eval: 20'] → [2 Export log JSON: 10'] → [3 Copy-paste sang Sheets: 45'] <-- bottleneck → [4 Format bảng: 10'] → [5 Gửi Slack: 5']

FUTURE STATE — 5 phút

[1 Run eval: 2'] → [2 Python Script auto-push Sheets API: 1'] → [3 Auto Webhook Slack: 1'] → [4 Tech Lead review: 1'] <-- human boundary

Fallback: nếu API Google Sheets bị lỗi authentication, fallback về việc export file CSV thủ công.
```
File đính kèm: `01-individual-problem-scan-workflow-card-2.png`

---

#### Problem Card #3 — [Lọc Hallucination/Bad Outputs từ Production LogTên proble]

```text
Problem 1 câu:
AI Engineer mất 3–4 giờ mỗi tuần đọc thủ công hàng trăm log chat trên Production để lọc các phản hồi bị hallucination hoặc vi phạm format nhằm gán tag dữ liệu cải thiện mô hình.

Actor:
AI Engineer, Domain Expert / QA.

Thời điểm / bối cảnh:
Định kỳ giữa tuần khi cần thu thập bad cases để chuẩn bị dữ liệu fine-tune hoặc update prompt.

Current workflow 3-7 bước:
1. Pull dữ liệu chat log từ Production DB.
2. Đọc từng đoạn hội thoại giữa User và AI.
3. Đánh giá ngữ cảnh để phát hiện câu trả lời bị hallucination hoặc sai format.
4. Gán tag (Good / Bad / Hallucination / Format Error) thủ công vào file Excel.
5. Note lại các case điển hình vào danh sách "Golden Test Set".

Bottleneck:
Bước 2 & 3 (Đọc và lọc hàng trăm đoạn log không cấu trúc) tốn 180/240 phút, tốn rất nhiều năng lượng suy nghĩ.

Impact:
Mất 3–4 giờ/tuần. Do lượng log quá lớn, engineer chỉ lọc được khoảng 10-20% tổng số log, bỏ sót nhiều bug nguy hiểm.

Success metric:
Giảm thời gian lọc log từ 240 phút xuống dưới 45 phút/tuần, tăng tỉ lệ bao phủ log kiểm tra lên 80%.

Non-AI alternative:
Dùng Keyword Matching/Filter theo từ khóa tiêu cực (ví dụ: "xin lỗi", "tôi không biết", "lỗi"). (Hạn chế: Bỏ sót các câu AI trả lời rất tự tin nhưng sai sự thật - hallucination).

AI hypothesis:
Dùng AI làm bước pre-filter để quét toàn bộ log, phân loại và gán nhãn sơ bộ các case có nguy cơ cao, sau đó chuyển cho Engineer review chốt cuối.

Quick gut:
[ ] No AI / process fix
[ ] Rule
[X] Workflow
[ ] Agent
[ ] Chưa biết
```
**Draft workflow Card #3:**

```text
CURRENT STATE — 240 phút

[1 Pull DB Log: 15'] → [2 Đọc từng log chat: 120'] <-- bottleneck → [3 Phát hiện Hallucination: 60'] <-- bottleneck → [4 Gán tag Excel: 35'] → [5 Note Golden Set: 10']

FUTURE STATE — 40 phút

[1 Pull DB Log: 5'] → [2 AI Pre-filter & Tagging: 5'] → [3 Engineer review case nghi vấn: 25'] <-- human boundary → [4 Confirm & Export Golden Set: 5']

Fallback: nếu AI Pre-filter bỏ sót lỗi, quay lại lọc thủ công sample 50 log ngẫu nhiên mỗi tuần để kiểm tra chéo (spot-check).
```
File đính kèm: `01-individual-problem-scan-workflow-card-3.png`

---

### 2.3. Card muốn pitch nhất (chuẩn bị 2 phút)

**Card tôi muốn pitch nhất:**

```text
Card #1: Debug Prompt Regression
```
**Vì sao (2-3 câu: workflow gì, số đo gì, impact gì):**

```text
Workflow này giải quyết khâu testing thủ công mỗi khi refactor system prompt, vốn là bước nghẽn nhất trong quy trình release feature AI. Việc tự động hóa giúp giảm thời gian kiểm thử 30+ edge cases từ 120 phút xuống dưới 20 phút mà không bỏ sót lỗi. Tác động trực tiếp là giúp team tự tin release nhanh hơn, tránh nguy cơ gãy prompt trên Production làm tốn 4–5 giờ hotfix và lãng phí chi phí token của công ty.
```
**Câu hỏi tôi muốn nhóm challenge (1-2 câu hỏi đúng chỗ yếu):**

```text
1. Dùng LLM-as-a-Judge để chấm điểm một LLM khác thì làm sao đảm bảo con "Giám khảo" không bị hallucination hoặc chấm điểm cảm tính (bias)?
2. Chi phí gọi API và thời gian cho con AI "Giám khảo" chạy kiểm thử có đủ rẻ và nhanh hơn việc một engineer tự đọc không?
```
**AI phản biện Card (nếu có):**

- Điểm yếu AI chỉ ra:

  - Bài toán có nguy cơ sa lầy vào "vòng lặp vô tận" (dùng LLM để đánh giá LLM)<sup></sup> và tiêu chuẩn đánh giá "PASS/FAIL" đối với văn bản tự do dễ bị mơ hồ, thiếu nhất quán<sup></sup>.
  - **Phụ thuộc hoàn toàn vào AI Evaluator:** Bỏ qua các bước lọc cứng (Rule-based) khiến tốn tiền gọi API và tăng độ trễ khi chạy testing<sup></sup>.
  - **Chi phí API & Latency cao:** Nếu bộ test-set mở rộng (ví dụ từ 30 lên 100+ cases), việc gọi các model đắt tiền (như GPT-4o) sẽ gây tốn chi phí lớn<sup></sup>.
- Tôi sửa gì:

  - Thiết lập Human Boundary & Rubric chuẩn hóa:
    - AI Evaluator chỉ đóng vai trò phân loại sơ bộ và đưa ra gợi ý, AI Engineer chỉ cần đọc và duyệt lại các case bị đánh dấu FAIL (thay vì đọc toàn bộ 30 cases)<sup></sup>.
    - Định nghĩa rõ Ground Truth đi kèm với Eval Rubric chi tiết, ép AI Evaluator trả về dạng JSON cố định gồm 2 field: `status: PASS/FAIL` và `reason: <giải thích ngắn gọn>`<sup></sup>.
  - Chuyển sang Architecture 2 lớp (Hybrid Approach):
    - Lớp 1 (Rule-based): Dùng Python script kiểm tra lỗi cứng (JSON schema, regex, length). Lỗi ở đâu gạch tên ngay, không tốn API token<sup></sup>.
    - Lớp 2 (AI-based): Chỉ gửi các case đỗ Lớp 1 sang cho LLM-as-a-Judge đánh giá ngữ nghĩa<sup></sup>.
  - Tối ưu hóa Model Evaluator: Thay thế model đắt tiền bằng các dòng model nhỏ, rẻ và nhanh hơn (như GPT-4o-mini, Claude 3 Haiku, Gemini 1.5 Flash) kết hợp với System Prompt Evaluator được tối ưu ngắn gọn<sup></sup>.

### Self-check nộp phần 01

- [X]  Có 5+ problems + top 3 Cards đủ field
- [X]  Mỗi Card có workflow trước/sau + bottleneck + metric + fallback
- [X]  Đã chọn 1 card pitch + câu hỏi challenge
