<template>
    <div>
        <div class="tweet" v-for="tweet in tweets" :key="tweet.id">
        <p class="userName">{{userName}}</p>
        <p>{{tweet.content}}</p>
        </div>        
        
    </div>
</template>
<script>
export default {
    name:'TweetSection',
    props:{
        userName:{
            type:String,
            required:true
        },
        tweets:{
            type:Object,
            required:true
            }
    }
    
}
</script>
<style lang="scss" scoped>
.tweet{
    .userName{
    font-weight: bold;
    }
    padding: 15px;
    margin: 20px 30px;
    margin-top:0 ;
    background-color: white;
    border-radius: 5px;
    border: 1px solid #DFE3E8;
    box-sizing: border-box;
    cursor: pointer;
    transition: all 0.25s ease;
    &:hover {
    transform: scale(1.1, 1.1);

    }
}
</style>
