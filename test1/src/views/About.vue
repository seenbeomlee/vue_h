<template>
  <div class="about">
    <h1>This is an about page</h1>
    <seenblee>
      <template #header>
        <p>header11</p>
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