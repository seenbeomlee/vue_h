<template>
  <div>
    <form action>
      <h1>This is Home page</h1>
      <InputField :name="name" @update-name="updateName" />
      <br />
      <button>Submit</button>
    </form>
    {{ name }}
  </div>
</template>

<script>
import InputField from "@/components/InputField.vue";
export default {
  components: {
    InputField
  },
  data() {
    return {
      name: ""
    };
  },
  methods: {
    updateName(name) {
      this.name = name;
    }
  }
};
</script>

<style scoped>
h1 {
  color: red;
}
</style>