# Track 1 — Day 17: Finding and Validating Pain Points

> Bài làm chung của **Nguyễn Quý Dũng** và **Trần Thị Kiều Trang**. Sau khi hoàn thiện, mỗi thành viên fork/đổi tên repo để nộp. Các nội dung ở Chặng 1 là giả thuyết; hai cuộc phỏng vấn trong buổi lab là dữ liệu luyện tập, chưa đủ để tuyên bố pain đã được validated.

## 1. Thông tin cá nhân và nhóm

| Thành viên | MHV |
| --- | --- |
| Nguyễn Quý Dũng | 2A202601200 |
| Trần Thị Kiều Trang | 2A202601498 |

- **Nhóm:** Quý Dũng – Kiều Trang
- **Case đã chọn:** Case A — AI Tutor: Diagnostic Refresher

## 2. Problem Hypothesis Brief

### 2.1. Solution directive

Thêm nút “Tôi vẫn chưa hiểu” vào bài học. Khi học viên bấm nút, AI Tutor sử dụng bài hiện tại, các câu trả lời gần đây và lịch sử học tập để đặt 2–3 câu hỏi chẩn đoán, chọn một khái niệm nền cần ôn, tạo phần giải thích ngắn rồi đưa học viên trở lại bài đang học.

### 2.2. Capability trung tính

Giúp học viên đang mắc kẹt xác định điểm kiến thức cần bổ sung, nhận hỗ trợ phù hợp và lấy lại đủ hiểu biết để tiếp tục phần đang học.

Capability này không mặc định phải được triển khai bằng một nút bấm, AI Tutor hoặc một giao diện cụ thể.

### 2.3. Chuỗi thay đổi được kỳ vọng

```text
Học viên gặp chỗ chưa hiểu
→ nhận ra mình cần trợ giúp và chủ động yêu cầu
→ làm rõ nguyên nhân gây vướng
→ nhận hỗ trợ tập trung vào nguyên nhân đó
→ thử áp dụng lại vào phần hiện tại
→ tiếp tục bài với mức độ hiểu tốt hơn
```

- **Output team có thể tạo:** câu hỏi làm rõ, nội dung hỗ trợ và đường quay lại bài hiện tại.
- **Hành vi phải thay đổi:** học viên chủ động dừng lại, yêu cầu hỗ trợ và thử áp dụng nội dung được cung cấp.
- **Outcome team chỉ có thể ảnh hưởng:** mức độ hiểu, thời gian xử lý chỗ vướng và khả năng tiếp tục/hoàn thành bài. Outcome còn phụ thuộc vào chất lượng bài học, động lực, thời gian và bối cảnh của học viên.

### 2.4. Actor

| Actor | Họ đang làm gì? | Pain hoặc hậu quả có thể có | Họ hưởng lợi thế nào? |
| --- | --- | --- | --- |
| Học viên | Cố hiểu và hoàn thành phần đang học | Không xác định được điểm vướng; tìm kiếm lan man; mất nhịp, bỏ qua hoặc dừng bài | Nhận ra điểm vướng và tiếp tục học với ít gián đoạn hơn |
| Giảng viên/coach | Hỗ trợ nhiều học viên trong thời gian giới hạn | Không thể phản hồi ngay từng trường hợp; phải giải thích lặp lại | Tập trung thời gian vào những ca cần con người hỗ trợ |
| Người thiết kế nội dung | Xây dựng bài và chuỗi kiến thức | Khó dự đoán mọi chỗ học viên có thể hiểu sai hoặc bị thiếu nền | Nhận diện điểm gây vướng để cải thiện nội dung |

**Actor điều tra trước:** học viên đã có lúc không hiểu một phần bài học gần đây và đã phải tìm cách xử lý.

**Lý do:** học viên trực tiếp trải nghiệm tình huống, thực hiện workaround và chịu hậu quả. Các actor còn lại liên quan nhưng không sở hữu pain chính trong giả thuyết Case A.

### 2.5. Situation & Job

