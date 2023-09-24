<template>
  <nav class="navbar">
    <div class="menu-toggle" @click="toggleMobileMenu">☰</div>
    <ul class="menu" :class="{ active: isMobileMenuOpen }">
      <li @click="toggleMobileMenu"><RouterLink to="/">Home</RouterLink></li>
      <!--      <li @click="toggleMobileMenu"><RouterLink to="/about">About</RouterLink></li>
      <li @click="toggleMobileMenu"><RouterLink to="/contact">Contact</RouterLink></li> -->
      <li @click="toggleMobileMenu"><RouterLink to="/projects">Projets</RouterLink></li>
      <li @click="toggleMobileMenu"><RouterLink to="/experiences">Parcours</RouterLink></li>
      <!--       <li @click="toggleMobileMenu"><RouterLink to="/education">Education</RouterLink></li> -->
    </ul>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      isMobileMenuOpen: false
    }
  },
  methods: {
    toggleMobileMenu() {
      this.isMobileMenuOpen = !this.isMobileMenuOpen
    }
  }
}
</script>

<style scoped>
.navbar {
  width: 100%;
  position: fixed;
  padding: 10px;
  background-color: #ffffff36;
  color: #fff;
}

.menu {
  list-style: none;
  display: flex;
  align-items: center;
  justify-content: center;
}

.menu li {
  margin-right: 20px;
}

.menu a {
  text-decoration: none;
  font-weight: 700;
  font-size: 1.2rem;
  color: #fff;
}

.menu-toggle {
  display: none;
  font-size: 24px;
  cursor: pointer;
}

@media (max-width: 768px) {
  .menu {
    display: none;
  }

  .menu.active {
    width: 100%;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    position: absolute;
    top: 60px;
    left: 0;
    background-color: #000000bb;
    text-align: left;
    font-size: 2rem;
    text-transform: uppercase;
  }

  .menu.active li {
    margin: 0;
  }

  .menu-toggle {
    display: block;
  }
}
</style>
