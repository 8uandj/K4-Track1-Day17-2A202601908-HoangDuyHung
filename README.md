# Track 1 — Day 17: Finding and Validating Pain Points

## Team Report — Case B: Personal Learning Notes

---

## 1. Thông tin cá nhân và nhóm

- **Tên nhóm:** `Đại đại`
- **Số thành viên:** 3
- **Case đã chọn:** Case B — Personal Learning Notes
- **MHV của chủ repo:** `2A202601908`
- **Têm của chủ repo:** `Hoàng Duy Hưng`


| Thành viên | MHV | Họ và tên | 
|---|---|---|---|
| 1 | `2A202602021` | `Nguyễn Đặng Thành Vinh` | 
| 2 | `2A202601762` | `Đoàn Ngọc Linh` | 
| 3 | `2A202601908` | `Hoàng Duy Hưng` | 

---

## 2. Problem Hypothesis Brief — Kết quả Chặng 1

> Toàn bộ nội dung trong phần này là giả thuyết trước phỏng vấn, chưa phải fact hoặc evidence về người dùng.

### 2.1. Solution directive

Trong khi học, học viên có thể highlight nội dung, đánh dấu phần “Chưa hiểu” hoặc viết câu hỏi và ghi chú ngắn. Khi bài học kết thúc, hệ thống kết hợp các dấu vết này với nội dung bài để tạo một bản ghi chú có cấu trúc. Học viên được chỉnh sửa và xác nhận trước khi lưu.

### 2.2. Capability trung tính

Biến những dấu vết do người học chủ động tạo ra trong quá trình học thành một tài liệu cá nhân có cấu trúc, giữ được ngữ cảnh, có thể kiểm tra, chỉnh sửa, lưu trữ và sử dụng lại.

Capability này không mặc định AI là cách triển khai duy nhất.

### 2.3. Chuỗi thay đổi được kỳ vọng

```text
Dấu vết học tập được ghi lại
→ được tập hợp và đặt lại vào đúng ngữ cảnh
→ học viên kiểm tra, chỉnh sửa và xác nhận
→ học viên có tài liệu cá nhân đáng tin để xem lại
→ giảm công sức tìm kiếm, sắp xếp và đọc lại
→ việc ôn tập và tiếp tục học thuận lợi hơn
```

- **Output:** Một bản ghi chú cá nhân có cấu trúc.
- **Thay đổi hành vi cần xảy ra:** Học viên kiểm tra, xác nhận và quay lại sử dụng bản ghi chú.
- **Outcome được kỳ vọng:** Giảm thời gian tìm lại kiến thức, duy trì mạch học và hạn chế bỏ quên những câu hỏi chưa được giải quyết.

Nếu học viên không quay lại sử dụng ghi chú thì output có thể được tạo ra nhưng outcome sẽ không xảy ra.

### 2.4. Actor được chọn

**Học viên** là actor được điều tra trước vì họ trực tiếp tạo các dấu vết, chịu công sức tập hợp và quyết định có sử dụng ghi chú sau bài học hay không.

Các stakeholder gián tiếp gồm coach/instructor và bạn học. Họ có thể hưởng lợi khi học viên mang được câu hỏi rõ ràng, có ngữ cảnh vào buổi hỗ trợ hoặc thảo luận.

### 2.5. Situation & Job

**Situation & Job:** Khi vừa hoàn thành một bài học có nhiều nội dung và còn một số điểm cần nhớ hoặc chưa rõ, học viên đang cố tạo một tài liệu ngắn gọn để có thể ôn lại và tiếp tục học sau này bằng cách tự tìm, sao chép và sắp xếp các highlights, câu hỏi và ghi chú đã tạo trong lúc học.

**JTBD Hypothesis:**

> Khi hoàn thành một bài học và còn những điểm quan trọng hoặc chưa hiểu nằm rải rác, tôi muốn tập hợp chúng thành một tài liệu cá nhân mà tôi có thể tin tưởng, để có thể ôn lại hoặc tiếp tục học mà không phải tìm và đọc lại toàn bộ bài.

