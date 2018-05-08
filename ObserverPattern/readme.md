### Usage

##### 1、引入库文件

```javascript
import ObserverPattern from './ObserverPattern'
```

##### 2、实例化观察者和目标对象模型

```javascript
// 实例化观察者和目标模型
let observer = new ObserverPattern.Observer();
let subject = new ObserverPattern.Subject();
```

##### 3、定义一个目标对象并扩展

```javascript
let sub12oclock = {
    name: '我是12点的主题事件目标'
};

// 扩展目标对象
ObserverPattern.extend(subject, sub12oclock);
```

##### 4、定义观察者对象并扩展

```javascript
let peikizhuObs = {
    name: 'Pikeizhu'
}

// 扩展观察者对象
ObserverPattern.extend(observer, peikizhuObs);
peikizhuObs.update = function (ctn){
    console.log("I'm " + this.name + ' 我订阅了一个12点要干的事情：' + ctn);
}

// 添加目标对象的观察者
sub12oclock.addObserver(peikizhuObs);

let pikachuObs = {
    name: 'Pikachu'
}

// 扩展观察者对象
ObserverPattern.extend(observer, pikachuObs);
pikachuObs.update = function (ctn){
    console.log("不一样的自我介绍：我是 " + this.name + ' 我订阅了一个12点要干的事情：' + ctn);
}

// 添加目标对象的观察者
sub12oclock.addObserver(pikachuObs);
```

##### 5、目标对象通知观察者对象内容事件

```javascript
// 12点钟声敲响，通知所有的观察者
sub12oclock.notify('大家去吃午餐～');
```



### Effect

![2F2400B1-1A91-436A-B272-11AA9290C709](/Users/qiudw/Library/Containers/com.tencent.eimmac/Data/Library/Application Support/QQ/Users/2880968557/QQ/Temp.db/2F2400B1-1A91-436A-B272-11AA9290C709.jpg)

