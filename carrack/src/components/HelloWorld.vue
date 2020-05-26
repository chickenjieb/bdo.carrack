<template>
  <div class="hello">
    <div class="container py-3">
      <h1>Epheria Carrack</h1>
      <div class="row mx-0 py-5">
        <!-- deer -->
        <div class="col-3">
          <router-link to="/deer">
            <div class="card" style="">
              <img class="card-img-top" src="../assets/deer.jpg" alt="Card image cap">
              <div class="card-body">
                <p class="card-text">BALANCE<br><small>สมดุล</small></p>
              </div>
            </div>
          </router-link>
        </div>

        <!-- horse -->
        <div class="col-3">
          <router-link to="/horse">
            <div class="card" style="">
              <img class="card-img-top" src="../assets/horse.jpg" alt="Card image cap">
              <div class="card-body">
                <p class="card-text">ADVANCE<br><small>ทนทาน</small></p>
              </div>
            </div>
          </router-link>
        </div>

        <!-- bird -->
        <div class="col-3">
          <router-link to="/bird">
            <div class="card" style="">
              <img class="card-img-top" src="../assets/bird.jpg" alt="Card image cap">
              <div class="card-body">
              <p class="card-text">VOLANTE<br><small>ฉุกเฉิน</small></p>
              </div>
            </div>
          </router-link>
        </div>


        <!-- lion -->
        <div class="col-3">
          <router-link to="/lion">
            <div class="card" style="">
              <img class="card-img-top" src="../assets/lion.jpg" alt="Card image cap">
              <div class="card-body">
                <p class="card-text">VALOR<br><small>แข็งแกร่ง</small></p>
              </div>
            </div>
          </router-link>
        </div>


      </div>
    </div>
    <!-- <h1>{{ msg }}</h1>
    <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
    <h3>Installed CLI Plugins</h3>
    <ul>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel" target="_blank" rel="noopener">babel</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-router" target="_blank" rel="noopener">router</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-vuex" target="_blank" rel="noopener">vuex</a></li>
    </ul>
    <h3>Essential Links</h3>
    <ul>
      <li><a href="https://vuejs.org" target="_blank" rel="noopener">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank" rel="noopener">Forum</a></li>
      <li><a href="https://chat.vuejs.org" target="_blank" rel="noopener">Community Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank" rel="noopener">Twitter</a></li>
      <li><a href="https://news.vuejs.org" target="_blank" rel="noopener">News</a></li>
    </ul>
    <h3>Ecosystem</h3>
    <ul>
      <li><a href="https://router.vuejs.org" target="_blank" rel="noopener">vue-router</a></li>
      <li><a href="https://vuex.vuejs.org" target="_blank" rel="noopener">vuex</a></li>
      <li><a href="https://github.com/vuejs/vue-devtools#vue-devtools" target="_blank" rel="noopener">vue-devtools</a></li>
      <li><a href="https://vue-loader.vuejs.org" target="_blank" rel="noopener">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank" rel="noopener">awesome-vue</a></li>
    </ul> -->
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.card-img-top{
  object-fit: cover;
  height: 300px;
}
.card-body{
  padding-top: 15px;
  padding-bottom: 15px;
}
.card-text{
  color:#333333;
  font-weight: 600;
  font-size: 1.2rem;
}
.card-text small{
  font-size: 0.9rem;
}
</style>
