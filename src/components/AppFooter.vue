
<script>
export default {
    name: 'AppFooter',
    data() {
        return {
            dcComicsLinks: ['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News'],
            shopLinks: ['Shop DC', 'Shop DC Collectibles'],
            dcLinks: ['Terms Of Use', 'Privacy policy (New)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshops', 'CPSC Certificates', 'Shop Help', 'Contact US'],
            sitesLinks: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa'],

            socials: [
                {
                    img: './src/assets/img/footer-facebook.png',
                    href: '##'
                },
                {
                    img: './src/assets/img/footer-twitter.png',
                    href: '##'
                },
                {
                    img: './src/assets/img/footer-youtube.png',
                    href: '##'
                },
                {
                    img: './src/assets/img/footer-pinterest.png',
                    href: '##'
                },
                {
                    img: './src/assets/img/footer-periscope.png',
                    href: '##'
                },

            ]
        }
    }
}
</script>

<template>
    <footer>

        <div class="footer_top">
            <div class="container">
                <div class="row">
                    <div class="col-6 py-5">
                        <div class="d-flex gap-5">

                            <div>
                                <h3>dc comics</h3>
                                <ul class="list-unstyled">
                                    <li v-for="link in dcComicsLinks">
                                        <a href="#">{{ link }}</a>
                                    </li>
                                </ul>


                                <h3>shop</h3>
                                <ul class="list-unstyled">
                                    <li v-for="link in shopLinks">
                                        <a href="#">{{ link }}</a>
                                    </li>
                                </ul>
                            </div>

                            <div>
                                <h3>dc</h3>
                                <ul class="list-unstyled">
                                    <li v-for="link in dcLinks">
                                        <a href="#">{{ link }}</a>
                                    </li>
                                </ul>
                            </div>

                            <div>
                                <h3>sites</h3>
                                <ul class="list-unstyled">
                                    <li v-for="link in sitesLinks">
                                        <a href="#">{{ link }}</a>
                                    </li>
                                </ul>
                            </div>

                        </div>
                    </div>
                    <div class="col-6 logo">

                    </div>
                </div>
            </div>
        </div>

        <div class="footer_bottom">
            <div class="container d-flex justify-content-between h-100">

                <div class=" d-flex align-items-center">
                    <a href="##">
                        <button class="btn btn-outline-primary text-uppercase text-white rounded-0 fs-5">
                            sign-up now!
                        </button>
                    </a>
                </div>

                <div id="socials" class=" d-flex align-items-center gap-4">
                    <h3>follow us</h3>
                    <a v-for="social in socials" href="social.href">
                        <img :src="social.img" alt="">
                    </a>
                </div>


            </div>

        </div>

    </footer>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/viariables' as *;

.footer_top {

    height: 400px;
    background-image: url('../assets/img/footer-bg.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    overflow-y: hidden;

    h3 {

        text-transform: uppercase;
        color: white;
        font-weight: bolder;
        font-size: 1.25rem;

    }

    a {

        color: gray;
        text-decoration: none;

        &:hover {

            color: white;

        }
    }

    .logo {

        background-image: url('../assets/img/dc-logo-bg.png');
        background-repeat: no-repeat;
        background-position: center;

    }
}

.footer_bottom {

    height: 110px;
    background-color: $dc_dark;

    h3 {

        text-transform: uppercase;
        color: $dc_primary;
        font-weight: bold;
        font-size: 1.25rem;
        padding-top: 0.5rem;

    }

    #socials a img:hover {

        filter: brightness(3);

        transition: filter, 0.5s;
    }

}
</style>