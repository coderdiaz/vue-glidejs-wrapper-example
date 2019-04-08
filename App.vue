<template>
  <div id="app">
    <glide>
      <glide-slide>1</glide-slide>
      <glide-slide>2</glide-slide>
      <glide-slide>3</glide-slide>
      <glide-slide>4</glide-slide>
    </glide>
  </div>
</template>
<script>
import Glide from './components/Glide.vue';
import GlideSlide from './components/GlideSlide.vue';

export default {
  name: 'App',
  components: {
    Glide,
    GlideSlide,
  },
};
</script>

