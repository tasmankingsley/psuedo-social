<script setup>
import Post from './Post.vue'

let posts = [
    {post_id: 1, username: 'tasman', content: 'This is the 1st post, This is the 1st post, This is the 1st post, This is the 1st post, This is the 1st post'},
    {post_id: 2, username: 'tasman', content: 'This is the 2nd post'},
    {post_id: 3, username: 'tasman', content: 'This is the 3rd post'},
    {post_id: 4, username: 'tasman', content: 'This is the 4th post'},
    {post_id: 5, username: 'tasman', content: 'This is the 5th post'},
    {post_id: 6, username: 'tasman', content: 'This is the 6th post'},
    {post_id: 7, username: 'tasman', content: 'This is the 7th post'},
    {post_id: 8, username: 'tasman', content: 'This is the 8th post'},
    {post_id: 9, username: 'tasman', content: 'This is the 9th post'},
    {post_id: 10, username: 'tasman', content: 'This is the 10th post'}
]


</script>

<template>
    <div class="feed-container">
        <Post/>
        <div class="post-container" v-for="item in posts">
            <div class="post-div">
                <div class="profile"></div>
                <span class="username"><b>{{item.username}}</b>@{{item.username}}</span>
                <span class="content">{{item.content}}</span>
            </div>
        </div>
    </div>
    <!-- <div class="ghost-div"></div> -->
</template>

<style scoped>
.feed-container {
    background-color: #080808;
    border-left: #303443 1px solid;
    border-right: #303443 1px solid;
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
    grid-template-rows: 70px 1fr;
    grid-template-columns: 70px 1fr 1fr;
    text-align: left;
    /* border-bottom: #303443 1px solid; */
    font-size: 1.2rem;
    gap: 10px;
    border-bottom: #303443 1px solid;
}

.profile {
    grid-row: 1;
    grid-column: 1 / 2;
    width: 60px;
    height: 60px;
    border-radius: 50%;
    background-color: #fff;
    margin: 20px;
}

.username {
    grid-row: 1;
    grid-column: 2 / 3;
    line-height: 60px;
    margin: 20px;
}

.content {
    grid-row: 2 span;
    grid-column: 1 / 4;
    margin: 30px;
}

.ghost-div {
    height: 50px;
    width: 100%;
    background-color: #0c0c12;
}


</style>