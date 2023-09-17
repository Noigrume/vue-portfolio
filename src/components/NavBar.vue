<template>
  <!-- <nav>
    <div class="menu-toggle" @click="toggleMenu">
      <div class="bar"></div>
      <div class="bar"></div>
      <div class="bar"></div>
    </div>
    <ul class="menu" :class="{ active: isMenuOpen }">
      <li><router-link to="/">Home</router-link></li>
      <li><router-link to="/about">About</router-link></li>
      <li><router-link to="/contact">Contact</router-link></li>
      <li><router-link to="/resume">Resume</router-link></li>
      <li><router-link to="/education">Education</router-link></li>
    </ul>
  </nav> -->

  <nav class="nav-menu">
    <i class="fas fa-bars" @click="showMenu()"> </i>
    <div class="nav-content" :class="this.showMobileMenu ? 'open-menu' : 'closed-menu'">
      <div class="logo">
        <!-- <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="20" height="20" /> -->
      </div>

      <ul class="nav-items">
        <li><RouterLink to="/">01.Home</RouterLink></li>
        <li><RouterLink to="/about">02.About</RouterLink></li>
        <li><RouterLink to="/contact">03.Contact</RouterLink></li>
        <li><RouterLink to="/projects">04.Projects</RouterLink></li>
        <li><RouterLink to="/experiences">05.Experiences</RouterLink></li>
        <li><RouterLink to="/education">06.Education</RouterLink></li>
      </ul>
    </div>
  </nav>
</template>

<!-- <script>
console.log('test')
export default {
  data() {
    return {
      showMobileMenu: false
    }
  },
  methods: {
    showMenu() {
      this.showMobileMenu = !this.showMobileMenu
    }
  }
}
</script> -->

<style scoped>
@media (min-width: 1024px) {
}

.nav-menu {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background-color: #ffffff17;
  color: #fff;
  padding: 10px 0;
  text-align: center;
  z-index: 1000;
}

nav ul {
  list-style: none; /* Supprime les puces de liste */
  padding: 0;
  margin: 0;
}

nav li {
  display: inline-block; /* Les éléments sont affichés côte à côte */
  margin-right: 20px; /* Espacement entre les éléments */
}

nav a {
  text-decoration: none; /* Supprime les soulignements des liens */
  color: #fff; /* Couleur du texte des liens */
  font-weight: bold; /* Texte en gras */
}
/* .nav-content {
  display: flex;
  justify-content: space-between;
  padding: 2px;
  align-items: center;
  color: black;
}
.nav-items,
a {
  color: black;
  font-size: larger;
  display: flex;
  justify-content: center;
  align-items: center;
  list-style: none;
  margin: 0;
  padding: 0;
  li {
    padding: 0 10px;
  }
}
i {
  display: none;
} */

/* Mobile version */
@media screen and (max-width: 768px) {
  .nav-menu {
    padding-top: 10px;
    position: absolute;
    width: 100%;
  }
  .open-menu {
    opacity: 1;
    height: 150px;
  }
  .closed-menu {
    opacity: 0;
    height: 0;
    padding: 0;
  }
  .nav-content {
    flex-direction: column;
    z-index: 100;
    position: relative;
    transition: all 0.2s ease-out;
  }
  .nav-items {
    flex-direction: column;
  }
  i {
    display: block;
    text-align: right;
    padding: 0 10px 10px 0;
  }
}
</style>

<script>
export default {
  data() {
    return {
      isMenuOpen: true
    }
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen
    }
  }
}
</script>
