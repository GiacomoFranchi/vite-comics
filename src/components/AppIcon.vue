<script>
export default {
  data() {
    return {
        icons:[
            {
                iconName: "DIGITAL COMICS",
                iconImg: "digital-comics.png",
            },
            {
                iconName: "DC MERCHANDISE",
                iconImg: "merchandise.png",
            },
            {
                iconName: "SUBSCRIPTION",
                iconImg: "shop-locator.png",
            },
            {
                iconName: "COMIC SHOP LOCATOR",
                iconImg: "subscriptions.png",
            },
            {
                iconName: "DC POWER VISA",
                iconImg: "power-visa.svg",
            },
        ]
    }
},
    methods:{
        getImgUrl(iconImg) {
            return new URL(`../assets/img/buy-comics-${iconImg}`, import.meta.url).href;
        }
    }
};
</script>

<template>
    <section>   
        <div class="section-icon" >
            <div class="icon" v-for="icon in icons">
                <div class="img-icon">
                    <img :src="getImgUrl(icon.iconImg)"
                     :alt="`${icon.iconName} icon`" />
                </div>
                <span>{{icon.iconName}}</span>
            </div>   
        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;
    section{
        width: 100%;
        background-color: $activeColor;
        .section-icon{
            padding: 1rem 0;
            width: 80%;
            margin: 0 auto;
            @include flex(space-between, center, row);
            .icon{
                @include flex("", center, row);
                flex-wrap: wrap;
                width: calc(100% / 5);
                .img-icon{
                    width: 35px;
                    margin-right: 5px;
                    img{
                        width: 100%;
                    }
                }
                span{
                    width: calc(100% - 50px - 1rem);
                    color: white;
                    font-size: 0.6rem;
                    margin: 0 0.2rem;
                }
            }
        }
    }   
</style>