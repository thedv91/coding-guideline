# Query

- `Query` nên được viết riêng rẽ phục vụ cho business logic của dự án
- Các `Logic` có nhiều hơn 10 `Function` nên chia ra thành các file nhỏ, mỗi file là 1 Function rồi import vào `index.js`
- Các `options` hoặc `params` trong query nên có giá trị mặc định