**Situation & Job:** Khi gặp một đoạn giải thích hoặc bài tập chưa hiểu trong lúc học, học viên đang cố tìm ra điều khiến mình bị mắc và bổ sung đủ hiểu biết để tiếp tục bài bằng cách đọc lại, xem nội dung trước đó, tìm nguồn khác hoặc hỏi người khác.

**JTBD Hypothesis:**

> Khi gặp một phần chưa hiểu trong lúc học, tôi muốn xác định mình đang vướng ở đâu và lấy lại đủ kiến thức cần thiết, để có thể tiếp tục bài hiện tại mà không mất quá nhiều thời gian hoặc học tiếp trong trạng thái mơ hồ.

### 2.6. Hai Pain Hypothesis cạnh tranh

**Hypothesis A — không xác định được lỗ hổng kiến thức nền**

> Khi gặp một phần chưa hiểu trong bài học, học viên gặp khó khăn trong việc tiếp tục vì không xác định được khái niệm nền nào mình đang thiếu hoặc hiểu sai. Họ phải đọc lại, tìm nhiều nguồn hoặc hỏi người khác, dẫn đến mất thời gian, gián đoạn nhịp học và có thể bỏ qua phần chưa hiểu hoặc dừng bài.

**Hypothesis B — nguyên nhân chính không nằm ở kiến thức nền**

> Khi gặp một phần chưa hiểu, học viên gặp khó khăn chủ yếu vì đã bỏ lỡ lời giải thích, cách trình bày hiện tại chưa phù hợp, thiếu ví dụ hoặc ngại hỏi trong bối cảnh lớp học. Khi đó, ôn kiến thức nền không xử lý đúng rào cản; học viên cần khôi phục phần giải thích đã bỏ lỡ, một ví dụ/cách giải thích khác hoặc một kênh hỏi thuận tiện hơn.

**Giả thuyết chọn điều tra trước:** Hypothesis A.

**Lý do chọn:** đây là giả định quan trọng nhất nằm sau solution directive. Cơ chế chẩn đoán kiến thức nền chỉ có ý nghĩa nếu một phần đáng kể những lần “chưa hiểu” thực sự liên quan đến lỗ hổng mà học viên chưa tự xác định được. Hypothesis B được giữ lại để buộc nhóm tìm evidence có thể làm A yếu đi.

### 2.7. Evidence Map

| Cần kiểm tra | Evidence làm nhóm tin hơn | Evidence làm nhóm nghi ngờ hoặc bác bỏ |
| --- | --- | --- |
| Situation có thật | Kể được lần gần nhất gồm bối cảnh, mục tiêu, điểm bắt đầu vướng và diễn biến | Không nhớ được sự kiện gần đây; chỉ nói chung chung |
| Pain có ý nghĩa | Bị gián đoạn, mất thời gian, thay đổi kế hoạch hoặc không thể tiếp tục | Đọc lại một lần là hiểu; chỉ là bất tiện nhỏ |
| Workaround tồn tại | Đã đọc lại, quay về bài trước, tìm nguồn/AI hoặc hỏi người khác | Không cần thực hiện hành động nào để xử lý |
| Consequence tồn tại | Bỏ lỡ phần sau, trả lời sai, bỏ qua, dừng bài hoặc chậm tiến độ | Không ảnh hưởng đến tiến độ, mức độ hiểu hoặc kết quả |
| Pattern có lặp | Kể được thêm những lần tương tự và một kiểu vướng lặp lại | Chỉ xảy ra một lần do sự cố cá biệt |
| Nguyên nhân là kiến thức nền | Xác định và bổ sung đúng khái niệm nền giúp học viên hiểu tiếp | Chỉ cần nghe lại phần đã bỏ lỡ, một ví dụ hoặc cách giải thích khác |

### 2.8. Problem Hypothesis mang sang Chặng 2

