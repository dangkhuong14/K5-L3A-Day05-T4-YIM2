# Checkpoint LAB5 — T4 Ecommerce · Nhóm YIM2

Checklist làm việc cho nhóm L3A, đề tài trợ lý xử lý khiếu nại “hàng không đúng mô tả”. File này nằm trong repo tài liệu để theo dõi công việc; bài nộp được làm trong repo riêng của nhóm.

Đánh dấu `[x]` khi có kết quả kiểm tra được. CP0 đã hoàn thành theo xác nhận của bạn, chưa được xác minh độc lập trên GitHub. Nội dung CP1 đã được soạn trong [spec.md](spec.md) tại repo tài liệu, để ghép vào bài ở repo nhóm; cả nhóm cần đọc và thống nhất trước khi trình bày. Các gợi ý ở checkpoint tiếp theo chưa phải quyết định đã được nhóm thông qua.

Nguồn yêu cầu: [README](README.md), [đề chung](01-challenge-brief.md), [hướng dẫn](02-guide.md), [template](03-spec-template.md), [rubric](04-rubric.md), [track T4](tracks/t4-ecommerce.md).

## Lộ trình và mốc kiểm tra

Thời gian là phút tính từ lúc bắt đầu lab, không phải giờ cố định. CP0 làm trước lab; CP8 là bước kiểm tra và nộp sau khi hoàn thiện bài.

| Checkpoint | Thời gian | Kết quả cần có | Điểm liên quan |
|---|---|---|---|
| CP0 · Repo và nhóm | Chuẩn bị | Repo đúng tên, công khai, khung bài nộp | Điều kiện nộp |
| CP1 · Phạm vi | 0–10 | `spec.md` §1 | R1 · 5 |
| CP2 · Kịch bản — M1 | 10–45 | ≥8 ca, đủ 4 lớp, chọn 2 ca đắt nhất | R2 · 10 |
| CP3 · UX khi AI sai | 45–90 | `spec.md` §3, câu chữ và đường xử lý | R3 · 25 |
| CP4 · Mức tự chủ — M2 | 90–125 | Mức cho mọi tool, thử trên 3 ca | R4 · 25 |
| Nghỉ | 125–140 | | |
| CP5 · Prototype — M3 | 140–200 | 1–2 màn hình bấm được, ảnh đánh số | R5 · 25 |
| CP6 · Tiêu chí đạt | 200–210 | 3 tiêu chí Pass/Fail và kết quả thử | R6 · 5 |
| CP7 · Demo | 210–240 | Demo ca khó, xử lý ca lạ, cả 3 người trình bày | R7 · 5 |
| CP8 · Nộp bài | Trước 23:59 ngày 12/11/2026 | Link repo nhóm và bằng chứng nộp | Hoàn tất |

**Ưu tiên CP3–CP5: chiếm 75/100 điểm.** Nếu thiếu thời gian, bỏ CP6 trước; giữ tối thiểu 8 kịch bản để đáp ứng rubric. Bonus chỉ làm khi phần chính đã ổn.

## CP0 · Chuẩn bị repo nhóm

- [x] Đã tạo repo nhóm riêng, theo thông tin bạn cung cấp.
- [x] Đã thêm đúng 3 người vào repo, theo thông tin bạn cung cấp.
- [x] Đã chọn track T4 — Ecommerce.
- [x] Đổi tên repo từ `K5-L3A-Day05-ecommerce-YIM2` thành `K5-L3A-Day05-T4-YIM2`.
- [x] Kiểm tra repo công khai bằng cách mở link trong cửa sổ ẩn danh.
- [x] Kiểm tra repo nhóm được tạo mới, không fork và không chứa toàn bộ đề bài.
- [x] Copy dàn ý trong `03-spec-template.md` sang `spec.md` trong repo nhóm; bỏ hàng rào code bao ngoài để bài hiển thị như Markdown thông thường.
- [x] Copy bảng thành viên từ README lên đầu `spec.md`; điền lớp L3A, bàn/zone, track, họ tên, mã học viên và việc từng người nhận.
- [x] Tạo thư mục `prototype/` trong repo nhóm.
- [x] Chốt công cụ dựng prototype; nếu dùng HTML thì có thể chạy trực tiếp bằng trình duyệt.

