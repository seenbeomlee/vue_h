<template>
  <div>
    <h1>This is Home page</h1>
    <InputField v-model="name" />
    <br />
    <button @click="updateName">Submit</button>
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
      name: "seenblee"
    };
  },

  /* these are all hook for life-cycle */
  /* when vue instance is being made or eliminated, this life-cycle hook is also progressed */

  beforeCreate() {
    alert("beforeCreate");
    /* cant use Data(this.title...), Method() and events(vm$on, vm.$emit...) cause they are not setted yet */
  },

  created() {
    alert("Created");
    /* you can track the data and computed, methods, watch ... are valid */
    /* but you can't use $el yet. because DOM does not mounted yet  */
  },

  beforeMount() {
    alert("beforeMount");
    /* before the first rendering(DOM). this.$el doesn't exist yet */
  },

  mounted() {
    alert("Mount");
    /* after create the DOM. it can approach all elements */
  },

  beforeUpdate() {
    alert("beforeUpdate");
    /* if you change the value of some data in this section, it does not call the beforeUpdate hook. */
  },

  updated() {
    alert("updated");
    /* if you clicked the button, update is being progressed and display an alert */

    /* after re-rendering(DOM) */
    /* if you change data in this hook, it can make a infinite loop */
  },
  beforeDestroy() {
    alert("beforeDestroy");
    /* before eliminate the vue instance. so you can approach all instance. */
  },
  destroyed() {
    alert("destroyed");
    /* if you change the view-router to About */

    /* after elimanate the vue instance */
  },
  methods: {
    updateName() {
      this.name = "hello update";
    }
  }
};
</script>

<style scoped>
h1 {
  color: red;
}
</style>