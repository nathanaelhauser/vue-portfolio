<template>
  <div id="nav">
    <div id="left-nav">
      <span>Nathanael Hauser</span>
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
      <router-link to="/portfolio">Portfolio</router-link>
    </div>
    <div id="right-nav">
      <a href="#" id="github-repo">Github</a>
    </div>
  </div>
  <router-view />
</template>

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
  display: flex;
  justify-content: space-between;
  position: sticky;
  top: 0;
  left: 0;
}

#left-nav {
  display: flex;
  justify-content: left;
}

#left-nav a {
  font-weight: bold;
  color: #2c3e50;
  margin-left: 2em;
}

#left-nav a.router-link-exact-active {
  color: #42b983;
}

#right-nav {
  display: flex;
  justify-content: right;
}
</style>
