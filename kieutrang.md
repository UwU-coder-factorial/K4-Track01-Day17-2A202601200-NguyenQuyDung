# Nháp cá nhân Chặng 1 — Kiều Trang

> **Case đã chọn:** Case A — AI Tutor: Diagnostic Refresher  
> **Trạng thái:** Đây là các giả thuyết ban đầu để đưa ra thảo luận nhóm, chưa phải fact về user và chưa được validated. 

## 1. Solution — Gỡ solution khỏi hình thức cụ thể

### Solution directive

Thêm nút “Tôi vẫn chưa hiểu” vào bài học. Khi học viên bấm nút, AI Tutor sử dụng nội dung bài hiện tại, các câu trả lời gần đây và lịch sử học tập để đặt 2–3 câu hỏi chẩn đoán ngắn, chọn một khái niệm nền cần ôn, tạo phần giải thích ngắn rồi đưa học viên trở lại bài đang học.

### Capability trung tính

Giúp học viên đang bị mắc kẹt trong một bài học xác định phần kiến thức còn thiếu, ôn lại đúng nội dung cần thiết và lấy lại đủ hiểu biết để tiếp tục bài đang học.

Capability này không bắt buộc phải được triển khai bằng một nút bấm, AI Tutor hay một giao diện cụ thể.

## 2. Change — Chuỗi thay đổi được kỳ vọng

```text
Học viên gặp chỗ chưa hiểu
→ nhận ra mình cần trợ giúp và chủ động yêu cầu
→ trả lời một số câu hỏi làm rõ
→ xác định được lỗ hổng kiến thức cụ thể
→ ôn lại nội dung nền phù hợp
→ áp dụng lại vào phần đang học
→ tiếp tục bài với mức độ hiểu tốt hơn
```

### Các thay đổi được kỳ vọng

- Học viên chuyển từ việc chỉ biết “mình không hiểu” sang nhận biết rõ phần kiến thức nào đang cản trở mình.
- Học viên thay việc tìm kiếm hoặc ôn lại lan man bằng một hoạt động ôn tập tập trung hơn.
- Sau khi ôn, học viên quay lại bài hiện tại và thử tiếp tục thay vì bỏ qua, đoán đáp án hoặc dừng học.
- **Output của solution:** câu hỏi chẩn đoán, khái niệm nền được chọn và phần giải thích ngắn.
- **Outcome solution chỉ có thể ảnh hưởng:** học viên hiểu bài hơn, ít mất thời gian hơn và có khả năng hoàn thành bài. Outcome này còn phụ thuộc vào chất lượng nội dung, động lực, thời gian và cách học của học viên.

Nếu học viên không chủ động yêu cầu trợ giúp, không trả lời câu hỏi hoặc không áp dụng phần ôn lại vào bài đang học thì outcome kỳ vọng khó xảy ra.

## 3. Actor — Các nhóm người có liên quan

| Actor | Họ đang làm gì? | Pain hoặc hậu quả có thể có | Họ hưởng lợi thế nào? |
| --- | --- | --- | --- |
| Học viên | Cố hiểu và hoàn thành bài học hiện tại | Không biết mình thiếu kiến thức nào; đọc lại hoặc tìm kiếm lan man; mất thời gian, nản hoặc bỏ qua phần chưa hiểu | Xác định được điểm vướng, ôn đúng phần cần thiết và tiếp tục học |
| Giảng viên/coach | Giải thích và hỗ trợ học viên khi họ gặp khó khăn | Không có đủ thời gian để hỗ trợ ngay từng trường hợp; phải giải thích lại các kiến thức nền | Giảm các yêu cầu hỗ trợ lặp lại và tập trung vào trường hợp cần con người can thiệp |
| Người thiết kế nội dung | Xây dựng bài học và chuỗi kiến thức | Khó dự đoán mọi lỗ hổng kiến thức nền hoặc mọi cách hiểu sai của học viên | Nhận biết các điểm học viên thường bị mắc để cải thiện nội dung |

**Actor đề xuất điều tra trước:** Học viên đã có lúc không hiểu một phần bài học trong vòng 7 ngày gần đây và đã phải tìm cách xử lý.

**Lý do chọn:** Học viên là người trực tiếp trải nghiệm tình huống, thực hiện workaround và chịu hậu quả nếu không giải quyết được. Giảng viên và người thiết kế nội dung là các actor liên quan nhưng không sở hữu pain chính trong giả thuyết của Case A.

## 4. Situation & Job — User đang cố làm gì trong tình huống nào?

