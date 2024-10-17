<script setup>
import moment from 'moment';
import Avatar from './components/Avatar.vue';
import Profile from './components/Profile.vue';
import FloatingNav from './components/FloatingNav.vue';

const today = moment(new Date()).format('dddd, DD MMMM YYYY');
</script>

<template>
  <header>
    <h1>Daily Quest</h1>
    <p>{{ today }}</p>
  </header>

  <main>
    <!-- <TheWelcome /> -->
    <Avatar />
    <Profile />
  </main>

  <FloatingNav />
</template>

<style scoped>
header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  /* border: 1px solid red; */
}

@media (min-width: 1024px) {
  header {
    width: 1024px;
  }

  header h1 {
    font-size: 64px;
    font-weight: 600;
  }

  header p {
    font-size: 20px;
  }

  main {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 28px;
  }
}
</style>
