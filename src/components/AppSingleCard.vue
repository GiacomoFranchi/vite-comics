<script>
export default {
  props: {
    thumb: String,
    series: String
  },
};
</script>

<template>
    <div class="card" >
      <img :src="thumb" alt="{{ series }}" />
      <h3>{{ series }}</h3>
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;

.card{
    height: 100%;
    img{
        width: 100%;
        height: 70%;
    }
    h3{
        font-size: 0.7rem;
        color: white;
    }
}
</style>