> Khi đang học và gặp một đoạn giải thích hoặc bài tập chưa hiểu, một số học viên gặp khó khăn trong việc tiếp tục vì không xác định được khái niệm nền nào mình đang thiếu hoặc hiểu sai. Họ phải đọc lại, xem bài trước, tìm nhiều nguồn hoặc hỏi người khác; quá trình này có thể làm mất thời gian, gián đoạn nhịp học và khiến họ bỏ qua phần chưa hiểu, học tiếp trong trạng thái mơ hồ hoặc dừng bài.

**Điều phải đúng để giả thuyết đứng vững:**

- Tình huống xảy ra đủ gần và đủ rõ để học viên kể lại bằng hành vi cụ thể.
- Học viên muốn tiếp tục nhưng không xác định được điểm kiến thức đang cản mình.
- Workaround hiện tại có chi phí về thời gian, công sức hoặc sự gián đoạn.
- Việc không xử lý tạo ra hậu quả quan sát được.
- Bổ sung đúng kiến thức nền giúp học viên tiếp tục phần hiện tại.

**Điều khiến nhóm sửa hoặc bác bỏ:**

- Tình huống hiếm hoặc thường được giải quyết ngay bằng cách đọc lại.
- Học viên biết rõ điểm vướng và workaround hiện tại đã đủ tốt.
- Nguyên nhân chính là mất tập trung, bỏ lỡ lời giảng, cách giải thích hoặc ví dụ — không phải thiếu kiến thức nền.
- Pain không tạo hậu quả đáng kể.
- Ôn kiến thức nền không giúp học viên tiếp tục.

### 2.9. Solution Parking Lot

| Hướng giải quyết có thể có | Phân loại |
| --- | --- |
| Hỏi một số câu ngắn để xác định lỗ hổng và tạo phần ôn phù hợp | AI |
| Tóm tắt phần nội dung học viên vừa bỏ lỡ và cho phép quay lại đúng mốc | AI |
| Cung cấp bản đồ kiến thức nền và liên kết thủ công đến bài liên quan | Không sử dụng AI |
| Bổ sung nhiều ví dụ, cách giải thích và bài tập mẫu ở điểm thường gây nhầm | Không sử dụng AI |
| Cho phép gửi câu hỏi nhanh đến bạn học, mentor hoặc giảng viên | Không sử dụng AI |
| Dùng kết quả bài kiểm tra ngắn để đề xuất lộ trình ôn tập | AI |

## 3. Conversation Guide — phiên bản cuối sau luyện tập

### 3.1. Tín hiệu rút ra từ hai lượt luyện

- Câu hỏi về **lần gần nhất** đã mở được sự kiện cụ thể thay vì ý kiến chung.
- Một người kể việc bị phân tâm trong lớp, bỏ lỡ phần giải thích, sau đó không nối được sang nội dung tiếp theo; họ tìm trên Internet/công cụ AI và hỏi bạn bên cạnh.
- Ở lượt của Kiều Trang, người tham gia gặp khó khi phân biệt **capability của model** với **giá trị riêng của wrapper** và mất khoảng **20 phút**. Hậu quả là họ không tham gia được phần thảo luận và ban đầu hiểu nhầm wrapper chỉ là giao diện bên ngoài.
- Người này từng không phân biệt được **foundation model** và **application layer**, phải hỏi trợ giảng sau giờ học. Họ hiểu được khi nghe giải thích rằng model có thể tích hợp dần tính năng, còn sản phẩm giữ phần **policy và trách nhiệm**, rồi tự trình bày lại được ý của slide.
- Trong một tình huống đối chứng, họ hiểu “policy layer” ngay khi nhận được ví dụ về kiểm soát quyền truy cập. Lần đó rào cản là thiếu ví dụ, không phải bỏ lỡ cả chuỗi lập luận.
- Những tín hiệu này cho thấy nguyên nhân cạnh tranh như bỏ lỡ lời giảng hoặc cần cách giải thích/ví dụ khác phải được kiểm tra nghiêm túc. Chúng chưa chứng minh Hypothesis A.
- Các lượt luyện còn quá ngắn; interviewer đã chuyển câu hỏi sớm và chưa đào đủ trình tự, chi phí, kết quả cuối cùng và mức độ lặp lại.

