# ES6

* Cheatsheet: [ES6 Cheatsheet](https://github.com/DrkSephy/es6-cheatsheet)
* Coding style: [airbnb](https://github.com/airbnb/javascript)

## Variable

* Sử dụng `let` và `const` thay cho `var`
* Sử dụng code ES6

> _Ý nghĩa: _`let`_ và _`const`_ sử dụng hợp lý sẽ giúp tránh dư thừa bộ nhớ và giúp code trở nên chặt chẽ với ES6_

## Function

* Các class chứa nhiều hơn 10 function xử lý nên được chia nhỏ ra thành nhiều file rồi import vào file `index.js`

Ex: `index.js`

```js
const Function1 = require('./Function1');
const Function2 = require('./Function2');
module.exports = {
    Function1,
    Function2
}
```

> _Ý nghĩa: Giúp cho việc chia nhỏ các block code_

* Các function nên được import trực tiếp vào khi sử dụng

> _Ý nghĩa: Giúp cho việc _`develop`_ mà _`maintain`_ dễ ràng hơn nhờ tính năng _`Go to definition`_ và _`Auto suggestion`_ của Editor._



