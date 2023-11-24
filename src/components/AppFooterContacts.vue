<script>
export default {
  data() {
    return {
        sections:[
            {
                nameSec: "DC COMICS",
                links:["Characters","Comics","Movies","TV","Games","Videos","News"] 
            },
            {
                nameSec: "SHOP",
                links:["Shop DC","Shop DC Collectibles"]
            },
            {
                nameSec: "DX",
                links:["Tetms of use","Privacy policy (New)","Ad Choices","Advertising","Jobs","Subscriptions","Talent Workshop", "CPSC Certificates", "Ratings","Shop Help","Contact US"]
            },
            {
                nameSec: "SITES",
                links:["DC","MAD MAgazine","DC Kids","DC Universe", "DC Power Visa"]
            }

        ]
    };
  },
};
</script>

<template>
    <section class="footer-top">
        <div class="footer-sect">
            <div v-for="(section, index) in sections">
                <h3>{{ section.nameSec }}</h3>
                <ul>
                    <li v-for="(link , index) in sections[index].links">
                        <a href="">{{ link }}</a>
                    </li>
                </ul>
            </div>
            <img class="logo-bkg" src="../assets/img/dc-logo-bg.png" alt="logo DC Background">
        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

.footer-top{
    position: relative;
    width: 100%;
    background-image: url(../assets/img/footer-bg.jpg);
    z-index: -2;
    .footer-sect{
        width: 80%;
        display: flex; 
        margin: 0 auto;
        div{
            margin: 0.5rem;
            h3{
            color: white;
            }
            li{
                list-style: none;
                line-height: 0.5rem;
                a{
                    color:whitesmoke;
                    font-size: 0.6rem;
                    text-decoration: none;
                }
            }
        }
        .logo-bkg{
            position: absolute;
            width: 200px;
            right: 10%;
            top: 50%;
            transform: translateY(-50%);
            z-index: -1;
        }
    }   
}
</style>