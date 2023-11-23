<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppIcon from './components/AppIcon.vue';
import AppFooterContacts from './components/AppFooterContacts.vue';
import AppFooter from './components/AppFooter.vue';
export default {
  components: {
    AppHeader,
    AppMain,
    AppIcon,
    AppFooterContacts,
    AppFooter,
},
};
</script>

<template>
  <AppHeader />
  <AppMain />
  <AppIcon />
  <AppFooterContacts />
  <AppFooter />
</template>

<style lang="scss">
@use "./style/general.scss"
</style>
