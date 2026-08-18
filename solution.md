# Ba Solution Cuối — Personal Learning Notes

## Quyết định chốt

Ba option cùng giải một task: sau một bài học, học viên tập hợp highlights, ghi chú và phần chưa hiểu thành tài liệu cá nhân đáng tin để tìm lại, ôn lại hoặc tiếp tục học mà không cần đọc lại toàn bộ bài.

Khác biệt cần test không phải UI, mà là **ai diễn giải traces và ai khởi tạo bản note**.

### Trigger riêng của Option A / Wild

- Ngay sau mỗi highlight trong lúc học, learner phân loại: **Điểm chính / Chưa hiểu-câu hỏi / Tham khảo**.
- Khi learner mở note hoặc kết thúc bài, AI dùng các trace đã được phân loại để tạo brief.
- Escalation chỉ xuất hiện khi learner chủ động gửi một mục cần làm rõ.

Không có trigger chung trong constants. Option B và C vẫn dùng trigger cuối bài.

| Option / level | Solution | Cơ chế cốt lõi | Ai khởi tạo/diễn giải |
|---|---|---|---|
| C / Standard | **Guided End-of-Lesson Template** | Mẫu “Điểm chính – Chưa hiểu – Việc tiếp theo” | Learner tự tạo và tự diễn giải |
| B / Standard++ | **Context Notebook** | Gom trace nguyên văn, giữ link về source | Hệ thống tổ chức; learner diễn giải/tổng hợp |
| A / Wild | **AI Review Brief + Contextual Escalation** | Learner phân loại trace ngay khi highlight; AI tạo note nháp có evidence và mở escalation khi context cần | Learner gắn ý định; AI đề xuất; learner review/quyết định escalation |

## 1. Parking Lot đã mở lại

| # | Hướng | Trạng thái |
|---|---|---|
| 1 | AI tự động nhóm trace thành note, learner kiểm tra/xác nhận | Dùng trong Wild, được mở rộng bằng escalation |
| 2 | Mẫu cuối bài “Điểm chính – Chưa hiểu – Việc tiếp theo” | Chọn làm Standard |
| 3 | Notebook thu thập highlight nguyên văn và backlink đúng vị trí | Chọn làm Standard++ |
| 4 | Flashcard/lịch ôn tập từ note đã xác nhận | Không chọn: chủ yếu đo Pain Hypothesis B |
| 5 | Learner tự chọn ba ý chính và một câu hỏi | Không chọn riêng: biến thể hẹp của #2 |
| 6 | AI tách mục chưa chắc/chưa hiểu để learner mang hỏi coach/bạn học, kèm context | **Bổ sung duy nhất** vì pool chưa có human escalation khi context cần |

