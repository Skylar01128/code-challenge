<script setup>
  import Navbar from "./components/Navbar.vue"
  import Main from "./components/Main.vue"
  import Footer from "./components/Footer.vue"

  const links = ['About Us', 'Blog', 'Resources', 'Contact']
</script>

<template>
  <header>
    <Navbar :navLinks="links"/>
  </header>

  <main>
    <Main />
  </main>

  <footer id="footer">
    <Footer />
  </footer>
</template>

<style scoped>
  #footer{
    display: grid;
    justify-content: center;
  }
</style>
