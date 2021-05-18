<template>
    <div class="userPanel-Container">
        <div class="user-profile">
            <p>@{{user.userName}}</p>
            <button  @click="Follow">follow</button>
        </div>
        <div class="user-profile-admin-badge" v-if="user.isAdmin">
            Admin
        </div>
        <div>
            <p>Followers:{{followers}}</p>
        </div>
        <div>
            <textarea rows="4"/>
        </div>
    </div>
</template>
<script>

export default {
    name:'UserPanel',
    data(){
        return {
            followers:0,
            user:{
                id:1,
                userName:"_ShivamJadhav",
                email:'shivamjadhav2000@gmail.com',
                isAdmin:true
            }
        }
    },
    methods:{
        Follow(){
            this.followers=this.followers+1
        }
    }
    
}
</script>
<style lang="scss" scoped>
.userPanel-Container{
    padding:10px;
    margin: 0 10px;
    background: white;
    border-radius:5px ;
    max-height: 300px;
    .user-profile-admin-badge{
        background: rebeccapurple;
        color: white;
        border-radius:5px;
        width: 50px;
        padding: 3px 15px;
        font-weight: bold;
    }
    .user-profile{
        display: flex;
        align-items: center;
        justify-content: space-between;
        button{
            width:80px ;
            background: blue;
            text-decoration: none;
            border: none;
            outline: none;
            padding: 5px 2px;
            color: rgb(255, 255, 255);
            border-radius:5px ;
            font-weight: bold;

        }
    }
}

</style>
