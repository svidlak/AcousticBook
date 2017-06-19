<template>
<div id="app">
  <div id="particleJS-container"></div>
  <span class="rest">
    <div class="container">
    <div class="row margin-top">
      <div class="col-xs-5 text-center">
        <h1>Welcome to AcousticBook</h1>
        <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
      </div>
      <div class="col-xs-offset-2 col-xs-5 text-center ">
          <app-login @viewChange="show = !show" v-if="!show"></app-login>
          <app-register v-else></app-register>
        </div>
    </div>
    </div>
  </span>
</div>
</template>

<script>
import Login from './components/Login.vue'
import Register from './components/Register.vue'

export default {
  data(){
    return{
        show: false,
    }
  },
  components:{
    appLogin: Login,
    appRegister: Register,
  },
}
</script>

<style>
body{
  background-image: url('/src/assets/bg.jpg');
  background-repeat:no-repeat;
  background-size:cover;
  height: 100vh;
  color: white;
}

.rest{
  top: 0;
  left: 0;
  position: absolute;
  width: 100%;
  z-index: 5;
}

.margin-top{
  margin-top: 10%;
}

</style>
