<template>
  <div class="flex gap-2 text-center">
    <div v-for="(value, label) in timeLeft" :key="label" class="flex flex-col items-center">
      <div class="p-4 bg-[#DBEAFF]/40 rounded-md w-20 lg:w-24 lg:p-6 text-2xl lg:text-3xl lg:p-6">
        {{ value }}
      </div>
      <div class="mt-1 text-xs uppercase tracking-wide raleway uppercase font-bold text-red-700">
        {{ label }}
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const targetDate = new Date('2026-06-13T00:00:00')

const timeLeft = ref({
  Days: '00',
  Hours: '00',
  Minutes: '00',
  Seconds: '00',
})

const updateCountdown = () => {
  const now = new Date()
  const diff = targetDate - now

  if (diff <= 0) {
    timeLeft.value = {
      Days: '00',
      Hours: '00',
      Minutes: '00',
      Seconds: '00',
    }
    return
  }

  const totalSeconds = Math.floor(diff / 1000)
  const days = Math.floor(totalSeconds / (3600 * 24))
  const hours = Math.floor((totalSeconds % (3600 * 24)) / 3600)
  const minutes = Math.floor((totalSeconds % 3600) / 60)
  const seconds = totalSeconds % 60

  timeLeft.value = {
    Days: String(days).padStart(2, '0'),
    Hours: String(hours).padStart(2, '0'),
    Minutes: String(minutes).padStart(2, '0'),
    Seconds: String(seconds).padStart(2, '0'),
  }
}

let interval
onMounted(() => {
  updateCountdown()
  interval = setInterval(updateCountdown, 1000)
})
onUnmounted(() => {
  clearInterval(interval)
})
</script>
