# User Test Guide — Personal Learning Notes

## Mục tiêu

Kiểm tra ba mechanism trên cùng một lesson và cùng một bộ learning traces:

- **C — Guided Learning Template:** learner tự phân loại ngay sau highlight.
- **B — Context Notebook:** hệ thống gom nguyên văn và backlink sau lesson; learner tự tổng hợp.
- **A — AI Review Brief:** AI tổng hợp draft có evidence; learner review và có thể handoff câu hỏi cho mentor.

Không kiểm tra mức độ “thích UI”. Cần quan sát liệu mechanism có giảm công sức tập hợp/tìm lại mà vẫn giữ được trust, ownership và hành vi quay lại dùng note hay không.

## Nguyên tắc phỏng vấn

- Hỏi về việc user vừa làm, không hỏi user muốn một feature tương lai như thế nào.
- Không nói trước option nào “thông minh hơn”, “nhanh hơn” hay “đáng tin hơn”.
- Không giải thích cơ chế trước khi user tự thử, trừ khi user bị kẹt thao tác.
- Ghi lại hành vi, thời gian, lần mở source và câu nói nguyên văn; không chỉ ghi nhận đánh giá ưa thích.
- Cho user quyền bỏ qua một task nếu họ không muốn gửi câu hỏi cho mentor.

## Lời mở đầu đọc cho user

> Mình đang tìm hiểu cách bạn ghi lại và dùng lại nội dung sau một bài học. Đây là prototype, không phải bài kiểm tra khả năng học của bạn. Mình quan tâm đến việc bạn sẽ tự nhiên làm gì, chỗ nào khó hiểu và điều gì khiến bạn tin hoặc không tin một note. Bạn cứ nói thành tiếng suy nghĩ của mình; nếu có phần nào không rõ, hãy nói ra thay vì cố đoán.

> Mình sẽ không giải thích solution trước. Mình muốn xem bạn tự khám phá flow như thế nào.

## Recruitment check

> Trong bảy ngày gần đây, bạn có highlight, ghi chú, viết câu hỏi hoặc lưu một nội dung học tập để xem lại sau không?

Nếu không, cảm ơn và dừng test. Câu này chỉ dùng để tuyển đúng người, không tính là evidence.

## Fixture cố định

Cho user dùng cùng lesson “From RAG workflow to Agentic RAG” và cùng hai nội dung mẫu:

1. Một ý về **Workflow RAG**: retrieve context rồi generate theo pipeline một chiều.
2. Một ý về **Agentic RAG**: planning, tool selection và self-correction.

Sau mỗi option, reset session để không mang traces của option trước sang option sau.

## Baseline trước prototype — 3 phút

### Câu hỏi hành vi quá khứ

1. Lần gần nhất bạn highlight hoặc ghi chú để xem lại là khi nào?
2. Bạn đã lưu ở đâu và đã làm những bước nào từ lúc highlight đến lúc kết thúc buổi học?
3. Khi cần tìm lại, bạn đã mở những nguồn nào? Mất khoảng bao lâu?
4. Bạn có viết lại hoặc sắp xếp các trace không? Vì sao?
5. Sau đó bạn có quay lại dùng note không? Lần đầu quay lại bạn tìm điều gì?

### Probe trung lập

- Lúc đó chuyện gì xảy ra tiếp theo?
- Bạn đã quyết định giữ đoạn đó dựa trên điều gì?
- Có bước nào bạn bỏ qua không?
- Chuyện gì khiến cách hiện tại thuận tiện hoặc bất tiện?

## Task 1 — Option C: Guided Learning Template

### Setup

Đổi sang `C · Template`, reset session.

### Prompt giao cho user

> Hãy học nhanh hai slide này như cách bạn thường học. Highlight một ý bạn muốn nhớ, một ý bạn chưa chắc, rồi hoàn thành note để sau này xem lại.

Không đọc các nhãn “Điểm chính/Chưa hiểu/Tham khảo” trước nếu user chưa nhìn thấy.

### Quan sát cần ghi

- User có nhận ra phải bôi đen text và xác nhận Highlight không?
- Sau highlight, user có hiểu vì sao phải phân loại không?
- User mất bao lâu để chọn nhãn?
- User có phân loại khi chưa hiểu rõ nội dung không?
- User có tiếp tục đọc hay bị dừng mạch?
- User có thêm note thủ công không?
- User có dùng backlink để kiểm tra context không?

