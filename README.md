## watson

[![NPM version][npm-image]][npm-url]

### 一、简介

基于[dox](https://github.com/tj/dox)的文档生成工具，支持nodejs模块文档生成，以及纯Js结构目录文档生成。
### 二、安装

    npm install watson-doc -g

    或者

    npm install watson-doc --save-dev
    
     
### 三、用例

全局安装模式CLI：

    watson-doc (-t -n -o 参见 命令行参数)

本地安装代码用例：

```js
var watsons = require('watson-doc');

watsons.make({
    loader: 'module', //文件加载方式 目前支持 module 或者 dir
    target: '', //如果loader是module则设置nodejs 模块名称,如果Loader为dir则为目录路径
    ext: '.js$', //过滤文件，默认为.js
    out: './docs', //文档输出目录，
    //pgk 默认读取package.json
    pgk: {
        version: '', //文档版本 在loader为module时自动从package.json中取
        title: '', //文档标题 在loader为module时自动从package.json中取
        repository: null
    }
});
```

### 四、命令行参数解释

* **loader** 文件加载方式 目前支持 module 或者 dir
* **target** 如果loader是module则设置nodejs 模块名称,如果Loader为dir则为目录路径
* **ext**    过滤文件，默认为.js
* **out**    文档输出目录，例如:./docs
* **pgk**    默认读取package.json 具体参见package.json规范
    * **pgk.version** 文档版本
    * **pgk.title** 文档标题
    * **pgk.repository** 版本库

### 五、生成效果

    ![image](https://raw.githubusercontent.com/Beven91/watson-doc/master/screenshots/index.png)
    ![image](https://raw.githubusercontent.com/Beven91/watson-doc/master/screenshots/fun.png)
    ![image](https://raw.githubusercontent.com/Beven91/watson-doc/master/screenshots/source.png)
  

### 六、开源许可
基于 [MIT License](http://zh.wikipedia.org/wiki/MIT_License) 开源，使用代码只需说明来源，或者引用 [license.txt](https://github.com/sofish/typo.css/blob/master/license.txt) 即可。

[npm-url]: https://www.npmjs.com/package/watson-doc
[npm-image]: https://img.shields.io/npm/v/watson-doc.svg