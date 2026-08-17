# Khai phá Problem & Solution Template

## 1. Solution — Gỡ solution khỏi hình thức cụ thể

**Case đã chọn:** Case A — AI Tutor: Diagnostic Refresher

Thêm nút “Tôi vẫn chưa hiểu” vào bài học.

Khi học viên bấm nút, AI Tutor sử dụng nội dung bài hiện tại, các câu trả lời gần đây và lịch sử học tập để:

Đặt 2–3 câu hỏi chẩn đoán ngắn.
* Chọn một khái niệm nền để học viên ôn lại.
* Tạo một phần giải thích ngắn.
* Đưa học viên trở về bài đang học.

### Câu hỏi dẫn dắt:

- Câu nào trong directive đang mô tả giao diện, tên feature hoặc công nghệ?
    - Thêm nút “Tôi vẫn chưa hiểu” vào bài học
- Nhóm có đang mặc định cách triển khai được giao là cách duy nhất không?
    - Không
- Capability có thể được mô tả mà không dùng tên feature không?
    - Không

**Solution directive:**

> Thêm nút “Tôi vẫn chưa hiểu” vào bài học.

**Capability trung tính:**

> Khả năng tiếp nhận tín hiệu gặp khó khăn của học viên ngay trong bài học, tự động chẩn đoán lỗ hổng kiến thức nền tảng và cung cấp nội dung ôn tập phù hợp trước khi tiếp tục.

---

## 2. Change — Làm lộ chuỗi thay đổi được kỳ vọng

Đừng nhảy thẳng từ feature tới outcome. Viết các mắt xích mà team đang ngầm tin sẽ xảy ra.

### Câu hỏi dẫn dắt:

- User sẽ biết hoặc làm được điều gì khác?
    - Thay vì phải tự hỏi, hệ thống sẽ tự động đưa ra câu hỏi và giải thích.
- Hành vi nào phải thay đổi để outcome xảy ra?
    - Người dùng phải chủ động bấm nút “Tôi vẫn chưa hiểu”
- Trạng thái hoặc kết quả nào được kỳ vọng thay đổi?
    - Người dùng bắt đầu thực sự hỏi tutor nhiều hơn
- Đâu là output team tạo ra, đâu là outcome team chỉ có thể ảnh hưởng?
    - Output team tạo ra: Câu trả lời hợp lý, ngắn gọn, chuẩn xác
    - Outcome team chỉ có thể ảnh hưởng: Học viên thực sự hiểu bài, tự tin hơn, chủ động hỏi tutor hơn
- Nếu user không thay đổi hành vi, solution còn tạo được outcome không?
    - Không

```text
Solution → 
    Thêm nút “Tôi vẫn chưa hiểu” vào bài học 
→ 
    Người dùng phải chủ động bấm nút “Tôi vẫn chưa hiểu”
→ 
    Học viên thực sự hiểu bài, tự tin hơn, chủ động hỏi tutor hơn
```

**Các thay đổi được kỳ vọng:**

- Tần suất sử dụng chế độ AI tăng
- Tăng user retention: người học ở lại trên nền tảng, không chỉ trong giờ học
- Phản hồi tốt từ user

---

## 3. Actor — Xác định các nhóm người có liên quan

Một solution có thể liên quan đến nhiều nhóm user hoặc stakeholder khác nhau. Người trực tiếp sử dụng feature chưa chắc là người đang gặp pain chính, phải thay đổi hành vi hoặc chịu hậu quả.

*Ví dụ với AI Support Radar trên VLearn:* learner là người có hành vi học tập được phân tích; instructor là người xem Support Queue và quyết định can thiệp; coach là người có thể trực tiếp hỗ trợ learner. Cả ba đều là actor liên quan nhưng có job, pain và lợi ích khác nhau.

### Câu hỏi dẫn dắt:

- Ai trực tiếp sử dụng solution?
    - Người học trong giờ không hiểu bài
    - người tự học trước ở nhà
    - Người học đang ôn lại bài
