<template>
  <div id="app">
    <div style="background-color: #e6e6e6;">
      <Table1 v-if="table1" /> 
      <Table2 v-else />
    </div>
    <b-button @click="() => table1 = !table1">Switch table</b-button>
  </div>
</template>

<script>
import Vue from 'vue'
import BootstrapVue from 'bootstrap-vue';
import Table1 from './components/Table1';
import Table2 from './components/Table2';

import 'bootstrap/dist/css/bootstrap.css';
import 'bootstrap-vue/dist/bootstrap-vue.css';

Vue.use(BootstrapVue);

export default {
  name: 'App',
  components: {
    Table1,
    Table2
  },
  data: () => {
    return {
      table1: true
    };
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
