三、 构造函数模式
为了解决从原型对象生成实例的问题，Javascript提供了一个构造函数（Constructor）模式。
所谓"构造函数"，其实就是一个普通函数，但是内部使用了this变量。对构造函数使用new运算符，就能生成实例，并且this变量会绑定在实例对象上。

<pre>
    function Cat(name,color){
　　　　this.name=name;
　　　　this.color=color;
　　}
</pre>
我们现在就可以生成实例对象了。
<pre>
    var cat1 = new Cat("大毛","黄色");
　　var cat2 = new Cat("二毛","黑色");
　　alert(cat1.name); // 大毛
　　alert(cat1.color); // 黄色
</pre>
这时cat1和cat2会自动含有一个constructor属性，指向它们的构造函数

<pre>
    alert(cat1.constructor == Cat); //true
　　alert(cat2.constructor == Cat); //true
</pre>

Javascript还提供了一个instanceof运算符，验证原型对象与实例对象之间的关系。

<pre>
    alert(cat1 instanceof Cat); //true
　　alert(cat2 instanceof Cat); //true
</pre>
