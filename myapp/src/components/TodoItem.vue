<template class="item">
    <li  class="item">
        <input type="checkbox" v-model="checked">
        <slot name="item"></slot>
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

<style>  
    .item {
        color: red;
    }
</style>