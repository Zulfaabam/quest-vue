<script setup>
const navItems = [
  {
    path: '/',
    icon: '/src/assets/icons/home.svg',
  },
  {
    path: '/achievement',
    icon: '/src/assets/icons/trophy.svg',
  },
  {
    path: '/profile',
    icon: '/src/assets/icons/user.svg',
  },
];
</script>

<template>
  <nav class="floating-nav pixel-corners--dark-purple">
    <ul>
      <li v-for="item in navItems">
        <a :href="item.path">
          <img :src="item.icon" alt="icon" width="36" height="36" />
        </a>
      </li>
    </ul>
  </nav>
</template>

<style>
.floating-nav {
  position: fixed;
  bottom: 48px;
  left: 50%;
  transform: translateX(-50%);
  width: 500px;
  height: 80px;
  background-color: var(--gray);
}

.floating-nav ul {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  height: 100%;
}
</style>
