### Usage

##### 1、引入库文件

```javascript
import PubsubPattern from './PubsubPattern'
```

##### 2、订阅事件

```javascript
let peikiToken = pubsub.subscribe("12 o'clock", function(){
    console.log('佩奇猪订阅一个12点事件：继续玩耍！');
});
let pikaToken = pubsub.subscribe("12 o'clock", function(){
    console.log('皮卡丘订阅一个12点事件：要去吃饭！');
});
```

##### 3、发布事件

```javascript
pubsub.publish("12 o'clock");
```

##### 4、取消订阅

```javascript
pubsub.unsubscribe(pikaToken);
```



### Effect

![image](https://github.com/qiudongwei/pattern-struct/raw/master/PubsubPattern/images/ef.jpg)

