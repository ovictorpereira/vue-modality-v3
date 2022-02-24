<script>
import { defineComponent } from 'vue';
import VueModalityV3 from '@/vue-modality-v3.vue';

export default defineComponent({
  name: 'ServeDev',
  components: {
    VueModalityV3
  }
});
</script>

<template>
  <div id="app">
    <vue-modality-v3 />
  </div>
</template>