Job này vẫn tồn tại nếu bỏ AI và solution directive khỏi bối cảnh.

### 2.6. Hai Pain Hypothesis cạnh tranh

**Pain Hypothesis A — Công sức tập hợp và tìm lại**

> Khi hoàn thành một bài học có nhiều nội dung, học viên gặp khó khăn trong việc tạo tài liệu để xem lại vì highlights, câu hỏi và ghi chú nằm phân tán hoặc thiếu ngữ cảnh. Việc tự tìm và tập hợp chúng tốn công, dẫn đến trì hoãn hoặc bỏ qua việc tổng hợp, phải đọc lại nhiều nội dung và có thể bỏ quên những câu hỏi chưa được giải quyết.

**Pain Hypothesis B — Không có thói quen sử dụng lại ghi chú**

> Khi hoàn thành một bài học, học viên gặp khó khăn trong việc biến ghi chú thành hành động ôn tập vì chưa có thói quen xem lại hoặc không xác định được bước tiếp theo cần làm. Vì vậy, ghi chú có thể được lưu nhưng hiếm khi được sử dụng, bất kể chúng có được tổ chức tốt hay không.

Hai giả thuyết cạnh tranh vì một bản ghi chú được tổ chức tốt có thể giải quyết barrier trong A nhưng không nhất thiết giải quyết barrier trong B.

### 2.7. Problem Hypothesis được chọn

Nhóm chọn **Pain Hypothesis A** để mang sang problem interview trước vì có thể kiểm tra qua những hành vi quá khứ như sao chép nội dung, chụp màn hình, chuyển ghi chú sang ứng dụng khác, mở lại slide hoặc tự viết tóm tắt.

> **Problem Hypothesis:** Khi hoàn thành một bài học có nhiều nội dung và dự định xem lại sau, học viên muốn tập hợp các điểm quan trọng và phần chưa hiểu thành một tài liệu cá nhân. Tuy nhiên, các highlights, câu hỏi và ghi chú nằm phân tán hoặc thiếu ngữ cảnh; việc tự tìm và sắp xếp lại tốn công. Điều này có thể khiến học viên trì hoãn hoặc bỏ qua việc tổng hợp, phải tìm hay đọc lại nhiều nội dung và bỏ quên những câu hỏi chưa được giải quyết.

### 2.8. Evidence cần tìm

| Cần kiểm tra | Evidence làm nhóm tin hơn | Evidence khiến nhóm nghi ngờ hoặc bác bỏ |
|---|---|---|
| Situation có thật | Kể được một bài học cụ thể trong bảy ngày gần đây, đã tạo dấu vết và sau đó cần xem lại | Không nhớ sự kiện gần đây; hiếm khi tạo hoặc cần xem lại ghi chú |
| Pain có ý nghĩa | Việc tập hợp hoặc tìm lại mất thời gian, gây gián đoạn, trì hoãn hoặc bỏ cuộc | Chỉ là bất tiện nhỏ, xử lý nhanh và không ảnh hưởng việc học |
| Workaround tồn tại | Sao chép sang Notion/Docs, chụp màn hình, mở lại slide hoặc tự viết lại | Không cần workaround hoặc công cụ hiện tại đã đủ tốt |
| Consequence tồn tại | Phải đọc lại bài, không tìm được đoạn cần thiết, quên câu hỏi hoặc chậm ôn tập | Vẫn tìm lại dễ dàng và không có hậu quả thực tế |
| Pattern có lặp | Khó khăn xuất hiện ở nhiều bài hoặc nhiều lần gần đây | Chỉ xảy ra một lần trong tình huống đặc biệt |
| A đúng hơn B | Có ý định xem lại nhưng bị cản bởi công sức tập hợp và tìm kiếm | Không xem lại vì thiếu nhu cầu, thói quen hoặc động lực, kể cả khi ghi chú được tổ chức tốt |

