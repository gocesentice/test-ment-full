<script setup lang="ts">
import { useHead } from '@vueuse/head'

import { useViewWrapper } from '/@src/stores/viewWrapper'

const viewWrapper = useViewWrapper()
viewWrapper.setPageTitle('Grid Cards 1')

useHead({
  title: 'Grid Cards 1 - Sidebar - Vuero',
})
</script>

<template>
  <div class="page-content-inner">
    <MentUsersGridV3 />
  </div>
</template>
