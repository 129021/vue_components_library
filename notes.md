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
## 1.3. 
