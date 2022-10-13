<template>
  <div class="userInfo">
    <active-user :name="name" :age="age" />
    <user-data @set-userInfo="setUserInfo" />
  </div>
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
    setUserInfo(name, age) {
      this.name = name;
      this.age = age;
    },
  },
};
</script>

<style>
.userInfo {
  display: flex;
}
</style>
