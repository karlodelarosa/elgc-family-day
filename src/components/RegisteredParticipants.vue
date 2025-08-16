<script setup>
import { computed, toRef } from 'vue'

const props = defineProps({
  totalSlots: { type: Number, default: 100 },
  registeredSlots: { type: Number, default: 44 },
  size: { type: Number, default: 30 },
  showLabel: { type: Boolean, default: true },
  sheetUrl: { type: String, default: 'https://docs.google.com/spreadsheets/d/1AyWIxlx25UlXicoSUVi2mvwTHiEdUhDTtbnHjWTRadI/edit?usp=sharing' }
})

const total = toRef(props, 'totalSlots')
const registered = toRef(props, 'registeredSlots')

const slots = computed(() =>
  Array.from({ length: total.value }, (_, i) => ({
    id: i + 1,
    taken: i < registered.value
  }))
)
</script>

<template>
  <div class="w-full">
    <h3 class="text-2xl font-bold text-gray-700 mb-4 text-center">Participants</h3>

    <div class="max-w-3xl mx-auto">
      <!-- Gradient for taken slots -->
      <svg width="0" height="0" class="absolute">
        <defs>
          <linearGradient id="slotGradient" x1="0" x2="1" y1="0" y2="1">
            <stop offset="0" stop-color="#FB923C" />
            <stop offset="0.5" stop-color="#EC4899" />
            <stop offset="1" stop-color="#7C3AED" />
          </linearGradient>
        </defs>
      </svg>

      <!-- Participant icons -->
      <div
        class="flex flex-row flex-wrap items-center gap-1 py-1"
        role="list"
        :aria-label="`${registered}/${total} participants registered`"
      >
        <template v-for="slot in slots" :key="slot.id">
          <svg
            role="listitem"
            :width="size"
            :height="size"
            viewBox="0 0 24 24"
            class="flex-shrink-0 transition-transform duration-300"
            :class="slot.taken ? 'scale-110' : 'scale-100'"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              :fill="slot.taken ? 'url(#slotGradient)' : '#E5E7EB'"
              d="M12 12a4 4 0 1 0 0-8 4 4 0 0 0 0 8zm0 2c-4.418 0-8 2.239-8 5v1h16v-1c0-2.761-3.582-5-8-5z"
            />
          </svg>
        </template>
      </div>

      <!-- Label and link -->
      <div class="mt-4 text-center">
        <p v-if="showLabel" class="text-sm text-gray-600 mb-2">
          <span class="font-semibold text-purple-700">{{ registered }}/{{ total }}</span> are registered.
        </p>
        <a
          :href="sheetUrl"
          target="_blank"
          rel="noopener"
          class="inline-flex items-center mt-3 gap-1 px-3 py-1.5 text-sm font-medium text-white bg-orange-400 hover:bg-orange-500 rounded-full shadow-sm transition-colors"
        >
          <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
              d="M14 3h7m0 0v7m0-7L10 14m-4 7h4a2 2 0 002-2v-4"/>
          </svg>
          Open Registration List
        </a>
      </div>
    </div>
  </div>
</template>

<style scoped>
div[role="list"]::-webkit-scrollbar {
  height: 6px;
}
div[role="list"]::-webkit-scrollbar-thumb {
  background: rgba(0,0,0,0.08);
  border-radius: 999px;
}
</style>
