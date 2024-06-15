<template>
  <div class="hello">
    <div class="column">
        <h1>Kristen Picard</h1>
    <h3>Software Engineer</h3>
    </div>
    <div class="column">
        Column 2 content goes here
    </div>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  props: {
    msg: String
  },
  setup(props) {
    const message = ref(props.msg);
    
    return {
      message
    };
  }
};
</script>

<style lang="scss" scoped>
.hello {
  color: white;
  font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  display: flex;
  padding: 5.5rem;
  height: 75vh;
}

.column {
    flex: 1; /* This makes the columns grow to fill the available space */
    border: 1px solid #ccc;
}

h1 {
  font-size: 3rem;
  line-height: 1;
  margin-bottom: 1rem;
}

h3 {
  margin: 0;
}
</style>
