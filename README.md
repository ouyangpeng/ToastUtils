# 吐司工具类

> 博客地址：[只需体验三分钟，你就会跟我一样，爱上这款Toast](https://www.jianshu.com/p/9b174ee2c571)

> [Toast通知栏权限填坑指南](https://www.jianshu.com/p/1d64a5ccbc7c)

> 已投入公司项目多时，没有任何毛病，可胜任任何需求，[点击此处下载Demo](https://raw.githubusercontent.com/getActivity/ToastUtils/master/ToastUtils.apk)

> 想了解实现原理的可以点击此链接查看：[ToastUtils](https://github.com/getActivity/ToastUtils/blob/master/library/src/main/java/com/hjq/toast/ToastUtils.java) 源码

![](ToastUtils.gif)

#### 集成步骤

    dependencies {
        implementation 'com.hjq:toast:5.0'
    }

#### 初始化Toast

    // 在Application中初始化
    ToastUtils.init(this);

#### 显示Toast

    ToastUtils.show("我是吐司");

#### 获取Toast对象

    ToastUtils.getToast();

#### 设置Toast布局

    ToastUtils.setView();

#### 自定义Toast样式

> 如果对Toast的默认样式不满意，可以在Application初始化样式，具体可参考[ToastBlackStyle](https://github.com/getActivity/ToastUtils/blob/master/library/src/main/java/com/hjq/toast/style/ToastBlackStyle.java)类的实现

    ToastUtils.initStyle(new IToastStyle());

#### 框架亮点

* 无需权限：不管有没有授予通知栏权限都不影响吐司的弹出

* 功能强大：不分主次线程都可以弹出Toast，自动区分资源id和int类型

* 使用简单：只需传入文本，会自动根据文本长度决定吐司显示的时长

* 性能最佳：单例吐司，整个Toast只有一个TextView，并且通过代码创建

* 体验最优：限制Toast短时间内弹出的次数，避免频繁弹出造成不良的用户体验

* 支持多种样式：默认为黑色样式，夜间模式可使用白色样式，还有仿QQ吐司样式

* 支持自定义样式：吐司（背景、圆角、重心、偏移），文字（大小、颜色、边距）

* 支持自定义扩展：支持获取ToastUtils中的Toast对象，支持重新自定义Toast布局

* 支持全局配置样式：可以在Application中初始化Toast样式，达到一劳永逸的效果

* 框架兼容性良好：本框架不依赖任何第三方库，支持Eclipse和Studio的集成使用

#### 关于通知栏权限

> 本框架已经完美解决这个问题（禁用通知栏权限后需要重启应用才能后生效，请以[Demo](https://raw.githubusercontent.com/getActivity/ToastUtils/master/ToastUtils.apk)测试为主）

> 具体解决方案可见：[Toast通知栏权限填坑指南](https://www.jianshu.com/p/1d64a5ccbc7c)

![](issue_taobao.gif)

![](issue_utils.gif)

#### Android技术讨论Q群：78797078

#### 如果您觉得我的开源库帮你节省了大量的开发时间，请扫描下方的二维码随意打赏，要是能打赏个 10.24 :monkey_face:就太:thumbsup:了。您的支持将鼓励我继续创作:octocat:

![](pay_ali.png) ![](pay_wechat.png)

## License

```text
Copyright 2018 Huang Jinqun

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