### 3.2. Những sửa đổi so với guide trước luyện

1. Sau story opener, yêu cầu người tham gia kể theo trình tự trước khi chuyển sang câu hỏi khác.
2. Mỗi workaround phải được đào sâu bằng: vì sao chọn, mất bao lâu, có hiệu quả không và sau đó làm gì.
3. Thêm checkpoint bắt buộc về hậu quả, kết quả cuối cùng và pattern lặp lại trước khi kết thúc.
4. Giữ câu hỏi nguyên nhân ở dạng trung tính để phân biệt lỗ hổng nền với mất tập trung, cách trình bày hoặc thiếu ví dụ.
5. Bỏ câu xác nhận dẫn dắt như “việc đó cũng làm ảnh hưởng tiến độ của bạn đúng không?” và thay bằng “việc đó ảnh hưởng thế nào?”.

### 3.3. Tiêu chí tuyển người

Nhóm cần nói chuyện với người đã có ít nhất một lần không hiểu một đoạn giải thích hoặc bài tập và đã phải tìm cách xử lý trong vòng **7 ngày gần đây**.

**Recruitment check — không tính là evidence chính:**

> Trong 7 ngày gần đây, bạn có lần nào đang học mà gặp một đoạn giải thích hoặc bài tập chưa hiểu và đã phải tìm cách xử lý không?

### 3.4. Lời mở đầu và xin phép ghi âm

> Cảm ơn bạn đã tham gia. Nhóm mình đang tìm hiểu cách người học xử lý khi gặp một phần chưa hiểu. Mình muốn nghe về trải nghiệm thực tế của bạn; không có câu trả lời đúng hay sai và mình sẽ không giới thiệu một tính năng. Nếu bạn đồng ý, mình xin ghi âm chỉ để xem lại, ghi notes và phục vụ bài học. Bạn có đồng ý cho mình ghi âm không?

Interviewer chỉ bắt đầu ghi sau khi nhận được câu trả lời đồng ý rõ ràng.

### 3.5. Big 3

| Big 3 | Điều cần học | Evidence cần tìm | Điều khiến nhóm xem lại giả thuyết |
| --- | --- | --- | --- |
| 1. Sự kiện và hành vi | Học viên đang cố làm gì, bắt đầu vướng ở đâu và đã xử lý theo trình tự nào? | Câu chuyện gần đây, hành động và workaround thực tế | Không có sự kiện gần đây hoặc tự xử lý ngay |
| 2. Mức độ pain | Workaround tốn bao nhiêu thời gian/công sức; hậu quả và pattern ra sao? | Chi phí, gián đoạn, ảnh hưởng kết quả và lần lặp lại | Chỉ là bất tiện nhỏ, hiếm và không ảnh hưởng mục tiêu |
| 3. Nguyên nhân thật sự | Điều gì cuối cùng giúp học viên tiếp tục và vì sao? | Diễn biến trước–sau và một tình huống đối chứng | Chỉ cần nghe lại, ví dụ/cách giải thích khác hoặc workaround hiện tại đã đủ tốt |

### 3.6. Story opener và câu hỏi chính

1. Kể cho mình nghe về **lần gần nhất trong 7 ngày vừa qua** bạn gặp một phần chưa hiểu khi đang học.
2. Lúc đó bạn ở đâu, đang học nội dung gì và đang cố hoàn thành việc gì?
3. Bạn nhận ra mình bị vướng từ chi tiết nào? Từ lúc đó, chuyện gì xảy ra tiếp theo?
4. Bạn đã làm gì đầu tiên? Vì sao chọn cách đó? Sau đó bạn còn thử gì khác?
5. Với từng cách đã thử: bạn mất bao lâu/công sức ra sao và điều gì cho thấy nó có hoặc không có tác dụng?
6. Việc chưa hiểu ảnh hưởng cụ thể thế nào đến buổi học, phần thảo luận, bài làm, tiến độ hoặc quyết định tiếp tục/dừng lại?
7. Cuối cùng bạn có hiểu và tiếp tục được không? Điều gì cụ thể tạo ra thay đổi đó?
8. Theo bạn, lúc đó mình đang thiếu điều gì để hiểu tiếp? Chi tiết nào trong câu chuyện khiến bạn nghĩ vậy?
9. Lần gần nhất trước đó bạn gặp tình huống tương tự là khi nào? Bạn đã xử lý giống hay khác lần này?
10. Kể một lần gần đây bạn thoát khỏi chỗ vướng nhanh hơn. Điều gì khác giữa hai lần?

