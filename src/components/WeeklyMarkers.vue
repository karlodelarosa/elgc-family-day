<script setup>
import { computed } from 'vue'

// Constants
const startDate = new Date('2025-08-03')
const today = new Date()
const msInWeek = 7 * 24 * 60 * 60 * 1000

// Current week (clamped between 1 and 40)
const currentWeek = computed(() => {
  const diff = Math.floor((today - startDate) / msInWeek) + 1
  return Math.min(Math.max(diff, 1), 40)
})

// Generate weeks with date ranges
const weeks = computed(() => {
  const result = []
  for (let i = 0; i < 40; i++) {
    const start = new Date(startDate.getTime() + i * msInWeek)
    const end = new Date(start.getTime() + msInWeek - 1)
    result.push({
      number: i + 1,
      start,
      end,
    })
  }
  return result
})

// Format dates (Aug 3–Aug 9)
const formatDate = (date) => {
  return date.toLocaleDateString('en-US', {
    month: 'short',
    day: 'numeric',
  })
}
</script>

<template>
  <!-- Weekly Contribution Tracker -->
  <div class="relative z-10 mb-12">
    <h3 class="text-2xl font-bold text-purple-700 mb-2">Weekly Contribution Plan</h3>
    <p class="text-gray-700 mb-4 text-sm">
      ₱50 per week • 40 weeks • Started August 3, 2025
    </p>

    <!-- Week Boxes with Date Ranges -->
    <div class="grid grid-cols-2 sm:grid-cols-4 lg:grid-cols-5 gap-4">
      <div
        v-for="week in weeks"
        :key="week.number"
        class="border rounded p-2 text-xs text-center transition-all duration-300"
        :class="week.number === currentWeek
          ? 'bg-gradient-to-r from-orange-400 via-pink-400 to-purple-400 text-white font-semibold shadow-sm border border-purple-400'
          : 'border border-gray-300 bg-white text-gray-600'"
      >
        <div>Week {{ week.number }}</div>
        <div class="raleway">{{ formatDate(week.start) }} – {{ formatDate(week.end) }}</div>
      </div>
    </div>



    <!-- Contribution Info -->
    <div class="mt-6 p-4 bg-purple-50 border-l-4 border-purple-300 rounded">
      <p class="text-sm font-medium bg-gradient-to-r from-orange-400 via-pink-500 to-purple-600 bg-clip-text text-transparent animate-gradient">
        We're now on <span class="font-semibold">Week {{ currentWeek }}</span>
        ({{ formatDate(weeks[currentWeek - 1].start) }} – {{ formatDate(weeks[currentWeek - 1].end) }}).
        By now, you should have contributed:
        <span class="font-bold">₱{{ currentWeek * 50 }}</span>
      </p>
    </div>
  </div>
</template>
