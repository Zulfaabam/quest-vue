<script setup>
const props = defineProps(['title', 'exp', 'icon']);
</script>

<template>
  <div class="quest-bar pixel-corners">
    <div class="quest-details">
      <div class="quest-icon--wrapper">
        <img :src="icon" alt="icon" />
      </div>
      <div class="quest-details--text">
        <div>
          <p class="quest-title">{{ title }}</p>
          <p class="quest-exp">+ {{ exp }} exp</p>
        </div>
        <div>
          <button class="quest-btn achieved">Achieved</button>
          <span>/</span>
          <button class="quest-btn not-achieved">Not achieved</button>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.quest-bar {
  background-color: var(--gray-purple);
  width: 320px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-direction: column;
  padding: 10px 28px;
}
.quest-details {
  display: flex;
  align-items: center;
  gap: 20px;
  width: 100%;
}
.quest-icon--wrapper {
  background-color: var(--lighter-purple);
  transform: rotate(45deg);
  display: flex;
  justify-content: center;
  align-items: center;
}
.quest-icon--wrapper img {
  transform: rotate(-45deg);
}
.quest-title {
  font-size: 16px;
}
.quest-exp {
  font-size: 12px;
  color: var(--light-blue);
}
.quest-btn {
  font-size: 14px;
  border: none;
  background: none;
  font-family: var(--pixel-font);
  cursor: pointer;
  padding: 0;
}
.achieved {
  color: var(--teal);
  margin-right: 2px;
}
.not-achieved {
  color: #f97676;
  margin-left: 2px;
}

@media (min-width: 1024px) {
  .quest-bar {
    width: 916px;
    padding: 10px 72px;
    flex-direction: row;
  }
  .quest-title {
    font-size: 20px;
  }
  .quest-exp {
    font-size: 14px;
  }
  .quest-btn {
    font-size: 20px;
  }
  .quest-details--text {
    display: flex;
    justify-content: space-between;
    width: 100%;
    align-items: center;
  }
  .quest-icon--wrapper {
    width: 48px;
    height: 48px;
  }
}
</style>
