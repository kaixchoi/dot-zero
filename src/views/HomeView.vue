<script setup>
import BrandMark from '../components/BrandMark.vue'
import CountdownTimer from '../components/CountdownTimer.vue'
import NotifyForm from '../components/NotifyForm.vue'
</script>

<template>
  <main class="landing-shell">
    <header class="site-header page-grid">
      <BrandMark />
      <span class="header-status"><i></i> Launching soon</span>
    </header>

    <section class="hero page-grid">
      <div class="hero-copy">
        <p class="eyebrow reveal reveal-delay-1">A new starting point</p>
        <h1 class="reveal reveal-delay-2">Make room<br /><em>for what’s next.</em></h1>
        <p class="hero-intro reveal reveal-delay-3">
          Dot Zero is a new kind of creative studio for ideas that deserve a little more space to become real.
        </p>
        <CountdownTimer />
        <NotifyForm />
      </div>

      <div class="hero-art reveal reveal-delay-2" aria-label="Abstract blue and orange orbital artwork" role="img">
        <div class="orbit orbit-large"></div>
        <div class="orbit orbit-small"></div>
        <div class="core"><span>0</span></div>
        <span class="art-label art-label-top">01 / 01</span>
        <span class="art-label art-label-bottom">Begin anywhere</span>
      </div>
    </section>

    <footer class="site-footer page-grid">
      <span>© 2026 Dot Zero</span>
      <span>Ideas in progress</span>
      <a href="mailto:hello@dotzero.studio">hello@dotzero.studio <span aria-hidden="true">&#8599;</span></a>
    </footer>
  </main>
</template>
