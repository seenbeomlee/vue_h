<template>
  <div>
    <p>header</p>
    <slot name="header"></slot>
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
      //required: false /* props is optional == false, mendatory == true */
      default: "default title"
    },
    name: {
      type: String,
      default: "default name"
    }
  },

  data() {
    return {
      //name: "seenblee"
    };
  },

  methods: {
    /*     updateName() {
      this.name = "seenblee updated";
    } */
  }
};
</script>

<style scoped></style>