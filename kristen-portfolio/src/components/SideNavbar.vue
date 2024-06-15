<template>
  <div class="container">
    <nav class="navbar">
      <ul class="nav-links">
        <li v-for="link in links" :key="link.id" class="nav-item">
          <a :href="link.url" class="nav-link">{{ link.text }}</a>
        </li>
      </ul>
    </nav>
    <div class="content">
      <HelloWorld :msg="message"/>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue';
import HelloWorld from './HelloWorld.vue';

export default {
  components: {
    HelloWorld
  },
  setup() {
    const links = ref([
      { id: 1, text: 'Home', url: '#' },
      { id: 2, text: 'About', url: '#about' },
      { id: 3, text: 'Portfolio', url: '#portfolio' },
      { id: 4, text: 'Contact', url: '#contact' }
    ]);

    const message = ref('Welcome to Your Vue.js App');

    return { links, message };
  }
};
</script>

<style lang="scss">
.container {
  display: flex;
}

.navbar {
  width: 5rem;
  height: 100vh;
  background-color: #333;
  color: white;
}

.nav-item {
  display:block;
  margin-bottom: 0.5rem;
  
}

.nav-link {
  color: white;
  text-decoration: none;
  align-content: flex-end;
  transition: color 0.3s;
}

.nav-link:hover {
  color: rgb(45, 162, 201);
}

.content {
  flex: 1; /* Make the content fill the remaining space */
}
</style>
