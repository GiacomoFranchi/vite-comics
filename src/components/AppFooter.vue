<script>
export default {
  data() {
    return {
        icons:["facebook","periscope","pinterest","twitter","youtube"]
    }
  },
  methods:{
    getImgUrl(icon){
        return new URL(`../assets/img/footer-${icon}.png`, import.meta.url).href;
    }
  }
};
</script>

<template>
    <footer>
        <div class="footer-container">
            <button>SING-UP NOW!</button>
            <div>
                <h3>FOLLOW US</h3>
                <div class="logo-img" v-for="icon in icons">
                    <img :src="getImgUrl(icon)" alt="asd">
                </div>
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
    padding: 1rem;
    .footer-container{
        @include flex(space-between, center, row);
        width: 80%;
        margin: 0 auto;
        button{
            background-color: $bgColor;
            color: white;
            border: 2px solid $activeColor;
            padding: 1rem;
        }
        div{
            @include flex(space-between, center, row);
            h3{
                color: $activeColor;
                margin-right: 20px;
            }
            .logo-img{
                width: 25px;
                padding: 0.2rem;
                img{
                width: 100%;
                color: white;
                }
            }
        }
    }
}
</style>