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
  font-size: 20px;
  font-weight: 500;
  color: var(--teal);
  line-height: 1;
}

.level {
  font-size: 12px;
  color: var(--light-blue);
}

progress {
  border: none;
  width: 120px;
  height: 10px;
  -webkit-appearance: none;
  appearance: none;
}
progress::-webkit-progress-bar {
  background-color: white;
}
progress::-webkit-progress-value {
  background-color: var(--light-blue);
}
progress::-moz-progress-bar {
  background-color: white;
}

@media (min-width: 1024px) {
  .username {
    font-size: 40px;
  }

  .level {
    font-size: 16px;
  }

  progress {
    width: 150px;
  }
}
</style>
