<template>
  <section class="activeUser">
    <h2>User Name: {{ name }}</h2>
    <h3>Age: {{ age }}</h3>
  </section>
</template>
<script>
export default {
  props: {
    name: {
      type: String,
      required: true,
    },
    age: {
      required: true,
    },
  },
};
</script>
