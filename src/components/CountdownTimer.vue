<script setup>
import { onBeforeUnmount, onMounted, reactive } from 'vue'

const targetDate = new Date('2027-01-01T00:00:00')
const timeLeft = reactive({
  days: 0,
  hours: 0,
  minutes: 0,
  seconds: 0,
})

let timerId

function updateCountdown() {
  const remaining = Math.max(0, targetDate.getTime() - Date.now())
  const totalSeconds = Math.floor(remaining / 1000)

  timeLeft.days = Math.floor(totalSeconds / 86400)
  timeLeft.hours = Math.floor((totalSeconds % 86400) / 3600)
  timeLeft.minutes = Math.floor((totalSeconds % 3600) / 60)
  timeLeft.seconds = totalSeconds % 60
}

onMounted(() => {
  updateCountdown()
  timerId = window.setInterval(updateCountdown, 1000)
})

onBeforeUnmount(() => {
  window.clearInterval(timerId)
})
</script>

<template>
  <section class="countdown" aria-label="Countdown to 1 January 2027">
    <p class="countdown-label">The clock is moving</p>
    <div v-if="timeLeft.days || timeLeft.hours || timeLeft.minutes || timeLeft.seconds" class="countdown-grid">
      <div class="countdown-unit">
        <strong>{{ timeLeft.days }}</strong>
        <span>Days</span>
      </div>
      <div class="countdown-unit">
        <strong>{{ String(timeLeft.hours).padStart(2, '0') }}</strong>
        <span>Hours</span>
      </div>
      <div class="countdown-unit">
        <strong>{{ String(timeLeft.minutes).padStart(2, '0') }}</strong>
        <span>Minutes</span>
      </div>
      <div class="countdown-unit">
        <strong>{{ String(timeLeft.seconds).padStart(2, '0') }}</strong>
        <span>Seconds</span>
      </div>
    </div>
    <p v-else class="countdown-complete">We’re here.</p>
  </section>
</template>