### Probe sau task

1. Bạn vừa nghĩ gì khi hệ thống yêu cầu phân loại highlight?
2. Bước đó giúp bạn điều gì, nếu có?
3. Có lúc nào bạn muốn bỏ qua bước này không? Vì sao?
4. Nếu xem lại note sau một ngày, phần nào sẽ giúp bạn tìm nhanh hơn?
5. Bạn cảm thấy note này do bạn tạo ra hay do hệ thống tạo ra? Vì sao?

### Tín hiệu xác nhận/ bác bỏ

- **Ủng hộ:** user phân loại nhất quán, nói context còn rõ và note dễ quay lại.
- **Nghi ngờ:** user chọn nhãn ngẫu nhiên, bỏ qua nhiều lần hoặc nói micro-step làm gián đoạn việc học.

## Task 2 — Option B: Context Notebook

### Setup

Đổi sang `B · Notebook`, reset session.

### Prompt giao cho user

> Hãy highlight các ý bạn muốn giữ trong lesson. Khi xong, dùng notebook để chuẩn bị một bản tổng hợp ngắn cho lần xem lại sau.

### Quan sát cần ghi

- User có highlight tự nhiên hơn C không?
- User có hiểu trace được giữ nguyên văn không?
- User có mở backlink về đúng slide không?
- User có tìm được ý quan trọng trong notebook không?
- User mất bao lâu để tự viết summary?
- User có phải mở nhiều nơi hoặc quay lại source nhiều lần không?

### Probe sau task

1. Bạn mong đợi notebook này làm gì khi mở lần đầu?
2. Việc giữ nguyên văn giúp hoặc cản trở bạn ở điểm nào?
3. Bạn đã dùng backlink lúc nào? Nó có đủ context không?
4. Bạn đã quyết định ý nào cần đưa vào summary như thế nào?
5. Nếu không có AI diễn giải, phần việc nào vẫn còn nhiều nhất?

### Tín hiệu xác nhận/ bác bỏ

- **Ủng hộ:** user tìm lại đúng source nhanh hơn, tin nội dung vì còn nguyên văn và viết summary được.
- **Nghi ngờ:** notebook chỉ thành danh sách rời rạc, user không biết bắt đầu summary ở đâu hoặc vẫn phải copy/paste.

## Task 3 — Option A: AI Review Brief + Mentor Handoff

### Setup

Đổi sang `A · AI Brief`, reset session.

### Prompt giao cho user

> Hãy highlight hai ý bạn muốn dùng lại. Khi kết thúc lesson, review bản note được đề xuất. Chỉ giữ nội dung bạn thấy đúng và gửi câu hỏi cho mentor nếu bạn thực sự cần.

Không gọi đây là “AI summary” trước khi user tự đọc draft.

### Quan sát cần ghi

- User có hiểu draft là đề xuất, không phải note đã được lưu không?
- User có kiểm tra evidence/backlink trước khi giữ không?
- User có phát hiện điểm AI diễn giải rộng hơn trace không?
- User có chỉnh sửa draft không?
- User có phân biệt raw trace và AI synthesis không?
- User có hiểu mentor handoff gồm câu hỏi, traces liên quan và source không?
- User có chủ động bấm gửi hay do nghĩ đó là bước bắt buộc?

### Probe sau task

1. Theo bạn, bản draft này được tạo từ những gì?
2. Phần nào là nội dung bạn đã viết, phần nào là hệ thống đề xuất?
3. Bạn đã kiểm tra evidence ở đâu trước khi giữ?
4. Điều gì khiến bạn tin hoặc không tin draft?
5. Bạn có muốn sửa câu hỏi trước khi gửi mentor không? Vì sao?
6. Bạn nghĩ mentor sẽ nhận được những gì? Có thông tin nào bạn không muốn gửi không?
7. Nếu AI không tạo draft, bạn sẽ phải làm thêm bước nào?

### Tín hiệu xác nhận/ bác bỏ

- **Ủng hộ:** user phân biệt được draft và source, kiểm tra evidence, chỉnh sửa khi cần và thấy giảm công sức rõ ràng.
- **Nghi ngờ:** user mặc định tin draft, không biết draft đến từ đâu, không thấy cần review hoặc không muốn handoff vì privacy/trust.

