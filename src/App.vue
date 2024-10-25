<template>
  <div class="background" :class="{ 'show-background': showBackground }">
    <div class="background-image" :style="backgroundStyle" @transitionend="onTransitionEnd"></div>

    <div class="waves-container" :class="{ 'move-up': showTitle }">
      <Wave class="wave wave-left" />
      <Wave class="wave wave-right" />
    </div>

    <div class="svg-container" :class="{ 'show-svg': showContent, 'move-up': showTitle }">
      <svg
        class="first-svg"
        xmlns="http://www.w3.org/2000/svg"
        width="302"
        height="302"
        viewBox="0 0 302 302"
        fill="none"
      >
        <path
          d="M301.946 150.917C301.946 234.267 234.379 301.834 151.029 301.834C67.6786 301.834 0.112122 234.267 0.112122 150.917C0.112122 67.5665 67.6497 0 151 0C234.35 0 301.917 67.5665 301.917 150.917"
          fill="#F5F5F5"
        />
        <path
          d="M249.96 132.845C245.443 138.058 240.316 139.187 233.945 137.16C227.197 135.017 220.478 132.758 213.556 131.339C201.885 128.935 191.053 131.571 182.597 140.085C174.285 148.426 166.755 157.549 158.906 166.324C154.099 171.711 149.465 177.3 144.484 182.542C136.693 190.738 127.744 197.284 116.652 200.701C122.879 206.812 129.25 208.318 135.622 203.365C144.744 196.27 153.346 188.364 161.455 180.081C169.593 171.769 176.66 162.443 184.45 153.784C197.917 138.782 216.626 139.245 234.003 150.193C230.18 154.537 225.517 155.927 220.072 155.087C218.364 154.827 216.713 154.218 215.033 153.871C207.272 152.162 200.234 153.436 194.587 159.344C189.374 164.818 184.363 170.466 179.382 176.113C174.372 181.76 169.709 187.726 164.496 193.2C159.428 198.529 153.896 203.423 148.944 209.447C152.796 208.086 156.734 206.957 160.441 205.277C170.491 200.672 178.6 193.461 186.13 185.554C191.343 180.081 196.382 174.433 201.653 169.046C206.2 164.384 211.355 164.384 216.597 169.104C200.9 184.859 187.839 203.337 167.537 214.081C147.206 224.855 127.744 222.509 109.238 209.708C94.6415 199.601 83.5493 186.134 73.6156 171.653C65.7672 160.213 57.9766 148.745 45.8418 141.186C45.002 140.664 44.4807 138.463 44.8282 137.363C51.4893 116.424 72.7468 106.664 92.9038 115.265C104.778 120.363 114.596 128.385 123.979 137.653C121.691 140.375 119.577 142.837 117.057 145.82C115.146 144.111 113.582 142.373 111.7 141.099C103.677 135.625 96.0316 129.341 87.4012 125.112C75.7298 119.436 64.2612 124.215 58.44 134.814C66.3464 144.661 73.9052 154.218 81.6379 163.689C87.2274 170.552 95.2497 172.667 104.257 169.886C111.729 167.569 117.55 162.82 122.502 156.97C131.915 145.964 141.211 134.843 150.595 123.838C167.044 104.55 187.752 95.1954 213.267 97.6571C231.744 99.4527 248.744 105.882 264.847 114.86C265.223 115.063 265.455 115.526 265.744 115.845C261.168 121.145 256.013 122.158 248.773 118.944C235.567 113.064 222.013 108.807 207.416 108.402C191.575 107.967 177.268 112.254 166.205 123.838C155.46 135.075 145.584 147.181 135.332 158.881C133.247 161.256 131.248 163.66 129.105 165.977C120.359 175.505 109.817 181.529 96.5819 182.108C99.1884 188.393 105.154 191.723 111.613 190.449C119.259 188.972 126.006 185.294 131.277 179.791C140.197 170.495 148.509 160.648 157.111 151.033C162.15 145.414 167.016 139.622 172.344 134.264C184.276 122.274 198.641 117.524 215.468 120.392C227.66 122.477 239.071 126.56 249.903 132.729"
          fill="#A1B4D1"
        />
      </svg>
      <svg
        class="second-svg"
        xmlns="http://www.w3.org/2000/svg"
        width="598"
        height="140"
        viewBox="0 0 598 140"
        fill="none"
      >
        <path
          d="M69.3375 139.971C69.3375 139.971 64.0376 134.671 57 134.497L12.255 17.9286C6.95505 4.05616 0.612549 3.88237 0.265015 3.88237V3.53485H32.9912V3.88237C32.4699 3.88237 24.0711 4.05614 24.0711 11.7598C24.0711 13.4685 24.4187 15.5248 25.4323 17.9286L68.4687 129.864L111.997 17.9286C113.011 15.351 113.359 13.2948 113.359 11.7598C113.359 4.05614 105.134 3.88237 104.612 3.88237V3.53485H136.672V3.88237H136.325C133.921 3.88237 122.945 4.57742 117.992 17.4362L70.5249 140H69.3375V139.971Z"
          fill="#314664"
        />
        <path
          d="M134.645 134.121C135.832 134.121 147.156 133.774 147.156 120.741V17.3786C147.156 4.69355 136.353 4.17226 134.818 4.17226H134.645V3.47717H223.44L227.726 24.0396L225.843 24.7347C225.843 24.7347 221.21 6.89457 206.99 6.89457H172.526C160.71 7.41588 158.48 11.8759 158.48 17.3496V120.365C158.48 126.186 161.057 130.993 174.93 130.993L210.233 130.82C224.453 130.82 230.448 113.675 230.448 113.675H232.157L226.857 134.411L134.645 134.585V134.063V134.121Z"
          fill="#314664"
        />
        <path
          d="M276.207 134.469V133.947C277.394 133.947 288.718 133.6 288.718 120.567L288.197 18.7397C288.197 10.5147 284.432 8.6322 276.381 8.6322L265.926 8.45844C253.936 8.45844 243.799 10.1671 238.5 25.7772H236.791C238.847 17.3785 241.077 8.80598 243.307 0.407227H245.016C245.016 0.407227 249.65 3.50605 255.645 3.50605H332.45C338.618 3.50605 343.252 0.407227 343.252 0.407227H344.961C347.191 8.80598 348.726 17.2047 350.435 25.7772H348.726C343.426 10.1671 333.29 8.45844 321.3 8.45844L310.845 8.6322C302.793 8.6322 299.028 10.5147 299.028 18.7397L299.55 120.567C299.55 133.6 310.874 133.947 312.061 133.947V134.469H276.236H276.207Z"
          fill="#314664"
        />
        <path
          d="M363.12 134.121C364.308 134.121 375.631 133.774 375.631 120.741V17.3786C375.631 4.69355 364.829 4.17226 363.294 4.17226H363.12V3.47717H451.915L456.201 24.0396L454.319 24.7347C454.319 24.7347 449.685 6.89457 435.465 6.89457H401.001C389.185 7.41588 386.955 11.8759 386.955 17.3496V120.365C386.955 126.186 389.533 130.993 403.405 130.993L438.709 130.82C452.929 130.82 458.924 113.675 458.924 113.675H460.633L455.333 134.411L363.12 134.585V134.063V134.121Z"
          fill="#314664"
        />
        <path
          d="M566.051 34.7261C566.051 20.5062 557.826 6.77859 542.043 6.77859H509.982C496.11 6.77859 493.359 11.5862 493.359 17.2336V65.9174H536.395C556.436 65.9174 566.051 50.1625 566.051 34.7261ZM559.188 115.47C542.216 92.8513 529.01 70.2326 507.086 70.2326H506.913C499.875 70.2326 493.359 71.2462 493.359 78.6313V120.625C493.359 133.658 504.683 134.005 505.87 134.005V134.526H470.219V134.005H470.393C471.435 134.005 482.382 133.658 482.73 121.32V16.5964C482.382 4.25897 471.406 3.91142 470.393 3.91142H470.219V3.39014H545.807C568.252 3.39014 579.402 18.4789 579.402 34.4076C579.402 51.7264 566.022 69.8851 539.291 70.2326H531.066C565.356 83.2651 576.999 134.179 597.561 134.179H597.735V134.526L585.05 134.7C573.726 134.7 572.017 132.818 559.159 115.499"
          fill="#314664"
        />
        <path
          d="M235.43 57.7214C234.474 58.793 233.576 59.9225 232.563 60.9651C229.348 64.3536 225.67 67.2207 221.586 69.5087C219.443 70.6961 217.184 71.7097 214.896 72.6075C212.406 73.5922 209.857 74.5189 207.251 75.1851C202.269 76.4883 197.143 76.8648 191.988 76.749C182.547 76.4883 173.424 74.3741 164.33 72.0572C157.264 70.2616 150.168 68.4661 143.044 66.9021C136.875 65.541 130.59 65.0486 124.277 65.512C118.311 65.9754 112.547 67.3655 107.161 70.03C105.307 70.9567 103.627 72.2021 101.861 73.3026C101.629 73.4474 101.368 73.6211 100.905 73.9108C101.05 73.4763 101.108 73.3026 101.195 73.1578C103.396 69.5666 106.408 66.7573 109.854 64.3246C113.677 61.6312 117.963 60.0094 122.365 58.6772C125.696 57.6635 129.142 57.2002 132.618 56.9685C142.667 56.2734 152.427 58.098 162.129 60.3569C169.63 62.1236 177.131 64.006 184.661 65.6568C191.698 67.1918 198.852 67.8289 206.063 67.1628C210.06 66.7863 213.999 66.0912 217.85 64.9038C219.675 64.3536 221.529 63.9192 223.266 63.1662C226.51 61.776 229.667 60.1832 232.852 58.6772C233.634 58.3007 234.387 57.8663 235.169 57.4608C235.256 57.5477 235.314 57.6346 235.401 57.7214"
          fill="#F5F5F5"
        />
        <path
          d="M452.349 57.7214C451.394 58.793 450.496 59.9225 449.482 60.9651C446.268 64.3536 442.589 67.2207 438.506 69.5087C436.363 70.6961 434.104 71.7097 431.816 72.6075C429.325 73.5922 426.777 74.5189 424.17 75.1851C419.189 76.4883 414.063 76.8648 408.908 76.749C399.466 76.4883 390.343 74.3741 381.25 72.0572C374.183 70.2616 367.088 68.4661 359.963 66.9021C353.794 65.541 347.51 65.0486 341.196 65.512C335.23 65.9754 329.467 67.3655 324.08 70.03C322.227 70.9567 320.547 72.2021 318.78 73.3026C318.549 73.4474 318.288 73.6211 317.825 73.9108C317.969 73.4763 318.027 73.3026 318.114 73.1578C320.315 69.5666 323.327 66.7573 326.774 64.3246C330.596 61.6312 334.883 60.0094 339.285 58.6772C342.615 57.6635 346.062 57.2002 349.537 56.9685C359.587 56.2734 369.347 58.098 379.049 60.3569C386.549 62.1236 394.05 64.006 401.58 65.6568C408.618 67.1918 415.771 67.8289 422.983 67.1628C426.979 66.7863 430.918 66.0912 434.77 64.9038C436.594 64.3536 438.448 63.9192 440.186 63.1662C443.429 61.776 446.586 60.1832 449.772 58.6772C450.554 58.3007 451.307 57.8663 452.089 57.4608C452.176 57.5477 452.234 57.6346 452.32 57.7214"
          fill="#F5F5F5"
        />
      </svg>
    </div>

    <div class="content-container" :class="{ 'show-content': showTitle }">
      <h1 class="title">
        Атмосферный <br />
        квартал
      </h1>
      <button class="details-button" @click="showModal = true">Узнать подробности</button>
      <p class="content-container__info-paragraph">
        Застройщик ООО “СЗ СУ1-ЗАТОН”. Проектная декларация размещена на сайте
        <a href="https://наш.дом.рф" target="_blank" class="text-white text-decoration-underline">наш.дом.рф</a>
        <br />

        Политика конфиденциальности
      </p>
    </div>
  </div>
  <GlassModal v-model="showModal" />
