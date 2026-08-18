# Ba Solution Cuối — Personal Learning Notes

## Quyết định chốt

Ba option cùng giải một task: sau một bài học, học viên tập hợp highlights, ghi chú và phần chưa hiểu thành tài liệu cá nhân đáng tin để tìm lại, ôn lại hoặc tiếp tục học mà không cần đọc lại toàn bộ bài.

Khác biệt cần test không phải UI, mà là **ai diễn giải traces và ai khởi tạo bản note**.

### Trigger riêng của Standard

- Ngay sau mỗi highlight trong lúc học, learner phân loại: **Điểm chính / Chưa hiểu-câu hỏi / Tham khảo**.
- Việc phân loại được ghi trực tiếp vào ba vùng của note; hệ thống không diễn giải hay tạo brief.
- Khi kết thúc bài, learner chỉ rà lại và lưu note đã được tích lũy trong lúc học.

Không có trigger chung trong constants. Standard++ và Wild vẫn dùng trigger cuối bài.

| Option / level | Solution | Cơ chế cốt lõi | Ai khởi tạo/diễn giải |
|---|---|---|---|
| C / Standard | **Guided Learning Template** | Learner phân loại trace vào “Điểm chính – Chưa hiểu – Tham khảo” ngay khi highlight | Learner tự tạo và tự diễn giải |
| B / Standard++ | **Context Notebook** | Gom trace nguyên văn, giữ link về source | Hệ thống tổ chức; learner diễn giải/tổng hợp |
| A / Wild | **AI Review Brief + Contextual Escalation** | AI tạo note nháp có evidence sau bài và mở escalation khi context cần | AI đề xuất; learner review/quyết định escalation |

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

## 3. Standard — Guided Learning Template

**Promise:** “Mỗi highlight được đặt đúng chỗ ngay lúc học, để cuối bài bạn đã có bản ghi ngắn do chính bạn chốt.”

### Mechanism

Ngay sau mỗi highlight trong lúc học, hệ thống mở một lựa chọn ngắn: **Điểm chính / Chưa hiểu-câu hỏi / Tham khảo**. Learner gắn nhãn và, nếu cần, viết note ngắn; trace được đưa thẳng vào vùng tương ứng của note. Đến cuối bài, learner rà lại các vùng và tự thêm “Việc tiếp theo” trước khi lưu. Hệ thống không tóm tắt, nhóm hay suy luận; traces gốc vẫn xem được làm reference.

### User và actors

1. Ngay sau mỗi highlight, learner chọn nhãn phân loại ngắn và có thể viết note.
2. Khi kết thúc lesson, learner rà lại note đã tích lũy, thêm Việc tiếp theo rồi lưu.
3. Khi cần ôn, learner mở note hoặc source link.
4. Hệ thống chỉ cung cấp khung, lưu note và giữ reference. Coach/instructor không tham gia flow chính.

### Trigger và trade-off

- **Classification trigger:** ngay sau mỗi highlight trong lúc learner đang học tài liệu; không chờ đến cuối bài.
- **Review trigger:** khi kết thúc lesson, learner chỉ rà lại và lưu note đã tích lũy.
- **Được:** bắt được ý định của learner ngay tại thời điểm highlight, khi context còn rõ; giảm gánh nặng phải nhớ lại “vì sao mình highlight đoạn này” ở cuối bài. Note có cấu trúc sẵn từ hành vi học thật, ownership và trust cao vì learner tự phân loại từng trace.
- **Đổi lại:** tạo micro-friction trong lúc đọc/học; learner có thể chọn nhãn vội, chọn sai hoặc bỏ qua nếu đang muốn giữ nhịp học. Chất lượng note phụ thuộc vào việc learner hiểu đủ để phân loại tại khoảnh khắc đó, nhất là với các đoạn đang mơ hồ.

### Cần test

Learner có chịu phân loại ngay sau highlight mà không thấy bị đứt mạch học không? Việc gắn nhãn tại chỗ có tạo note cuối bài dễ dùng hơn so với gom trace sau bài không, hay chỉ làm tăng thao tác mà không cải thiện khả năng tìm lại và hiểu lại context?

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

Khi learner mở phần note hoặc kết thúc lesson, AI dùng lesson source và traces để tạo **bản nháp** gồm Điểm chính, Chưa hiểu và Việc tiếp theo. Mỗi đề xuất phải có evidence/backlink. Các traces chưa đủ căn cứ để diễn giải nằm trong **Cần làm rõ**. Learner tự sửa/giữ/xóa, tự tìm lại source hoặc gửi contextual question card cho coach/instructor/bạn học. Không lưu hoặc gửi nội dung nào khi learner chưa review.

### User và actors

1. Learner mở brief, review evidence, sửa/giữ/bỏ từng cụm và xác nhận note final.
2. Với Cần làm rõ, learner quyết định tự xử lý hoặc chọn người nhận.
3. Nếu gửi, learner kiểm tra card gồm câu hỏi, trace liên quan, section/timestamp và source link; sau phản hồi learner tự đóng/giữ mở câu hỏi.
4. AI/hệ thống đề xuất cấu trúc, gộp traces có evidence và dựng context card. Coach/instructor/bạn học chỉ nhận câu hỏi learner chủ động gửi.

### Trigger và trade-off

- **Brief trigger:** khi learner mở note hoặc kết thúc bài, AI dùng lesson source và traces để tạo brief.
- **Escalation trigger:** chỉ xuất hiện khi learner chủ động gửi một mục cần làm rõ; không dựa vào suy đoán AI.
- **Được:** giảm mạnh công sức cấu trúc; không để câu hỏi bị chôn trong note; người hỗ trợ nhận đúng context.
- **Đổi lại:** AI có thể gộp hoặc diễn giải sai; review là friction cần thiết để bảo vệ trust. Escalation phụ thuộc người nhận, thời gian phản hồi và quyền riêng tư.

### Cần test

Learner có tin, review và dùng lại AI brief hơn Context Notebook không? Contextual handoff có được chọn khi thật sự có điểm chưa hiểu không?

## 6. Distance check và quy tắc quyết định

| So sánh | Khác biệt mechanism, không phải UI |
|---|---|
| Standard vs Standard++ | Standard thu nhãn learner ngay khi highlight và tích lũy note theo nhãn; Standard++ chỉ gom/định vị nguyên văn sau bài, learner vẫn tự diễn giải. |
| Standard++ vs Wild | Standard++ chỉ tổ chức nguyên văn; Wild cho AI diễn giải/gộp traces thành bản nháp có evidence và escalation khi cần. |
| Wild vs Standard | Wild khởi tạo note bằng AI draft sau bài để learner review; Standard để learner tự phân loại và tạo note từng trace trong lúc học. |

Chỉ đưa hướng đi tiếp nếu nó cải thiện quan sát được về công sức tập hợp, khả năng tìm đúng context, trust **và** hành vi quay lại dùng. Nếu cả ba được lưu nhưng không được mở lại, dừng tối ưu UI/summary và quay lại kiểm tra Pain Hypothesis B.
