# 03 — Individual Reflection

> Viết bằng lời của bạn (Phase 7 trong `01-worksheet.md`). Có thể dùng AI gợi ý câu hỏi tự soi, không dùng AI viết thay. 8-12 câu, có chuyện cụ thể.

## Thông tin cá nhân

- Họ và tên: Nguyễn Hải Đăng
- Mã học viên: 2A202602963
- Nhóm: A1
- Candidate problem nhóm chọn: ID switch detection

---

## 1. Tôi đã tham gia vào phần nào?

Ghi việc cụ thể + kết quả cụ thể. Không ghi chung chung kiểu "tham gia thảo luận".


| Hoạt động                   | Tôi đã làm gì? (việc cụ thể)                                                                                                           | Kết quả / ảnh hưởng tới nhóm                                                                                                      |
| ------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| Scan cá nhân                 | Tự tra cứu và hệ thống hóa lại các tác vụ hằng tuần của một Intern AI Engineer.                                                  | Đưa ra danh sách 10 bài toán sát thực tế, đa dạng lăng kính cho cá nhân.                                                   |
| Pitch Problem Card             | Pitch đề xuất "Debug Prompt Regression" với quy trình và metric lường trước rõ ràng.                                               | Được nhóm đánh giá là đề xuất hay, tuy nhiên nhóm quyết định chọn bài toán ID Switch Tracking vì tính chuyên sâu. |
| Challenge bài của bạn khác | Đặt câu hỏi và tranh luận sâu về các workflow, tập trung vào bài toán accuracy và giải pháp để mô hình không hallucinate. | Giúp nhóm chỉ ra các điểm nghẽn kỹ thuật và lỗ hổng logic trong quy trình xử lý.                                          |
| Gom trùng / cluster           | Đánh giá, phân loại và lọc các đề xuất bài toán hay, khó và mang tính chuyên sâu của cả nhóm.                             | Nhóm thu hẹp được danh sách candidate từ nhiều bài toán rời rạc.                                                             |
| Chọn candidate problem        | Bảo vệ bài toán prompt regression của cá nhân nhưng vẫn đưa ra các đánh giá khách quan, ủng hộ bài toán ID tracking.       | Tạo sự đồng thuận cao trong nhóm khi chốt chọn candidate problem cuối cùng.                                                    |
| Validation / research          | Thu thập, sàng lọc tài liệu trên mạng; tranh luận độ hữu ích thực tế và bảo vệ nguồn tài liệu YOLO/Ultralytics Tracking.   | Cung cấp cơ sở kỹ thuật chuẩn xác và đáng tin cậy cho bài toán nhóm chọn.                                                 |
| Problem Statement              | Thảo luận chi tiết về các pain point của AI Engineer đảm nhiệm rà soát model ở các frame bị skip tracking.                       | Định hình chính xác Boundary và Bottleneck thực tế cho Problem Statement nhóm.                                                  |
| Rule / Workflow / Agent        | Brainstorm ý tưởng về các luồng workflow kiểm soát lỗi, kể cả những phương án không đưa vào bản nộp cuối.                | Mở rộng góc nhìn so sánh giữa các mức độ can thiệp của AI/Rule.                                                              |
| Decision                       | Thực hiện voting trực tiếp về độ khả thi của kế hoạch triển khai bài toán nhóm đã chọn.                                      | Đưa ra quyết định No-Go dựa trên năng lực và nguồn lực thực tế của nhóm.                                                 |

**Dấu tay rõ nhất của tôi trong artifact cuối (1-2 câu):**

```text
Dấu tay rõ nhất của tôi nằm ở việc tìm kiếm, xác thực bộ tài liệu chuẩn YOLO/Ultralytics Tracking cho phần Research, đồng thời đóng góp lập luận phản biện sắc bén về rủi ro ở các frame bị skip tracking để nhóm đưa ra quyết định No-Go thực tế nhất.
```

---

## 2. Bảng dùng AI (mỗi dòng 1 phase có dùng AI — 2 cột cuối bắt buộc)