</template>

<script>
import GlassModal from "./components/GlassModal.vue";
import Wave from "./components/Wave.vue";
import bg1 from "./assets/bg1.png";
import bg2 from "./assets/bg2.png";

export default {
  components: { Wave, GlassModal },
  data() {
    return {
      showContent: false,
      showTitle: false,
      showModal: false,
      showBackground: false,
      currentImageIndex: 0,
      scale: 1,
      isZooming: false,
      animationComplete: false,
      backgroundImages: [bg1, bg2],
      windowWidth: window.innerWidth,
      windowHeight: window.innerHeight,
    };
  },
  computed: {
    backgroundStyle() {
      const baseScale = this.getBaseScale();
      return {
        backgroundImage: this.showBackground ? `url(${this.backgroundImages[this.currentImageIndex]})` : "none",
        transform: `scale(${this.scale * baseScale})`,
        transition: this.isZooming ? "transform 20s linear" : "opacity 1s ease, background-image 1s ease",
      };
    },
  },
  mounted() {
    this.startAnimation();
    window.addEventListener("resize", this.handleResize);
    this.handleResize();
  },
  beforeUnmount() {
    window.removeEventListener("resize", this.handleResize);
  },
  methods: {
    handleResize() {
      this.windowWidth = window.innerWidth;
      this.windowHeight = window.innerHeight;
    },
    getBaseScale() {
      const aspectRatio = this.windowWidth / this.windowHeight;
      if (aspectRatio > 1.8) {
        return 1.2;
      } else if (aspectRatio < 0.8) {
        return 1.5;
      }
      return 1;
    },
    startAnimation() {
      setTimeout(() => {
        this.showContent = true;
      }, 200);

      setTimeout(() => {
        this.showTitle = true;
      }, 2000);

      setTimeout(() => {
        this.showBackground = true;
        setTimeout(() => {
          this.startZooming();
        }, 1000);
      }, 4000);
    },
    startZooming() {
      if (this.animationComplete) return;

      this.isZooming = true;
      this.scale = 1.3;

      setTimeout(() => {
        this.changeBackground();
      }, 5000);
    },
    changeBackground() {
      this.isZooming = false;

      this.currentImageIndex = 1;

      setTimeout(() => {
        this.isZooming = true;
        this.scale = 1.6;

        setTimeout(() => {
          this.isZooming = false;
          this.animationComplete = true;
        }, 20000);
      }, 1000);
    },
  },
};
</script>