- Ai trực tiếp trải nghiệm pain?
    - Nhóm người sử dụng solution nhưng không hiểu
- Ai phải thay đổi hành vi để outcome xảy ra?
    - Nhóm người solution nhắm tới
- Ai chịu hậu quả nếu problem không được giải quyết?
    - Người học: không hoàn thành khóa học
- Ai hưởng lợi gián tiếp?
    - VinUni, với chất lượng học viên AI thực chiến tăng
- Người nhận feature có chắc là người sở hữu pain chính không?
    - Có?

| Actor | Họ đang làm gì? | Pain hoặc hậu quả có thể có | Họ hưởng lợi thế nào? |
| ----- | ------------------- | --------------------------------- | --------------------------- |
| Người học  | Người học trong giờ không hiểu bài. Người tự học trước ở nhà. Người học đang ôn lại bài | Không hiểu bài dẫn đến việc bỏ dở bài học. Không hoàn thành khóa học. Không tự tin khi giao tiếp với AI thực chiến sau này | Tăng trải nghiệm học tập. Tăng sự tự tin. Hoàn thành khóa học. Tăng khả năng giao tiếp với AI thực chiến sau này |
| Giảng viên | Đứng lớp và thấy người học không hiểu bài. Không thể trả lời hết câu hỏi của học viên. Không có thời gian để hỗ trợ từng học viên một | Người học không hiểu bài dẫn đến việc bỏ dở bài học. Không hoàn thành khóa học. Không tự tin khi giao tiếp với AI thực chiến sau này | Tăng trải nghiệm học tập. Tăng sự tự tin. Hoàn thành khóa học. Tăng khả năng giao tiếp với AI thực chiến sau này |
| VinUni | Người học không hiểu bài dẫn đến việc bỏ dở bài học. Không hoàn thành khóa học. Không tự tin khi giao tiếp với AI thực chiến sau này | Tăng trải nghiệm học tập. Tăng sự tự tin. Hoàn thành khóa học. Tăng khả năng giao tiếp với AI thực chiến sau này | Tăng trải nghiệm học tập. Tăng sự tự tin. Hoàn thành khóa học. Tăng khả năng giao tiếp với AI thực chiến sau này |

- **Actor nhóm chọn để điều tra trước:** Người học
- **Vì sao chọn nhánh này thay vì actor khác:** 
    - Vì họ là người sử dụng solution trực tiếp và là người trải nghiệm pain chính
- **Vì sao chọn nhánh này thay vì actor khác:** 
    - Vì khó khăn này thực tế

---

## 4. Situation & Job — User đang cố làm gì trong tình huống nào?

Chọn một khoảnh khắc cụ thể mà actor có thể đã trải qua. Mô tả hoàn cảnh và việc họ đang cố hoàn thành, chưa kết luận pain nằm ở đâu. Job phải còn tồn tại ngay cả khi bỏ AI và feature khỏi bối cảnh.

### Câu hỏi dẫn dắt:

- Tình huống bắt đầu khi chuyện gì xảy ra?
    - Đang ngồi trong lớp, xử lý công việc 1 tẹo, quay mặt lên đã không hiểu.
- Lúc đó user đang cố hoàn thành việc gì?
    - Bắt kịp với lớp
- Vì sao việc đó quan trọng với họ?
    - Quan trọng vì phải hoàn thành bài học.
- Hiện tại họ đang thực hiện việc đó như thế nào?
    - Họ quyết định để sau là làm việc tiếp.
- Họ bắt đầu gặp vướng mắc ở điểm nào?
    - không match kịp tiến độ với lớp.

```text
Đang ngồi trong lớp bị phân tâm/xử lý việc riêng một chút
→ Muốn bắt kịp lại tiến độ bài giảng cùng với lớp
→ Quyết định "để sau tính" và tiếp tục xử lý công việc riêng
→ Không match kịp kiến thức mới, bị tụt lại so với lớp
```

