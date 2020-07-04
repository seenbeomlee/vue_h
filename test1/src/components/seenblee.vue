<template>
  <div>
    <h1>{{title}}</h1>
    <p>{{ name }}</p>
    <button @click="updateName">Change Name</button>
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