<script>
export default {
  name: 'card'
}
</script>

<template>
  <div class='card'>
    <slot />
  </div>
</template>

<style scoped>
.card {
  position: relative;
  min-width: 30em;
  min-height: 40%;
  background-color: #f6f6f6;
  border-radius: 15px;
  box-shadow: 20px 20px 60px #d1d1d1, -20px -20px 60px #ffffff;
  font-family: 'Inter', sans-serif;
  font-weight: 300;
  overflow-x: hidden; 
  overflow-y: scroll;
  padding-right: 10px;
}
</style>