Không thêm hướng khác. Pool đã có user-led/no-inference (#2, #3); hướng #6 chỉ lấp khoảng trống human escalation.

## 2. Constants — contract giữ nguyên giữa ba prototype

| Thành phần | Giữ nguyên |
|---|---|
| Target user | Học viên vừa hoàn thành một lesson có nhiều nội dung |
| Situation | Đã tạo highlight, note ngắn, câu hỏi hoặc đánh dấu “chưa hiểu” và dự định xem lại sau |
| Input fixture | Cùng một lesson và cùng bộ traces cố định cho cả ba prototype |
| Core job/outcome | Tạo tài liệu đáng tin để tìm lại ý quan trọng và phần chưa hiểu; giảm công sức tìm/sắp xếp; không bỏ quên câu hỏi |
| Context | Mỗi trace có section/timestamp và link mở lại đúng đoạn source |
| Quyền learner | Có quyền sửa, bỏ, xác nhận mọi nội dung trước khi lưu hoặc gửi |
| Return test | Sau 24 giờ, tìm lại một ý quan trọng và một điểm chưa hiểu từ lesson đó |
| Loại trừ | Không thêm reminder, flashcard, lịch ôn tập, gamification hoặc thay đổi lesson |
| Metrics | Thời gian hoàn tất; số nơi phải mở; số lần quay lại source; tỷ lệ tìm đúng; trust; có quay lại dùng tài liệu hay không |

## 3. Standard — Guided End-of-Lesson Template

**Promise:** “Kết thúc bài học bằng một bản ghi ngắn, do chính bạn chốt.”

### Mechanism

Hệ thống mở mẫu trống có ba vùng: **Điểm chính / Chưa hiểu / Việc tiếp theo**. Learner tự chọn và gõ nội dung. Hệ thống không tóm tắt, nhóm hay suy luận; traces gốc vẫn xem được làm reference.

### User và actors

1. Learner kết thúc lesson, mở mẫu, tự nhớ/chọn nội dung, viết rồi lưu.
2. Khi cần ôn, learner mở note hoặc source link.
3. Hệ thống chỉ cung cấp khung, lưu note và giữ reference. Coach/instructor không tham gia flow chính.

### Trigger và trade-off

- **Trigger:** ngay sau khi learner bấm kết thúc lesson.
- **Được:** ownership và trust cao; không có rủi ro AI diễn giải sai.
- **Đổi lại:** tốn công nhất, phụ thuộc trí nhớ/kỷ luật; learner có thể bỏ dở bước tổng hợp.

### Cần test

Nếu chỉ cho khung rõ ràng, learner có tự tổng hợp, lưu và tìm lại được note không?

## 4. Standard++ — Context Notebook

**Promise:** “Mọi dấu vết bạn đã tạo được gom về một nơi, luôn quay lại đúng ngữ cảnh gốc.”

### Mechanism

Khi lesson kết thúc, hệ thống thu thập **nguyên văn** highlight, note và câu hỏi, sắp theo section/thời điểm. Mỗi item có type, metadata và backlink. Hệ thống không diễn giải hay tự viết summary. Learner giữ/bỏ/tag trace và tự viết phần tổng hợp.

### User và actors

1. Learner mở notebook đã gom sẵn, xem trace trong context và tự viết tổng hợp rồi lưu.
2. Khi ôn, learner tìm trace hoặc đi về source.
3. Hệ thống trích xuất, tổ chức và định vị context; không suy luận. Coach/instructor không tham gia flow chính.

### Trigger và trade-off

- **Trigger:** ngay sau khi learner bấm kết thúc lesson.
- **Được:** giảm copy/paste, phân tán và công sức tìm lại; trust cao vì source còn nguyên.
- **Đổi lại:** learner vẫn tự chọn ý chính và viết tổng hợp; notebook có thể chỉ là danh sách rời rạc.

### Cần test

Việc gom traces và giữ context có đủ giảm barrier để learner tổng hợp/lưu note và tìm lại tốt hơn Template không?

## 5. Option A / Wild — AI Review Brief + Contextual Escalation

**Promise:** “Bạn nhận bản nháp có cấu trúc từ chính dấu vết của mình; phần chưa chắc giữ nguyên context để bạn tự quyết định hỏi người phù hợp.”

### Mechanism

Ngay sau mỗi highlight trong lúc học, learner phân loại trace thành **Điểm chính**, **Chưa hiểu/câu hỏi** hoặc **Tham khảo**. AI dùng lesson source cùng các traces đã được learner phân loại để tạo **bản nháp** gồm Điểm chính, Chưa hiểu và Việc tiếp theo. Mỗi đề xuất phải có evidence/backlink. Các traces chưa đủ căn cứ để diễn giải nằm trong **Cần làm rõ**. Learner tự sửa/giữ/xóa, tự tìm lại source hoặc gửi contextual question card cho coach/instructor/bạn học. Không lưu hoặc gửi nội dung nào khi learner chưa review.

### User và actors

1. Ngay sau khi highlight, learner chọn một nhãn phân loại ngắn.
2. Learner review evidence, sửa/giữ/bỏ từng cụm trong brief và xác nhận note final.
3. Với Cần làm rõ, learner quyết định tự xử lý hoặc chọn người nhận.
4. Nếu gửi, learner kiểm tra card gồm câu hỏi, trace liên quan, section/timestamp và source link; sau phản hồi learner tự đóng/giữ mở câu hỏi.
5. AI/hệ thống đề xuất cấu trúc, gộp traces có evidence và dựng context card. Coach/instructor/bạn học chỉ nhận câu hỏi learner chủ động gửi.

### Trigger và trade-off

- **Classification trigger:** ngay sau mỗi highlight trong lúc học, learner phân loại: **Điểm chính / Chưa hiểu-câu hỏi / Tham khảo**. Learner chủ động làm việc này, không chờ tới cuối bài.
- **Brief trigger:** khi learner mở note hoặc kết thúc bài, AI dùng các traces đã được phân loại để tạo brief.
- **Escalation trigger:** chỉ xuất hiện khi learner chủ động gửi một mục cần làm rõ; không dựa vào suy đoán AI.
- **Được:** giảm mạnh công sức cấu trúc; không để câu hỏi bị chôn trong note; người hỗ trợ nhận đúng context.
- **Đổi lại:** AI có thể gộp sai hoặc phân loại sai; review là friction cần thiết để bảo vệ trust. Escalation phụ thuộc người nhận, thời gian phản hồi và quyền riêng tư.

### Cần test

Learner có tin, review và dùng lại AI brief hơn Context Notebook không? Contextual handoff có được chọn khi thật sự có điểm chưa hiểu không?

## 6. Distance check và quy tắc quyết định

| So sánh | Khác biệt mechanism, không phải UI |
|---|---|
| Standard vs Standard++ | Standard bắt learner tạo note từ mẫu trống; Standard++ gom/định vị toàn bộ trace, nhưng learner vẫn tự diễn giải. |
| Standard++ vs Wild | Standard++ chỉ tổ chức nguyên văn sau bài; Wild thu ý định của learner ngay khi highlight, rồi cho AI diễn giải/gộp thành bản nháp có evidence và escalation khi cần. |
| Wild vs Standard | Wild bắt đầu bằng learner phân loại từng highlight trong lúc học, sau đó AI dựng draft để review; Standard bắt learner tự viết toàn bộ note từ đầu sau bài. |

Chỉ đưa hướng đi tiếp nếu nó cải thiện quan sát được về công sức tập hợp, khả năng tìm đúng context, trust **và** hành vi quay lại dùng. Nếu cả ba được lưu nhưng không được mở lại, dừng tối ưu UI/summary và quay lại kiểm tra Pain Hypothesis B.
