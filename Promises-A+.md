# Promises/A+
**这是实施者为实施者提供的一个开源且共同操作的JavaScript promises规范。**

一个promise代表一个异步操作的最终结果。promise相互影响的主要方式是是通过其then方法，该方法注册者通过回调会收到promise的最终结果或者一个不能完成promise的理由。

本规范详细列出了then的行为，它可以依赖所有符合Promises / A +的promise实现来提供可互操作的基础库。