<template>
  <div class="footer">
    <p>{{copyright}}</p>
  </div>
</template>

<script>
    export default {
        name: "Footer",
        data() {
            return {
                copyright: "@Copyright 2019 Vue Demo"
            }
        }
    }
</script>

<style scoped>
  .footer {
    background: #006dff;
    padding: 10px;
  }

  h1 {
    color: black;
    text-align: center;
  }
</style>