Không cần đọc máy móc toàn bộ câu hỏi. Interviewer follow câu chuyện nhưng phải thu được đủ bối cảnh, hành vi, workaround, chi phí, hậu quả, kết quả và pattern trước khi kết thúc.

### 3.7. Probe bank

- “Lúc đó chuyện gì xảy ra tiếp theo?”
- “Bạn đã làm gì cụ thể?”
- “Vì sao bạn chọn cách đó?”
- “Bạn mất khoảng bao nhiêu thời gian hoặc công sức?”
- “Cách đó giúp đến đâu? Bạn dựa vào đâu để biết?”
- “Bạn đã thử cách nào khác chưa?”
- “Việc đó kéo theo hậu quả gì?”
- “Lần gần nhất trước đó là khi nào?”

### 3.8. Phản xạ khi dữ liệu lệch

| User đưa ra | Phản xạ | Cách quay lại evidence |
| --- | --- | --- |
| Lời khen | Deflect | Cảm ơn ngắn rồi quay lại sự kiện thực tế |
| Câu chung chung/lời hứa tương lai | Anchor | “Lần gần nhất chuyện đó xảy ra là khi nào?” |
| Ý tưởng hoặc feature request | Dig | “Điều đó giúp bạn làm được gì? Hiện tại bạn xử lý ra sao?” |

## 4. Practice Reflection

> **Lưu ý:** Đây là phần cá nhân trong repo làm chung. Mỗi thành viên phải tự nghe lại đúng lượt mình làm interviewer, xác nhận nội dung và chỉnh về giọng cá nhân trước khi fork/đổi tên repo để nộp.

### 4.1. Nguyễn Quý Dũng

#### Câu hỏi nào giúp user kể một tình huống cụ thể?

Câu “Lúc đó bạn đang ở đâu và đang cố làm gì?” giúp làm lộ bối cảnh quan trọng: người tham gia vẫn ở trong lớp nhưng đang trả lời một tin nhắn trên điện thoại, nên bỏ lỡ phần giảng. Câu “Ngay sau đó bạn đã làm gì?” tiếp tục mở ra hai hành vi thật là tìm trên Internet/công cụ AI và hỏi bạn bên cạnh.

#### Chỗ nào tôi cần làm tốt hơn ở lần phỏng vấn thật?

Tôi đã chuyển giữa các câu hỏi quá nhanh và kết thúc khi câu chuyện mới chỉ mở ra. Tôi chưa hỏi đủ thời gian/công sức, hiệu quả của từng workaround, kết quả cuối cùng, mức độ lặp lại và liệu người học có thực sự thiếu kiến thức nền hay chỉ bỏ lỡ lời giải thích. Câu gần cuối có dạng xác nhận “cũng làm ảnh hưởng tiến độ... đúng không?” nên mang tính dẫn dắt. Lần sau tôi cần dùng câu trung tính, chờ người tham gia kể xong và follow từng tín hiệu bằng “chuyện gì xảy ra tiếp theo?” hoặc “điều gì cho thấy cách đó có tác dụng?”.

#### Nhóm đã sửa Conversation Guide ở đâu và vì sao?

Nhóm bổ sung một chuỗi probe bắt buộc cho từng workaround, thêm câu hỏi về kết quả cuối cùng và pattern, đồng thời viết lại câu hỏi hậu quả theo dạng mở. Nhóm cũng mở rộng Hypothesis B để bao gồm việc bỏ lỡ lời giảng và nhu cầu về ví dụ/cách giải thích khác, vì đây là các cách giải thích cạnh tranh đã xuất hiện trong hai lượt luyện.

