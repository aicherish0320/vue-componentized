# Vue 组件化开发、组件库

## 处理组件的边界情况

- $root：访问根实例
- $parent/$children：父组件、子组件
- $refs：子组件
- 依赖注入 provide/inject
- $attrs
  - 把父组件中非 prop 属性绑定到内部组件
- $listeners
  - 把父组件中的 DOM 对象的原生事件绑定到内部组件

## 快速原型开发

- VueCLI 中提供了一个插件可以进行原型快速开发
- 需要先额外安装一个全局的扩展
  - `npm install -g @vue/cli-service-global`
- vue serve
  - vue serve 如果不指定参数默认会在当前目录找一下的入口文件
    - main.js index.js App.vue app.vue
  - 可以指定要加载的组件
    - vue serve ./src/login.vue
- 安装 ElementUI
  - 初始化 package.json
  - npm init -y
  - 安装 ElementUI
    - vue add element
  - 加载 ElementUI，使用 Vue.use() 安装插件

## 组件开发

### 组件分类

- 第三方组件
  - Element、IView
- 基础组件
  - 文本框、按钮、表单组件
- 业务组件
  - 结合特定的行业使用场景的组件、可以根据用户的行为输出特定的页面展示给用户

### 表单组件

- Form
- FormItem
- Input
- Button

#### Input 组件验证

- Input 组件中触发自定义事件 validate
- FormItem 渲染完毕注册自定义事件 validate

## Storybook

- 可视化的组件展示平台
- 在隔离的开发环境中，以交互式的方式展示组件
- 独立开发组件
- 支持的框架
  - React、Vue、Angular

### Storybook 安装

- 自动安装
  - `npx -p @storybook/cli sb init --type vue`
  - `yarn add vue`
  - `vue yarn add vue-loader vue-template-compiler --dev`

## Monorepo

### 两种项目的组织方式

- Multirepo(Multiple Repository)
  - 每一个项目对应一个项目
- Monorepo(Monolithic Repository)
  - 一个项目仓库中管理多个模块/包

## 基于模板生成包的结构

## lerna + yarn workspaces

### lerna 介绍

- lerna 是一个优化使用 git 和 npm 管理多包仓库的工作流工具
- 用于管理具有多个包的 JavaScript 项目
- 它可以一键把代码提交到 git 和 npm 仓库

### 使用

- 全局使用
  - `yarn global add lerna`
- 初始化
  - `lerna init`
- 发布
  - `lerna publish`

### yarn workspaces

#### 开启 yarn 的工作区

- 项目根目录的 package.json

```js
  "private": true,
  "workspaces": [
    "packages/*"
  ]
```

#### yarn workspaces 使用

- 给工作区根目录安装开发依赖
  - `yarn add jest -D -W`
- 给指定工作区安装依赖
  - `yarn workspace ac-button add lodash@4`
- 给所有工作区安装依赖
  - `yarn install`

## 组件测试

### Vue 组件的单元测试

#### 好处

- 提供描述组件行为的文档
- 节省手动测试的时间
- 减少研发新特性时产生的 bug
- 改进设计
- 促进重构

> `Vue Test Utils`、`Jest`、`vue-jest`、`babel-jest`、

## Rollup 打包