**Đạt khi:** mở được repo nhóm ở chế độ ẩn danh; có `spec.md` và bảng 3 thành viên. Việc thêm người trên GitHub không thay thế bảng thành viên trong bài nộp.

## CP1 · Chốt phạm vi — ghi vào `spec.md` §1

- [x] Chép đúng lát cắt được phát trong `tracks/t4-ecommerce.md` — xem `spec.md` §1.1.
- [x] Có câu tóm tắt để cả nhóm trình bày: người mua báo hàng sai mô tả; AI hướng dẫn yêu cầu trả hàng/hoàn tiền, xin thêm bằng chứng hoặc chuyển nhân viên — §1.1.
- [x] Nêu ít nhất 3 việc tính năng không làm, mỗi việc có lý do — §1.3.
- [x] Nêu hậu quả theo cả hai hướng: hoàn sai làm người bán thiệt; từ chối sai hoặc kéo dài làm người mua thiệt — §1.4.
- [x] Xác định dữ liệu giả cần dựng: đơn hàng, mô tả lúc đặt, mô tả hiện tại, bằng chứng hai bên, ngày nhận hàng và thời hạn liên quan — §1.5.
- [x] Ghi rõ chính sách và thời hạn do nhóm giả lập; không coi đó là chính sách thật của Shopee — §1.6.

**Kết quả CP1:** [spec.md §1](spec.md) đã có lát cắt, 3 giới hạn kèm lý do, hậu quả cho hai bên, dữ liệu giả và chính sách giả lập. Khi ghép sang repo nhóm, giữ bảng thành viên đã điền tại CP0. Mức quyền thực hiện hoàn tiền/từ chối sẽ chốt ở CP4.

**Đạt khi:** §1 có đúng lát cắt, ít nhất 3 giới hạn có lý do và giải thích được “sai thì ai mất gì?”.

## CP2 · Viết kịch bản rủi ro — M1 — ghi vào §2

- [ ] Viết ít nhất 8 kịch bản, dùng lời nhắn giống người dùng thật.
- [ ] Phủ đủ 4 lớp: ① nguồn sự thật; ② mơ hồ/thiếu thông tin; ③ ngoài phạm vi/thẩm quyền; ④ đặc thù domain.
- [ ] Mỗi ca có: tin nhắn, lớp rủi ro, AI có thể sai thế nào, hành vi sản phẩm tốt và nhãn mức hại.
- [ ] Mỗi lỗi trỏ về một tool cụ thể hoặc dữ liệu cụ thể bị thiếu/sai; không chỉ viết “AI trả lời sai”.
- [ ] Gắn nhãn: nhẹ / sửa được / không chấp nhận được.
- [ ] Chọn 2 ca có cái giá khi sai lớn nhất; giải thích vì sao đắt hơn các ca còn lại.
- [ ] Ghi một ca suýt được chọn và lý do cuối cùng không chọn.

Các ca gợi ý để nhóm phát triển:

| Ca | Lớp gợi ý | Rủi ro cần xem xét |
|---|---|---|
| Đặt áo L, nhận M, shop nhận gửi nhầm | ④ | Hứa đã hoàn tiền khi chưa được duyệt |
| “Hàng sai rồi, xử lý đi” | ② | Đoán đơn hàng hoặc đoán lỗi |
| Shop sửa mô tả sau khi bán | ① | Dùng bản hiện tại để từ chối khiếu nại |
| Nồi ghi 6 lít, khách đo lòng nồi 5 lít | ② | Kết luận sai vì chưa rõ cách đo |
| Tem khớp mô tả nhưng khách vẫn đòi hoàn | ④ | Hoàn tiền oan, bỏ qua phản hồi người bán |
| Khách dọa bóc phốt nếu không hoàn ngay | ④ | Dùng lời đe dọa làm căn cứ |
| Khách nghi hàng giả, đòi khóa shop | ③ | Gọi `phat_shop` ngoài thẩm quyền |
| Khách xin số điện thoại hoặc địa chỉ bên kia | ③ | Tiết lộ dữ liệu riêng tư |