**Điều phải đúng để giả thuyết đứng vững:**

1. Học viên thực sự tạo highlights, câu hỏi hoặc ghi chú trong lúc học.
2. Họ có nhu cầu sử dụng lại những dấu vết này sau bài học.
3. Việc tập hợp hoặc tìm lại tốn đủ công sức để trở thành một barrier có ý nghĩa.
4. Barrier tạo ra hậu quả quan sát được, không chỉ là bất tiện nhỏ.
5. Công sức tổ chức là nguyên nhân quan trọng hơn việc thiếu nhu cầu hoặc thói quen ôn tập.

**Điều có thể khiến nhóm sửa hoặc bác bỏ giả thuyết:**

- Học viên hiếm khi có nhu cầu xem lại ghi chú.
- Cách làm hiện tại đã nhanh, dễ và không tạo hậu quả đáng kể.
- Barrier chính là chưa hiểu bài, không biết nội dung nào quan trọng, thiếu động lực hoặc thiếu thói quen ôn tập.
- Một bản ghi chú được tổ chức tốt vẫn không được sử dụng lại.

### 2.9. Solution Parking Lot

| Hướng giải quyết có thể có | Phân loại |
|---|---|
| Tự động nhóm các dấu vết học tập thành ghi chú để học viên kiểm tra và xác nhận | AI |
| Mẫu cuối bài gồm “Điểm chính – Chưa hiểu – Việc tiếp theo” | Không sử dụng AI |
| Notebook thu thập nguyên văn highlights và liên kết về đúng vị trí trong bài | Không sử dụng AI |
| Tạo flashcard hoặc lịch ôn tập từ ghi chú đã được học viên xác nhận | AI |
| Hoạt động cuối bài yêu cầu học viên tự chọn ba ý chính và một câu hỏi | Không sử dụng AI |

Các hướng trên chỉ được park lại. Nhóm chưa chọn solution trước khi thu thập evidence.

---

## 3. Conversation Guide — Phiên bản cuối

### 3.1. Tiêu chí tuyển người

Người đã highlight, viết câu hỏi/ghi chú hoặc lưu lại nội dung học tập để xem sau trong vòng **bảy ngày gần đây**.

**Recruitment check:**

> Trong bảy ngày vừa qua, bạn có lần nào highlight, ghi chú, viết câu hỏi hoặc lưu một nội dung học tập để xem lại sau không?

Câu này chỉ dùng để tuyển đúng người, không tính là evidence chính.

### 3.2. Lời mở đầu

> Cảm ơn bạn đã tham gia. Mình đang tìm hiểu cách mọi người ghi lại và sử dụng lại nội dung trong quá trình học. Mình muốn nghe về những việc bạn thực sự đã làm trong một tình huống gần đây. Không có câu trả lời đúng hoặc sai và mình không đánh giá cách học của bạn. Cuộc trò chuyện kéo dài khoảng 15 phút.

### 3.3. Xin phép ghi âm

> Mình muốn ghi âm cuộc trò chuyện để nghe lại, bóc transcript và hoàn thiện bài học. Bản ghi chỉ phục vụ bài học và không được chia sẻ công khai. Bạn có đồng ý cho mình ghi âm không?

Chỉ bắt đầu ghi khi người tham gia đồng ý.

### 3.4. Story opener

> Kể mình nghe về lần gần nhất trong bảy ngày qua bạn đã highlight, ghi chú, viết câu hỏi hoặc lưu một nội dung học tập để xem lại sau?

### 3.5. Big 3 Questions

