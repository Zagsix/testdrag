<template>
  <div>
    <div v-for="(item, index) in items" :key="index" @insert="() => {}">
      <slot name="item" v-bind:item="item"> </slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "DropList",
  props: {
    items: {
      type: Array,
      default: () => {
        return [];
      },
    },
  },
};
</script>