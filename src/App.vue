<template>
  <div id="app">
    <Header/>
    <img src="./assets/logo.png">
    <HelloWorld/>
    <Test/>
    <Footer/>
  </div>
</template>

<script>
    import HelloWorld from './components/HelloWorld'
    import Test from './components/Test'
    import Header from "./components/Header";
    import Footer from "./components/Footer";

    export default {
        name: 'App',
        components: {
            Footer,
            Header,
            HelloWorld,
            Test
        }
    }
</script>

<style  >
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
</style>
