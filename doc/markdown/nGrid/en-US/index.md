# Grid栅格

24 栅格系统。

## 基础
从堆叠到水平排列。使用单一的一组 Row 和 Col 栅格组件，就可以创建一个基本的栅格系统，所有列（Col）必须放在 Row 内。

### 代码演示
:::demo
```html
<template>
    <n-row>
        <n-col span="12">
            <div v-bind:style="styleObjectOne">
                12
            </div>
        </n-col>
        <n-col span="12">
            <div v-bind:style="styleObjectTwo">
                12
            </div>
        </n-col>
    </n-row>
    <n-row>
        <n-col span="8">
            <div v-bind:style="styleObjectOne">
                8
            </div>
        </n-col>
        <n-col span="8">
            <div v-bind:style="styleObjectTwo">
                8
            </div>
        </n-col>
        <n-col span="8">
            <div v-bind:style="styleObjectOne">
                8
            </div>
        </n-col>
    </n-row>
    <n-row>
        <n-col span="6">
            <div v-bind:style="styleObjectOne">
                6
            </div>
        </n-col>
        <n-col span="6">
            <div v-bind:style="styleObjectTwo">
                6
            </div>
        </n-col>
        <n-col span="6">
            <div v-bind:style="styleObjectOne">
                6
            </div>
        </n-col>
        <n-col span="6">
            <div v-bind:style="styleObjectTwo">
                6
            </div>
        </n-col>
    </n-row>
</template>
<script>
    export default {
        data: function () {
            return {
                styleObjectOne: {
                    background: `rgba(0, 160, 233, 0.7)` ,
                    color: '#fff',
                    height:'50px',
                },
                styleObjectTwo: {
                    background: `#00a0e9` ,
                    color: '#fff',
                    height:'50px',
                }
            }
        }
    }
</script>
```

:::

### API

#### Row

| 参数 | 说明 | 类型 | 默认值 |
| :--- | :--- | :--- | :--- |
| align | flex 布局下的垂直对齐方式：`top` `middle` `bottom` | String | center |
| gutter | 栅格间隔，可以写成像素值或支持响应式的对象写法来设置水平间隔  | Number/String | - |
| justify    | flex 布局下的水平排列方式：`start` `end` `center` `space-around` `space-between` | String | center |

#### Col
| 参数 | 说明 | 类型 | 默认值 |
| :--- | :--- | :--- | :--- |
| span | 栅格占位格数 | String/Number | - |
| offset | 栅格左侧的间隔格数，间隔内不可以有栅格  | Number/String | - |
