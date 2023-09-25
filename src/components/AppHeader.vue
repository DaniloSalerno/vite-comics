<script>
export default {
    name: 'AppHeader',
    data() {
        return {

            activeLink: 0,

            navItems: [
                {
                    name: 'characters',
                    current: false
                },

                {
                    name: 'comics',
                    current: true
                },

                {
                    name: 'movies',
                    current: false
                },

                {
                    name: 'tv',
                    current: false
                },

                {
                    name: 'games',
                    current: false
                },

                {
                    name: 'collectibles',
                    current: false
                },
                {
                    name: 'videos',
                    current: false
                },
                {
                    name: 'fans',
                    current: false
                },
                {
                    name: 'news',
                    current: false
                },
                {
                    name: 'shop',
                    current: false
                }

            ]

        }
    }
}
</script>

<template>
    <header>

        <div class="header_wrapper container d-flex justify-content-between align-items-center w-75">

            <a href="##">

                <img width="75" src="../assets/img/dc-logo.png" alt="">

            </a>

            <div>

                <nav class="navbar navbar-expand navbar-light">

                    <ul class="nav navbar-nav">

                        <li v-for="(item, index) in navItems" class="nav-item">

                            <a class="nav-link" :class="{ 'active': item.current }" href="#" aria-current="page">{{
                                item.name
                            }}</a>

                        </li>

                    </ul>

                </nav>

            </div>

        </div>

    </header>
</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/viariables' as *;

header {
    height: 120px;

    .header_wrapper {
        height: 100%;

        li {

            a {
                text-transform: uppercase;

                &.active {
                    color: $dc_primary;
                }
            }

            & a.active {
                border-bottom: 2px solid $dc_primary;
            }
        }
    }
}
</style>