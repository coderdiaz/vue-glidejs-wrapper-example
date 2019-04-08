<template>
  <div class="glide">
    <div class="glide__track" data-glide-el="track">
      <ul class="glide__slides">
        <slot />
      </ul>
    </div>
    <div v-if="slidesCount > 0" data-glide-el="controls[nav]">
      <glide-bullet
        v-for="(i, index) in slidesCount"
        :key="index"
        :index="index"></glide-bullet>
    </div>
  </div>
</template>
<script>
import Glide from '@glidejs/glide';
import GlideBullet from './GlideBullet.vue';
import "@glidejs/glide/dist/css/glide.core.min.css";

export default {
  name: 'Glide',
  data() {
    return {
      $glide: null,
    };
  },
  mounted() {
    this.init();
  },
  methods: {
    init() {
      this.$glide = new Glide(this.$el).mount();
    },
  },
  computed: {
    slidesCount () {
      return (this.$slots.default) ? this.$slots.default.filter(
        c => c.componentOptions && c.componentOptions.tag === 'glide-slide'
      ).length : 0;
    },
  },
  components: {
    GlideBullet,
  },
};
</script>
