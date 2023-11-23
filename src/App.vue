<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppIcon from './components/AppIcon.vue';
export default {
  components: {
    AppHeader,
    AppMain,
    AppIcon
  },
};
</script>

<template>
  <AppHeader />
  <AppMain />
  <AppIcon />
</template>

<style lang="scss">
@use "./style/general.scss"
</style>
