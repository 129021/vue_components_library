# something-ui 组件库

### 快速开始
#### 1. 安装组件库
```bash
npm i something-ui
```
#### 2. 引用组件库
```javascript
//全部引用
import "something/dist/css/index.css";
import SUI from 'something-ui',
Vue.use(SUI);

//按需引用
import 'something-ui/dist/css/demo.css';
import { Demo } from 'something-ui';
Vue.use(Demo);
```