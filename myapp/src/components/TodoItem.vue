<template class="item">
    <li  class="item">
        <input type="checkbox" v-model="checked">
        <!--
            作用域插槽的需求：选中和非选中显示不同的颜色
            解决方案：通过子组件TodoItem传递出一些状态供父组件App使用，
                    通过传递出来的状态进一步控制传递的内容
        -->
        <!--1、将checked状态传递出去-->
        <slot name="item" v-bind="{checked}"></slot>
    </li>
</template>

<script>
export default {
    props: ['item'],
    data () {
        return {
            checked: false
        }
    }
}
</script>

<style scoped>  
    .item {
        color: red;
    }
</style>