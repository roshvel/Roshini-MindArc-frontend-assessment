<template>
  <div>
    <NavBar :nav-bar-items="navBarItems" @on-change-active-nav="onChangeActiveNav"/>
    <component :is="navBarItems.find(x => x.isActive) && navBarItems.find(x => x.isActive).link" />
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue'
import Exercise1 from './components/Ex-1.vue'
import Exercise2 from './components/Ex-2.vue'

export default {
  name: 'App',
  components: {
    NavBar,
    Exercise1,
    Exercise2
  },
  data() {
    return {
      navBarItems: [
        {
          name: 'Exercise 1',
          link: 'exercise-1',
          isActive: true
        },
        {
          name: 'Exercise 2',
          link: 'exercise-2',
          isActive: false
        },
      ]
    }
  },
  methods: {
    onChangeActiveNav (e) {
      this.navBarItems = this.navBarItems.map(x => {
        if(x.link === e) {
          return {
            ...x,
            isActive: true
          }
        } else {
          return {
            ...x,
            isActive: false
          }
        }
      })
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>