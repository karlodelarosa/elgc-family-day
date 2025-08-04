<script setup>
import Brand from './components/icons/Brand.vue';
import Countdown from './components/Countdown.vue';
import ImageCarousel from './components/ImageCarousel.vue';
import ProgressPerks from './components/ProgressPerks.vue';
</script>

<template>
  <div class="relative min-h-screen overflow-hidden bg-white">
    <div class="relative z-10 h-screen">
      <div class="background h-screen" style="z-index: -1;">
        <span></span>
        <span></span>
        <span></span>
        <span></span>
        <span></span>
        <span></span>
        <span></span>
        <span></span>
        <span></span>
        <span></span>
        <span></span>
        <span></span>
        <span></span>
        <span></span>
        <span></span>
        <span></span>
        <span></span>
        <span></span>
        <span></span>
        <span></span>
      </div>

      <header class="container mx-auto flex items-center justify-center lg:justify-between p-4">
        <div class="flex flex-col lg:flex-row items-center justify-center">
          <Brand />
          <p class="text-sm text-left raleway lg:hidden">Emmanuel's Living Gospel Church</p>
          <div class="flex flex-col items-start hidden lg:block">
            <p class="text-sm text-left raleway">Emmanuel's</p>
            <p class="text-sm text-left raleway">Living</p>
            <p class="text-sm text-left raleway">Gospel</p>
            <p class="text-sm text-left raleway">Church</p>
          </div>
        </div>

        <div class="flex flex-row gap-8 raleway">
          <div class="bg-blue-300/30 py-1 px-3 text-xs rounded-md hover:bg-blue-300/60 transition-all cursor-pointer">Event Details</div>
          <div class="bg-blue-300/30 py-1 px-3 text-xs rounded-md hover:bg-blue-300/60 transition-all cursor-pointer">Perks</div>
          <div class="bg-blue-300/30 py-1 px-3 text-xs rounded-md hover:bg-blue-300/60 transition-all cursor-pointer">Contact</div>
        </div>

        <a class="hidden lg:block pr-4" href="https://docs.google.com/forms/d/e/1FAIpQLSePEVjMQiBHBggpPCSGhXThAVvLX57KfuFgmBX5LCca3q6m5A/viewform?usp=dialoga" target="_blank" rel="noopener">
          <button class="raleway bg-orange-400 w-fit py-3 px-6 text-white rounded-lg">Sign up now</button>
        </a>
      </header>

      <div class="w-full flex flex-col items-center justify-center">
        <img src="/src/assets/hero2.png" class="w-full lg:w-2/5 xl:w-5/12 floating" alt="Floating Hero" />

        <h1 class="text-4xl text-center text-black/80 font-bold lg:text-6xl text-transparent bg-clip-text text-2xl animated-sunset-text bg-gradient-to-r from-orange-400 via-pink-500 to-purple-600">Family Day 2026</h1>

        <div class="flex flex-col gap-y-6 items-center pt-6 lg:pt-10">
          <div class="flex flex-col items-center justify-center">
            <p class="text-black/80">
              June 13, 2026
            </p>

            <Countdown />
          </div>

          <div class="pt-5 block lg:hidden">
            <a href="https://docs.google.com/forms/d/e/1FAIpQLSePEVjMQiBHBggpPCSGhXThAVvLX57KfuFgmBX5LCca3q6m5A/viewform?usp=dialoga" target="_blank" rel="noopener">
              <button class="raleway bg-orange-400 w-fit py-3 px-6 text-white rounded-lg">Sign up now</button>
            </a>
          </div>
        </div>
      </div>
    </div>

    <div class="relative z-10 h-screen bg-red-100 p-6">
      <div class="container mx-auto h-full">
        <div class="grid grid-cols-2 h-full flex items-center justify-center gap-x-5">
          <div class="flex flex-col gap-y-10 ">
            <h2 class="text-5xl text-black/80 font-bold lg:text-6xl text-transparent bg-clip-text text-2xl animated-sunset-text bg-gradient-to-r from-orange-400 via-pink-500 to-purple-600">More Than Just a Getaway</h2>

            <div class="flex flex-col gap-y-6 text-xl">
              <p class="raleway">
                Church isn’t just what happens inside four walls — it’s a family that grows, laughs, rests, and worships together.
              </p>

              <p class="raleway">
                This Family Day is more than a break from routine — it’s a moment to reconnect with each other, build lasting memories, and enjoy God’s creation. Whether through a quiet moment by the sea or a laugh shared during a game, our goal is simple: to strengthen our bonds as one body in Christ.
              </p>

              <p class="raleway">
                Let’s rest, rejoice, and remember why we’re better together.
              </p>
            </div>

            <div class="raleway">
              <strong class="italic">
                “How good and pleasant it is when God’s people live together in unity!” – Psalm 133:1
              </strong>
            </div>
          </div>

          <div class="lg:pl-10 w-full">
            <img src="https://i.ibb.co/Lhz5psL8/family-1976162-1280-1-1.png" alt="Family" class="w-full floating">
          </div>
        </div>
      </div>
    </div>

    <div class="relative z-10 h-screen">
      <div class="container mx-auto px-6 py-12 bg-white">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
      
          <!-- Image / Placeholder -->
          <div class="aspect-[6/8] bg-gray-100 rounded-xl shadow-inner">
            <ImageCarousel />
          </div>

          <!-- Event Details -->
          <div class="space-y-12">
            <h2 class="text-5xl text-black/80 font-bold lg:text-6xl text-transparent bg-clip-text text-2xl animated-sunset-text bg-gradient-to-r from-orange-400 via-pink-500 to-purple-600">Event Details</h2>

            <div class="space-y-1">
              <h3 class="text-3xl font-semibold text-gray-700">Pinewoods Beach Resort</h3>
              <p class="text-gray-500 text-base">Infanta, Quezon</p>
            </div>

            <div class="space-y-1">
              <p class="text-gray-600">
                <span class="font-medium">Date:</span> June 13–14, 2026 (Saturday–Sunday)
              </p>
            </div>

            <div class="raleway">
              <p class="text-gray-600 font-medium mb-2"><strong>Inclusions:</strong></p>
              <ul class="list-disc list-inside text-gray-700 space-y-1">
                <li>Transit Bus</li>
                <li>Accommodation</li>
                <li>Meals</li>
                <li>Activities</li>
              </ul>
            </div>

            <div class="pt-2 border-t">
              <p class="text-gray-600 text-sm">
                <span class="font-medium">Things to bring:</span> To be announced.
              </p>
            </div>
          </div>

        </div>
      </div>
    </div>

    <div class="relative z-10 h-screen p-6">
      <div class="container mx-auto h-full flex flex-col justify-center items-center">
        <h2
          class="text-5xl pb-4 lg:text-6xl font-bold bg-gradient-to-r from-orange-400 via-pink-500 to-purple-600 bg-clip-text text-transparent animate-gradient"
        >
          Progress Perks
        </h2>

        <ProgressPerks />
      </div>
    </div>

    <div class="relative z-10 h-screen p-6">
  <div class="container mx-auto h-full flex flex-col justify-center items-center text-center space-y-6">
    <h2
      class="text-5xl lg:text-7xl font-extrabold bg-gradient-to-r from-orange-400 via-pink-500 to-purple-600 bg-clip-text text-transparent animate-gradient-slow drop-shadow-md"
    >
      See you there!
    </h2>

    <p class="text-lg text-gray-600 max-w-md raleway">
      Join us in making this Family Day unforgettable — fun, laughter, and surprises await.
    </p>

    <a class="hidden lg:block pr-4" href="https://docs.google.com/forms/d/e/1FAIpQLSePEVjMQiBHBggpPCSGhXThAVvLX57KfuFgmBX5LCca3q6m5A/viewform?usp=dialoga" target="_blank" rel="noopener">
      <button class="raleway bg-orange-400 w-fit py-3 px-6 text-white rounded-lg">Sign up now</button>
    </a>
  </div>
