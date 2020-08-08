# js operator

[MDN介绍](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Optional_chaining)

## Optional chaining(?.)

> obj?.prop<br/>
> obj?.[expr]<br/>
> arr?.[index]<br/>
> func?.(args)

```js

let user = {
    adderss: 'shen zhen'
};

let ant = user && user.name;

```


当有了 `optional chaining` 之后，可以这样操作

```js

let ant = user ?. name;

```

#### 使用 `optional chaining` 与函数调用

```js

function doSomething(onError){
    try {
        // ...
    } catch (err) {
        onError?.();
    }
}

```

#### 表达式

```js

let prop = obj?.['prop' + 'Name'];

```


#### 数组

```js

let arrItem = arr?.[42];

```



## 