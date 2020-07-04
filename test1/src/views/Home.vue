<template>
  <div>
    <h1>Kossie Coder</h1>

    <seenblee title="home title" name="seenblee name" />
  </div>
</template>

<script>
import seenblee from "@/components/seenblee.vue"; /* @ means src folder */

export default {
  components: {
    seenblee
  },

  data() {
    return {
      name: "Kossie Coder"
    };
  }
};
</script>

<style scoped>
h1 {
  color: red;
}
</style>