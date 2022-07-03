# 1. vue UI组件库开发流程
## 1.1. 创建项目
使用vue-cli创建vue项目
```js
vue create something-ui
```
## 1.2. 修正项目结构
1. 删除项目自带的hello world组件
2. UI组件库的主要代码将会放在components文件夹下，所以将components提到根目录下
3. 将src文件夹更名为examples，以防产生误会
4. 因为src的名称的修改，所以要在`vue.config.js`中重新配置一下：
    ```js
    module.exports={
        pages:{
            index:{
                entry:'examples/main.js',
                template:'public/index.html',
                filename:'index.html'
            }
        }
    }
    ```
## 1.3. sass的安装与使用
### 安装
1. 将node.js版本改为14.18.0
   1. 卸载当前node.js
   1. 安装node管理软件nvm.exe 地址：https://github.com/coreybutler/nvm-windows/releases
   2. nvm安装完成后控制台输入nvm v出现版本号说明安装成功
   3. nvm ls available查看可用node版本
   4. nvm install 14.18.0 安装指定版本node.js
   5. nvm use 14.18.0使用指定版本
   6. node -v，npm-v查看版本号
2. 安装sass-loader@7
3. 安装sass@7
4. 安装node-sass@4

## 1.4. 创建一个demo组件

一个demo组件要有自己的结构和样式
结构放在`lib/demo/src/main.vue`中
样式放在`css/demo.scss`中


demo组件要在main.js中注册并在App.vue中使用

其中在注册的时候一个组件的使用方法是用
```js
import '../components/css/demo.scss'
import Demo from  '../components/lib/demo/index.js'

Vue.use(Demo)
```
这里直接使用`Vue.use()`是不行的，因为`Vue.use()`在执行的时候是调用的`install()`方法，在`install()`方法中执行了`Vue.component()`方法

所以只要在一个适当的位置（比如`components/lib/demo/index.js`中）写一下Demo.install方法就好了：
```js
Demo.install=function (Vue) {
    Vue.component(Demo.name,Demo)
}
```

这样我们就可以像使用UI组件库一样使用这个Demo组件了

今天没干活，明天要认真干活了


