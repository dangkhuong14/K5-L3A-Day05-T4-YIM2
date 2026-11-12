# Bài nộp LAB5 — T4 Thương mại điện tử · Nhóm YIM2

> Bản soạn CP1. Chép §1 vào `spec.md` của repo nhóm, giữ bảng thành viên đã điền ở CP0.

## §1. Lát cắt & phạm vi

### 1.1. Lát cắt

Trong **Trò chuyện với Shopee**, khi **người mua** đang báo "hàng nhận không đúng mô tả", **AI tự hướng dẫn gửi yêu cầu trả hàng hoàn tiền, xin thêm bằng chứng, hay chuyển nhân viên**, để người mua biết đúng bước tiếp theo, và người bán không bị xử thua khi họ đúng.

### 1.2. AI được thêm vào đâu?

Theo mô tả sản phẩm nền trong đề T4, người mua hiện chọn đơn, chọn lý do và gửi bằng chứng qua luồng có sẵn. Trợ lý được thiết kế để hiểu lời khiếu nại, đối chiếu với **mô tả lúc đặt**, xác định bằng chứng còn thiếu và chọn bước hỗ trợ tiếp theo. Quyền thực hiện từng tool sẽ chốt ở §4; hướng dẫn gửi yêu cầu không đồng nghĩa đã hoàn tiền.

### 1.3. Ba việc tính năng không làm

| Không làm | Vì sao? |
|---|---|
| Không cung cấp số điện thoại, địa chỉ riêng của bên kia | Không cần cho việc đối chiếu bằng chứng và có thể dẫn đến quấy rối ngoài sàn; T4 yêu cầu bảo vệ thông tin này |
| Không tự kết luận hàng giả hoặc xử phạt shop trong luồng khiếu nại thường | Cần bộ phận chuyên trách xác minh; phạt sai ảnh hưởng cả shop và khó đảo lại |
| Không xử lý đổi địa chỉ giao hàng, tư vấn mua hàng hoặc tác vụ ngoài khiếu nại sai mô tả | Vượt lát cắt được phát và không có tool tương ứng trong T4 |

Chọn tập trung vào khiếu nại sai mô tả để kiểm soát căn cứ và hậu quả cho hai bên. Loại phương án trợ lý hỗ trợ mọi việc sau mua vì vượt bộ tool và phạm vi prototype 1–2 màn hình.

### 1.4. AI làm sai thì ai mất gì?

| Hành động sai | Ai chịu thiệt? | Khả năng đảo lại theo đề |
|---|---|---|
| `soan_hoan_tien` khi người bán đã giao đúng | Người bán mất tiền, có thể mất cả hàng | Khó: tiền đã về người mua |
| `tu_choi_khieu_nai` khi người mua thực sự nhận sai hàng, ví dụ AI dùng mô tả đã bị sửa | Người mua mất tiền và giữ hàng sai | Khó: khiếu nại đóng, tiền về người bán |
| `phat_shop` chỉ vì khách đe dọa hoặc nghi ngờ hàng giả | Người bán bị trừ uy tín hoặc khóa shop oan | Khó: ảnh hưởng cả shop |

Sai cả hai hướng đều có người chịu thiệt; không mặc định hoàn tiền hoặc từ chối. Phải xét mô tả lúc đặt và bằng chứng hai bên. Đây là các hậu quả chính để chốt phạm vi; §2 sẽ viết đủ kịch bản, §4 sẽ đánh giá cả 5 tool.
