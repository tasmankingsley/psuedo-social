<script setup>
import { store } from './store';

function toggle_menu() {
    if(store.menu_width === 300){
        store.menu_width = 0;
    }
}
</script>

<template>
<transition>
    <div class="menu" v-if="store.menu_width === 300">
        <div class="menu_options">
            <!-- <span @click="toggle_menu">x</span> -->
            <span>Home</span>
            <span>Explore</span>
            <span>Notifications</span>
            <span>Messages</span>
            <span>Profile</span>
            <span>Settings</span>
        </div>
    </div>
</transition>
</template>

<style scoped>
.menu {
    font-size: 1.5rem;
    background-color: #0c0c12;
    color: #3658a6;
    position: fixed;
    width: 369px;
    height: 100%;
    top: 50px;
    transition: width 0.3s;
    z-index: 3;
}

.v-enter-active,
.v-leave-active {
  transition: all 0.3s ease;
}
.v-enter-from,
.v-leave-to {
  opacity: 0;
  transform: translateX(-200px);
}
.menu_options {
    display: grid;
    grid-auto-flow: row;
    grid-template-rows: repeat(7, 100px);
    background-color: #0c0c12;
    /* gap: 20px 0; */
    /* text-align: left; */
}

span {
    line-height: 100px;
    cursor: pointer;
    width: 100%;
    height: 100%;
    text-align: left;
    text-indent: 25%;
    /* text-justify: distribute; */
    /* border-bottom: #fff 1px solid; */
}

span:hover {
    background-color: #fff;
}

</style>