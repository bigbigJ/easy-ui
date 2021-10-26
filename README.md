##  easy-ui

> easy-ui 是利用VUE框架、JS、LESS等前端技术自主开发的一个私有的前端组件库，采用统一的安装和调用方式

###  安装
> npm install easy-ui -S

###  引入 easy-ui
你可以引入整个 easy-ui，或是根据需要仅引入部分组件。我们先介绍如何引入完整的 easy-ui。

#### 完整引入：

在 main.js 中写入以下内容：

```javascript
import Vue from 'vue'
import easyui from 'easy-ui'
import 'easy-ui/lib/theme/index.css'
Vue.use(easyui)
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
        "libraryName": "easy-ui",
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
import {Button, Select} from 'easy-ui'

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
} from 'easy-ui'

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
<ea-button></ea-button>
```
