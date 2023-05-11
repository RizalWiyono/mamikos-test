<!-- eslint-disable prettier/prettier -->
<template>
  <div id="app">
    <NavBar />
    
    <main>
        <div class="container">
            <router-view />
        </div>
    </main>
  </div>
</template>
<!-- eslint-disable prettier/prettier -->
<script>
import NavBar from '@/components/Navbar/Navbar.vue'

export default {
  components: {
    NavBar,
  }
}
</script>
<!-- eslint-disable prettier/prettier -->
<style>
    #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    padding: 0;
    }

    main {
        align-items: center;
        display: flex;
        justify-content: center;
    }

    .container {
        text-align: left;
        width: 1170px;
    }

    nav {
    padding: 30px;
    }

    nav a {
    font-weight: bold;
    color: #2c3e50;
    }

    nav a.router-link-exact-active {
    color: #42b983;
    }
</style>
