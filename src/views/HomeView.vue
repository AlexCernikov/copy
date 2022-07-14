<template>
  <div class="home">
    <HeroSectionComponent msg="Welcome  to Your Vue.js + TypeScript App"/>
    <SpaceMainComponent />
  </div>
</template>

<script lang="ts">

import { defineComponent } from 'vue';
import HeroSectionComponent from '@/components/HomeViewComponents/HeroSectionComponent.vue'; // @ is an alias to /src
import SpaceMainComponent from '@/components/HomeViewComponents/SpaceMainComponent.vue';

export default defineComponent({

  name: 'app',
  components: {
    HeroSectionComponent,
    SpaceMainComponent,
  },
});
</script>
