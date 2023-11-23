<script>
export default {
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
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

header{
    width: 80%;
    margin: 0 auto;
    padding: 1rem;
    @include flex(space-between, center, row);
    .logo{
        text-align: center;
        img{
            width: 100px;
        }
    }
    nav{
        width: calc(70% - 90px);
        ul{
            @include flex(space-evenly, center, row);
            list-style: none;
            font-size: 0.8rem;
            li{
                a {
                    padding: 1rem;
                    padding-bottom: 2.9rem;
                    text-decoration: none;
                    color: black;
                    font-weight: bold;
                    &.active {
                    border-bottom: 4px solid $activeColor;
                    }
                    &:hover {
                        border-bottom: 2.5px solid $activeColor;
                    color: $activeColor;
                    }
                }
            }
        }
    }
}
</style>