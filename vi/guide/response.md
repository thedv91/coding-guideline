# Response

### Lọc dữ liệu trước khi trả về cho client

Khuyến cáo dùng 2 cách sau:

- Cách 1: Loại bỏ những giá trị không cần thiết từ dữ liệu trả về sử dụng BaseDTO trong model
- Cách 2: Chỉ lấy những giá trị cần thiết theo pattern schema đã định nghĩa

__*Ưu điểm*__

Cách 1: Khi có thêm hoặc sửa dữ liệu trong Model thì cũng sẽ không lo lắng việc trả về thiếu dữ liệu

Cách 2: Chỉ lấy về đúng các trường theo định nghĩa, tránh việc không may có dữ liệu nhạy cảm được lấy về

__*Nhược điểm*__

Cách 1: Sẽ khó khăn trong việc lọc và loại bỏ dữ liệu lồng nhau

Cách 2: Khi Model thay đổi thì pattern schema cũng phải thay đổi theo

