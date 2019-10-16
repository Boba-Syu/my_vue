<template>
  <div class="header">
    <h1>{{title}}</h1>
  </div>
</template>

<script>
    export default {
        name: "Header",
        data() {
            return {
                title: "Vue Demo Header",
            }
        }
    }
</script>

<style scoped>
  .header {
    background: aqua;
    padding: 10px;
  }

  h1 {
    color: black;
    text-align: center;
  }
</style>
