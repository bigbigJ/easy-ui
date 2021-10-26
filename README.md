##  下载此组件包请联系管理员

##  mgn-ui

> mgn-ui 是迈基诺前端团队利用VUE框架、JS、LESS等前端技术自主开发的一个私有的前端组件库，采用统一的安装和调用方式，其涵盖了迈基诺所有IT项目中用到的前端组件，分为PC端组件、H5端组件、小程序组件等，每端又详细划分了特殊业务定制组件以及共用组件，详细API查看和使用方式请访问迈基前端网站

##  mgn-ui API
组件API详情请查看： [迈基诺前端网站](https://192.168.0.79/mygenofe/web/#/login)

###  安装
> npm install mgn-ui -S

###  引入 mgn-ui
你可以引入整个 mgn-ui，或是根据需要仅引入部分组件。我们先介绍如何引入完整的 mgn-ui。

#### 完整引入：

在 main.js 中写入以下内容：

```javascript
import Vue from 'vue'
import mgnui from 'mgn-ui'
import 'mgn-ui/lib/theme/index.css'
Vue.use(mgnui)
```
#### 按需引入：

借助 babel-plugin-component，我们可以只引入需要的组件，以达到减小项目体积的目的。

首先，安装 babel-plugin-component：

```javascript
npm install babel-plugin-component -D
```
然后，将 .babelrc (cli3则是babel.config.js) 修改为：

```javascript
{
  "presets": [{ "modules": false }]],
  "plugins": [
    [
      "component",
      {
        "libraryName": "mgn-ui",
        "styleLibrary": {
          "name": "theme",
          "base": false
        }
      }
    ]
  ]
}
```
接下来，如果你只希望引入部分组件，比如 Button 和 Select，那么需要在 main.js 中写入以下内容：

```javascript
import Vue from 'vue'
import {Button, Select} from 'mgn-ui'

Vue.component(Button.name, Button)
Vue.component(Select.name, Select)
/* 或写为
 * Vue.use(Button)
 * Vue.use(Select)
 */
```
完整组件列表和引入方式

```javascript
import Vue from 'vue'
import {
  AnchorNav,
  Avatar,
  Backtop,
  Badge,
  BlurSearch,
  Breadcrumb,
  Button,
  Card,
  Cascader,
  Checkbox,
  ClientDialog,
  Collapse,
  ComplexSearch,
  DateTimePicker,
  Dialog,
  Drawer,
  Dropdown,
  Echarts,
  FixNav,
  Icon,
  Info,
  Input,
  InputNumber,
  ItemSearch,
  Lamp,
  List,
  Loading,
  Menu,
  MultipleLines,
  Page,
  Popover,
  Preview,
  Progress,
  Radio,
  Rate,
  ReportUpload,
  Select,
  Slider,
  Steps,
  Swiper,
  Switch,
  Table,
  Tabs,
  Tag,
  Timeline,
  Title,
  Tooltip,
  Transfer,
  Tree,
  Upload,
  VerticalTable,
  Message,
  MessageBox,
  Notice
} from 'mgn-ui'

Vue.use(AnchorNav)
Vue.use(Avatar)
Vue.use(Backtop)
Vue.use(Badge)
Vue.use(BlurSearch)
Vue.use(Breadcrumb)
Vue.use(Button)
Vue.use(Card)
Vue.use(Cascader)
Vue.use(Checkbox)
Vue.use(ClientDialog)
Vue.use(Collapse)
Vue.use(ComplexSearch)
Vue.use(DateTimePicker)
Vue.use(Dialog)
Vue.use(Drawer)
Vue.use(Dropdown)
Vue.use(Echarts)
Vue.use(FixNav)
Vue.use(Icon)
Vue.use(Info)
Vue.use(Input)
Vue.use(InputNumber)
Vue.use(ItemSearch)
Vue.use(Lamp)
Vue.use(List)
Vue.use(Loading)
Vue.use(Menu)
Vue.use(MultipleLines)
Vue.use(Page)
Vue.use(Popover)
Vue.use(Preview)
Vue.use(Progress)
Vue.use(Radio)
Vue.use(Rate)
Vue.use(ReportUpload)
Vue.use(Select)
Vue.use(Slider)
Vue.use(Steps)
Vue.use(Swiper)
Vue.use(Switch)
Vue.use(Table)
Vue.use(Tabs)
Vue.use(Tag)
Vue.use(Timeline)
Vue.use(Title)
Vue.use(Tooltip)
Vue.use(Transfer)
Vue.use(Tree)
Vue.use(Upload)
Vue.use(VerticalTable)
Vue.use(Message)
Vue.use(MessageBox)
Vue.use(Notice)
```

使用示例

```html
<mgn-button></mgn-button>
```




###  版本说明
[1.0.0 ---------------------------------------------- 发布组件共29个，涵盖云平台所有的组件](https://192.168.0.79/mygenofe/web/#/pcUpdate?nav=0&pIdex=1&chIndex=-1&version=100)

[1.0.1 ---------------------------------------------- 发布组件共35个，涵盖云平台所有的组件，新增：tree、breadcrumb、reportUpload、steps、progress、menu等6个组件](https://192.168.0.79/mygenofe/web/#/pcUpdate?nav=0&pIdex=1&chIndex=-1&version=101)

[1.0.2 ---------------------------------------------- 发布组件共36个，涵盖云平台所有的组件，新增：upload、dateTimePicker等2个组件，修复：notice、message、input、upload、select、page、itemSearch组件问题，解决tree性能问题](https://192.168.0.79/mygenofe/web/#/pcUpdate?nav=0&pIdex=1&chIndex=-1&version=102)

[1.0.3 ---------------------------------------------- 发布组件共37个，涵盖云平台所有的组件，新增：timeline组件，修复：dateTimePicker select、page、itemSearch、complexSearch等组件问题，优化：input、table、collapse、dialog、radio、upload、progress组件](https://192.168.0.79/mygenofe/web/#/pcUpdate?nav=0&pIdex=1&chIndex=-1&version=103)

[1.0.4 ---------------------------------------------- 发布组件共42个，涵盖云平台所有的组件，新增：avatar组件，messageBox组件、card组件、switch、cascader组件 修复menu、avatar、dialog、tabs、dateTimePicker、verticalTable、select、itemSearch、complexSearch、radio、checkbox、tooltip、list、info、blurSearch组件问题](https://192.168.0.79/mygenofe/web/#/pcUpdate?nav=0&pIdex=1&chIndex=-1&version=104)

[1.0.5 ---------------------------------------------- 发布组件共42个，涵盖云平台所有的组件，修复input、select、itemSearch、dateTimePicker组件问题](https://192.168.0.79/mygenofe/web/#/pcUpdate?nav=0&pIdex=1&chIndex=-1&version=105)

[1.0.6 ---------------------------------------------- 发布组件共55个，涵盖云平台所有的组件，新增transfer、inputNumber、rate、slider、badge、drawer、swiper、backtop、fixnav、lamp、multiplelines、anchornav、editor组件，修复list、vertiacltable、menu、avatar、page、upload、button、dropdown、title、card、reportUpload、switch、progress、blursearch、breadcrumb组件问题](https://192.168.0.79/mygenofe/web/#/pcUpdate?nav=0&pIdex=1&chIndex=-1&version=106)

[1.0.7 ---------------------------------------------- 组件npm包整体架构调整，实现按需加载，表格组件内嵌到npm包中](https://192.168.0.79/mygenofe/web/#/pcUpdate?nav=0&pIdex=1&chIndex=-1&version=107)