<style scoped>
.background {
  position: relative;
  width: 100%;
  height: 100vh;
  overflow: hidden;
  background-color: #9fb4d2;
}

.background-image {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-size: cover;
  background-position: center;
  opacity: 0;
  will-change: transform;
}

.show-background .background-image {
  opacity: 1;
}

@keyframes slowZoom {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.125);
  }
  100% {
    transform: scale(1.25);
  }
}

.svg-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2rem;
  opacity: 0;
  transform: translateY(20px);
  transition: all 1s cubic-bezier(0.4, 0, 0.2, 1);
  z-index: 10;
}

.svg-container.show-svg {
  opacity: 1;
  transform: translateY(0);
}

.svg-container.move-up {
  transform: translateY(-20vh) scale(0.8);
}

.content-container {
  position: absolute;
  bottom: -100%;
  opacity: 0;
  transition: all 1s cubic-bezier(0.4, 0, 0.2, 1);
  text-align: center;
  z-index: 10;
}

.content-container__info-paragraph {
  color: white;
  margin-top: 2rem;
}

.content-container.show-content {
  bottom: 20%;
  opacity: 1;
}

.content-container.show-content {
  opacity: 1;
  bottom: 10%;
}

.waves-container {
  position: absolute;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  transition: all 1s cubic-bezier(0.4, 0, 0.2, 1);
}

