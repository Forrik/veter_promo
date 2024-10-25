<template>
  <div class="animations-container">
    <div class="reveal-container">
      <div class="image-reveal clip-path">
        <img src="../assets/Vector2.png" alt="Wave image" />
      </div>
    </div>
  </div>
</template>

<style scoped>
.animations-container {
  display: flex;
  flex-direction: column;
  gap: 2rem;
  padding: 1rem;
}

.reveal-container {
  width: 400px;
}

.image-reveal {
  position: relative;
  width: 1400px;
  height: 700px;
  overflow: hidden;
}

img {
  object-fit: cover;
}

.clip-path img {
  clip-path: inset(0 100% 0 0);
  animation: revealClip 1s ease-out forwards;
}

@keyframes revealClip {
  0% {
    clip-path: inset(0 100% 0 0);
  }
  100% {
    clip-path: inset(0 0 0 0);
  }
}
</style>
