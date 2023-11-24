<script>
import AppCard from './AppCard.vue';
export default {
  components:{
    AppCard
  },
    data() {
      return {
        
      }
    }
}
</script>

<template>
  <main>
    <AppCard />
  </main>
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

main{
  background-color: $bgColor;
  section{
    width: 80%;
    margin: 0 auto;
    h2{
      color: white;
      padding: 3rem;
    }
  }
}
</style>