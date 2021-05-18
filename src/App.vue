<template>
  <div id="nav">
    <router-link to="/">Home</router-link>
    <router-link to="/user">User</router-link>
    <p>@_ShivamJadhav</p>
  </div>
  <router-view/>
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  a {
    font-weight: bold;
    color: #ffffff;
    text-decoration: none;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
  background: rgb(245, 65, 155);
    color: white;
    height: 50px;
    
    border: 1px solid rgb(245, 65, 155);
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 2%
}
</style>
