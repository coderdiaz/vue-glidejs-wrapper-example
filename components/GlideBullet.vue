<script>
export default {
  name: 'GlideBullet',
  props: {
    index: {
      type: Number,
      required: true,
    },
  },
  render(h) {
    return h('button', {
      attrs: {
        class: 'glide__bullet',
        'data-glide-dir': '=' + this.index,
      }
    });
  },
};
</script>