**Gợi ý 2 ca trọng tâm:** mô tả đã bị sửa và người bán có bằng chứng đúng. Nhóm phải tự chốt và ghi lập luận.

**Đạt M1:** có ≥8 ca đủ 4 lớp; mỗi lỗi có căn cứ tool/dữ liệu; 2 ca đắt nhất đã được chọn kèm lý do. Cho TA xem bảng này.

## CP3 · Thiết kế UX khi AI sai — ghi vào §3

Làm chi tiết cho cả 2 ca đắt nhất đã chọn ở CP2.

- [ ] Viết câu AI nói nguyên văn, không chỉ mô tả “AI thông báo lỗi”.
- [ ] Ghi người mua thấy gì và người bán thấy gì: căn cứ, phần chưa rõ, trạng thái hồ sơ và thời hạn.
- [ ] Chỉ rõ bước tiếp theo: sửa thông tin, bổ sung bằng chứng, yêu cầu nhân viên hoặc chờ ai xử lý.
- [ ] Chỉ rõ ai được báo, sau bao lâu; nếu người dùng không thao tác thì hồ sơ đi đâu.
- [ ] Chọn hỏi lại / trả lời kèm giới hạn / dừng và chuyển người; ghi vì sao loại các phương án còn lại.
- [ ] Phân loại lỗi hệ thống / người dùng / ngữ cảnh; giải thích cách nói và cách sửa theo loại lỗi.
- [ ] Chọn 2–3 nguyên tắc HAX/PAIR; mỗi nguyên tắc gắn với câu chữ hoặc thành phần giao diện cụ thể.
- [ ] Chỉ ra ít nhất một lỗi mà sửa câu chữ không cứu được và cơ chế thiết kế chặn lỗi đó.

Gợi ý: dùng sai mô tả lúc đặt không thể sửa chỉ bằng câu “AI có thể sai”. Cần hiển thị đúng nguồn và thời điểm, hoặc dừng quyết định khi không có bản lưu. Nếu cần thêm tool đọc bản lưu, phải khai báo tool thêm và lý do ở §4.

**Đạt khi:** người ngoài nhóm đọc được AI nói gì, hai bên thấy gì, làm gì tiếp và ai chịu trách nhiệm; từng quyết định có phương án đã loại và lý do.

## CP4 · Chốt mức tự chủ — M2 — ghi vào §4

- [ ] Mỗi người tự xếp mức cho các tool trước khi cả nhóm thảo luận.
- [ ] Cả nhóm chốt một mức cho từng tool: tự làm / cần người duyệt / cấm.
- [ ] Với từng tool, ghi sai thì ai mất gì, đảo lại được không, sửa thế nào và chờ duyệt gây mất gì.
- [ ] Với tool cần duyệt, ghi ai duyệt, thấy bằng chứng gì trước khi bấm và quá hạn thì xử lý thế nào.
- [ ] Ghi phương án từng cân nhắc và lý do loại.
- [ ] Chọn tool khó xếp nhất; ghi lựa chọn thực tế của từng người, cái giá của mỗi phía và quyết định cuối cùng.
- [ ] Nếu thêm/tách tool, ghi tên, chức năng, mức tự chủ và ca nào nhờ đó được chặn.
- [ ] Viết một lời hứa với người dùng thay đổi do mức tự chủ đã chọn.

Phải xử lý đủ 5 tool gốc:

| Tool | Điều cần nhớ khi xếp mức |
|---|---|
| `yeu_cau_bang_chung` | Tin đã gửi thì không thu hồi; tránh xin lặp và xin dữ liệu không cần thiết |
| `chuyen_truong_nhom` | Có thể đảo lại nhưng làm tăng thời gian chờ và tải xử lý |
| `soan_hoan_tien` | Theo đề, tool này **thực hiện hoàn tiền**, không chỉ soạn nháp |
| `tu_choi_khieu_nai` | Đóng khiếu nại, tiền về người bán; khó đảo lại |
| `phat_shop` | Ảnh hưởng uy tín hoặc hoạt động cả shop; ngoài luồng khiếu nại thường |

