<template>
  <div id="app">
    Data z rodiče: {{ msg }}
    <hr />
    <Formik v-model="msg" />
  </div>
</template>

<script>
import Formik from './components/Formik.vue';

export default {
  name: 'App',
  components: {
    Formik,
  },
  data() {
    return {
      msg: 'pica2',
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
