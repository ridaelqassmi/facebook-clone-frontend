<template>
<div class="container">
  <header-component msg="Welcome to Your Vue.js App"/>
  <div class="body">
    <side-bar />
    <main-bar />
  </div>
</div>
  
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import SideBar from './components/SideBar/SideBar.vue';
import MainBar from './components/MainBar/MainBar.vue';
export default {
  name: 'App',
  components: {
    HeaderComponent,
    SideBar,
    MainBar
  }
}
</script>

<style >
*{
  margin:0;
  padding:0;
}
.container{
  background:#f0f2f5;
  
}
.body{
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
}

</style>
