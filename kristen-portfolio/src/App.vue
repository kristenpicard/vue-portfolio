<template>
  <div class="custom-cursor"></div>
  <BodyContent />
</template>

<script>
import { ref } from 'vue';
import BodyContent from './components/BodyContent.vue'

export default {
  name: 'App',
  components: {
    BodyContent
  },
  setup() {
    const message = ref('Welcome to Your Vue.js App');
    document.addEventListener('mousemove', (e) => {
        const cursor = document.querySelector('.custom-cursor');
        cursor.style.top = e.pageY + 'px';
        cursor.style.left = e.pageX + 'px';
    });
    return {
      message
    };
  }
};
</script>
<style lang="scss">
#app {
  height: 100vh;
  background-color: #01170f;
  // padding: 6rem 9rem 0 6rem;
  align-items: center;
}

body {
  margin: unset;
  overflow: hidden;
  
}

.custom-cursor {
  width: 1px;
  height: 1px;
  background-color: transparent;
  border: 2px solid #333;
  border-radius: 50%;
  position: absolute;
  pointer-events: none;
  // z-index: 9999; /* Make sure the cursor is on top of everything */
  box-shadow: 0px 0px 150px 30px rgb(250, 249, 249); /* Box shadow effect */
}
</style>
