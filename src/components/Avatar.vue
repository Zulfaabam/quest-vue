<template>
  <div class="avatar pixel-corners--lighter-purple">
    <img src="../assets/abam-pixel.png" alt="avatar image" />
  </div>
</template>

<style>
.avatar {
  width: 120px;
  height: 120px;
  background-color: rgb(232, 232, 232);
  display: flex;
  justify-content: center;
  align-items: center;
}

.avatar img {
  width: 45px;
  aspect-ratio: 9 / 16;
  object-fit: contain;
}

@media (min-width: 1024px) {
  .avatar {
    width: 180px;
    height: 180px;
  }

  .avatar img {
    width: 90px;
  }
}
</style>
