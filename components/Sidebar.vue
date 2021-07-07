<template>
  <nav>
    <ul>
      <li><NuxtLink to='/'>管理者トップ</NuxtLink></li>
      <li><NuxtLink to='/customer'>お客様情報</NuxtLink></li>
      <li><NuxtLink to='/abc'>メニューその2</NuxtLink></li>
      <li><NuxtLink to='/abc'>メニューその3</NuxtLink></li>
    </ul>
  </nav>
</template>

<style>
  nav {
    width: 240px;
    height: calc(100vh - 50px);
    color: #fff;
    background-color: #343434;
    
  }
  li {
    height: 64px;
    line-height: 64px;
  }
  a {
    color: #fff;
  }
  li a.nuxt-link-exact-active {
    background-color: #666;
    pointer-events: none;
  }
</style>
