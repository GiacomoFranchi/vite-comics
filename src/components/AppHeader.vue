<script>
import AppHero from './AppHero.vue';
export default {
  components:{
    AppHero
  },
  data() {
    return {
      navItems: [
        {
          sezioneHead: "CHARACTERS",
          active: false,
        },
        {
          sezioneHead: "COMICS",
          active: true,
        },
        {
          sezioneHead: "MOVIES",
          active: false,
        },
        {
          sezioneHead: "TV",
          active: false,
        },
        {
          sezioneHead: "GAMES",
          active: false,
        },
        {
          sezioneHead: "COLLECTIBLES",
          active: false,
        },
        {
          sezioneHead: "VIDEOS",
          active: false,
        },
        {
          sezioneHead: "FANS",
          active: false,
        },
        {
          sezioneHead: "NEWS",
          active: false,
        },
        {
          sezioneHead: "SHOP",
          active: false,
        },
      ],
    };
  },
};
</script>

<template>
    <div class="header-top"></div>
    <header>
        <div class="logo">
            <img src="../assets/img/dc-logo.png" alt="DC Logo" />
        </div>
        <nav>
            <ul>
                <li v-for="item in navItems" :key="item.sezioneHead">
                    <a :class="{ active: item.active }" href="">{{ item.sezioneHead }}</a>
                </li>
            </ul>
        </nav>
    </header>
    <AppHero />
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

.header-top{
  width: 100%;
  height: 10px;
  background-color: $bgColor;
}

header{
    width: 80%;
    margin: 0 auto;
    padding: 0.2rem;
    @include flex(space-between, center, row);
    .logo{
        text-align: center;
        img{
            width: 70px;
        }
    }
    nav{
        width: calc(80% - 90px);
        ul{
            @include flex(space-evenly,shrink , row);
            list-style: none;
            font-size: 0.8rem;
            li{
                a {
                    padding: 0.2rem;
                    padding-bottom: 1.85rem;
                    text-decoration: none;
                    color: black;
                    font-weight: bold;
                    &.active {
                    border-bottom: 6px solid $activeColor;
                    padding-bottom: 1.7rem;
                    }
                    &:hover {
                        border-bottom: 4px solid $activeColor;
                    color: $activeColor;
                    }
                }
            }
        }
    }
}
</style>