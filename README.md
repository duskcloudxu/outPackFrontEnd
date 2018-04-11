Copied from：https://github.com/bailicangdu/vue2-manage
# 服务外包前端界面
It is a management FrontEnd developed from the vue2-manage, maintained by myself as the practice of Vue.js and elementUI.
### 到现在为止做的改动
#### 页面更改
1. 修改了主页的样式
2. 增加了一页document.vue用来展示合同管理界面
3. 对于VueEdit做了一些修改使适应其需求。
 ***
#### 架构更改
将每页的stylesheet用单独的架构存储在~/src/style文件夹下，满足低耦合需求，方便
 进行stylesheet的重用。
### 运行
nodeJS 环境

在项目根目录下运行以下代码安装依赖项
```aidl
npm install
```
安装完毕后，运行以下代码以启动后台服务器
```aidl
npm run dev
```
