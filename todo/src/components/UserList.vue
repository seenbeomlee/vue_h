<template>
  <div>
    User List
    <div v-for="user in people" :key="user.id">
      {{ user.name }}
    </div>
  </div>
</template>

<script>
import { mapState, mapActions } from "vuex";
export default {
  created() {
    this.getUsers();
  },
  computed: {
    // using object
    ...mapState("user", {
      users: (state) => state.users,
    }),
  },
  methods: {
    // using array
    ...mapActions("user", ["getUsers"]),
  },
};
</script>

<style></style>
