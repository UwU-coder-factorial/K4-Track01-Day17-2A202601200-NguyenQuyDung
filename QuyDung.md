# Khai phá Problem & Solution Template

## 1. Solution — Gỡ solution khỏi hình thức cụ thể

**Case đã chọn:** ........................................................................

Ghi lại directive nguyên văn, sau đó diễn đạt lại dưới dạng một capability trung tính.

### Câu hỏi dẫn dắt:
- Câu nào trong directive đang mô tả giao diện, tên feature hoặc công nghệ?
- Nếu bỏ tên nút, màn hình và AI action, khả năng cần tạo ra là gì?
- Nhóm có đang mặc định cách triển khai được giao là cách duy nhất không?
- Capability có thể được mô tả mà không dùng tên feature không?

**Solution directive:**
> ..........................................................................................

**Capability trung tính:**
> ..........................................................................................

---

## 2. Change — Làm lộ chuỗi thay đổi được kỳ vọng

Đừng nhảy thẳng từ feature tới outcome. Viết các mắt xích mà team đang ngầm tin sẽ xảy ra.

### Câu hỏi dẫn dắt:
- User sẽ biết hoặc làm được điều gì khác?
- Hành vi nào phải thay đổi để outcome xảy ra?
- Trạng thái hoặc kết quả nào được kỳ vọng thay đổi?
- Đâu là output team tạo ra, đâu là outcome team chỉ có thể ảnh hưởng?
- Nếu user không thay đổi hành vi, solution còn tạo được outcome không?

```text
Solution → ................................ → ................................ → Outcome
```

**Các thay đổi được kỳ vọng:**
- ........................................................................................
- ........................................................................................
- ........................................................................................

---

## 3. Actor — Xác định các nhóm người có liên quan

Một solution có thể liên quan đến nhiều nhóm user hoặc stakeholder khác nhau. Người trực tiếp sử dụng feature chưa chắc là người đang gặp pain chính, phải thay đổi hành vi hoặc chịu hậu quả.

*Ví dụ với AI Support Radar trên VLearn:* learner là người có hành vi học tập được phân tích; instructor là người xem Support Queue và quyết định can thiệp; coach là người có thể trực tiếp hỗ trợ learner. Cả ba đều là actor liên quan nhưng có job, pain và lợi ích khác nhau.

### Câu hỏi dẫn dắt:
- Ai trực tiếp sử dụng solution?
- Ai trực tiếp trải nghiệm pain?
- Ai phải thay đổi hành vi để outcome xảy ra?
- Ai chịu hậu quả nếu problem không được giải quyết?
- Ai hưởng lợi gián tiếp?
- Người nhận feature có chắc là người sở hữu pain chính không?

| Actor | Họ đang làm gì? | Pain hoặc hậu quả có thể có | Họ hưởng lợi thế nào? |
| --- | --- | --- | --- |
| | | | |
| | | | |
| | | | |

- **Actor nhóm chọn để điều tra trước:** ........................................................
- **Vì sao chọn nhánh này thay vì actor khác:** ..................................................

---

## 4. Situation & Job — User đang cố làm gì trong tình huống nào?

Chọn một khoảnh khắc cụ thể mà actor có thể đã trải qua. Mô tả hoàn cảnh và việc họ đang cố hoàn thành, chưa kết luận pain nằm ở đâu. Job phải còn tồn tại ngay cả khi bỏ AI và feature khỏi bối cảnh.

### Câu hỏi dẫn dắt:
- Tình huống bắt đầu khi chuyện gì xảy ra?
- Lúc đó user đang cố hoàn thành việc gì?
- Vì sao việc đó quan trọng với họ?
- Hiện tại họ đang thực hiện việc đó như thế nào?
- Họ bắt đầu gặp vướng mắc ở điểm nào?

```text
Tình huống bắt đầu
→ User muốn hoàn thành việc gì
→ Hiện tại họ làm như thế nào
→ Điểm bắt đầu gặp vướng mắc
```

**Mô tả Situation & Job:**
> Khi [tình huống/trigger], [actor] đang cố [việc cần hoàn thành] bằng cách [cách họ đang làm hiện tại].
> 
> ..........................................................................................

**JTBD Hypothesis:**
> Khi [situation], tôi muốn [progress], để có thể [desired outcome].
> 
> ..........................................................................................

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

**Pain Hypothesis A:**
> Khi [situation], [actor] gặp khó khăn trong việc [job] vì [barrier], dẫn đến [consequence].
> 
> ..........................................................................................

**Pain Hypothesis B — cách giải thích cạnh tranh:**
> Khi [situation], [actor] gặp khó khăn trong việc [job] vì [barrier], dẫn đến [consequence].
> 
> ..........................................................................................

- **Giả thuyết nhóm chọn để điều tra trước:** A / B
- **Lý do chọn:** ...............................................................................

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
| Situation có thật | | |
| Pain có ý nghĩa | | |
| Workaround tồn tại | | |
| Consequence tồn tại | | |
| Pattern có lặp | | |

---

## Chốt Problem Hypothesis và park solution

**Problem Hypothesis nhóm mang sang Chặng 2:**
> ..........................................................................................

**Điều gì phải đúng để giả thuyết đứng vững:**
> ..........................................................................................

**Điều gì có thể khiến nhóm sửa hoặc bác bỏ giả thuyết:**
> ..........................................................................................

### Solution Parking Lot
*Brainstorm ít nhất năm hướng, trong đó có ít nhất một hướng không sử dụng AI.*

| Hướng giải quyết có thể có | AI / Không sử dụng AI |
| --- | --- |
| 1. | |
| 2. | |
| 3. | |
| 4. | |
| 5. | |
