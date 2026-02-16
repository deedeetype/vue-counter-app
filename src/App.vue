<script setup>
import { ref } from 'vue'

const count = ref(0)

const increment = () => {
  count.value++
}

const reset = () => {
  count.value = 0
}
</script>

<template>
  <div class="min-h-screen bg-gradient-to-br from-slate-900 via-slate-800 to-slate-900 flex items-center justify-center">
    <div class="text-center">
      <h1 class="text-6xl font-bold text-white mb-6">
        vue-counter-app
      </h1>
      <p class="text-xl text-slate-300 mb-8">
        Interactive counter app built with Vue.js 3 and Vite
      </p>
      <div class="flex gap-4 justify-center">
        <button
          @click="increment"
          class="px-8 py-3 bg-green-500 text-white rounded-lg hover:bg-green-600 transition"
        >
          Count: {{ count }}
        </button>
        <button
          @click="reset"
          class="px-8 py-3 bg-white/10 text-white rounded-lg hover:bg-white/20 transition"
        >
          Reset
        </button>
      </div>
    </div>
  </div>
</template>
