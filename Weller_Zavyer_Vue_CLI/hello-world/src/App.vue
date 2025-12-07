<template>
  <div id="app">
    <nav class="navbar navbar-dark py-3">
      <div class="container d-flex align-items-center">
        <router-link to="/" class="navbar-brand main-title mb-0">Zavyer Weller</router-link>
        <div class="ms-auto d-flex gap-3 align-items-center">
          <router-link to="/" class="nav-link text-light">Home</router-link>
          <router-link to="/about" class="nav-link text-light">About</router-link>
          <router-link to="/portfolio" class="nav-link text-light">Portfolio</router-link>
        </div>
      </div>
    </nav>
    <router-view/>
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=Roboto:wght@300;400;700&display=swap');

:root {
  --primary-bg: #0a192f;
  --secondary-bg: #112240;
  --secondary-text: #8892b0;
  --tea-green: hsla(75, 83%, 84%, 1);
  --accent-color: var(--tea-green);
  --accent-hover: hsla(75, 83%, 74%, 1);
  --main-text: #e6f1ff;
  --card-bg: rgba(17, 34, 64, 0.5);
  --shadow-sm: 0 2px 8px rgba(0, 0, 0, 0.1);
  --shadow-md: 0 4px 16px rgba(0, 0, 0, 0.2);
  --shadow-lg: 0 8px 32px rgba(0, 0, 0, 0.3);
  --shadow-accent: 0 0 20px rgba(204, 214, 161, 0.3);
  --transition-normal: 0.3s ease;
}

#app {
  font-family: 'Inter', 'Roboto', Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-color: var(--primary-bg);
  color: var(--secondary-text);
  min-height: 100vh;
}

.navbar {
  background-color: rgba(10, 25, 47, 0.8);
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(10px);
  border-bottom: 1px solid rgba(136, 146, 176, 0.1);
  position: sticky;
  top: 0;
  z-index: 1000;
  transition: all var(--transition-normal);
}

.navbar .navbar-brand {
  color: var(--main-text);
  font-weight: 700;
  font-size: 1.5rem;
  letter-spacing: -0.5px;
  transition: all var(--transition-normal);
  text-decoration: none;
}

.navbar .navbar-brand:hover {
  color: var(--accent-color);
  transform: translateY(-2px);
}

.nav-link {
  color: var(--secondary-text) !important;
  font-weight: 500;
  font-size: 0.95rem;
  padding: 0.5rem 1rem !important;
  border-radius: 6px;
  transition: all var(--transition-normal);
  position: relative;
  text-decoration: none;
}

.nav-link::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 50%;
  width: 0;
  height: 2px;
  background-color: var(--accent-color);
  transition: all var(--transition-normal);
  transform: translateX(-50%);
}

.nav-link:hover {
  color: var(--accent-color) !important;
  background-color: rgba(204, 214, 161, 0.1);
}

.nav-link:hover::after {
  width: 80%;
}

.nav-link.router-link-exact-active {
  color: var(--accent-color) !important;
}

.nav-link.router-link-exact-active::after {
  width: 80%;
}
</style>
