<script setup lang="ts">
const title = 'Roadmap — SuperQuery'
useSeoMeta({ title })
</script>

<template>
  <section class="py-[100px]">
    <div class="container-content max-w-3xl text-center">
      <span class="eyebrow text-rust-orange">In progress</span>
      <h1 class="mt-6 font-display text-5xl font-bold tracking-tight text-deep-ink">
        Roadmap<span class="text-signal-red">.</span>
      </h1>
      <p class="mt-6 text-lg text-neutral-600">
        This page is being built from the SuperQuery design handoff.
      </p>
      <UButton
        to="/"
        icon="i-lucide-arrow-left"
        variant="outline"
        class="mt-10 border border-cool-border font-mono text-xs uppercase tracking-wider text-deep-ink"
      >
        Back to home
      </UButton>
    </div>
  </section>
</template>
