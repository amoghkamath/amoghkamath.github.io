<template>
  <div class="sidebar">
    <div class="container">
      <h2 v-for="tab in tabs" @click="$router.push('/' + tab.page)" :key="tab.name">{{tab.name}}</h2>
    </div>
  </div>
</template>

<script type="text/javascript">
  export default {
    name: 'sidebar',
    data () {
      return {
        tabs: [
          {name: 'Home', page: 'home'},
          {name: 'About', page: 'about'}
        ]
      }
    }
  }
</script>

<style lang="scss">
  #app {
    position: relative;
    left: 0px;
    transition: .6s;
  }
  #app.active {
    left: 300px;
  }
  .sidebar {
    position: fixed;
    width: 300px;
    left: -300px;
    height: 100%;
    background: white;
    top: 0px;
    transition: .6s;
    .container {
      width: 100%;
      height: 100%;
      display: flex;
      justify-content: center;
      flex-direction: column;
    }
    .container h2 {
      cursor: pointer;
      text-align: left;
      padding-left: 40px;
      margin: 20px 0px;
      font-weight: 200;
      font-size: 28px;
      transition: .2s;
      &:hover {
        color: #999;
      }
    }
  }
  .sidebar.active {
    left: 0px;
    box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);
  }
</style>
