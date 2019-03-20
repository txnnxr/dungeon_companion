<template>
  <div id="app">
      <b-navbar toggleable="lg" type="dark" variant="dark">
          <b-navbar-brand href="/">DM Companion</b-navbar-brand>
          <b-navbar-toggle target="nav_collapse" />
          <b-collapse is-nav id="nav_collapse">
            <b-navbar-nav class="ml-auto">
              <b-nav-item href="/about">About</b-nav-item>
              <b-nav-item href="/random-tables">Random Tables</b-nav-item>
            </b-navbar-nav>
            </b-navbar-nav>
          </b-collapse>
        </b-navbar>
    <router-view/>
  </div>
</template>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