**Mô tả Situation & Job:**

> Khi [tình huống/trigger], [actor] đang cố [việc cần hoàn thành] bằng cách [cách họ đang làm hiện tại].
>
> Khi đang ngồi trong lớp và lỡ mất tập trung một đoạn ngắn do xử lý việc riêng, người học đang cố bắt kịp lại tiến độ bài giảng cùng với lớp bằng cách tạm thời chặc lưỡi "để sau tính" và tiếp tục làm việc riêng, dẫn đến việc ngắt nhịp kiến thức và không theo kịp các phần tiếp theo.

**JTBD Hypothesis:**

> Khi [situation], tôi muốn [progress], để có thể [desired outcome].
>
> Khi bị lỡ mất nhịp bài giảng trên lớp do xao nhãng tạm thời, tôi muốn nhanh chóng chẩn đoán và lấy lại kiến thức nền vừa bị trôi qua mà không làm gián đoạn lớp học, để có thể lập tức bắt kịp tiến độ bài giảng cùng cả lớp và tự tin hoàn thành buổi học.

---

## 5. Pain — Viết các cách giải thích cạnh tranh

Pain là barrier cản actor hoàn thành job và consequence đi kèm; không phải sự vắng mặt của feature.

### Câu hỏi dẫn dắt:

- Barrier cụ thể nào đang cản actor hoàn thành job?
- Actor thiếu thông tin, kỹ năng, thời gian hay sự hỗ trợ?
- Họ có nhận ra mình đang gặp pain không?
- Nếu không xử lý, hậu quả thực tế là gì?
- Actor có thể sống chung với sự bất tiện này không?
- Có cách giải thích nào khác cho cùng hành vi?
- Pain có còn tồn tại nếu solution directive biến mất khỏi đầu nhóm không?

**Pain Hypothesis A (Rào cản về chẩn đoán kiến thức):**

> Khi lỡ nhịp bài giảng trên lớp, người học gặp khó khăn trong việc bắt kịp tiến độ vì họ không biết chính xác mình đang bị hổng khái niệm nền nào để tự tra cứu hay đặt câu hỏi, dẫn đến việc bị ngắt nhịp kiến thức và tích tụ lỗ hổng ở các bài tiếp theo.

**Pain Hypothesis B — cách giải thích cạnh tranh (Rào cản về tâm lý & môi trường):**

> Khi lỡ nhịp bài giảng trên lớp, người học gặp khó khăn trong việc bắt kịp tiến độ vì ngại làm gián đoạn lớp học và ngại hỏi giảng viên trước mặt bạn bè, dẫn đến việc lựa chọn im lặng, chặc lưỡi "để sau tính" và bỏ dở bài học.

- **Giả thuyết nhóm chọn để điều tra trước:** A
- **Lý do chọn:** Ngay cả khi không ngại hỏi, trong thời gian ngắn trên lớp người học cũng khó tự định hình được mình đang thiếu kiến thức nền nào để tra cứu hay nhờ giảng viên hỗ trợ nhanh.

---

## 6. Evidence — Xác định điều cần tìm trước khi viết câu hỏi

Evidence phải đến từ sự kiện, hành vi, workaround và hậu quả đã xảy ra; một problem statement nghe hợp lý chưa phải evidence.

### Câu hỏi dẫn dắt:

- User có kể được một sự kiện gần đây với trình tự cụ thể không?
- Trong sự kiện đó, họ thực sự đã làm gì?
- Họ đã dùng workaround nào và bỏ ra bao nhiêu công sức?
- Tình huống có lặp lại không?
- Hậu quả quan sát được là gì?
- Họ đã chủ động tìm cách xử lý chưa?
- Điều gì cho thấy pain không đủ quan trọng?
- Evidence nào sẽ khiến nhóm sửa hoặc bác bỏ hypothesis?

