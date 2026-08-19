# Kịch bản thuyết trình — Thiết kế 3 solution Personal Learning Notes

Thời lượng gợi ý: 10–12 phút. Mục tiêu của buổi demo là giúp người nghe hiểu **vì sao có ba mechanism khác nhau**, sau đó nhìn thấy sự khác nhau đó trong prototype. Không trình bày ba màn hình như ba phiên bản UI.

## 0. Chuẩn bị trước khi demo

- Mở [index.html](./index.html) qua local server để các tương tác trình duyệt hoạt động ổn định.
- Giữ cùng một fixture cho cả ba option: lesson “From RAG workflow to Agentic RAG”, năm slide tương tác, cùng một hoặc hai highlight mẫu.
- Xóa session cũ bằng `Reset session` trước khi bắt đầu.
- Quy ước trong script: A = Wild / AI Review Brief, B = Standard++ / Context Notebook, C = Standard / Guided Learning Template. Có thể demo theo thứ tự C → B → A để đi từ ít suy luận đến nhiều suy luận.

## 1. Mở bài: đây là một bài test mechanism, không phải bài thi UI — 45 giây

**Lời nói**

> Nhóm không bắt đầu bằng câu hỏi “nên làm AI Notes như thế nào?”. Nhóm bắt đầu từ một job: sau một bài học nhiều nội dung, học viên muốn gom những điểm quan trọng và phần chưa hiểu thành một tài liệu cá nhân đáng tin để tìm lại, ôn lại và tiếp tục học mà không cần đọc lại toàn bộ bài.

> Ba option hôm nay cùng phục vụ đúng job này. Vì vậy input, source, quyền chỉnh sửa và outcome được giữ nguyên. Chúng ta chỉ thay đổi một biến quan trọng: ai khởi tạo note và ai diễn giải traces.

**Chỉ vào prototype**

1. Slide deck có cùng năm slide cho cả ba tab.
2. Bôi đen một đoạn text: đây là cùng một learning trace.
3. Chỉ vào source slide/backlink: mọi option phải trả lời được “ý này đến từ đâu?”.

## 2. Khung Standard → Standard++ → Wild — 90 giây

### Trục thiết kế

Giải thích ba option trên hai trục:

| Trục | Standard | Standard++ | Wild |
|---|---|---|---|
| Ai diễn giải trace? | Learner | Learner, hệ thống chỉ tổ chức | AI đề xuất, learner kiểm duyệt |
| Khi nào note được khởi tạo? | Ngay sau từng highlight | Cuối lesson, từ trace nguyên văn | Cuối lesson hoặc khi mở note, từ AI draft |
| Mức suy luận của hệ thống | Không suy luận | Không suy luận | Gộp/diễn giải có evidence |
| Handoff sang người khác | Không có trong flow chính | Không có trong flow chính | Learner chủ động gửi contextual question card |

**Lời nói**

> Standard là điểm neo an toàn nhất: không AI, learner tự đặt trace vào đúng vùng. Standard++ thêm tổ chức tự động nhưng vẫn giữ nguyên văn. Wild mở thêm diễn giải bằng AI và escalation, nhưng bắt buộc review.

> Đây là một spectrum về ownership, timing và inference. Không phải ba skin của cùng một màn hình.

## 3. Constants và constraints — 90 giây

**Những gì bắt buộc giống nhau**

- Target user: học viên vừa hoàn thành lesson nhiều nội dung.
- Situation: đã tạo highlight, note ngắn, câu hỏi hoặc đánh dấu chưa hiểu.
- Input fixture: cùng lesson và cùng traces.
- Core outcome: tìm lại ý quan trọng và điểm chưa hiểu; giảm công sức tập hợp; không bỏ quên câu hỏi.
- Context contract: mỗi trace có section/slide/timestamp và backlink về source.
- Learner control: learner được sửa, bỏ, giữ và xác nhận trước khi lưu hoặc gửi.
- Return test: sau 24 giờ tìm lại một ý quan trọng và một điểm chưa hiểu.
- Exclusion: không thêm reminder, flashcard, lịch ôn tập, gamification hoặc thay đổi lesson.

**Lời nói**

> Nếu thay cả source, người dùng, số trace và outcome cùng lúc thì không biết kết quả khác nhau đến từ mechanism hay do fixture. Vì vậy constants là contract để distance check có ý nghĩa.

> Constraint quan trọng nhất là AI không được tự lưu hoặc tự gửi. Wild chỉ được đề xuất; quyền quyết định vẫn ở learner. Standard và Standard++ không được âm thầm diễn giải, nếu không chúng sẽ không còn là baseline.

