# DoAnCTDL-CNTN15

## Quy ước:


Mỗi lớp được viết thành 1 file riêng, đặt tên file = tên lớp.

Để tránh phức tạp thêm cho cái đồ án, ở đây không sử dụng tính kế thừa và đa hình của OOP nhé, trừ khi có giải thích hợp lý sự cần thiết việc sử dụng 2 tính chất này. Tính đóng gói vẫn bắt buộc.
Các lớp:

## Lớp Warehouse sẽ có các thuộc tính và phương thức sau:

1. Thuộc tính: private

_x, _y, _dx, _dy có kiểu là int, trong đó _x, _y là toạ độ điểm trái trên của kho hàng, _dx, _dy lần lượt là kích thước của kho hàng trên trục Ox, Oy ứng với góc nghiêng là 0. Ghi chú: hệ trục toạ độ Oxy được xây dựng theo chuẩn giống như [link](https://goo.gl/IgImbI)

_angle có kiểu là double (do các hàm toán học có sẵn trong C# dùng kiểu double), đại diện cho góc nghiêng của kho hàng. Ghi chú: quy ước quay, xem phần Rotating của [link](https://goo.gl/CV2Ndm)

_data có kiểu là mảng 2 chiều của Goods (vẫn chưa thống nhất về tổ chức cấu trúc dữ liệu ở đây, có nên sử dụng bảng thưa hay không, cần có bài viết bàn về cái này), đại diện cho danh sách các kiện hàng có trong kho.

2. Phương thức: public → Cái này có thể chỉnh sửa lại cho phù hợp

Khởi tạo: mặc định, kèm theo đó là 1 loạt các phương thức set. Khi đó việc khởi tạo sẽ như thế này: Warehouse dummy = (new Warehouse).setX(dummyX)....
	
Input(String fileName): void → Nhập dữ liệu từ file
	
OutputConsole(void): void → Xuất dữ liệu ra màn hình Console (đây là yêu cầu 1)
	
MoveConsole(String command): bool → Chuyển kiện hàng trong màn hình Console (đây là yêu cầu 2)
	
OutputGUI(void): void → Xuất dữ liệu dạng GUI (đây là yêu cầu 3)

**Yêu cầu 4 và 5 thiết kế sau, vẫn chưa hình dung được yêu cầu 4 và 5 thiết kế ra sao. Yêu cầu 5 chắc phải thiết kế 1 lớp trung gian riêng để giao tiếp các máy với nhau**


## Lớp Goods sẽ có các thuộc tính và phương thức sau:

1. Thuộc tính: private

_row, _col, _size, _price có kiểu là int, trong đó _row, _col là toạ độ theo dòng và theo cột của kiện hàng trong, _size là kích thước kiện hàng (1 hoặc 2), _price là đơn giá kiện hàng.
	
_id có kiểu là String, đại diện cho mã kiện hàng.
	
_importDate có kiểu là DateTime (một kiểu dữ liệu trong C# được dùng để lưu ngày tháng năm), đại diện cho ngày nhập kho.

2. Phương thức: public → Cái này có thể chỉnh sửa lại cho phù hợp

Khởi tạo: mặc định, kèm theo đó là 1 loạt các phương thức set. Khi đó việc khởi tạo sẽ như thế này: Goods dummy = (new Goods).setRow(dummyRow)....

Các hàm xuất thông tin get. VD: int Goods.getX, …

### Tạm thời cứ theo mấy cái này, sau này sẽ bổ sung vào sau, nếu có vấn đề. Đặc biệt cần phải giải quyết gấp các vấn đề in đậm ở trên.
