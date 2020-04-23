本项目用来记录unity webgl 平台读取本地图片的实现。
* 思路：通过html能够读取文件。将图片文件转为字符串通过send message发送到unity进行解析。
* 缺点：
    * html input标签还没有找到使用代码来打开文件选择对话框的方法。
    * webgl全屏会将除去 画布之外的body标签内的内容隐藏掉，即使在style里面设置很大的z-index也不行。
* 实现： 通过定制webgl模板文件，将js代码添加到webgl页面，通过 application.ExternCall来调用便可。