## 4. Vì sao đúng là ba solution này? — 75 giây

**Lời nói**

> Pool giải pháp ban đầu có cả template, notebook, AI grouping, flashcard và lịch ôn tập. Nhóm chỉ giữ ba hướng tạo ra ba mức inference khác nhau và cùng giải đúng pain A: công sức tập hợp và tìm lại context.

1. **Guided Learning Template** kiểm tra xem learner có sẵn sàng trả một micro-step ngay lúc highlight để có ownership và cấu trúc tốt hơn không.
2. **Context Notebook** kiểm tra xem chỉ cần tự động gom nguyên văn và giữ backlink đã đủ giảm pain chưa, không cần AI diễn giải không.
3. **AI Review Brief + Contextual Escalation** kiểm tra giá trị và rủi ro khi giao việc cấu trúc/diễn giải cho AI, đồng thời không chôn câu hỏi chưa hiểu.

> Flashcard, reminder và lịch ôn tập không được chọn vì chúng chuyển sang kiểm tra Pain Hypothesis B — thói quen quay lại dùng note — thay vì cô lập pain A. Chúng có thể là hướng sau, không phải biến số của vòng test này.

## 5. Option C — Standard / Guided Learning Template — 2 phút

### Mechanism cần nói trước khi click

> Ở Standard, mỗi highlight mở một lựa chọn ngắn: Điểm chính, Chưa hiểu–Câu hỏi hoặc Tham khảo. Learner tự diễn giải và hệ thống chỉ lưu vào ba vùng. Note được khởi tạo dần trong lúc học; cuối lesson chỉ rà lại và lưu.

### Thao tác demo

1. Chọn tab **C · Template**. Việc đổi option reset session; nói rõ đây là deliberate reset để không mang traces của option trước sang option sau.
2. Bôi đen câu “Search runs only once before LLM invocation.”
3. Bấm popup `Highlight` để xác nhận.
4. Chọn vùng **Điểm chính** trong panel.
5. Bôi đen một ý về “multi-hop reasoning”, xác nhận rồi chọn **Chưa hiểu**.
6. Bấm backlink `Slide 4` trong template để quay lại source.
7. Bấm `+ Note thủ công`, nhập: “Cần so sánh latency giữa fixed pipeline và agent loop.”

### Lời nói sau thao tác

> Ở đây hệ thống không nói highlight này có nghĩa gì. Learner nói. Vì vậy trust và ownership cao, source vẫn có backlink, nhưng learner chịu micro-friction và có thể phân loại vội hoặc bỏ qua.

### Câu hỏi cần test

> Người học có chịu bị ngắt mạch sau mỗi highlight không? Note có dễ tìm lại hơn đủ để bù cho thao tác phân loại không?

## 6. Option B — Standard++ / Context Notebook — 2 phút

### Mechanism cần nói trước khi click

> Standard++ bỏ classification trigger trong lúc đọc. Learner highlight tự nhiên. Khi kết thúc lesson, hệ thống gom nguyên văn theo section/thời điểm, gắn metadata và backlink. Learner vẫn tự chọn ý chính và viết tổng hợp.

### Thao tác demo

1. Chọn tab **B · Notebook**; session C bị reset.
2. Bôi đen hai đoạn ở slide 3 và slide 4; xác nhận popup mỗi lần.
3. Thêm một **Note thủ công** để mô phỏng câu hỏi learner tự viết.
4. Bấm `Kết thúc lesson & mở notebook`.
5. Trong notebook, bấm `Mở source ↗` trên một trace. Chỉ ra prototype quay đúng slide, không phải một danh sách text rời rạc.
6. Viết một câu vào vùng summary cá nhân.

### Lời nói sau thao tác

> B và C có cùng mức inference: không AI diễn giải. Khác biệt là timing và ownership. C bắt learner tạo cấu trúc ngay tại thời điểm highlight; B trì hoãn cấu trúc đến cuối bài nhưng giảm copy/paste và phân tán.

### Câu hỏi cần test

> Gom trace nguyên văn và giữ context có đủ giảm barrier để learner thực sự tổng hợp và quay lại dùng không? Hay notebook chỉ trở thành một danh sách rời rạc?

## 7. Option A — Wild / AI Review Brief + Contextual Escalation — 2 phút

### Mechanism cần nói trước khi click

