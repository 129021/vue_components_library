# 快速开始
#### 安装组件库


```bash
npm i something-ui
```

#### 引用组件库
> 在main.js中引用组件库

```javascript
//全部引用
import 'something-ui/dist/css/index.css';
import SUI from 'something-ui';
Vue.use(SUI);

按需引用
import 'mooc-ui/dist/css/demo.css';
import { Demo } from 'something-ui';
Vue.use(Demo);
```
