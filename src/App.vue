<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppIcon from './components/AppIcon.vue';
import AppFooterContacts from './components/AppFooterContacts.vue';
export default {
  components: {
    AppHeader,
    AppMain,
    AppIcon,
    AppFooterContacts
},
};
</script>

<template>
  <AppHeader />
  <AppMain />
  <AppIcon />
  <AppFooterContacts />
</template>

<style lang="scss">
@use "./style/general.scss"
</style>
