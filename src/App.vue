<template>
  <the-header></the-header>
  <router-view></router-view>
  <the-footer></the-footer>
</template>

<script>
import TheHeader from '@/components/layout/TheHeader.vue';
import TheFooter from '@/components/layout/TheFooter.vue';

export default {
  name: 'App',
  components: {
    TheHeader,
    TheFooter
  }
}
</script>


<style>
@import '@/assets/style.css';

body{
  background-image: url('@/assets/background.png');
}

</style>
