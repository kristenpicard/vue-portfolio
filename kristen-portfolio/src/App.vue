<template>
  <SideNavbarVue />
</template>

<script>
import { ref } from 'vue';
import SideNavbarVue from './components/SideNavbar.vue';

export default {
  name: 'App',
  components: {
    SideNavbarVue
  },
  setup() {
    const message = ref('Welcome to Your Vue.js App');
    
    return {
      message
    };
  }
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

body {
  margin: unset;
}
</style>
