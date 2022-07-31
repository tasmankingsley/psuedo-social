<script setup>
import { store } from './store';

function toggle_menu() {
    if (store.menu_width === 0){
        store.menu_width = 300;
    }
}
</script>

<template>
    <div class="top">
        <span class="menu" @click="toggle_menu">menu</span>
        <span>feed</span>
    </div>

    <!-- <div class="bottom">
        <span>bottom tabs</span>
    </div> -->

</template>

<style scoped>
div {
    font-size: 1.5rem;
    background-color: #0c0c12;
    color: #f9f9f9;
    position: sticky;
    width: 100%;
    height: 50px;
    line-height: 50px;
}

.top {
    top: 0px;
}

.bottom {
    bottom: 0px;
    position: fixed;
}

.menu {
    left: 10px;
    position: absolute;
}

span {
    cursor: pointer;
}

</style>