### 4.2. Trần Thị Kiều Trang

#### Câu hỏi nào giúp user kể một tình huống cụ thể?

Câu “Phần nào khó hoặc tốn công nhất?” giúp người tham gia chỉ ra đúng điểm vướng là phân biệt capability của model với giá trị riêng của wrapper và định lượng được chi phí khoảng 20 phút. Câu “Việc đó ảnh hưởng thế nào đến buổi học?” tiếp tục làm lộ hậu quả cụ thể: không tham gia được thảo luận và ban đầu hiểu nhầm wrapper chỉ là giao diện bên ngoài.

#### Chỗ nào tôi cần làm tốt hơn ở lần phỏng vấn thật?

Tôi đã lấy được chi phí, hậu quả và một tình huống đối chứng, nhưng chưa đào đầy đủ trình tự của sự kiện hiện tại: người tham gia đã làm gì đầu tiên, đã thử những workaround nào trước khi được giải thích và mỗi cách có hiệu quả ra sao. Lần sau tôi cần giữ câu chuyện ở một sự kiện đủ lâu, dùng “chuyện gì xảy ra tiếp theo?” và hỏi rõ thời điểm/tần suất để bảo đảm người tham gia đúng tiêu chí tuyển trong 7 ngày gần đây.

#### Nhóm đã sửa Conversation Guide ở đâu và vì sao?

Nhóm thêm probe về trình tự, thời gian, hiệu quả của từng workaround và evidence trước–sau. Guide cũng bổ sung tình huống đối chứng để phân biệt một lỗ hổng kiến thức nền với trường hợp người học chỉ thiếu ví dụ hoặc bỏ lỡ chuỗi lập luận. Việc sửa này xuất phát trực tiếp từ trường hợp “policy layer”: một ví dụ về kiểm soát quyền truy cập đã giúp người tham gia hiểu nhanh.

## 5. AI Support Log

| AI đã hỗ trợ gì? | Điểm sai/hời hợt hoặc rủi ro | Cách nhóm xử lý |
| --- | --- | --- |
| So sánh hai nháp Chặng 1 và sắp xếp Problem Hypothesis Brief theo rubric | AI có thể làm giả thuyết nghe chắc chắn hơn evidence thực có | Giữ nhãn “hypothesis”, nêu rõ điều kiện bác bỏ và không tuyên bố validated |
| Rà soát câu hỏi dẫn dắt và đề xuất Conversation Guide sau luyện | Một guide dài có thể khiến interviewer đọc máy móc | Ghi rõ guide là xương sống; follow câu chuyện và dùng probe khi cần |
| Chép lời sơ bộ hai bản ghi bằng nhận dạng giọng nói cục bộ | Một số thuật ngữ kỹ thuật bị nhận dạng sai; exact quote có nguy cơ sai | Nhóm cung cấp lại phần hỏi–đáp chuẩn để sửa các thuật ngữ `wrapper`, `foundation model`, `application layer` và `policy layer`; phần không nghe rõ không được dùng làm exact quote |
| Đối chiếu bài với bốn gate và tạo cấu trúc `interview/notes.md` | AI không được bịa interview data hoặc viết reflection thay cho việc tự nghe lại | Mọi evidence đều truy về bản ghi/nội dung hỏi–đáp; Dũng và Trang phải tự nghe, xác nhận và chỉnh Reflection cá nhân trước khi nộp |

## 6. Tệp phỏng vấn

- Interview Record của cả hai lượt luyện: [`interview/notes.md`](interview/notes.md)
- Bản ghi lượt Nguyễn Quý Dũng: [`interview/recording-quy-dung.m4a`](interview/recording-quy-dung.m4a)
- Bản ghi lượt Kiều Trang dùng để chỉnh guide chung: [`interview/recording-kieu-trang.m4a`](interview/recording-kieu-trang.m4a)

Các bản ghi chỉ được dùng để review và phục vụ bài học.
