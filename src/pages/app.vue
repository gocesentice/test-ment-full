<script setup lang="ts">
/**
 * This is a Vue Component that will be
 * automatically mapped to a entry on vue-router.
 *
 * You will be able to access this page at http://localhost:3000/starters/sideblock-blank-page-1
 * Page uri will match related path to src/pages folder
 *
 * Read more about routing:
 * @see /vite.config.ts
 * @see /src/router.ts
 */

import { useHead } from '@vueuse/head'
import { useViewWrapper } from '/@src/stores/viewWrapper'

const viewWrapper = useViewWrapper()
viewWrapper.setPageTitle('Blank Page 1')

useHead({
  title: 'Blank Page 1 - Sideblock - Vuero',
})
</script>

<template>
  <SideblockLayout open-on-mounted>
    <!-- Content Wrapper -->
    <div class="page-content-inner">
      <RouterView v-slot="{ Component }">
        <Transition name="fade-fast" mode="out-in">
          <component :is="Component" :key="route.fullPath" />
        </Transition>
      </RouterView>
    </div>
  </SideblockLayout>
</template>
