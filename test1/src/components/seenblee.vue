<template>
  <div>
    <p>{{ name }}</p>
    <button @click="updateName">Change Name</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "seenblee"
    };
  },

  methods: {
    updateName() {
      this.name = "seenblee updated";
    }
  }
};
</script>

<style scoped></style>