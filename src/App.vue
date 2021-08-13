<template>
  <login/>
  <chatroom/>
</template>

<script>
import Login from './components/Login.vue'
import Chatroom from './components/Chatroom.vue'

export default {
  name: 'App',
  components: {
    Login,
    Chatroom
  }
}
</script>

<style>
@import url('./assets/css/CssReset.css');
html, body, #app{
  height: 100%;
}
</style>
