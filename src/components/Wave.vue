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
  width: 100%;
}

.image-reveal {
  position: relative;
  width: 73vw; /* Относительно viewport width */
  height: 20.5vw; /* Сохраняем пропорцию 2:1 */
  overflow: hidden;
}

img {
  width: 100%;
  height: 100%;
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

/* Для очень больших экранов */
@media (min-width: 2560px) {
  .image-reveal {
    width: 70vw;
    height: 20vw;
  }
}

/* Для маленьких экранов */
@media (max-width: 768px) {
  .image-reveal {
    width: 75vw;
    height: 20vw;
  }
  .animations-container {
    gap: 1rem;
  }
}
</style>
