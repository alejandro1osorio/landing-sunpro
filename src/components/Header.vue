<template>
  <header class="header">
    <img src="../assets/logos-sellos/logo-sunpro.webp" alt="Logo" class="header-logo" />
    <nav class="header-nav">
      <ul class="nav-list" v-if="isMenuOpen || !isMobile">
        <li class="nav-item">
          <a href="#" class="nav-link active">Inicio</a>
        </li>
        <li class="nav-item">
          <a href="#50color" class="nav-link">Color 50 SPF</a>
        </li>
        <li class="nav-item">
          <a href="#90" class="nav-link">90 SPF</a>
        </li>
        <li class="nav-item">
          <a href="#50" class="nav-link">50 SPF</a>
        </li>
      </ul>
      <div class="menu-toggle" @click="toggleMenu" v-if="isMobile">
        <span v-if="!isMenuOpen">&#9776;</span>
        <span v-else>&#10005;</span>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      isMenuOpen: false,
      isMobile: window.innerWidth <= 768,
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    },
    handleResize() {
      this.isMobile = window.innerWidth <= 768;
      if (!this.isMobile) {
        this.isMenuOpen = false;
      }
    },
  },
  mounted() {
    window.addEventListener("resize", this.handleResize);
  },
  beforeDestroy() {
    window.removeEventListener("resize", this.handleResize);
  },
};
</script>

<style scoped>
.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1rem 2rem; /* Uniform padding for consistent spacing */
  position: absolute;
  top: 0;
  width: 100%;
  background-color: transparent; /* Transparent header */
  z-index: 10;
}

.header-logo {
  width: 150px;
  height: auto;
  margin-left: 2rem; /* Add left margin to separate from the edge */
}

.header-nav {
  flex-grow: 1;
  display: flex;
  justify-content: flex-end;
  padding-right: 2rem; /* Add right padding to the navigation */
}

.nav-list {
  display: flex;
  gap: 1.5rem;
  list-style: none;
  margin: 0;
  padding: 0.8rem 2rem;
  background-color: rgba(255, 255, 255, 0.8);
  border-radius: 20px;
}

.nav-item {
  text-align: center;
}

.nav-link {
  text-decoration: none;
  color: #214F79;
  font-weight: 400;
  position: relative;
  transition: color 0.3s ease;
}

.nav-link::after {
  content: "";
  display: block;
  width: 0;
  height: 2px;
  background-color: #F4A61E;
  margin: 0 auto;
  transition: width 0.3s ease;
}

.nav-link:hover::after,
.nav-link.active::after {
  width: 50%;
}

.nav-link.active {
  font-weight: bold;
  color: #214F79;
}

.nav-link:hover {
  font-weight: bold;
  color: #214F79;
}

.menu-toggle {
  display: none;
  cursor: pointer;
  font-size: 1.5rem;
  color: #214F79;
  /* background: #f2f2f2; */
  width: 10%;
  height: 10%;
  border-radius: 60%;
  display: flex;
  align-items: center;
  justify-content: center;
}

@media (max-width: 768px) {
  .header-logo {
    display: none;
  }

  /* .menu-toggle {
    display: block;
  } */

  span {
    color: #fff;
  }

  .nav-list {
    flex-direction: column;
    position: absolute;
    top: 60px;
    left: 50%;
    transform: translateX(-50%);
    background-color: rgba(255, 255, 255, 0.9);
    box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
    border-radius: 10px;
    padding: 1rem;
    gap: 1rem;
  }
}

@media (min-width: 800px) and (max-width: 950px) {
  .header-logo {
    display: none;
  }

  .header-nav {
    justify-content: center;
  }
}
</style>
