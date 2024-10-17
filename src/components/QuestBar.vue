<script setup>
const props = defineProps(['title', 'exp', 'icon']);
</script>

<template>
  <div class="quest-bar pixel-corners">
    <div class="quest-details">
      <div class="quest-icon--wrapper">
        <img :src="icon" alt="icon" />
      </div>
      <div>
        <p class="quest-title">{{ title }}</p>
        <p class="quest-exp">+ {{ exp }} exp</p>
      </div>
    </div>
    <div>
      <button>Achieved</button>
      <span>/</span>
      <button>Not achieved</button>
    </div>
  </div>
</template>

<style>
.quest-bar {
  background-color: var(--gray-purple);
  width: 916px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 72px;
  /* margin-top: 40px; */
}
.quest-details {
  display: flex;
  align-items: center;
  gap: 20px;
}
.quest-icon--wrapper {
  background-color: var(--lighter-purple);
  width: 48px;
  height: 48px;
  transform: rotate(45deg);
  display: flex;
  justify-content: center;
  align-items: center;
}
.quest-icon--wrapper img {
  transform: rotate(-45deg);
}
.quest-title {
  font-size: 20px;
}
.quest-exp {
  font-size: 14px;
  color: var(--light-blue);
}
</style>