## Task 4 — Return test sau khi đã thử cả ba

Cho user nhìn lại ba option nhưng không cho xem lại hướng dẫn.

> Hãy tìm lại một ý về Workflow RAG và một điểm bạn còn chưa chắc. Hãy nói cách bạn sẽ dùng note này nếu quay lại sau 24 giờ.

Ghi nhận:

- Thời gian tìm đúng hai ý.
- Số lần mở source.
- User có tìm được context đủ để hiểu lại không.
- User có biết bước tiếp theo cho điểm chưa hiểu không.
- User có chọn mở note hay mở lại toàn bộ lesson.

## So sánh sau cùng — không hỏi ngay “bạn thích cái nào?”

Hỏi theo thứ tự:

1. Trong ba cách, cách nào giúp bạn hoàn thành việc gom note với ít công sức nhất? Hãy chỉ vào bước cụ thể.
2. Cách nào khiến bạn cảm thấy nội dung vẫn là của mình nhất? Vì sao?
3. Cách nào khiến bạn tin nội dung nhất? Điều gì tạo ra trust?
4. Cách nào làm bạn bị gián đoạn nhiều nhất?
5. Cách nào giúp bạn tìm lại source/context tốt nhất?
6. Có option nào tạo ra output nhưng bạn không muốn quay lại dùng không?
7. Nếu chỉ được bỏ một cơ chế, bạn sẽ bỏ cơ chế nào? Vì sao?

Chỉ sau đó mới hỏi:

> Nếu phải chọn một cách để dùng trong những buổi học của bạn, bạn sẽ chọn cách nào? Điều gì có thể khiến bạn đổi lựa chọn?

## Bảng chấm quan sát

Chấm theo hành vi quan sát được, không chấm theo lời khen chung chung.

| Dimension | 1 — yếu | 3 — trung bình | 5 — mạnh |
|---|---|---|---|
| Completion effort | Bỏ task hoặc cần nhiều trợ giúp | Hoàn thành nhưng có pause | Hoàn thành mạch lạc |
| Context retrieval | Không tìm đúng source | Tìm đúng nhưng phải dò lại | Mở đúng source và hiểu lại nhanh |
| Trust | Tin mù quáng hoặc từ chối hoàn toàn | Có kiểm tra một phần | Biết lúc nào cần kiểm tra và vì sao |
| Ownership | Không biết ai tạo/diễn giải note | Nhận ra một phần | Phân biệt rõ phần của mình và hệ thống |
| Return value | Không biết dùng lại ra sao | Có thể dùng lại một ý | Tìm được ý quan trọng và điểm chưa hiểu |
| Interruption tolerance | Dừng học vì micro-step | Chấp nhận nhưng có friction | Phân loại tự nhiên, không mất mạch |

## Không được dùng các câu hỏi này

- Bạn có thích AI tự tóm tắt không?
- Bạn có muốn tính năng này không?
- Bạn thấy option nào hiện đại/đẹp hơn?
- Nếu có AI thì bạn có dùng thường xuyên không?
- Bạn có thấy cách này tốt hơn cách hiện tại không?

Các câu hỏi trên dẫn đến ý kiến tương lai hoặc đánh giá UI, không phải evidence hành vi.

## Mẫu ghi chép sau mỗi buổi

- Participant / ngày / lesson:
- Cách hiện tại trước prototype:
- Event cụ thể user đã kể:
- Option đã test:
- Task hoàn thành trong bao lâu:
- Số trace / số lần mở source:
- Quote về trust:
- Quote về ownership:
- Quote về interruption hoặc convenience:
- Có quay lại dùng note không:
- Evidence ủng hộ hoặc bác bỏ Pain Hypothesis A:
- Evidence nghiêng về Pain Hypothesis B:
- Điều cần thay đổi ở vòng test tiếp theo:

## Question bank mở rộng

Chỉ chọn các câu phù hợp với diễn biến; không hỏi toàn bộ trong một buổi.

### A. Kiểm tra user có hiểu cơ chế không

