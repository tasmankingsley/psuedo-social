<script setup>
import { transformVNodeArgs } from 'vue';



let posts = [
    {post_id: 1, username: 'tasman', content: 'This is the 1st post'},
    {post_id: 2, username: 'tasman', content: 'This is the 2nd post'},
    {post_id: 3, username: 'tasman', content: 'This is the 3rd post'},
    {post_id: 4, username: 'tasman', content: 'This is the 4th post'},
    {post_id: 5, username: 'tasman', content: 'This is the 5th post'},
    {post_id: 6, username: 'tasman', content: 'This is the 6th post'}
]


</script>

<template>
    <div class="feed-container" v-for="item in posts">
        <div class="post-div">
            <div class="profile"></div>
            <span><b>{{item.username}}</b>@{{item.username}}</span>
            <span>{{item.content}}</span>
        </div>

    </div>
    <!-- <div class="ghost-div"></div> -->
</template>

<style scoped>
.feed-container {
    background-color: #000;
    border-left: #303443 1px solid;
    border-right: #303443 1px solid;
    border-bottom: #303443 1px solid;
    height: 100%;
    width: 700px;
    text-align: center;
    margin: auto;
}

.post-div {
    height: auto;
    width: 100%;
    display: grid;
    grid-auto-flow: row;
    text-align: left;
    /* border-bottom: #303443 1px solid; */
    font-size: 1.2rem;
    padding: 20px;
}

.profile {
    width: 60px;
    height: 60px;
    border-radius: 50%;
    background-color: #fff;
}

.ghost-div {
    height: 50px;
    width: 100%;
    background-color: #0c0c12;
}


</style>