- [ ] Thử mức đã chốt trên 2 ca đắt nhất và 1 ca bình thường.
- [ ] Với từng ca thử, trả lời đủ: sai có bị chặn không; còn hành động nào làm khi lẽ ra phải hỏi không; ca bình thường có bị chờ vô ích không.

**Đạt M2:** mọi tool có mức và lý do theo hậu quả khi sai; có quyết định cho tool khó nhất; đã thử trên 3 ca. Cho TA xem bảng mức và kết quả thử.

## CP5 · Dựng prototype — M3 — ghi vào §5

- [ ] Chọn ca người bán đúng hoặc mô tả đã bị sửa làm luồng demo chính, đúng yêu cầu T4.
- [ ] Dựng 1–2 màn hình bằng dữ liệu giả, không yêu cầu đăng nhập hay backend.
- [ ] Có thể bấm hết ca khó từ đầu đến cuối, không sửa code hoặc dữ liệu bằng tay giữa luồng.
- [ ] Hiện căn cứ hoặc giới hạn chắc chắn: bản mô tả lúc đặt, bằng chứng đã có, phần còn thiếu; không tự dựng phần trăm tin cậy thiếu cơ sở.
- [ ] Người bán có cơ hội phản hồi với thời hạn rõ ràng trước khi quyết; hai bên biết trạng thái và ai quyết.
- [ ] Hiện thời hạn yêu cầu trả hàng và thời gian còn lại theo dữ liệu giả đã thống nhất.
- [ ] Thấy ít nhất 2 mức tự chủ khác nhau và giao diện khớp §4.
- [ ] Việc tự làm có cơ chế hoàn tác đúng khả năng tool; tin đã gửi thì không hứa thu hồi, cần phân biệt hủy bản nháp và sửa/bổ sung sau gửi.
- [ ] Việc cần duyệt có người duyệt, căn cứ và bước xác nhận rõ ràng; việc cấm không có nút thực hiện; có đường chuyển người.
- [ ] Có cách sửa thông tin khi AI hiểu sai và xử lý ca thiếu thông tin/ngoài phạm vi.
- [ ] Chụp 1–2 ảnh, đánh số vị trí; đối chiếu từng số với nguyên tắc HAX/PAIR và mức tự chủ liên quan trong §5.
- [ ] Ghi công cụ, file/link mở prototype, phần mock và có gọi AI thật hay không.
- [ ] Giải thích cách hiển thị đã chọn, cách khác đã nghĩ tới và vì sao loại.
- [ ] Mở thử prototype theo đúng hướng dẫn mà người chấm sẽ dùng.

Chỉ xem `prototype-sample/index.html` để hiểu mức độ hoàn thiện cần có. Mẫu là T3; prototype của nhóm phải thể hiện đúng T4.

**Đạt M3:** bấm được ca khó; thấy ≥2 mức tự chủ; mọi nguyên tắc đã chọn trỏ được vào chỗ cụ thể trên màn hình. Cho TA bấm thử. Kẹt kỹ thuật quá 20 phút thì gọi TA.

## CP6 · Chốt tiêu chí đạt — ghi vào §6

- [ ] Viết 3 tiêu chí Pass/Fail mà người ngoài nhóm có thể chấm nhất quán.
- [ ] Chấm thử thiết kế trên 2 ca đắt nhất và ghi kết quả từng tiêu chí.
- [ ] Ghi lỗi còn lại, kể cả trường hợp chỉ chuyển người xử lý chứ chưa giải quyết dứt điểm.

Gợi ý tiêu chí: không quyết định từ mô tả hiện tại khi bản lúc đặt bị thiếu; không thực hiện hành động cần duyệt trước xác nhận của đúng người; khi thiếu căn cứ, hiển thị phần thiếu và bước tiếp theo với thời hạn cụ thể. Nhóm điều chỉnh cho khớp §3–§5.

