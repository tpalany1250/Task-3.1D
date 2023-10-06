<script setup>
import { RouterLink, RouterView } from 'vue-router'
import AI from './components/AI.vue';
</script>

<template>

  <header>
     <!-- <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" /> -->

      <h1 style="color: rgb(101, 228, 185);">Prestige Lane</h1>

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/finance">Finance</RouterLink>
        <RouterLink to="/contact">Contact</RouterLink>
        <RouterLink to="/collectibles">Collectibles</RouterLink>
        <RouterLink to="/shop">Shop</RouterLink>
        
      </nav>
    
  </header>

  <AI />

  <RouterView />

  <footer>

    <div class="path">
      <h3 style="margin-left: -10px; padding: 12px;">PRESTIGELANE</h3>

      <nav>
        <!-- <ul></ul> -->
        <RouterLink to="/">Home</RouterLink>
        <ul></ul>
        <RouterLink to="/finance">Finance</RouterLink>
        <ul></ul>
        <RouterLink to="/contact">Contact</RouterLink>
        <ul></ul>
        <RouterLink to="/collectibles">Collectibles</RouterLink>
        <ul></ul>
        <RouterLink to="/shop">Shop</RouterLink>
        <!-- <ul></ul> -->
      </nav>
    </div>

    <br>

    <div class="copyright">
      <p>&copy; 2023 Prestige Lane. All rights reserved.</p>
    </div>
  </footer>

</template>

<style scoped>


header {
    position: fixed;
    top: 0;
    left: 0;    
    width: 100%;
    display: flex;
    justify-content: space-around;
    align-items: center;
    background-color: #1c1c1c; /* Change this to your desired header background color */
    color: #fff; /* Change this to your desired text color */
    padding: 15px;
    z-index: 1000;
}

/* Style the navigation links */
nav {
    display: flex;
    gap: 30px;
}

.path nav a{
  /* background-color: rgb(73, 77, 77); */
  padding: 1px;
  max-width: 31%;
  color: rgb(159, 165, 171);
}

.path nav a:hover {
  color: aliceblue;
}

nav ul {
  padding: 1px;
  border-left: 1px solid rgb(162, 168, 166);
}


footer {
  background-color: #2f2c2c;
  padding: 15px;
  

  margin-bottom: -30px;
  margin-left: -40px;
  margin-right: -32px;

}

.copyright {
  border-top: 1px solid rgb(101, 228, 185);
  padding-top: 20px;
  margin-left: 30px;
  margin-right: 30px;
}

.path {
  margin-left: 40px;
}


/* header {
  line-height: 1.5;
  max-height: 100vh;
} */

/* .logo {
  display: block;
  margin: 0 auto 2rem;
} */

/* nav {
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
} */

/* @media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  /* .logo {
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
} */
</style>
