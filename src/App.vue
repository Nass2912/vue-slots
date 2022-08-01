<template>
  <select v-model="componentName">
    <option value="home">home</option>
    <option value="about">about</option>
  </select>

  <KeepAlive>
    <component :is="componentName" ></component>
  </KeepAlive>
</template>

<script>
import Home from './components/Home.vue'
import About from './components/About.vue'

export default {
  name: "App",
  components: {
    Home,
    About
  },

  data () {
    return {
      componentName: "Home"
    }
  }
}
</script>
