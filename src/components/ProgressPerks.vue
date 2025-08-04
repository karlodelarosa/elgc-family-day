<script setup>
import { ref, onMounted } from 'vue'

const messages = [
  "Be part of something special — Family Day 2026!",
  "Together, let’s make this event unforgettable.",
  "Every contribution brings us closer to the celebration!"
]

const currentIndex = ref(0)
const message = ref(messages[currentIndex.value])

onMounted(() => {
  setInterval(() => {
    currentIndex.value = (currentIndex.value + 1) % messages.length
    message.value = messages[currentIndex.value]
  }, 4000)
})
</script>

<template>
  <div class="w-full sm:px-12 lg:px-24 py-20 lg:bg-gradient-to-br lg:from-indigo-50/40 lg:to-pink-50/40 rounded relative overflow-hidden">
  <div class="grid grid-cols-1 lg:grid-cols-2 gap-24 items-start">

    <!-- Left side: Story -->
    <div class="flex flex-col justify-center space-y-6 relative z-10">
      
      <div>
        <h2 class="text-4xl text-black/70">
          Help Us Reach Our Goals!
        </h2>
        <transition name="fade" mode="out-in">
          <p :key="message" class="text-gray-600">{{ message }}</p>
        </transition>
      </div>
      <p class="text-gray-600 text-lg leading-relaxed max-w-xl raleway">
        Every contribution fuels something special — from fun takeaways to comfortable travel to personalized keepsakes. As we reach each milestone, we unlock a unique reward for everyone involved.
      </p>
      <div class="h-2 w-full bg-gray-200 rounded-full overflow-hidden mt-4">
        <div class="bg-gradient-to-r from-orange-400 via-pink-500 to-purple-500 h-full rounded-full transition-all duration-500" style="width: 1%"></div>
      </div>
      <p class="text-sm text-gray-500 italic">Current progress: 1% funded</p>
    </div>

    <!-- Right side: Cards -->
    <div class="space-y-8">
      <div>
        <h4 class="text-2xl font-semibold text-gray-800">Your Personal Goal</h4>
        <p class="text-gray-600">
          Every member is encouraged to give
          <span class="font-bold text-purple-600">₱1,999.00</span> — a vital step in our shared vision.
        </p>
      </div>
      <!-- Card 1 -->
      <div class="bg-white/70 backdrop-blur-md border-l-8 border-yellow-400 shadow-xl rounded-2xl p-6 transition hover:-translate-y-1 hover:shadow-yellow-300/50">
        <div class="flex items-center gap-4">
          <div class="text-3xl">🎯</div>
          <div>
            <h3 class="text-xl font-bold text-purple-700">Milestone: 50%</h3>
            <p class="text-gray-700 font-semibold">₱1000</p>
            <p class="text-sm text-gray-500">🎁 Family Day Button Pins</p>
          </div>
        </div>
      </div>

      <!-- Card 2 -->
      <div class="bg-white/70 backdrop-blur-md border-l-8 border-green-400 shadow-xl rounded-2xl p-6 transition hover:-translate-y-1 hover:shadow-green-300/50">
        <div class="flex items-center gap-4">
          <div class="text-3xl">🚀</div>
          <div>
            <h3 class="text-xl font-bold text-purple-700">Milestone: 75%</h3>
            <p class="text-gray-700 font-semibold">₱1500</p>
            <p class="text-sm text-gray-500">🚌 Priority Bus Seat Selection</p>
          </div>
        </div>
      </div>

      <!-- Card 3 -->
      <div class="bg-white/70 backdrop-blur-md border-l-8 border-pink-400 shadow-xl rounded-2xl p-6 transition hover:-translate-y-1 hover:shadow-pink-300/50">
        <div class="flex items-center gap-4">
          <div class="text-3xl">🏆</div>
          <div>
            <h3 class="text-xl font-bold text-purple-700">Milestone: 100%</h3>
            <p class="text-gray-700 font-semibold">₱1999</p>
            <p class="text-sm text-gray-500">☕ Customized Mugs (First 20 Only)</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<style scoped>
.fade-enter-active, .fade-leave-active {
  transition: opacity 1s ease;
}
.fade-enter-from, .fade-leave-to {
  opacity: 0;
}
</style>