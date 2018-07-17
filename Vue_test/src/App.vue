<template>
  <div id="app">
    <img src="./assets/logo.png">
   <Main />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import LoginForm from "./components/LoginForm";
import Event from "./components/Event";
import login from "./components/login";
import StyleForm from "./components/StyleForm";
import father from "./components/father";
import parent from "./components/parent";
import Parent from "./components/slots/parentSlot";
import Main from "./components/changeView/mainView";
export default {
  name: "App",
  components: {
    HelloWorld,
    LoginForm,
    Event,
    login,
    StyleForm,
    father,
    parent,
    Parent,
    Main
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
