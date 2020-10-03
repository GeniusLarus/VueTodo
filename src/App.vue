<template>
  <div id="app">
    <h1>ToDo Application</h1>
    <hr>

    <router-view />
  </div>
</template>

<style>
a {
  text-decoration: none;
  color: #000;
  font-size: 20px;
  transition: .4s ease;
}
a:hover {
  text-shadow: 1px 1px 1px #000;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
