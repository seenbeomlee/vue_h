<template>
  <div class="about">
    <h1>This is an about page</h1>
    <seenblee>
      <template #header="tt">
        <p>header11 {{ tt.seenblee }}</p>
      </template>
      <template v-slot:default>hello!</template>
    </seenblee>
  </div>
</template>

<script>
import seenblee from "@/components/seenblee.vue"; /* @ means src folder */

export default {
  components: {
    seenblee
  }
};
</script>