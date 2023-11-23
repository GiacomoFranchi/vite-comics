<script>
export default {
    data() {
      return {}
    }
}
</script>

<template>
  <main>
    <section>
      <h2> - - > Content goes here </h2>
    </section>
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