<template>
  <router-view />
</template>

<style lang="scss">
body {
  margin: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  display: flex;
  justify-content: flex-end;
  background-color: white;
  border-bottom: 2px solid #9e876f71;

  a {
    padding: 1.5rem;
    font-size: 1rem;
    font-family: "Montserrat", sans-serif;
    color: #9e876f;
    text-decoration: none;
    &:hover{
      color: darken($color: #9e876f, $amount: 10);
      font-weight: bold;
    }

    &.router-link-exact-active {
      color: #9e876f;
      font-weight: bold;
    }
  }
}
</style>
