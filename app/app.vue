<script setup lang="ts">
const title = 'SuperQuery — High-Integrity Blockchain Infrastructure'
const description = 'A high-integrity indexing framework designed for the most demanding blockchain data pipelines. Performance of Rust, familiarity of SubQuery.'

useHead({
  meta: [
    { name: 'viewport', content: 'width=device-width, initial-scale=1' }
  ],
  link: [
    { rel: 'icon', href: '/superquery-app-icon.svg', type: 'image/svg+xml' }
  ],
  htmlAttrs: {
    lang: 'en'
  }
})

useSeoMeta({
  title,
  description,
  ogTitle: title,
  ogDescription: description,
  ogImage: '/superquery-mark.svg',
  twitterCard: 'summary_large_image'
})

const primaryNav = [
  { label: 'SDK', to: '/sdk' },
  { label: 'Documentation', to: '/docs' },
  { label: 'Examples', to: '/examples' },
  { label: 'Portal', to: '/portal' },
  { label: 'Roadmap', to: '/roadmap' },
  { label: 'Status', to: '/status' }
]

const footerDevelopers = [
  { label: 'Documentation', to: '/docs' },
  { label: 'SDK Reference', to: '/sdk' },
  { label: 'Rust Handlers', to: '/docs#handlers' },
  { label: 'GitHub Repository', to: 'https://github.com/superquery/superquery-sdk', target: '_blank' }
]

const footerCommunity = [
  { label: 'Discord Community', to: 'https://discord.gg/superquery', target: '_blank' },
  { label: 'Grants & Ecosystem', to: '/grants' },
  { label: 'Status Dashboard', to: '/status' },
  { label: 'Changelog', to: '/changelog' }
]

const email = ref('')
</script>

<template>
  <UApp>
    <header class="sticky top-0 z-50 border-b border-cool-border bg-cloud-gray/85 backdrop-blur-md">
      <div class="container-content flex h-16 items-center justify-between gap-8">
        <NuxtLink to="/" class="flex items-center gap-2 text-deep-ink">
          <AppLogo variant="mark" class="h-8 w-8 shrink-0" />
          <span class="font-display text-xl font-bold tracking-tight">SuperQuery</span>
        </NuxtLink>

        <nav class="hidden items-center gap-8 md:flex">
          <NuxtLink
            v-for="item in primaryNav"
            :key="item.to"
            :to="item.to"
            class="text-sm text-neutral-600 transition-colors hover:text-primary-600"
            active-class="!text-primary-600 border-b-2 border-primary-600 font-semibold"
          >
            {{ item.label }}
          </NuxtLink>
        </nav>

        <div class="flex items-center gap-2">
          <UButton
            to="https://github.com/superquery/superquery-sdk"
            target="_blank"
            icon="i-simple-icons-github"
            variant="ghost"
            color="neutral"
            aria-label="GitHub"
            class="hidden sm:inline-flex"
          />
          <UButton
            to="/sdk"
            color="primary"
            class="border border-deep-ink font-mono text-xs uppercase tracking-wider"
          >
            Get started
          </UButton>
        </div>
      </div>
    </header>

    <UMain>
      <NuxtPage />
    </UMain>

    <footer class="border-t border-cool-border bg-white pt-16 pb-8">
      <div class="container-content grid grid-cols-1 gap-8 md:grid-cols-4">
        <div class="space-y-3">
          <NuxtLink to="/" class="flex items-center gap-2 text-deep-ink">
            <AppLogo variant="mark" class="h-6 w-6" />
            <span class="font-display text-lg font-bold">SuperQuery</span>
          </NuxtLink>
          <p class="text-sm text-neutral-600">
            High-performance indexing infrastructure for the decentralized web.
          </p>
        </div>

        <div>
          <h4 class="eyebrow mb-4 text-deep-ink">
            Developers
          </h4>
          <ul class="space-y-2">
            <li v-for="item in footerDevelopers" :key="item.label">
              <NuxtLink
                :to="item.to"
                :target="item.target"
                class="text-sm text-neutral-600 transition-colors hover:text-primary-600"
              >
                {{ item.label }}
              </NuxtLink>
            </li>
          </ul>
        </div>

        <div>
          <h4 class="eyebrow mb-4 text-deep-ink">
            Community
          </h4>
          <ul class="space-y-2">
            <li v-for="item in footerCommunity" :key="item.label">
              <NuxtLink
                :to="item.to"
                :target="item.target"
                class="text-sm text-neutral-600 transition-colors hover:text-primary-600"
              >
                {{ item.label }}
              </NuxtLink>
            </li>
          </ul>
        </div>

        <div>
          <h4 class="eyebrow mb-4 text-deep-ink">
            Newsletter
          </h4>
          <form
            class="flex flex-col gap-2"
            @submit.prevent
          >
            <UInput
              v-model="email"
              type="email"
              placeholder="email@infrastructure.com"
              class="w-full"
              :ui="{ base: 'border border-cool-border bg-white rounded-sm' }"
            />
            <UButton
              type="submit"
              block
              class="bg-deep-ink font-mono text-xs uppercase tracking-wider text-white hover:bg-deep-ink/90"
            >
              Subscribe
            </UButton>
          </form>
        </div>
      </div>

      <div class="container-content mt-12 flex flex-col items-center justify-between gap-4 border-t border-cool-border pt-6 md:flex-row">
        <p class="text-xs text-neutral-600">
          © {{ new Date().getFullYear() }} SuperQuery. Built for high-integrity infrastructure.
        </p>
        <div class="flex items-center gap-6 text-neutral-600">
          <UButton
            to="https://github.com/superquery/superquery-sdk"
            target="_blank"
            icon="i-simple-icons-github"
            variant="ghost"
            color="neutral"
            size="sm"
            aria-label="GitHub"
          />
          <UButton
            to="https://discord.gg/superquery"
            target="_blank"
            icon="i-simple-icons-discord"
            variant="ghost"
            color="neutral"
            size="sm"
            aria-label="Discord"
          />
          <UButton
            to="/status"
            icon="i-lucide-activity"
            variant="ghost"
            color="neutral"
            size="sm"
            aria-label="Network status"
          />
        </div>
      </div>
    </footer>
  </UApp>
</template>
