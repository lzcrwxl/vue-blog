# vue + express + mongodb 打造个人博客

> 完全使用ajax交互, 无服务端模版渲染

使用技术:

* 前端
    1. vue
    2. vue-router 前端路由管理
    3. axios 发送ajax请求
    4. stylus css预处理
    5. element-ui 后台管理ui
    6. marked.js 新建文章支持markdown语法
    7. highlight.js 新建文章支持代码高亮

* 后端
    1. express
    2. body-parser 获取post请求内容
    3. cookies cookie处理模块
    4. mongoose 数据库操作模块

* 功能需求

前端:

1. 首页内容聚合
2. 列表页 —— 分类列表
3. 内容页 —— 评论
4. 注册
5. 登录

后台:

1. 登录
2. 分类管理

    * 分类列表
    * 添加分类
    * 修改分类
    * 删除分类
    * 查看分类下的所有博文 (暂未实现)

3. 文章管理

    * 文章列表 : 所有文章;  按分类查看文章 (暂未实现)
    * 添加文章
    * 修改文章
    * 删除文章
    * 查看文章下所有评论(暂未实现)

4. 评论管理 (暂未实现)

    * 评论列表 : 所有评论; 查看指定文章评论
    * 删除评论

5. 移动端适配 (暂未实现)

## 开始

``` bash
# server目录以及vue项目根目录均需npm install
npm install

# 进入mongodb的bin目录启动数据库 (需了解mongodb的初步启动)
mongod --dbpath=E:\project\blog\server\db 

# 进入server目录启动服务端
node app.js

# 启动浏览器端
npm run dev
```

### 注意

1. cookie相关:使用axios碰到的跨域cookie问题
参考:[axios cookie问题和表单上传问题探究](http://blog.csdn.net/hongchh/article/details/72675777)

2. markdown语法支持: marked.js + highlight.js
使用方法可参见源文件 src => pages => admin => markdown.vue 有详细的使用代码
