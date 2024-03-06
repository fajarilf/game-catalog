<script setup>
import { provide, ref } from 'vue';
// mport { RouterLink, RouterView } from 'vue-router'
import navbarComponent from './components/navbarComponent.vue';
import carouselComponent from './components/carouselComponent.vue';
import platformList from './components/platformList.vue';
import gameListComponent from './components/gameListComponent.vue';
import genreComponent from './components/genreComponent.vue'

const data = ref({
  navbarMenu: [
    { id: "#Home", title: "Home" },
    { id: "#About", title: "About" },
    { id: "#Platform", title: "Platform" },
    { id: "#Genre", title: "Genre" },
  ],
})

provide('id', data.value.navbarMenu)

</script>

<template>
  <header id="Home">
    <navbarComponent title="NAVBAR" />
    <section id="hero">
      <carouselComponent />
    </section>
  </header>

  <main class="container-fluid" id="About">
    <section>
      <platformList />
      <gameListComponent title="Popular Game" />
    </section>

    <section>
      <genreComponent title="Genre" />
    </section>
  </main>
</template>

<!-- <style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style> -->
