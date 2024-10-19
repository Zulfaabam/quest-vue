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
  <nav class="floating-nav">
    <ul class="pixel-corners--dark-purple">
      <li v-for="item in navItems">
        <a :href="item.path">
          <img :src="item.icon" alt="icon" />
        </a>
      </li>
    </ul>
  </nav>
</template>

<style>
.floating-nav {
  position: fixed;
  bottom: 16px;
  left: 50%;
  transform: translateX(-50%);
  width: 320px;
  height: 51.2px;
  filter: drop-shadow(0px 4px 4px rgb(232, 232, 232, 0.5));
  animation: bounce 1s ease-in-out infinite;
}

.floating-nav ul {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  height: 100%;
  background-color: var(--gray);
}

.floating-nav ul li a img {
  width: 23px;
  height: 23px;
}

@media (min-width: 1024px) {
  .floating-nav {
    bottom: 48px;
    width: 500px;
    height: 80px;
  }
}

@keyframes bounce {
  0% {
    bottom: 48px;
  }
  25% {
    bottom: 48.5px;
  }
  50% {
    bottom: 49px;
  }
  75% {
    bottom: 48.5px;
  }
  100% {
    bottom: 48px;
  }
}
</style>
