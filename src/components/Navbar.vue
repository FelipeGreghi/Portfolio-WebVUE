<template>
  <nav class="navbar">
    <router-link to="/" class="logo-link">
      <img src="@/assets/logo.png" alt="Logo" id="logo" />
      <p><b>Felipe</b> Greghi</p>
    </router-link>
    <ul class="nav-links">
      <li><router-link to="/">Home</router-link></li>
      <li><router-link to="/about">About Me</router-link></li>
      <li><router-link to="/portfolio">My Portfolio</router-link></li>
      <li><router-link to="/testimonials">Testimonials</router-link></li>
      <li><router-link to="/contact">Contact</router-link></li>
    </ul>
    <router-link to="/work-with-me" class="work-with-me">
      Work With Me
      <span class="work-icon">&#x2197;</span>
    </router-link>
  </nav>
</template>

<script>
export default {
  name: 'Navbar',
}
</script>

<style scoped>
.logo-link {
  display: flex;
  align-items: center;
  text-decoration: none;
}

.logo-link img {
  margin-right: 0.625em;
}

.logo-link p {
  margin: 0;
  font-size: 1.25em;
  text-decoration: none;
  color: #363E3E;
}

.navbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1.25em 5%;
  background-color: #faf8f4;
  font-family: Arial, sans-serif;
  border-bottom: solid 1px #e0e0e0;
}

#logo {
  width: 2.5em;
  height: 2.5em;
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 2.5em;
  margin: 0;
}

.nav-links li {
  display: inline;
}

.nav-links a {
  text-decoration: none;
  color: #363E3E;
  font-weight: bold;
  font-size: 1em;
}

.nav-links a:hover {
  color: #46BABE;
}

.work-with-me {
  background-color: #363E3E;
  color: white;
  padding: 10px 20px;
  border-radius: 50px;
  text-decoration: none;
  font-weight: bold;
  display: flex;
  align-items: center;
  gap: 10px;
  font-size: 1em;
}

.work-with-me .work-icon {
  background-color: #46BABE;
  color: white;
  border-radius: 50%;
  padding: 5px;
  width: 18px;
  height: 18px;
  font-size: 0.875em;
  display: flex;
  align-items: center;
  justify-content: center;
}

.work-with-me:hover {
  background-color: #46BABE;
  color: white;
}

.work-with-me:hover .work-icon {
  background-color: #363E3E;
}

a:active {
  color: #46BABE;
}
</style>