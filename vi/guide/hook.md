# Hooks

- Xử lý các validate nên được thực hiện ở `before` hook trước khi chạy vào hàm xử lý trong controller

Ex:
```js
const authentication = require('feathers-authentication');
const userPolicy = require('./policy/user.policy');
const authenticationHook = [authentication.hooks.authenticate('jwt'), userPolicy];
module.exports = {
    before: {
        all: [...authenticationHook],
        find: [],
        get: [],
        create: [],
        update: [],
        patch: [],
        remove: []
    }
};
```
>*Ý nghĩa: Giúp cho việc xử lý logic trở nên tường minh và chặt chẽ hơn.*

- Nên bind các giá trị vào mỗi route và có thể lấy ra từ `params`

Ex: url `/room/:roomId/message`

```js
module.exports = {
    before: {
        all: [getSubRoomByRoomId()],
        find: [],
        get: [],
        create: [],
        update: [],
        patch: [],
        remove: []
    }
};

function getSubRoomByRoomId() {
    return function(hook) {
        // Hooks can either return nothing or a promise
        // that resolves with the `hook` object for asynchronous operations
        return SubRoomLogic.get(hook.params.roomId).then(subRoom => {
            if (subRoom === null) {
                throw new NotFound('Room not found');
            }
            hook.params.subRoom = subRoom;
            return hook;
        });
    };
};
```

```js
class Service {

    find(data, params) {
        ...
        // get SubRoom in params
        const { subRoom } = params;
        ...
    }
}
```
>*Ý nghĩa: Giúp cho việc xử lý dữ liệu phía controller trở nên dễ dàng hơn đồng thời cũng validate exists.*

- Sử dụng các build-in hook của Feathersjs tại địa chỉ

[https://docs.feathersjs.com/api/hooks-common.html](https://docs.feathersjs.com/api/hooks-common.html)
