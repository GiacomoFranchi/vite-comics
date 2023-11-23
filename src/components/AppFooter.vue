<script>
export default {
  data() {
    return {
        icons:["facebook","periscope","pinterest","twitter","youtube"]
    }
  },
};
</script>

<template>
    <footer>
        <button>SING-UP NOW</button>
        <div>
            <h3>FOLLOW US</h3>
            <div class="logo-img" v-for="icon in icons">
                <img :src="`../assets/img/footer-${icon}.png`" alt="">
            </div>
        </div>
    </footer>
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;
footer{
    width: 100%;
    background-color: $bgColor;
    height: 100px;
    padding: 1.5rem;
    @include flex(space-between, center, row);
    button{
        background-color: $bgColor;
        color: white;
        border: 2px solid $activeColor;
        margin-left: 1.5rem;
        padding: 1rem;
    }
    div{
        @include flex(space-between, center, row);
        h3{
            color: $activeColor;
        }
        .logo-img{
            width: 30px;
            img{
                width: 100%;
                color: white;
            }
        }
    }
}
</style>