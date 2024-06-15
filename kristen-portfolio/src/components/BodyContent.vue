<template>
  <div class="hello">
    This will hold all the other components
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

</style>
