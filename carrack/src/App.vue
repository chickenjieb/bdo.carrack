<template>
  
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <!-- <router-link to="/about">About</router-link> | -->
      <router-link to="/deer">Balance</router-link> |
      <router-link to="/horse">Advance</router-link> |
      <router-link to="/bird">Volante</router-link> |
      <router-link to="/lion">Valor</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  /* color: #2c3e50; */
  background-color: #222222;
  color:white;
  min-height: 100vh;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
/* jieb custom */
.text-left{
  text-align: left;
}
table#deerTable,
table#horseTable,
table#birdTable,
table#lionTable{
  font-size: 0.8rem;
}
table#deerTable td,table#deerTable th,
table#horseTable td,table#horseTable th,
table#birdTable td,table#birdTable th,
table#lionTable td,table#lionTable th{
  border: none !important;
}
table#deerTable tr,
table#horseTable tr,
table#birdTable tr,
table#lionTable tr{
  border-top:1px solid #666666;
}
table#deerTable img,
table#horseTable img,
table#birdTable img,
table#lionTable img{
  width:35px;
  height:35px;
}
table#deerTable input,
table#horseTable input,
table#birdTable input,
table#lionTable input{
  font-size: 0.8rem;
  text-align: right;
  width: 80px;
  margin: auto;
}
.progress{
  height: 2rem;
}
.progress-bar{
  height:2rem;
  padding:10px;
  font-weight: 600;
  font-size: 1rem;
}
.green{
    border:2px solid #41d34b;
    color:#41d34b;
}
.blue{
    border:2px solid #0391c4;
    color:#0391c4;
}
.gold{
    border:2px solid #f6c232;
    color:#f6c232;
}
.orange{
    border:2px solid #d36300;
    color:#d36300;
}
</style>