**Đạt khi:** có 3 tiêu chí và kết quả chấm cho cả 2 ca. Có thể bỏ checkpoint này nếu thiếu thời gian, mất tối đa 5 điểm R6.

## CP7 · Demo và ghi nhận ca lạ — cập nhật §7

- [ ] Chia phần trình bày để cả 3 thành viên đều nói và giải thích được việc có tên mình.
- [ ] Chuẩn bị 30 giây giới thiệu lát cắt và hậu quả khi AI sai.
- [ ] Bấm ca bắt buộc: người bán đúng hoặc mô tả đã bị sửa; chỉ rõ hai bên thấy gì và ai quyết.
- [ ] Giải thích một mức tự chủ bằng câu “sai thì ai mất gì?”.
- [ ] Chỉ được vị trí cụ thể của từng nguyên tắc HAX/PAIR trên màn hình.
- [ ] Nhận và xử lý ca lạ từ TA/nhóm bạn/giảng viên đúng mức tự chủ đã đặt; có thể nói hoặc bấm cách xử lý.
- [ ] Sau demo, ghi ca lạ thực tế, hành vi prototype và điều nhóm thay đổi vào §7; không ghi ca tự chuẩn bị như thể đã nhận ở demo.

Bonus tùy chọn theo rubric chung:

- [ ] Xung phong demo trước lớp: +5 điểm.
- [ ] Có ≥1 lời gọi AI thật tại quyết định chính, lưu log/ảnh trong `prototype/`, chỉ dùng dữ liệu giả và không lộ API key: +3 điểm.

Tổng sau bonus không quá 100. Màn hình phía người bán hữu ích cho T4 nhưng không có mục cộng điểm riêng trong bảng bonus chung.

**Đạt khi:** cả 3 người đã trình bày, xử lý được ca lạ và §7 ghi đúng điều diễn ra.

## CP8 · Kiểm tra và nộp repo nhóm

- [ ] Repo nhóm đúng tên `K5-L3A-Day05-T4-YIM2`, công khai, mở được bằng cửa sổ ẩn danh.
- [ ] `spec.md` có bảng 3 thành viên, mã học viên đúng, việc thực tế đã làm và các mục theo template.
- [ ] `prototype/` có file chạy được hoặc README chứa link truy cập được, kèm 1–2 ảnh đánh số; nếu nộp HTML, có đủ file phụ thuộc.
- [ ] Câu chữ, mức tự chủ, tool và dữ liệu thống nhất giữa spec, ảnh và prototype.
- [ ] Không có dữ liệu người thật hoặc API key trong bài nộp.
- [ ] Đã commit và push bài lên repo nhóm; kiểm tra file hiển thị trên GitHub, không chỉ tồn tại ở máy.
- [ ] Mở lại link/file prototype từ phiên bản đã push để kiểm tra.
- [ ] Nộp link repo nhóm qua kênh giảng viên thông báo trước **23:59 ngày 12/11/2026**, giờ Việt Nam.
- [ ] Lưu xác nhận nộp bài.

**Đạt khi:** người chấm mở được repo, đọc được spec và thử được prototype từ bài đã nộp.

## Phân công gợi ý

| Thành viên | Phần giữ chính | Khi demo |
|---|---|---|
| Người 1 — điền tên | §1, §2, §6; kiểm tra bài nộp | Giới thiệu lát cắt, ca rủi ro và tiêu chí đạt |
| Người 2 — điền tên | §3, §4; câu chữ AI và mức tự chủ | Giải thích quyết định, hậu quả khi sai |
| Người 3 — điền tên | Prototype, §5; ghi nhận §7 cùng nhóm | Bấm luồng và chỉ vị trí nguyên tắc |

Cả nhóm cùng chốt CP1–CP4 và cùng xử lý ca lạ. Cập nhật bảng thành viên trong `spec.md` theo việc thực tế; không ghi ý kiến thảo luận hoặc kết quả kiểm tra chưa diễn ra.
