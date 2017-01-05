#DMP 网站 UI 套件
>适用于数据管理平台的 UI 套件

---
## 1 命名规范
---
### 1.1 WEB组件规范
### 1.2 JS/jQuery 规范
### 1.3 HTML/CSS 规范
####1.3.1 基本原则
* 以 `dmp` 为命名空间
* 命名注意事项
    1. 模块语义化

    如 dmp-tab、dmp-nav，不要使用 red、left 等表象的词命名
    2. 模块状态： {命名空间}-{模块名}-{状态描述}
    
    常用状态有：hover, current, selected, disabled, focus, blur, checked, success, error 等
    3. 子模块： {命名空间}-{模块名}-{子模块名}

    常用模块名有：bd(body)，cnt(content)，hd(header)，text(txt)，img(images/pic)，title，item，cell 等， 词义表达组件要实现的功能。
* 模块内部的类名继承自父级
```
<div class="dmp-box">
    <div class="dmp-box-head">

    </div>
    <div class="dmp-box-body">

    </div>
</div>
```
* 在与 JS 代码交互时,所有状态代码添加至父级 dom 中,减少交互操作,提高性能.
```
// 建议填写使用以下方式
<div class="dmp-box dmp-box-active">
    <div class="dmp-box-head">

    </div>
    <div class="dmp-box-body">

    </div>
</div>
```
```
// 不建议使用以下方式
<div class="dmp-box">
    <div class="dmp-box-head dmp-box-head-active">

    </div>
    <div class="dmp-box-body">

    </div>
</div>
```

* 不要添加任何浏览器兼容前缀,一律使用`Autoprefixer`自动添加前缀.

---
## 2 代码规范
---