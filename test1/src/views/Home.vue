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

  beforeCreate() {
    console.log("beforeCreate", this.name);
  },

  created() {
    console.log("created", this.name);
  },

  beforeMount() {
    alert("beforeMount");
    /* if you refresh the browser */
  },

  mounted() {
    alert("Mount");
    /* control DOM, it shows display */
  },

  beforeUpdate() {
    alert("beforeUpdate");
  },

  updated() {
    alert("updated");
    /* if you clicked the button, update is being progressed and display an alert */
  },
  beforeDestroy() {
    alert("beforeDestroy");
    /* why it does not work?! == nope, i just wrote it 'beforeDestoy' :D */
  },
  destroyed() {
    alert("destroyed");
    /* if you change the view-router to About */
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