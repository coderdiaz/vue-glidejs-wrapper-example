<script>
export default {
  name: 'GlideSlide',
  render(h) {
    return h('div', {
      class: 'glide__slide'
    }, this.$slots.default);
  },
};
</script>
