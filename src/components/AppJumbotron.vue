<script>
export default {
    name: 'AppJumbotron'
}
</script>

<template>
    <div id="jumbo">
        <div class="container"></div>
        <!-- CONTENT GOES HERE -->
    </div>
</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/viariables' as *;

#jumbo {
    min-height: 400px; //TO FIX AFTER ADDED CONTENT
    background-image: url('../assets/img/jumbotron.jpg');
}
</style>