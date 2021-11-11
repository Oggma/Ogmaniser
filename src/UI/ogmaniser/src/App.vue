<template>
  <div id="header">
    <img src="./assets/logo.png" />
  </div>
  <div id="main">
    <div id="leftMenu">
      <div id="nav">
        <router-link to="/">Home</router-link>
        <router-link to="/about">About</router-link>
      </div>
    </div>
    <div id="content">
      <router-view />
    </div>
  </div>
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #100f0f;
  display: flex;
  flex-direction: column;
}

#header {
  background-color: #ff0c3e;
  height: 60px;
  display: flex;
  padding: 0.3rem;
}

#leftMenu {
  background-color: #b3abab;
  width: 15%;
}

#main {
  display: flex;
  flex-direction: row;
  height: calc(100vh - 80px);
}

#content {
  padding: 1rem;
}

#nav {
  display: flex;
  flex-direction: column;

  a {
    font-weight: bold;
    color: #100f0f;
    text-decoration: none;
    padding: 1rem;

    &:hover {
      background-color: #d7d7d7;
    }

    &.router-link-exact-active {
      background-color: #ff0c3d60;
    }
  }
}
</style>
