<template>
  <div id="app">
    <Header></Header>
    <router-link to="/">List</router-link>
    <router-link to="/detail">Detail</router-link>
    <router-view></router-view>
 
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'

//import List from './components/Table.vue'

import Header from './components/Header.vue'
export default {
  name: 'App',
  components: {
    Header,

  }
}
</script>
