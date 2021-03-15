<template class="item">
    <li  class="item">
        <slot name="item"></slot>
    </li>
</template>

<script>
export default {
    props: ['item']
}
</script>

<style>  
    .item {
        color: red;
    }
</style>