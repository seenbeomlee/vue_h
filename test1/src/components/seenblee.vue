<template>
  <div>
    <p>header</p>
    <slot name="header" :seenblee="seenblee"></slot>
    <p>body</p>
    <slot></slot>
    <p>footer</p>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: "default title"
    },
    name: {
      type: String,
      default: "default name"
    }
  },

  data() {
    return {
      seenblee: "coder"
    };
  },

  methods: {}
};
</script>

<style scoped></style>