<script>
export default {
    name: 'AppBanner'/* ,
    data() {
        return {
            links: [
                {
                    img: '../assets/img/buy-comics-digital-comics.png',
                    label: 'digital comics'
                },
                {
                    img: '../assets/img/buy-comics-merchandise.png',
                    label: 'dc merchandise'
                },
                {
                    img: '../assets/img/buy-comics-subscriptions.png',
                    label: 'subscription'
                },
                {
                    img: '../assets/img/buy-comics-shop-locator.png',
                    label: 'comic shop locator'
                },
                {
                    img: "../assets/img/buy-dc-power-visa.svg",
                    label: 'dc power visa'
                },
            ]
        }
    } */
}
</script>

<template>
    <div id="banner" class="d-flex align-items-center">
        <div class="wrapper container d-flex justify-content-around align-items-center">


            <!-- :SRC DOESN'T WORK -->
            <!-- <a v-for="link in links" href="#" class="d-flex justify-content-center align-items-center gap-2">
                <img width="50" :src="link.img" alt="">
                <div class="label">{{ link.label }}</div>
            </a> -->

            <a href="#" class="d-flex justify-content-center align-items-center gap-2">
                <img width="50" src="../assets/img/buy-comics-digital-comics.png" alt="">
                <div class="label">digital comics</div>
            </a>
            <a href="#" class="d-flex justify-content-center align-items-center gap-2">
                <img width="50" src="../assets/img/buy-comics-merchandise.png" alt="">
                <div class="label">dc merchandise</div>
            </a>
            <a href="#" class="d-flex justify-content-center align-items-center gap-2">
                <img width="50" src="../assets/img/buy-comics-subscriptions.png" alt="">
                <div class="label">subscription</div>
            </a>
            <a href="#" class="d-flex justify-content-center align-items-center gap-2">
                <img width="50" src="../assets/img/buy-comics-shop-locator.png" alt="">
                <div class="label">comic shop locator</div>
            </a>
            <a href="#" class="d-flex justify-content-center align-items-center gap-2">
                <img width="50" src="../assets/img/buy-dc-power-visa.svg" alt="">
                <div class="label">dc power visa</div>
            </a>
        </div>
    </div>
</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/viariables' as *;

#banner {
    background-color: $dc_primary;
    height: 150px;

    .wrapper {
        height: 55px;

        a {
            text-decoration: none;

            img {
                height: 55px;
                object-fit: scale-down;
            }

            .label {

                color: white;
                text-transform: uppercase;
                font-size: 0.8rem;
            }


        }
    }

}
</style>