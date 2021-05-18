<template>
    <div >
       <div class="mainSection">
           <UserPanel />
           <TweetSection :userName="user.userName" :tweets="user.tweets"/>
           
       </div>
    </div>
</template>
<script>
import TweetSection from './TweetSection';
import UserPanel from './UserPanel';

export default {
    name:'TweeterContainer',
    components:{TweetSection,UserPanel},
    data(){
      return{
        user:{
                id:1,
                userName:"_ShivamJadhav",
                email:'shivamjadhav2000@gmail.com',
                isAdmin:true,
                tweets:[
                  {id:1,content:"twitter is amazing!!"},
                  {id:2,content:"iam a machine learning engineer"},
                  {id:3,content:"twitter is amazing!!"},
                  {id:4,content:"iam a machine learning engineer"}
                ]
            }
      }
    },
    
}
</script>
<style lang="scss" scoped>
.mainSection{
  display: grid;
  grid-template-columns:30% 60% ;
  margin: 50px 0px;
}
</style>
