<template>
  <div :class="{active: sidebarOpen}" id="app">
    <sidebar :class="{active: sidebarOpen}"></sidebar>
    <div class="navigation">
      <b-button @click="openSidebar"
          size="is-large" type="is-dark"
          icon-left="menu" style="border: none; box-shadow: none">
      </b-button>
    </div>
    <router-view/>
  </div>
</template>

<script type="text/javascript">
  import sidebar from './components/sidebar'
  export default {
    name: 'App',
    components: {sidebar},
    data () {
      return {
        sidebarOpen: false
      }
    },
    methods: {
      openSidebar: function () {
        this.sidebarOpen = !this.sidebarOpen
      }
    }
  }
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap');
html, body, #app {
  min-height: 100vh;
}
#app {
  font-family: Roboto, Helvetica, Arial, sans-serif;
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

h1,h2,h3,h4,h5,h6, p {
  margin: 0px;
}
.navigation {
  position: fixed;
  padding-left: 20px;
  padding-top: 12px;
  width: 100%;
  height: 60px;
  top: 0px;
  background: transparent;
  display: flex;
  button {
    background: none;
    outline: none;
    box-shadow: none;
    color: white;
  }
}
</style>
