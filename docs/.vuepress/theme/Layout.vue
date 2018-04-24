<template>
    <div class="theme-container">

        <!-- navbar -->
        <navbar></navbar>

        <!-- content -->
        <Content/>

        <!-- footer -->
        
    </div>
</template>

<script>

    export default {

        mounted(){
            document.title = this.$page.title;
        }
    }
</script>

<style src="./style.scss" lang="scss"></style>