# Simple RequireJS

## 机制

RequireJS 使用 head.appendChild() 将每一个依赖加载为一个 script 标签。
RequireJS 等待所有的依赖加载完毕，计算机出模块定义函数正确调用顺序，然后依次调用它们。

## 功能要求

1. require function - 程序入口
2. require.config - 配置模块与路径映射
3. define - 定义各个模块
4. loadScript
5. require.moduleObj - 全局对象，用于存储已经加载好的模块
6. Module - 模块的构造函数

## 框架

```
(function () {

  var Module = function () {
    this.status = 'loading'; //只具有loading与loaded两个状态
    this.depCount = 0; //模块依赖项
    this.value = null; //define函数回调执行的返回
  };


  var loadScript = function (url, callback) {

  };

  var config = function () {

  };

  var require = function (deps, callback) {

  };

  require.config = function (cfg) {

  };

  var define = function (deps, callback) {

  };

})();
```
