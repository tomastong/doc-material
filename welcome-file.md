
### 这两天在看vue的源码，发现作者定义映射字典的时候，喜欢用Object.create(null)，而不是直接定义一个对象字面量，那么两者有什么区别呢，又存在什么业务场景呢

```js
   let m = Object.create(null);
   let n = {};
   
   // 猜测下，m和n有什么区别呢
   console.log(m);
   console.log(n);
```

![](https://user-gold-cdn.xitu.io/2018/12/7/16787f0ca4685a80?w=598&h=228&f=png&s=22085)
> 就是一个纯粹的空对象

![](https://user-gold-cdn.xitu.io/2018/12/7/16787f1724f0f243?w=906&h=618&f=png&s=126761)
> 继承了对象原型的空对象，也就是说存在n.toString();
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTU0MDIzNDk3Ml19
-->