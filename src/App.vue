<template>
  <div class="d-flex flex-column flex-root">
    <div class="page d-flex flex-column flex-column-fluid">
      <TheHeader :key="$route.fullPath"></TheHeader>
      <div id="kt_content_container" class="d-flex flex-column-fluid align-items-stretch container-xxl ">
        <TheAside></TheAside>
        <router-view></router-view>

        <TheSidebar></TheSidebar>
      </div>
      <TheFooter></TheFooter>
    </div>
  </div>
</template>

<script lang="ts">
import TheHeader from '@/components/TheHeader.vue'
import TheFooter from "@/components/TheFooter.vue";
import TheAside from "@/components/TheAside.vue";
import TheSidebar from "@/components/TheSidebar.vue";
import { useRoute } from 'vue-router';

export default {
  name: 'App',
  setup() {
    const route = useRoute();
    return route
  },
  components: {
    TheHeader,
    TheFooter,
    TheAside,
    TheSidebar
  },

}
</script>

<style></style>
