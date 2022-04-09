<template>
  <my-container>
        <div class="navbar">
            <div class="logo">
                <img src="../assets/Foodieland.svg" alt="">
            </div>
            <nav class="menu">
                <router-link class="menu-items" to="/">Home</router-link>
                <router-link class="menu-items" to="/recipes">Recipes</router-link>
                <router-link class="menu-items" to="/blog">Blog</router-link>
                <router-link class="menu-items" to="/contact">Contact</router-link>
                <router-link class="menu-items" to="/about">About us</router-link>
            </nav>
            <div class="socials">
                <a href="" class="social-media">
                    <img src="../assets/socialMedia/facebook.svg" alt="">
                </a>
                <a href="" class="social-media">
                    <img src="../assets/socialMedia/twitter.svg" alt="">
                </a>
                <a href="" class="social-media">
                    <img src="../assets/socialMedia/instagram.svg" alt="">
                </a>
            </div>
        </div>
    <router-view/>
  </my-container>
</template>

<script>
export default {
    name: 'my-navbar',
}
</script>

<style scoped>
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.navbar::after {
    position: absolute;
    content: '';
    top: 70px;
    height: 1px;
    left: 0;
    right: 0;
    background: rgba(0, 0, 0, 0.1);
}
.menu-items {
    margin: 0 10px;
    text-decoration: none;
}
.socials a {
    margin: 0 10px;
}
.menu {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #FF7967;
}
</style>