```text
Học viên đang học một bài và gặp đoạn giải thích hoặc bài tập không hiểu
→ muốn hiểu đủ để hoàn thành phần hiện tại
→ đọc lại, xem lại bài trước, tìm trên Internet hoặc hỏi người khác
→ bị mắc khi không biết chính xác mình đang thiếu kiến thức nào
```

### Mô tả Situation & Job

Khi đang học một bài và gặp một đoạn giải thích hoặc bài tập không thể hiểu bằng kiến thức hiện có, học viên đang cố hiểu đủ nội dung để tiếp tục bài bằng cách đọc lại, xem ví dụ, tìm kiếm nguồn khác, quay lại bài trước hoặc hỏi người khác.

### JTBD Hypothesis

> Khi gặp một phần chưa hiểu trong lúc học, tôi muốn xác định mình đang vướng ở đâu và bổ sung đúng kiến thức cần thiết, để có thể tiếp tục bài hiện tại mà không mất quá nhiều thời gian hoặc học tiếp trong trạng thái mơ hồ.

## 5. Pain — Hai cách giải thích cạnh tranh

### Pain Hypothesis A — Thiếu kiến thức nền nhưng không xác định được

> Khi gặp một phần chưa hiểu trong bài học, học viên gặp khó khăn trong việc tiếp tục học vì không xác định được khái niệm nền nào mình đang thiếu hoặc hiểu sai. Vì vậy, họ có thể đọc lại cùng một nội dung, tìm kiếm quá rộng hoặc thử nhiều nguồn không phù hợp, dẫn đến mất thời gian, gián đoạn nhịp học và có thể bỏ qua phần chưa hiểu hoặc dừng bài.

### Pain Hypothesis B — Cách trình bày hiện tại không phù hợp

> Khi gặp một phần chưa hiểu trong bài học, học viên gặp khó khăn trong việc tiếp tục học không phải chủ yếu vì thiếu kiến thức nền, mà vì phần hiện tại được giải thích quá trừu tượng, quá nhanh hoặc thiếu ví dụ phù hợp. Vì vậy, việc ôn lại kiến thức nền có thể không giúp ích; học viên cần một cách giải thích, ví dụ hoặc cơ hội thực hành khác.

### Giả thuyết đề xuất điều tra trước

**Chọn Hypothesis A để điều tra trước.** Đây là giả định quan trọng nhất đang nằm phía sau solution directive: hệ thống chỉ có giá trị theo cách đã mô tả nếu một tỷ lệ đáng kể tình huống “chưa hiểu” thực sự xuất phát từ lỗ hổng kiến thức nền có thể xác định được.

Hypothesis B được giữ lại như cách giải thích cạnh tranh và là “câu hỏi đáng sợ”. Nếu phần lớn học viên hiểu kiến thức nền nhưng chỉ cần cách giải thích khác cho nội dung hiện tại, nhóm phải sửa giả thuyết và xem lại hướng solution.

## 6. Evidence — Điều cần tìm trong phỏng vấn

| Cần kiểm tra | Evidence làm tôi tin hơn | Evidence làm tôi nghi ngờ hoặc bác bỏ |
| --- | --- | --- |
| Situation có thật | Học viên kể được một lần cụ thể trong 7 ngày gần đây, gồm bài đang học, điểm bắt đầu bị vướng và diễn biến tiếp theo | Không nhớ được tình huống gần đây hoặc chỉ nói chung chung rằng đôi khi không hiểu |
| Pain có ý nghĩa | Học viên bị mắc đủ lâu để gián đoạn việc học, cảm thấy khó chịu hoặc phải thay đổi kế hoạch học | Học viên tự xử lý rất nhanh bằng cách đọc lại và xem đó là bất tiện nhỏ |
| Workaround tồn tại | Học viên đã đọc lại nhiều lần, quay lại bài cũ, tìm Google/YouTube/ChatGPT, hỏi bạn hoặc hỏi giảng viên | Học viên không cần làm gì thêm hoặc không chủ động tìm cách xử lý |
| Consequence tồn tại | Học viên mất thời gian đáng kể, trả lời sai, bỏ qua nội dung, dừng bài hoặc tiếp tục mà không hiểu | Tình huống không ảnh hưởng đến việc tiếp tục hoặc kết quả học |
| Pattern có lặp | Học viên kể được những lần tương tự và nhận thấy một kiểu vướng lặp lại | Đây là sự cố hiếm, mỗi lần do một nguyên nhân khác nhau và không tạo thành pattern |
| Nguyên nhân là kiến thức nền | Sau khi tìm hoặc được nhắc lại một khái niệm trước đó, học viên hiểu và tiếp tục được phần hiện tại | Học viên đã hiểu kiến thức nền; vấn đề chỉ được giải quyết khi có cách giải thích hoặc ví dụ khác |