.waves-container.move-up {
  transform: translateY(-20vh) scale(1);
}

.wave {
  position: absolute;
  top: 12-%;
  transition: transform 1s cubic-bezier(0.4, 0, 0.2, 1);
}

.wave-left {
  left: -27%;
  transform-origin: center;
  transform: translateY(-15%) rotate(5deg);
  width: 15%;
}

.wave-right {
  right: -27%;
  transform-origin: center;
  transform: translateY(-15%) rotate(-5deg) scaleX(-1);
  width: 15%;
}

/* Большие экраны */
@media (min-width: 1921px) and (min-height: 1081px) {
  .wave-left,
  .wave-right {
    display: none;
  }
  .content-container.show-content {
    bottom: -20%;
  }
  .svg-container {
    width: 150px;
    height: 350px;
  }
}

/* Комбинированные медиа-запросы для средних и маленьких экранов */
@media (max-width: 1760px) and (max-height: 1760px) {
  .wave-left {
    left: -35%;
    transform: translateY(-5%) rotate(3deg);
  }
  .wave-right {
    right: -35%;
    transform: translateY(-5%) rotate(-3deg) scaleX(-1);
  }
  .content-container.show-content {
    bottom: 15%;
  }
}

@media (max-width: 1560px) and (max-height: 1370px) {
  .wave-left {
    left: -47%;
    transform: translateY(-8%) rotate(3deg);
  }
  .wave-right {
    right: -47%;
    transform: translateY(-8%) rotate(-3deg) scaleX(-1);
  }
  .content-container.show-content {
    bottom: 5%;
  }
}

