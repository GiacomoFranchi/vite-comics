<script>
export default {
  data() {
    return {
        icons:[
            {
                iconName: "DIGITAL COMICS",
                iconImg: "digital-comics",
            },
            {
                iconName: "DC MERCHANDISE",
                iconImg: "merchandise",
            },
            {
                iconName: "SUBSCRIPTION",
                iconImg: "shop-locator",
            },
            {
                iconName: "COMIC SHOP LOCATOR",
                iconImg: "subscriptions",
            },
            {
                iconName: "DC POWER VISA",
                iconImg: "power-visa",
            },
        ]
    };
  },
};
</script>

<template>
    <section>   
        <div class="section-icon" >
            <div class="icon" v-for="icon in icons">
                <div class="img-icon">
                    <img :src="`../assets/img/buy-comics-${icon.iconImg}.png`"
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
                    width: 50px;
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