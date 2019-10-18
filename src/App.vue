<template>
  <div id="app">
    <Header/>
    <img src="./assets/logo.png">
    <HelloWorld/>
    <!--传值给子组件-->
    <Test @appDataChange="appDataChange" :appData="appData"/>
    <div>
      <!--动态组件绑定-->
      <!--keepAlive 可将动态组件缓存起来-->
      <KeepAlive>
        <component :is="component"></component>
      </KeepAlive>
      <button @click="component = 'FormOne'">changeFormOne</button>
      <button @click="component = 'FormTwo'">changeFormTwo</button>
    </div>
    <Footer/>
  </div>
</template>

<script>
    import HelloWorld from './components/HelloWorld'
    import Test from './components/Test'
    import Header from "./components/Header";
    import Footer from "./components/Footer";
    import FormOne from "./components/form/FormOne";
    import FormTwo from "./components/form/FormTwo";

    export default {
        name: 'App',
        data() {
            return {
                appData: '父组件的值',
                component: FormOne,
            }
        },
        components: {
            Footer,
            Header,
            HelloWorld,
            Test,
            FormOne,
            FormTwo
        },
        methods: {
            appDataChange(title) {
                this.appData = title;
            },
        }
    }
</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
</style>
