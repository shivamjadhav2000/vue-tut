<template>
    <div id="Navbar">
        <p>Twitter</p>
        <p>{{UserName}}</p>
    </div>
</template>
<script>

export default {
    name:"Navbar",
    props:{
        UserName:{
            type:String,
            required:true
        }
    }

}
</script>
<style lang='scss' scoped>
#Navbar{
    background: rgb(245, 65, 155);
    color: white;
    height: 50px;
    
    border: 1px solid rgb(245, 65, 155);
    display: flex;
    justify-content: space-between;
    padding: 0 2%;
}
</style>
