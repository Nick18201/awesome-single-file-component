<template>
  <p class="username">{{ username }}</p>
</template>

<script>
export default {
  props: {
    username: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
.username {
  font-size: 3rem;
  color: #dcae1d;
}
</style>
