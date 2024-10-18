<script setup>
import moment from 'moment';
import Avatar from './components/Avatar.vue';
import Profile from './components/Profile.vue';
import FloatingNav from './components/FloatingNav.vue';
import QuestBar from './components/QuestBar.vue';
import StarIcon from './components/icons/StarIcon.vue';

const today = moment(new Date()).format('dddd, DD MMMM YYYY');

const quests = [
  {
    icon: '/src/assets/icons/run.svg',
    title: 'Run 2 kilometer',
    exp: '100',
  },
  {
    icon: '/src/assets/icons/run.svg',
    title: 'Read 4 pages of the Quran or more',
    exp: '1000',
  },
  {
    icon: '/src/assets/icons/run.svg',
    title: 'Pray the Salah 5 times',
    exp: '2000',
  },
];
</script>

<template>
  <header>
    <div style="position: relative">
      <h1>Daily Quest</h1>
      <StarIcon class="star-bottom" />
      <StarIcon class="star-top" />
    </div>
    <p>{{ today }}</p>
  </header>

  <main>
    <!-- <TheWelcome /> -->
    <Avatar />
    <Profile />
    <div class="quest-wrapper">
      <QuestBar
        v-for="quest in quests"
        :icon="quest.icon"
        :title="quest.title"
        :exp="quest.exp"
      />
    </div>
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

.star-top {
  position: absolute;
  top: -8px;
  right: -20px;
}

.star-bottom {
  position: absolute;
  bottom: -20px;
  left: -20px;
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

  .quest-wrapper {
    margin-top: 28px;
    display: flex;
    flex-direction: column;
    gap: 24px;
  }
}
</style>