1. Bạn nghĩ chuyện gì vừa xảy ra sau khi bấm Highlight?
2. Theo bạn, trace này do bạn tạo, hệ thống tổ chức hay AI diễn giải?
3. Bạn nghĩ note hiện tại đã được lưu chưa? Vì sao bạn nghĩ vậy?
4. Bạn mong đợi nút tiếp theo sẽ làm gì?
5. Nếu muốn kiểm tra lại ý này, bạn sẽ bắt đầu từ đâu?
6. Bạn có thấy source slide và nội dung note đang liên kết với nhau không?
7. Có phần nào trong flow khiến bạn không biết phải quyết định không?

### B. Kiểm tra chất lượng bôi đen và trace capture

1. Bạn chọn đoạn này vì điều gì?
2. Bạn có muốn highlight cả đoạn dài hơn/ngắn hơn không?
3. Bạn có nhận ra đoạn vừa chọn đã được lưu chưa?
4. Bạn có muốn sửa text của trace trước khi tiếp tục không?
5. Khi một đoạn chứa cả ý quan trọng và ý chưa chắc, bạn sẽ xử lý thế nào?
6. Bạn có cần thêm một note riêng bên cạnh highlight không?
7. Nếu chọn nhầm, bạn mong muốn hoàn tác theo cách nào?

### C. Option C — câu hỏi về micro-step và ownership

1. Bạn có tiếp tục được mạch đọc sau khi phải phân loại không?
2. Bạn quyết định “Điểm chính” dựa trên tiêu chí nào?
3. Bạn phân biệt “Chưa hiểu” và “Tham khảo” như thế nào?
4. Có trường hợp nào bạn không đủ hiểu để chọn nhãn không?
5. Bạn muốn phân loại ngay hay gom lại cuối bài? Vì sao?
6. Nếu hệ thống tự gợi ý nhãn nhưng cho phép sửa, điều đó có giúp ích không?
7. Bạn có cảm thấy note này phản ánh cách hiểu của mình không?
8. Điều gì làm bạn tin template này sẽ hữu ích khi quay lại?
9. Có nhãn nào đang thiếu không?
10. Nếu bỏ bước phân loại, chất lượng note cuối bài sẽ thay đổi thế nào?

### D. Option B — câu hỏi về raw context và tổng hợp

1. Notebook này đang giúp bạn làm việc gì?
2. Bạn mong đợi hệ thống sắp xếp các trace theo thứ tự nào?
3. Bạn có cần lọc theo section, loại trace hoặc thời điểm không?
4. Backlink có đưa bạn đến đúng đoạn bạn cần kiểm tra không?
5. Bạn có tin nội dung hơn vì hệ thống giữ nguyên văn không?
6. Phần nào của việc tự tổng hợp vẫn còn tốn công?
7. Bạn sẽ bắt đầu summary từ trace nào? Vì sao?
8. Có trace nào bạn muốn bỏ trước khi viết summary không?
9. Nếu notebook có 30 traces, bạn sẽ tìm ý quan trọng bằng cách nào?
10. Bạn có quay lại notebook hay mở lại lesson gốc trước?

### E. Option A — câu hỏi về AI draft và evidence

1. Bạn nghĩ AI đã làm gì với các traces của bạn?
2. Đâu là phần AI tổng hợp mới, đâu là text gốc của bạn?
3. Draft này có claim nào nghe chắc chắn hơn evidence không?
4. Bạn kiểm tra evidence trước khi giữ draft ở mức nào?
5. Bạn muốn AI hiển thị những trace nào cạnh mỗi claim?
6. Khi draft sai, bạn muốn sửa, bỏ hay yêu cầu tạo lại?
7. Bạn có muốn AI tự đặt nhãn “Điểm chính/Chưa hiểu” không?
8. Khi nào bạn không muốn AI diễn giải?
9. Draft giúp bạn nhanh hơn ở bước nào cụ thể?
10. Review draft làm bạn thấy yên tâm hơn hay thêm việc hơn?
11. Bạn sẽ lưu draft ngay hay chờ kiểm tra hết evidence?
12. Nếu AI không có evidence/backlink, bạn có dùng draft không?

### F. Mentor handoff và contextual escalation

