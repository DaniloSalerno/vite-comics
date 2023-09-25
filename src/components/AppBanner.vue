<script>
export default {
    name: 'AppBanner',
    data() {
        return {
            links: [
                {
                    img: '../assets/img/buy-comics-digital-comics.png',
                    label: 'digital comics',
                    url: '##'
                },
                {
                    img: '../assets/img/buy-comics-merchandise.png',
                    label: 'dc merchandise',
                    url: '##'
                },
                {
                    img: '../assets/img/buy-comics-subscriptions.png',
                    label: 'subscription',
                    url: '##'
                },
                {
                    img: '../assets/img/buy-comics-shop-locator.png',
                    label: 'comic shop locator',
                    url: '##'
                },
                {
                    img: "../assets/img/buy-dc-power-visa.svg",
                    label: 'dc power visa',
                    url: '##'
                },
            ]
        }
    },
    methods: {
        getImageUrl(name) {
            return new URL(name, import.meta.url).href
        }
    }
}
</script>

<template>
    <div id="banner" class="d-flex align-items-center">

        <div class="wrapper container d-flex justify-content-around align-items-center">

            <a v-for="link in links" :href="link.url" class="d-flex justify-content-center align-items-center gap-2">
                <img width="50" :src="getImageUrl(link.img)" alt="">
                <div class="label">{{ link.label }}</div>
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