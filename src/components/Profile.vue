<template>
  <div class="profile-wrapper">
    <h2 class="username">Abam</h2>
    <progress value="50" max="100"></progress>
    <p class="level">Level 1</p>
  </div>
</template>

<style>
.profile-wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 4px;
  margin-top: 12px;
}

.username {
  font-size: 40px;
  font-weight: 500;
  color: var(--teal);
  line-height: 1;
}

.level {
  font-size: 16px;
  color: var(--light-blue);
}
</style>
