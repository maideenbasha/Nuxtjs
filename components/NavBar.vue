<template>
    <div class="nav">
      <nuxt-link to="/" class="brand">Welcome to Events</nuxt-link>
      <nav>
        <nuxt-link to="/login">Login</nuxt-link>&nbsp;|
        <nuxt-link to="/signup">Signup</nuxt-link>
      </nav>
    </div>
  </template>
  
  <style scoped>
  .brand {
    font-family: 'Montserrat', sans-serif;
    font-weight: 700;
    font-size: 1.5em;
    color: #39b982;
    text-decoration: none;
  }
  .nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 60px;
  }

  .nav .nav-item.router-link-exact-active {
    color: #39b982;
    border-bottom: solid 2px #39b982;
  }
  
  </style>