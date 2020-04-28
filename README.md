## 改动：
搜索fixed by huangliangxing即可看到改动点：
+ 1、updateDataToMP时通过diff进行数据增量更新（这里copy了uni-app中mpvue的diff算法）
+ 2、initDataToMP将数据深拷贝
+ 3、初始化页面时，仅执行最顶层的父组件的onLoad事件；去除VueComponent子组件的onLoad事件，统一使用mounted来进行组件初始化事件。