| Phase                   | Tôi dùng AI để làm gì?                                                          | AI hữu ích ở đâu?                                           | AI sai / hời hợt ở đâu?                                                                                 | Tôi sửa gì bằng nhận định của mình?*                                                                                   |
| ----------------------- | ------------------------------------------------------------------------------------- | ---------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------- |
| Scan                    | Gợi ý thêm các lăng kính bài toán từ công việc thực tế của AI Engineer. | Giúp liên tưởng nhanh các tác vụ tiềm năng.             | Một số gợi ý quá chung chung, mang tính lý thuyết.                                                   | Tự lọc và chỉ giữ lại 10 problem sát với trải nghiệm và workflows thực tế.                                         |
| Problem Card            | Phản biện Problem Card #1 để tìm ra điểm yếu khi pitch.                       | Chỉ ra nguy cơ sa lầy vào vòng lặp LLM-as-a-Judge.         | Tự động đề xuất lên Agent quá sớm mà chưa tối ưu Rule.                                          | Giữ nguyên mức Workflow và bổ sung Human Boundary kiểm tra case FAIL.                                                     |
| Workflow                | Nhờ gợi ý cấu trúc và xây dựng quy trình tối ưu workflow.                  | Giúp phác thảo nhanh khung quy trình ban đầu.              | Gợi ý workflow quá phức tạp, rườm rà và không phù hợp với thực tế kỹ thuật.                 | Đã tranh luận (debate) trực tiếp với AI để cắt giảm bước rác, tinh chỉnh workflow gọn và đúng thực tế hơn. |
| Research                | Tìm kiếm các pattern/tool đã giải quyết bài toán tương tự.                | Gợi ý các công cụ benchmark hiện có.                      | Trích dẫn một số thông tin thiếu nguồn xác thực đáng tin cậy.                                    | Tự tra cứu thủ công và bảo vệ tài liệu chính thống từ Ultralytics/YOLO.                                             |
| Problem Statement       | Phản biện các field mơ hồ trong Problem Statement v0.                            | Đặt câu hỏi giúp làm rõ Boundary bài toán.              | Gợi ý metric mang tính định tính, khó đo lường bằng số liệu.                                    | Tự điều chỉnh metric gắn liền với số khung hình bị skip tracking và tỉ lệ lỗi.                                    |
| Rule / Workflow / Agent | Phản biện ma trận lựa chọn giải pháp phù hợp.                                | Giúp phân tích ưu nhược điểm của từng mức can thiệp. | Đánh giá cao thái quá khả năng xử lý tự động của Agent.                                         | Giữ vững quan điểm ưu tiên Workflow kết hợp kiểm tra thủ công.                                                       |
| Decision                | Không dùng                                                                          | Không dùng                                                     | AI hay tâng bốc và hallucinate, đánh giá sai độ khả thi của bài toán khó như ID Tracking Skip. | Tự nghiên cứu và bỏ phiếu bầu "No-Go" dựa trên năng lực thực tế của nhóm vì bài toán out of scope.            |

> Nếu phase nào không dùng AI, ghi `Không dùng` và vì sao tự làm.

---

## 3. Reflection câu hỏi mở

Chọn 3-4 câu trong 6 câu dưới để viết thành đoạn 8-12 câu (không trả lời bullet 1 dòng):

- Tôi học được gì khi nghe top 3 problems của các bạn khác?
- Nhóm có lúc nào bị solution-first, đòi làm Agent cho ngầu không?
- Tôi có thay đổi ý kiến sau khi bị challenge không, vì sao đổi?
- Tôi đóng góp gì thật sự vào artifact cuối, phần nào có dấu tay của tôi?
- Điều khó nhất khi viết Problem Statement là gì, metric hay boundary?
- Nếu làm lại, tôi sẽ challenge nhóm mạnh hơn ở điểm nào?

**Reflection:**

```text
Từ top 3 bài toán từ các bạn trong nhóm — từ việc làm biên bản cuộc họp, rà soát annotation cho đến xử lý conflict môi trường khi setup project — tôi vạch ra được rất nhiều góc nhìn thực tế về những điểm nghẽn quy trình. Bản thân tôi vẫn giữ nguyên quan điểm bài toán "Debug Prompt Regression" của mình rất thiết thực với công việc hằng ngày của một AI Engineer. Dù vậy, tôi sẵn sàng lùi lại để nhóm ưu tiên một candidate mang tính chuyên sâu và có impact lớn hơn hẳn là "Phát hiện và sửa ID Switch Tracking giữa các frame". Trong suốt buổi làm việc, tôi đóng góp chủ yếu ở khâu phản biện và đặt câu hỏi đi sâu vào các điểm nghẽn kỹ thuật. Dù nhiều ý kiến tranh luận hay phương án dự phòng của tôi không xuất hiện trực tiếp trong kết quả cuối cùng, chúng đã giúp nhóm gọt giũa logic bài toán chặt chẽ hơn nhiều. Với tôi, phần khó nhất chính là xác định Boundary ở Problem Statement. Việc khoanh vùng ranh giới sao cho đúng — xác định rõ mô hình xử lý đến đâu khi gặp các frame nhầm ID — đòi hỏi sự thấu hiểu sâu về mặt kỹ thuật để không bị rơi vào bẫy solution-first hay chọn một scope quá sức so với nhóm.

```

---

## 4. Tự kiểm cuối bài (check trước khi nộp repo)

- [X]  [12đ] Cá nhân có 5+ problems + top 3 Problem Cards
- [X]  [12đ] Tôi đã pitch rõ + challenge nhóm đúng trọng tâm (ghi ở bảng mục 1)
- [X]  Nhóm có nhật ký hội tụ từ candidates về 1 bài
- [X]  [15đ] Nhóm có workflow trước/sau
- [X]  [20đ] Nhóm có PS v0/v1 với metric + boundary rõ
- [X]  [15đ] Nhóm có so sánh No AI / Rule / Workflow / Agent
- [X]  [10đ] Nhóm có Go / Not Yet / No-Go + lý do rõ
- [X]  [10đ] Reflection này có vai trò thật + AI giúp/sai ở đâu + điều học được + nếu làm lại đổi gì
- [X]  [6đ] Tôi tự giải thích được mạch problem → workflow → metric → boundary → độ phù hợp AI
