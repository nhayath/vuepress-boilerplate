<template>
    <nav class="navbar is-transparent">

        <!-- logo -->
        <div class="navbar-brand">
            <a class="navbar-item" href="https://bulma.io">
                <img src="https://bulma.io/images/bulma-logo.png" alt="Bulma: a modern CSS framework based on Flexbox" width="112" height="28">
            </a>
            <div class="navbar-burger burger" :class="{'is-active': isActive}" @click="isActive=!isActive">
                <span></span>
                <span></span>
                <span></span>
            </div>
        </div>

        <!-- menu -->
        <div class="navbar-menu" :class="{'is-active': isActive}">

            <!-- left -->
            <div class="navbar-start">
                <a href="/" class="navbar-item">Women</a>
                <a href="/" class="navbar-item">Men</a>
            </div>

            <!-- end -->
            <div class="navbar-end">
                <a href="/" class="navbar-item">Help</a>
            </div>

        </div>
    </nav>
</template>

<script>
    export default {
        name: 'navbar',
        data(){
            return {
                isActive: false
            }
        }
    }
</script>

<style scoped>

</style>