> Wild dùng lesson source và traces để tạo draft gồm Điểm chính, Cần làm rõ và Việc tiếp theo. Mỗi đề xuất có evidence/backlink. AI không được lưu thay learner. Mục Cần làm rõ chỉ chuyển thành question card khi learner chủ động review và gửi.

### Thao tác demo

1. Chọn tab **A · AI Brief**; session B bị reset.
2. Bôi đen hai trace liên quan đến fixed workflow và Agentic RAG; xác nhận từng popup.
3. Bấm `Kết thúc lesson & tạo AI brief`.
4. Chỉnh trực tiếp một draft để cho thấy learner có quyền sửa.
5. Bấm backlink evidence để quay lại đúng slide.
6. Bấm “Giữ” một đề xuất; mở mockdata **Contextual handoff · Mentor**.
7. Đọc card: người nhận “Mentor · Dr. Linh”, câu hỏi đã được AI diễn đạt lại, các traces liên quan và backlink về slide.
8. Chỉnh câu hỏi nếu cần rồi bấm “Gửi cho mentor”; chỉ ra trạng thái “Đã gửi cho mentor”.

### Lời nói sau thao tác

> A giảm mạnh công sức cấu trúc, nhưng đổi lại cần review bắt buộc vì AI có thể gộp sai hoặc diễn giải vượt evidence. Mockdata này cho thấy handoff không phải “AI tự gửi”: AI chỉ dựng card, còn learner kiểm tra người nhận, câu hỏi, traces và source rồi mới bấm gửi. Card cũng chỉ gửi context liên quan, không gửi toàn bộ note.

### Câu hỏi cần test

> Learner có tin và dùng lại draft nhiều hơn notebook không? Lợi ích cấu trúc có lớn hơn chi phí review và rủi ro sai không? Contextual handoff có được dùng khi thật sự có điểm chưa hiểu không?

## 8. Overlap và ranh giới — 90 giây

### Điểm overlap có chủ ý

- Cả ba đều nhận cùng loại trace: highlight/note/question.
- Cả ba đều giữ source backlink và learner control.
- Cả ba đều có thể tạo một tài liệu để tìm lại sau lesson.
- Cả ba đều có thể bị thất bại nếu learner không quay lại dùng note; đây là lý do vẫn phải đo Pain Hypothesis B.

### Ranh giới mechanism

| So sánh | Không phải khác nhau ở | Khác nhau thực sự ở |
|---|---|---|
| C vs B | Màu sắc, card, label | C phân loại ngay lúc highlight; B gom nguyên văn sau lesson |
| B vs A | Có cùng trace/source | B không diễn giải; A AI gộp và tạo draft có evidence |
| C vs A | Cùng có cấu trúc note cuối cùng | C learner khởi tạo từng item; A AI khởi tạo draft để learner review |

**Lời nói**

> Nếu chỉ đổi UI mà giữ cùng trigger và cùng ai diễn giải thì đó là một solution. Ba option này được tách vì mỗi option thay đúng một cơ chế có thể quan sát: timing, inference và ownership.

## 9. Vì sao phải tách thay vì trộn thành một sản phẩm? — 60 giây

> Nếu trộn cả ba vào một flow, chúng ta mất baseline. Không biết learner gặp friction vì phân loại, vì review AI hay vì việc tổng hợp sau bài.

> Tách ba solution giúp nhóm đo trade-off: thao tác thêm của C, công sức tổng hợp còn lại của B, và review/trust của A. Sau vòng test có thể chọn một hướng, hoặc dùng một hướng làm fallback; nhưng trước khi có evidence không nên gom chúng thành “AI Notes” chung chung.

## 10. Kết luận và decision rule — 45 giây

> Decision rule không phải “người dùng thích option nào”. Nhóm chỉ đưa một hướng đi tiếp nếu nó cải thiện đồng thời công sức tập hợp, khả năng tìm đúng context, trust và hành vi quay lại dùng.

> Nếu C giảm sai context nhưng micro-friction quá lớn, B có thể là baseline tốt hơn. Nếu B giảm công sức nhưng note vẫn không được mở lại, cần quay lại kiểm tra Pain Hypothesis B. Nếu A tiết kiệm nhiều thời gian nhưng learner không tin draft, không nên tối ưu thêm UI trước khi giải quyết trust và evidence.

**Kết thúc demo bằng:** mở `Lịch sử buổi học`, chỉ ra mỗi phiên được lưu theo option, số trace, source và thời gian. Đây là cầu nối cho return test sau 24 giờ, không phải một tính năng ngoài scope để làm demo đẹp hơn.
