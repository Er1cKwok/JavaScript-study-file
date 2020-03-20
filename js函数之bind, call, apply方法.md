### js函数之bind方法
```
var obj = {
  firstName: 'Eric',
  getName: function() {
    return this.firstName;
  }
};

var unbindGetName = obj.getName;
console.log(unbindGetName());  // undefined

var boundGetName = unbindGetName.bind(obj);
console.log(boundGetName());  // "Eric"
```

### js函数之call方法
```
function People(name, age) {
  this.name = name;
  this.age = age;
}

function Webber(name, age, job) {
  People.call(this, name, age);
  this.job = job;
}
var w1 = new Webber('Eric', 25, 'programmer');

console.log(w1.name, w1.age, w1.job); // "Eric" 25 "programmer"
```

### js函数之apply方法

#####注意：call()方法的作用和 apply() 方法类似，区别就是call()方法接受的是参数列表，而apply()方法接受的是一个参数数组。