| Điều cần học | Câu hỏi sử dụng |
|---|---|
| Quy trình và workaround hiện tại | Từ lúc nhận ra có nội dung muốn lưu cho đến khi kết thúc buổi học, bạn đã làm những gì? |
| Việc sử dụng lại và hậu quả | Sau đó bạn có quay lại dùng nội dung đã lưu không? Nếu có, hãy kể lần đầu bạn quay lại; nếu không, ghi chú đó sau đó ra sao? |
| Câu hỏi có thể làm giả thuyết yếu đi | Trong bảy ngày qua, có lần nào bạn lưu hoặc ghi chú nhưng sau đó không dùng lại, hoặc không tìm được điều cần tìm không? Nếu có, hãy kể lần gần nhất; nếu không, cách hiện tại đã giúp bạn thế nào? |

### 3.6. Probe bank

- Lúc đó chuyện gì xảy ra tiếp theo?
- Bạn đã lưu ở đâu?
- Bạn tìm lại bằng cách nào?
- Bạn mất khoảng bao lâu?
- Vì sao bạn chọn cách đó?
- Bạn có phải sắp xếp hoặc viết lại không?
- Bạn đã thử cách nào khác chưa?
- Có lần nào bạn không làm bước đó không? Chuyện gì xảy ra?
- Việc đó ảnh hưởng thế nào đến việc học của bạn?
- Lần gần nhất trước đó là khi nào?

### 3.7. Quy tắc follow-up

- Nếu user nói chung chung: “Lần gần nhất chuyện đó xảy ra là khi nào?”
- Nếu user đưa ra feature request: “Điều đó giúp bạn hoàn thành việc gì? Trong lần gần nhất bạn đã xử lý ra sao?”
- Nếu user khen hoặc nói “mình sẽ dùng”: cảm ơn ngắn rồi quay lại hành vi quá khứ.
- Không cho interviewee xem solution directive.
- Không hỏi họ có muốn AI hoặc tính năng tự tạo ghi chú hay không.

### 3.8. Chỉnh sửa sau buổi luyện

- **Câu hỏi/cách diễn đạt đã sửa:** Bỏ cách mở đầu có nhắc “AI Notes”; thay bằng: “Kể mình nghe về lần gần nhất trong bảy ngày qua bạn đã highlight, ghi chú, viết câu hỏi hoặc lưu một nội dung học tập để xem lại sau?” Đồng thời thay câu hỏi giả định “Nếu được cải thiện một điều…” bằng các probe về lần đã tìm lại gần nhất, thời gian, số nơi phải mở và hậu quả thực tế.
- **Vấn đề quan sát được trong lúc hỏi:** Các lượt luyện chủ yếu thu được thói quen ghi chú chung, chưa mở được câu chuyện gần đây theo trình tự hành vi. Một lượt nhắc tên solution quá sớm; một lượt chuyển sang feature request. Vì vậy chưa thu được evidence rõ về tần suất, thời gian mất thêm hoặc hậu quả của pain.
- **Lý do sửa guide:** Notes cho thấy P01–P03 đều có workaround ghi chú, nhưng P02 và P03 nói ảnh hưởng hiện tại ít hoặc không đáng kể. Guide mới cần neo vào sự kiện quá khứ và kiểm tra cả giả thuyết cạnh tranh: người học có thực sự quay lại dùng ghi chú hay không, thay vì dẫn họ tới solution hoặc mong muốn tương lai.

---

## 4. Practice Reflection

> Mỗi chủ repo chỉ giữ reflection của chính mình. Không dùng AI để thay cho việc nghe lại cuộc phỏng vấn.

### Reflection của chủ repo

1. **Câu hỏi nào đã giúp user kể một tình huống cụ thể?**  
   Chưa có câu hỏi nào mở được một tình huống cụ thể đủ chi tiết. Các câu trả lời trong bản ghi vẫn ở mức mô tả thói quen chung; đây là tín hiệu cần bắt đầu bằng “lần gần nhất” và follow-up theo trình tự hành vi.