1. Điểm nào khiến bạn muốn hỏi mentor thay vì tự tìm hiểu?
2. Câu hỏi trong card có diễn đạt đúng điều bạn chưa hiểu không?
3. Bạn muốn chỉnh câu hỏi trước khi gửi ở đâu?
4. Mentor cần thấy những trace nào để trả lời được?
5. Có trace nào bạn không muốn gửi không? Vì sao?
6. Bạn có muốn chọn mentor/coach/bạn học không?
7. Bạn cần biết mentor sẽ nhận được những thông tin nào trước khi bấm gửi không?
8. Điều gì khiến bạn tin rằng câu hỏi đã được gửi thành công?
9. Nếu chưa có phản hồi, bạn sẽ quay lại card hay bỏ qua?
10. Bạn muốn đóng câu hỏi sau khi đã hiểu bằng cách nào?

### G. So sánh ba solution bằng tình huống

Đưa từng tình huống, yêu cầu user chọn cách xử lý và giải thích:

1. Bạn chỉ có 5 phút cuối lesson và có 10 highlights. Chọn cách nào?
2. Bạn đang đọc một khái niệm hoàn toàn mới và chưa biết ý nào quan trọng. Chọn cách nào?
3. Bạn cần chứng minh summary dựa trên source gốc. Chọn cách nào?
4. Bạn có một câu hỏi cần mentor trả lời với context đầy đủ. Chọn cách nào?
5. Bạn không muốn AI diễn giải nội dung chuyên môn. Chọn cách nào?
6. Bạn đã highlight nhiều lần nhưng thường không quay lại. Cách nào có khả năng giúp bạn quay lại nhất?
7. Bạn sợ bị gián đoạn khi học. Cách nào ít gây interruption nhất?
8. Bạn cần một note gọn để đọc trong 2 phút. Cách nào phù hợp nhất?
9. Bạn phát hiện draft AI có một claim sai. Bạn sẽ làm gì?
10. Bạn muốn kết hợp hai solution. Bạn sẽ lấy cơ chế nào từ mỗi option?

### H. Kiểm tra trade-off và ngưỡng quyết định

1. Bạn chấp nhận thêm tối đa bao nhiêu giây cho một micro-step sau highlight?
2. Bao nhiêu traces thì việc tự tổng hợp bắt đầu trở nên khó khăn?
3. Bao nhiêu traces thì bạn muốn bật AI brief?
4. Bạn ưu tiên nhanh hơn hay kiểm chứng được source hơn trong lesson quan trọng?
5. Bạn chấp nhận AI sửa câu chữ đến mức nào?
6. Khi nào ownership quan trọng hơn convenience?
7. Khi nào convenience quan trọng hơn việc tự diễn giải?
8. Bạn có muốn hệ thống tự chuyển từ B sang A khi trace vượt ngưỡng không? Vì sao?
9. Bạn có muốn C chỉ xuất hiện khi bạn đánh dấu “Chưa hiểu” không?
10. Nếu chỉ giữ một backlink, bạn muốn backlink ở trace, draft hay question card?

### I. Return test mở rộng

Sau 24 giờ hoặc ở cuối buổi test, không cho xem hướng dẫn:

1. Hãy tìm ý giải thích “retrieve-then-generate”.
2. Hãy tìm điểm khác nhau giữa Workflow RAG và Agentic RAG.
3. Hãy tìm lại câu hỏi bạn chưa chắc.
4. Hãy mở source để kiểm tra claim của note.
5. Hãy nói bạn sẽ làm bước gì tiếp theo với câu hỏi đó.
6. Bạn có nhớ note nằm ở đâu mà không cần trợ giúp không?
7. Bạn có hiểu lại context khi chỉ đọc note không?
8. Bạn có cần mở lesson gốc toàn bộ không?
9. Có phần nào trong note khiến bạn hiểu sai không?
10. Sau lần quay lại này, bạn có tiếp tục lưu note theo cách đó không?

### J. Câu hỏi kết thúc mở

1. Điều gì trong prototype khiến bạn muốn dùng lại nhất?
2. Điều gì khiến bạn không muốn dùng lại?
3. Bước nào nên biến mất?
4. Bước nào đang thiếu?
5. Bạn sẽ giải thích mechanism này cho một người bạn như thế nào?
6. Bạn nghĩ solution này đang giúp việc học hay chỉ giúp việc lưu trữ?
7. Nếu phải tin một phần của hệ thống, bạn sẽ tin phần nào?
8. Nếu phải kiểm tra một phần, bạn sẽ kiểm tra phần nào?
9. Điều gì sẽ khiến bạn đổi từ solution hiện tại sang solution khác?
10. Có điều gì prototype khiến bạn kỳ vọng nhưng không làm được không?
