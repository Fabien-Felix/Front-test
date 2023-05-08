<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
    </div>
    <!-- <router-view/> -->
    
    <div v-for="people in peoples" :key="people.title">
      <people :people="people"></people>
    </div>
  </div>
</template>

<!-- Components ajoute -->
<script>
import People from './components/People'
export default {
  name: "App",
  components: { People },
  data() {
    return {
      peoples: [
        {
          title: 'Luke Skywalker'
        },
        {
          title: 'C-3PO'
        },
        {
          title: 'R2-D2'
        },
        {
          title: 'Darth Vader'
        },
        {
          title: 'Leia Organa'
        },
      ]
    }
  }
};
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
