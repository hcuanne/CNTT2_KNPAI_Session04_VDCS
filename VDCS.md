
# 1. Bối cảnh
Cửa hàng sử dụng AI để kiểm tra đơn hàng, tính tiền và phát hiện lỗi dữ liệu.

# 2. Yêu cầu đầu ra
- Xác định Input và Output.
- Viết prompt hoàn chỉnh.
- Đưa ra kết quả chạy thử.

# 3. Bài làm

## Bước 1: Thiết kế I/O
- Input: Mã đơn, tên khách, sản phẩm, số lượng, đơn giá.
- Output: Tổng tiền và trạng thái đơn hàng.

## Bước 2: Viết Prompt

"Bạn là AI quản lý đơn hàng. Hãy thực hiện:
1. Kiểm tra dữ liệu đầu vào.
2. Nếu hợp lệ, tính tổng tiền = Số lượng × Đơn giá.
3. Nếu thiếu dữ liệu, báo 'Thiếu dữ liệu'.
4. Nếu số lượng hoặc đơn giá <= 0, báo 'Không hợp lệ'.
5. Trình bày kết quả dạng bảng.
6. Nếu phản hồi bị ngắt, tiếp tục từ phần còn thiếu.

Áp dụng Chain-of-Thought để kiểm tra logic và Prompt Chaining để xử lý từng bước.

Dữ liệu:
- DH01, An, Chuột, 2, 150000
- DH02, Bình, Bàn phím, 0, 300000
- DH03, Nam, USB, 3, trống"

## Bước 3: Kết quả chạy thử

| Mã đơn | Tổng tiền | Trạng thái |
|---|---|---|
| DH01 | 300.000đ | Hợp lệ |
| DH02 | - | Không hợp lệ |
| DH03 | - | Thiếu dữ liệu |


