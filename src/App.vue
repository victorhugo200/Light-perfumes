<template>
  <div id="app">
   <Header />
   <Home />
  </div>
</template>

<script lang="ts">

import Vue from 'vue';
import Home from './pages/Home.vue';
import Header from './components/Header.vue';
import './style/style.scss';

export default Vue.extend({
  name: 'App',
 components: {
    Home,
    Header
  },
})
</script>

<style lang="scss">

</style>