| Cần kiểm tra | Evidence làm nhóm tin hơn | Evidence làm nhóm nghi ngờ hoặc bác bỏ |
| --- | --- | --- |
| **Situation có thật** | Người học kể lại được sự kiện cụ thể trong 1–2 tuần qua khi họ bị phân tâm trên lớp và tụt lại so với tiến độ. | Người học khẳng định luôn tập trung 100% hoặc lớp học có nhịp độ rất chậm nên không bao giờ bị lỡ bài. |
| **Pain có ý nghĩa** | Người học cảm thấy hoang mang, mất phương hướng khi giảng viên chuyển sang phần mới và ảnh hưởng đến kết quả bài làm. | Người học xem việc lỡ nhịp là bình thường, không ảnh hưởng tới khả năng tiếp thu các phần sau. |
| **Workaround tồn tại** | Đã từng cố chụp ảnh slide, xem lại ghi chú hoặc hỏi bạn bên cạnh nhưng vẫn không hiểu khái niệm gốc. | Không thực hiện bất kỳ hành động bù đắp nào, chấp nhận bỏ qua hoàn toàn. |
| **Consequence tồn tại** | Tỷ lệ hoàn thành bài tập giảm, bỏ dở bài học hoặc bị điểm kém ở các bài kiểm tra liên quan. | Người học vẫn đạt kết quả tốt và hiểu bài đầy đủ mà không cần xem lại. |
| **Pattern có lặp** | Tình huống này xảy ra thường xuyên (2–3 lần/tuần) ở các môn học hoặc bài học có hàm lượng kiến thức cao. | Tình huống chỉ xảy ra 1 lần duy nhất do sự cố cá nhân hi hữu. |

---

## Chốt Problem Hypothesis và park solution

**Problem Hypothesis nhóm mang sang Chặng 2:**

> Khi bị lỡ mất nhịp bài giảng trên lớp do mất tập trung tạm thời, người học không thể tự chẩn đoán được mình đang hổng khái niệm nền nào để tự bù đắp nhanh, dẫn đến bị mất đà học tập và tích tụ lỗ hổng kiến thức qua các bài tiếp theo.

**Điều gì phải đúng để giả thuyết đứng vững:**

> Người học thực sự có mong muốn bù đắp kiến thức ngay tại thời điểm đó nhưng rào cản lớn nhất là họ không biết chính xác điểm hổng kiến thức nền nằm ở đâu.

**Điều gì có thể khiến nhóm sửa hoặc bác bỏ giả thuyết:**

> Rào cản chính của người học thực ra là yếu tố tâm lý (ngại hỏi) chứ không phải do thiếu khả năng chẩn đoán kiến thức, hoặc họ không thực sự bận tâm đến việc phải bắt kịp bài giảng ngay trên lớp.

### Solution Parking Lot

*Brainstorm ít nhất năm hướng, trong đó có ít nhất một hướng không sử dụng AI.*

| Hướng giải quyết có thể có | AI / Không sử dụng AI |
| --- | --- |
| 1. **AI Diagnostic Refresher (Case A):** Đặt 2–3 câu hỏi chẩn đoán ngắn để phát hiện lỗ hổng và gợi ý kiến thức nền ôn lại. | AI |
| 2. **Real-time Lesson Summarizer:** AI tự động tóm tắt 3 ý cốt lõi của 10 phút bài giảng vừa qua theo dạng bullet points. | AI |
| 3. **Glossary & Concept Flashcards:** Cung cấp bộ thẻ từ khóa/khái niệm cốt lõi hiển thị cố định bên cạnh bài học để học viên tra cứu nhanh. | Không sử dụng AI |
| 4. **Peer/TA Q&A Flag:** Nút ẩn danh "Cần hỗ trợ đoạn này" gửi thông báo để Trợ giảng/Giảng viên tóm tắt lại vào giờ giải lao. | Không sử dụng AI |
| 5. **Smart Replay Bookmark:** Tự động lưu mốc thời gian bài giảng mà học viên bị ngắt quãng để gợi ý danh sách xem lại sau buổi học. | AI |
