# ES6

- Cheatsheet: [ES6 Cheatsheet](https://github.com/DrkSephy/es6-cheatsheet)
- Coding style: [airbnb](https://github.com/airbnb/javascript)

## Variable

- Sử dụng `let` và `const` thay cho `var`
- Sử dụng code ES6

>*Ý nghĩa: `let` và `const` sử dụng hợp lý sẽ giúp tránh dư thừa bộ nhớ và giúp code trở nên chặt chẽ với ES6*

## Function
- Các class chứa nhiều hơn 10 function xử lý nên được chia nhỏ ra thành nhiều file rồi import vào file `index.js`

Ex: `index.js`
```js
const Function1 = require('./Function1');
const Function2 = require('./Function2');
module.exports = {
    Function1,
    Function2
}
```
>*Ý nghĩa: Giúp cho việc chia nhỏ các block code*

- Các function nên được import trực tiếp vào khi sử dụng

>*Ý nghĩa: Giúp cho việc `develop` mà `maintain` dễ ràng hơn nhờ tính năng `Go to definition` và `Auto suggestion` của Editor.*