</div>


  </div>
</template>

<style scoped>
.animated-gradient {
  background: linear-gradient(120deg, #ff7eb3, #65d6ce, #ffc371);
  background-size: 200% 200%;
  animation: gradientMove 12s ease-in-out infinite;
  opacity: 0.25;
  mix-blend-mode: overlay;
}

@keyframes gradientMove {
  0% {
    background-position: -100% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: -100% 50%;
  }
}

.floating {
  animation: floatBounce 10s ease-in-out infinite;
}

@keyframes floatBounce {
  0% { transform: translateY(0); }
  25% { transform: translateY(-5px); }
  50% { transform: translateY(0); }
  75% { transform: translateY(5px); }
  100% { transform: translateY(0); }
}

@keyframes move {
    100% {
        transform: translate3d(0, 0, 1px) rotate(360deg);
    }
}
.background {
  position: fixed;
  width: 100vw;
  height: 100vh;
  top: 0;
  left: 0;
  background: white;
  overflow: hidden;
  z-index: 0;
}

.background span {
  width: 7vmin;
  height: 7vmin;
  border-radius: 7vmin;
  backface-visibility: hidden;
  position: absolute;
  animation: move 45s linear infinite;
}

.background span:nth-child(3n+1) {
  color: #FFD1DC;
}

.background span:nth-child(3n+2) {
  color: #C1E1C1; 
}

.background span:nth-child(3n+3) {
  color: #AEE6F9; 
}

.background span:nth-child(0) {
  top: 11%;
  left: 41%;
  animation-duration: 49s;
  animation-delay: -35s;
  transform-origin: 20vw 19vh;
  box-shadow: -40vmin 0 5.14vmin currentColor;
}
.background span:nth-child(1) {
  top: 74%;
  left: 28%;
  animation-duration: 10s;
  animation-delay: -5s;
  transform-origin: 22vw -18vh;
  box-shadow: -40vmin 0 5.38vmin currentColor;
}
.background span:nth-child(2) {
  top: 12%;
  left: 91%;
  animation-duration: 25s;
  animation-delay: -32s;
  transform-origin: -23vw 20vh;
  box-shadow: -40vmin 0 5.65vmin currentColor;
}
.background span:nth-child(3) {
  top: 25%;
  left: 35%;
  animation-duration: 49s;
  animation-delay: -27s;
  transform-origin: 25vw 3vh;
  box-shadow: -40vmin 0 5.94vmin currentColor;
}
.background span:nth-child(4) {
  top: 6%;
  left: 61%;
  animation-duration: 43s;
  animation-delay: -33s;
  transform-origin: -19vw 21vh;
  box-shadow: -40vmin 0 5.24vmin currentColor;
}
.background span:nth-child(5) {
  top: 43%;
  left: 38%;
  animation-duration: 39s;
  animation-delay: -28s;
  transform-origin: 3vw -4vh;
  box-shadow: -40vmin 0 5.05vmin currentColor;
}
.background span:nth-child(6) {
  top: 75%;
  left: 55%;
  animation-duration: 35s;
  animation-delay: -31s;
  transform-origin: -16vw -6vh;
  box-shadow: -40vmin 0 5.83vmin currentColor;
}
.background span:nth-child(7) {
  top: 44%;
  left: 80%;
  animation-duration: 20s;
  animation-delay: -25s;
  transform-origin: 24vw -9vh;
  box-shadow: -40vmin 0 5.55vmin currentColor;
}
.background span:nth-child(8) {
  top: 66%;
  left: 83%;
  animation-duration: 31s;
  animation-delay: -8s;
  transform-origin: -19vw 10vh;
  box-shadow: -40vmin 0 5.98vmin currentColor;
}
.background span:nth-child(9) {
  top: 47%;
  left: 36%;
  animation-duration: 21s;
  animation-delay: -1s;
  transform-origin: -7vw 10vh;
  box-shadow: -40vmin 0 5.4vmin currentColor;
}
.background span:nth-child(10) {
  top: 63%;
  left: 65%;
  animation-duration: 18s;
  animation-delay: -15s;
  transform-origin: 24vw -3vh;
  box-shadow: -40vmin 0 5.66vmin currentColor;
}
.background span:nth-child(11) {
  top: 26%;
  left: 66%;
  animation-duration: 43s;
  animation-delay: -5s;
  transform-origin: -13vw 3vh;
  box-shadow: -40vmin 0 5.46vmin currentColor;
}
.background span:nth-child(12) {
  top: 19%;
  left: 26%;
  animation-duration: 41s;
  animation-delay: -36s;
  transform-origin: 14vw 16vh;
  box-shadow: -40vmin 0 5.52vmin currentColor;
}
.background span:nth-child(13) {
  top: 47%;
  left: 13%;
  animation-duration: 14s;
  animation-delay: -21s;
  transform-origin: 25vw 10vh;
  box-shadow: -40vmin 0 5.09vmin currentColor;
}
.background span:nth-child(14) {
  top: 83%;
  left: 7%;
  animation-duration: 42s;
  animation-delay: -27s;
  transform-origin: -11vw 25vh;
  box-shadow: -40vmin 0 5.98vmin currentColor;
}
.background span:nth-child(15) {
  top: 43%;
  left: 80%;
  animation-duration: 20s;
  animation-delay: -18s;
  transform-origin: 7vw -17vh;
  box-shadow: -40vmin 0 5.11vmin currentColor;
}
.background span:nth-child(16) {
  top: 80%;
  left: 61%;
  animation-duration: 17s;
  animation-delay: -5s;
  transform-origin: -16vw -2vh;
  box-shadow: -40vmin 0 5.34vmin currentColor;
}
.background span:nth-child(17) {
  top: 44%;
  left: 10%;
  animation-duration: 20s;
  animation-delay: -16s;
  transform-origin: 13vw -1vh;
  box-shadow: -40vmin 0 5.42vmin currentColor;
}
.background span:nth-child(18) {
  top: 66%;
  left: 84%;
  animation-duration: 41s;
  animation-delay: -25s;
  transform-origin: 25vw 20vh;
  box-shadow: -40vmin 0 5.15vmin currentColor;
}
.background span:nth-child(19) {
  top: 63%;
  left: 50%;
  animation-duration: 38s;
  animation-delay: -4s;
  transform-origin: -6vw 16vh;
  box-shadow: -40vmin 0 5.01vmin currentColor;
}

@keyframes move {
  100% {
    transform: rotate(360deg);
  }
}

@keyframes sunsetGradientShift {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}

.animated-sunset-text {
  background-size: 200% 200%;
  animation: sunsetGradientShift 5s ease infinite;
}
</style>