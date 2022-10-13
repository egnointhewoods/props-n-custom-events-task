<template>
  <form @submit="updateUser">
    <input @keyup="setName" type="text" placeholder="name" v-model="name" />
    <input @keyup="setAge" type="number" placeholder="age" v-model="age" />
    <button>Set</button>
  </form>
</template>
<script>
export default {
  data() {
    return {
      name: "",
      age: null,
    };
  },
  methods: {
    setName(event) {
      this.name = event.target.value;
    },
    setAge(event) {
      this.age = event.target.value;
    },
    updateUser(e) {
      e.preventDefault();
      this.$emit("set-userInfo", this.name, this.age);
      this.name = "";
      this.age = null;
    },
  },
  emits: ["set-userInfo"],
};
</script>
<style>
form {
  margin-top: 30px;
  margin-left: 50px;
}
input {
  display: block;
  margin-bottom: 10px;
}
</style>
