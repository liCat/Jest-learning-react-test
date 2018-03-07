# React-learning-demo

## 使用方式

1. 克隆代码
2. npm i 安装依赖
3. 切换到特定分支
4. npm run dev

## 分支对应

- 初始代码  ---  begining
- 开发环境配置  ---  configuration
- render & JSX  ---  configuration
- 组件化 --- component
- 事件绑定  --- event-binding
- 列表  ---  list
- props  ---  props
- state  ---  state
- 组件间通信  ---  message-passing
- refs & DOM  ---  master
- 生命周期  --- master

## 各阶段操作

### 开发环境配置
1. tnpm i 安装依赖
2. 安装 babel 编译环境 `npm i babel-core babel-loader babel-preset-es2015 babel-preset-react --save-dev`
3. 安装 react 依赖 `npm i react react-dom --save`
4. 配置 `webpack.config.js`, 在 `module` 里的 `rules` 字段增加 `babel` 编译配置

```js
  {
    test: /\.jsx?$/,
    exclude: /node_modules/,
    use: {
        loader: 'babel-loader',
        options: {
            presets: ['es2015', 'react']
        }
    }
  }
```

5. `npm run dev` 看效果

### 组件化

- 演示一：在 index.js 增加 Input 组件 代码，在 style.css 加上 css 代码
- 演示二：增加 input 目录，把 Input 相关的代码都移进去

### 事件绑定

- 演示1: 添加事件绑定（没有 bind this）
- 演示2：添加 bind this

### list

1. 增加 fruits.js
2. 增加 list 目录，添加 List 组件代码
3. 修改 index.js
4. 给 li 增加 key 属性

### props

1. 增加 Item 组件
2. 修改 List 组件，引用 Item，并且通过 props 传递 item 属性

### state

1. 修改 `item/index.js` ，增加 state 属性和点击事件
2. 修改 `item/index.css`，增加点击后样式

### 组件间通信

1. 修改 `index.js`，增加 `keyword` state 属性， 增加 `onChange` 方法，并且传给 Item 组件
2. 修改 `item/index.js`，调用 onChange 回调
3. 修改 `index.js`, 将 `keyword` 属性传给 List 组件
4. 修改 `list/index.js`，根据 `keyword` 属性筛选列表

### refs 
1. 修改 `input/index.js`，给 `input` 标签增加 ref 属性
2. 增加 `componentDidMount` 方法，运行 `this.input.focus()`

### 生命周期
增加其他生命周期函数，console 出其调用的顺序
