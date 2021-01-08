# cnr_miniapp

## Project setup
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn serve
```

### Compiles and minifies for production
```
yarn build
```

### Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).





## components

### counter

用来追加商品数量

| 参数     | 说明                          |
| -------- | ----------------------------- |
| min      | 最小值，若比它还小，那么则为0 |
| max      | 最大值，不能超过最大值        |
| abs      | 默认值                        |
| abs.sync | 实现双向绑定                  |

| 事件    | 说明                         |
| ------- | ---------------------------- |
| changed | 数值发生变化时触发，返回数值 |



### check_box_selector

选择框

| 参数     | 说明             |
| -------- | ---------------- |
| 是否选中 | 让选择框默认选上 |



| 事件    | 说明                               |
| ------- | ---------------------------------- |
| changed | 状态发生改变时触发，返回true、fase |

