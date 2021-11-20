# 使用方法

```node
npm install libero-tools --save
or
yarn add libero-tools --save
```

## 1. equals
> 比较两个值是否相等
```js
    import { equals } from 'libero-tools';

    const a = {a:1}, b = {a:1};
    equals(a,b); // true
```

## 2. onClickSide
> 点击`container`之外的地方返回false,点击包括`container`的地方返回`true`
```js
    import { onClickSide } from 'libero-tools';

    const container = document.getElementById('container');
    window.addEventListener("click", (e) => {
      onClickSide(container,e.target, (bo) => {
        console.log(bo); // true or false
      });
    });
```