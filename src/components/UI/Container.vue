<template>
  <div class="container">
      <slot>

      </slot>
  </div>
</template>

<script>
export default {
    name: 'my-container'
}
</script>

<style scoped>
.container {
    margin: 0 80px;
}
</style>