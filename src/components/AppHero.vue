<script>
export default {
  data() {
    return {};
  },
};
</script>

<template>
    <div>
        <img src="../assets/img/jumbotron.jpg" alt="imm teen titans">
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

div{
    width: 100%;
    height: 300px;
    img{
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: top;
    }
}
</style>