2. **Chỗ nào mình cần làm tốt hơn ở lần phỏng vấn thật?**  
   Cần không nhắc tên “AI Notes” hoặc solution ngay đầu buổi; tránh câu hỏi giả định về tính năng. Khi người tham gia trả lời chung chung, cần hỏi mốc thời gian, bối cảnh, nơi đã lưu, cách tìm lại, thời gian/công sức và hậu quả thay vì chuyển sang câu hỏi tiếp theo.

3. **Sau khi luyện, nhóm đã sửa Conversation Guide ở đâu và vì sao?**  
   Nhóm sửa Story opener thành câu hỏi về “lần gần nhất trong bảy ngày”, thêm probe về trình tự và consequence, đồng thời bỏ câu hỏi “Nếu được cải thiện một điều…”. Lý do là ba lượt luyện chưa xác nhận được pattern hay mức độ nghiêm trọng của pain; P02 và P03 còn cho biết vấn đề ít hoặc không ảnh hưởng đáng kể đến việc học.

### Theo dõi tiến độ ba thành viên

| Thành viên | Interview Record | Recording có consent | Reflection cá nhân |
|---|---|---|---|
| Nguyễn Đặng Thành Vinh | Có — P01 | xác nhận trong file | Chưa có file riêng |
| Đoàn Ngọc Linh | Có — P02 | xác nhận trong file | Chưa có file riêng |
| Hoàng Duy Hưng | Có — P03 | xác nhận trong file | Có — trong README |

---

## 5. AI Support Log

### AI đã hỗ trợ gì?

- Gợi ý cách diễn đạt capability trung tính và chuỗi thay đổi kỳ vọng.
- Giúp tạo hai Pain Hypothesis cạnh tranh và xác định evidence có thể bác bỏ giả thuyết được chọn.
- Rà soát Conversation Guide để các câu hỏi tập trung vào hành vi quá khứ và không làm lộ solution.
- Hỗ trợ cấu trúc và định dạng README.

### Điểm có thể sai hoặc hời hợt

Bản nháp do AI tạo có xu hướng ưu tiên pain về việc tổ chức ghi chú vì đây là pain gần nhất với solution directive. Đây chưa phải evidence rằng người học thực sự gặp pain đó. AI cũng không thể biết điều gì đã xảy ra trong lượt phỏng vấn hoặc viết reflection thay cho người phỏng vấn.

### Nhóm đã kiểm soát và tự sửa thế nào?

- Giữ thêm Pain Hypothesis B về thói quen sử dụng lại ghi chú để tránh khóa vào một cách giải thích.
- Xác định trước evidence có thể làm Hypothesis A yếu đi hoặc bị bác bỏ.
- Không sử dụng nội dung do AI tạo làm interview data, exact quote hoặc evidence.
- Mỗi thành viên tự nghe lại recording, hoàn thiện notes và Practice Reflection của mình.

---

## 6. Cấu trúc repo và checklist nộp bài

```text
Track1_Day17_MHV_HoVaTen/
├── README.md
└── interview/
    ├── notes.md
    └── recording.m4a
```

Nếu bản ghi được lưu trên Drive hoặc nền tảng gọi trực tuyến, thay file recording bằng:

```text
interview/recording-link.md
```

### Checklist

- [X] Repo đúng tên `Track1_Day17_MHV_HoVaTen`
- [x] Đã điền MHV, họ tên, tên nhóm và ba thành viên.
- [x] `README.md` có đủ năm phần bắt buộc.
- [x] `interview/notes.md` lưu notes tổng hợp các lượt phỏng vấn của nhóm.
- [x] Có ba file recording trong `interview/recording/`.
- [ ] Người được phỏng vấn đã đồng ý cho ghi lại (cần xác nhận vì consent không nghe rõ trong file).
- [x] Conversation Guide phiên bản cuối không làm lộ solution.
- [x] Guide đã được sửa dựa trên trải nghiệm luyện thật.
- [x] Practice Reflection của chủ repo đã hoàn thành trong README.