### Những điều cần quan sát trong câu chuyện thực tế

- Học viên có tự nhận biết chính xác phần kiến thức mình thiếu không?
- Họ đã làm gì ngay sau khi nhận ra mình không hiểu?
- Họ đã thử bao nhiêu cách hoặc nguồn trước khi tiếp tục được?
- Workaround có thực sự giúp họ tìm ra lỗ hổng kiến thức không?
- Hậu quả có đủ lớn để họ muốn xử lý ngay hay họ có thể dễ dàng sống chung với nó?
- Khi vấn đề được giải quyết, yếu tố giúp ích là ôn kiến thức nền hay chỉ là một cách giải thích khác?

## 7. Chốt Problem Hypothesis và park solution

### Problem Hypothesis mang sang Chặng 2

> Khi đang học và gặp một phần không hiểu, một số học viên gặp khó khăn trong việc tiếp tục bài vì không xác định được kiến thức nền nào mình đang thiếu hoặc hiểu sai. Họ phải tự đọc lại, tìm kiếm nhiều nguồn hoặc hỏi người khác; điều này có thể làm mất thời gian, gián đoạn nhịp học và khiến họ bỏ qua phần chưa hiểu hoặc dừng bài.

Đây vẫn là giả thuyết cần kiểm chứng, không phải kết luận rằng pain đã được validated.

### Điều phải đúng để giả thuyết đứng vững

- Tình huống không hiểu bài xảy ra đủ gần đây và đủ thường xuyên để học viên nhớ được câu chuyện cụ thể.
- Khó khăn đáng kể nằm ở việc không biết mình thiếu kiến thức nền nào, không chỉ ở cách trình bày của bài hiện tại.
- Học viên đã bỏ công sức tìm cách xử lý và workaround hiện tại có chi phí hoặc hiệu quả chưa tốt.
- Việc không xử lý được tạo ra hậu quả quan sát được đối với thời gian, tiến độ hoặc mức độ hiểu bài.
- Khi kiến thức nền phù hợp được bổ sung, học viên có thể quay lại và tiếp tục phần hiện tại.

### Điều có thể khiến tôi sửa hoặc bác bỏ giả thuyết

- Học viên hiếm khi gặp tình huống này hoặc thường giải quyết rất nhanh bằng cách đọc lại.
- Họ đã biết chính xác mình vướng ở đâu và workaround hiện tại đủ nhanh, đủ tốt.
- Khó khăn chủ yếu đến từ cách giải thích, ví dụ hoặc giao diện của bài hiện tại chứ không phải kiến thức nền.
- Việc không hiểu không tạo hậu quả đáng kể; học viên vẫn hoàn thành mục tiêu mà không cần xử lý.
- Học viên không muốn dừng dòng học để chẩn đoán hoặc ôn lại vì chi phí chuyển ngữ cảnh lớn hơn lợi ích.

### Solution Parking Lot

| Hướng giải quyết có thể có | AI / Không sử dụng AI |
| --- | --- |
| 1. Hỏi một số câu ngắn để xác định lỗ hổng kiến thức và tạo phần ôn tập phù hợp | AI |
| 2. Cung cấp bản đồ kiến thức nền và liên kết thủ công từ bài hiện tại về các bài liên quan | Không sử dụng AI |
| 3. Bổ sung nhiều cách giải thích, ví dụ trực quan và bài tập mẫu cho các điểm thường gây nhầm lẫn | Không sử dụng AI |
| 4. Cho phép học viên gửi câu hỏi nhanh đến bạn học, mentor hoặc giảng viên | Không sử dụng AI |
| 5. Dùng kết quả các bài kiểm tra ngắn để đề xuất lộ trình ôn tập cá nhân | AI |
| 6. Tạo checklist tự chẩn đoán để học viên tự xác định mình đang thiếu khái niệm nào | Không sử dụng AI |

## 8. Các điểm mang sang thảo luận nhóm

- Nhóm cần thống nhất “tiếp tục được bài” có nghĩa là gì và evidence nào có thể quan sát được trong interview.
- Cần tránh mặc định mọi lần không hiểu đều do thiếu kiến thức nền.
- Cần hỏi sâu về lần gần nhất học viên xử lý thành công và không thành công để so sánh nguyên nhân.
- Câu hỏi quan trọng nhất cần mang sang Chặng 2: **Trong lần gần nhất, điều thực sự giúp học viên hiểu tiếp là ôn lại kiến thức nền hay một cách giải thích khác cho nội dung hiện tại?**