@media (max-width: 1385px) and (max-height: 920px) {
  .wave-left {
    left: -63%;
    transform: translateY(-8%) rotate(3deg);
  }
  .wave-right {
    right: -63%;
    transform: translateY(-8%) rotate(-3deg) scaleX(-1);
  }
  .content-container.show-content {
    bottom: 2%;
  }
}

@media (max-width: 1260px) {
  .wave-left {
    left: -70%;
  }
  .wave-right {
    right: -70%;
  }
}

@media (max-width: 1095px) {
  .wave-left {
    left: -90%;
  }
  .wave-right {
    right: -90%;
  }
}

@media (max-width: 935px) {
  .wave-left {
    left: -110%;
  }
  .wave-right {
    right: -110%;
  }
  .content-container.show-content {
    bottom: 10%;
  }
}

@media (max-width: 840px) {
  .wave-left {
    left: -130%;
  }
  .wave-right {
    right: -130%;
  }
}

@media (max-width: 740px) {
  .wave-left {
    left: -155%;
  }
  .wave-right {
    right: -155%;
  }
}

@media (max-width: 645px) {
  .wave-left {
    left: -185%;
    transform: translateY(-20%) rotate(5deg);
  }
  .wave-right {
    right: -185%;
    transform: translateY(-20%) rotate(-5deg) scaleX(-1);
  }
}

/* Малые экраны */
@media (max-width: 565px), (max-height: 750px) {
  .wave-left,
  .wave-right {
    display: none;
  }
  .content-container.show-content {
    bottom: 15%;
  }
  .svg-container {
    width: 150px;
    height: 275px;
    margin-bottom: 110px;
  }

  .title {
    font-size: 35px !important;
  }
}

.title {
  font-size: 3rem;
  color: white;
  margin-bottom: 2rem;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
  text-transform: uppercase;
  font-weight: 400;
}

.details-button {
  padding: 1rem 2rem;
  font-size: 1.2rem;
  background-color: #314664;
  border: 2px solid white;
  border-radius: 0px;
  font-size: 16px;
  color: white;
  cursor: pointer;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.details-button:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 8px rgba(0, 0, 0, 0.2);
}

.first-svg,
.second-svg {
  opacity: 0;
  transform: translateY(20px);
  animation: fadeInUp 1s cubic-bezier(0.4, 0, 0.2, 1) forwards;
}

.second-svg {
  animation-delay: 0.5s;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@media (max-width: 768px) {
  .content-container {
    padding: 1rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    height: 100vh;
  }

  .background-image {
    background-position: center center;
  }

  .content-container {
    padding-top: 40rem;
  }
}

@media (max-width: 480px) {
  .title {
    font-size: clamp(1.5rem, 4vw, 2.5rem);
  }

  .details-button {
    padding: 0.5rem 1rem;
    font-size: 1rem;
  }
}

@media (max-height: 950px) and (max-width: 768px) {
  .content-container {
    padding-top: 210rem;
  }

  .title {
    font-size: 2rem;
  }
}

@media (max-height: 500px) and (orientation: landscape) {
  .content-container {
    padding: 1rem;
    flex-direction: row;
    align-items: center;
    gap: 2rem;
  }

  .title {
    margin-bottom: 0;
  }
}

@media (min-width: 1920px) {
  .title {
    font-size: clamp(3rem, 4vw, 5rem);
  }

  .content-container {
    padding: 3rem;
  }
}
</style>
