<template>
  <div draggable="true" @dragstart="ondragstart">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "Drag",
  prosp: {
    item: {
      type: Object,
      default: () => {
        return {};
      },
    },
  },
  methods: {
    ondragstart(e) {
      e.dataTransfer.setData("text", e.target.id);
      console.log(e);
    },
  },
};
</script>