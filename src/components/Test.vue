<template>
  <div class="test">
    <p>{{msg}}</p>
    <p @click="changeData">{{appData}}</p>
    <ul>
      <li @click="data.show = !data.show" v-for="(data, index) in list" :key="index">
        <h2 v-show="data.show">{{data.name}}</h2>
      </li>
    </ul>
  </div>
</template>

<script>
    export default {
        name: "test",
        // 接受父组件的传值
        props: ['appData'],
        data() {
            return {
                msg: '这是一个学习模块',
                list: [
                    {name: "C++", show: true},
                    {name: "Java", show: true},
                    {name: "JavaScript", show: true},
                    {name: "Python", show: true},
                    {name: "GoLang", show: true},
                    {name: "Kotlin", show: true},
                    {name: "Ruby", show: true},
                ]
            }
        },
        methods: {
            changeData() {
                this.$emit("appDataChange", "changed.");
            }
        }
    }
</script>

<style scoped>
  .test {
    width: 100%;
    max-width: 1200px;
    margin: 40px auto;
    padding: 0 20px;
    box-sizing: border-box;
  }

  ul {
    display: flex;
    flex-wrap: wrap;
    list-style-type: none;
    padding: 0;
  }

  li {
    flex-grow: 1;
    flex-basis: 200px;
    text-align: center;
    padding: 30px;
    border: 1px solid black;
    margin: 10px;
  }
</style>
