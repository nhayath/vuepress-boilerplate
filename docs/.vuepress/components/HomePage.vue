<template>
    <section>
        <div class="tabs is-centered">
            <ul @click="onTabChange">
                <li :class="{'is-active': tab==='featured'}" data-target="featured"><a @click.prevent="tab='featured'">Featured</a></li>
                <li :class="{'is-active': tab==='men'}" data-target="men"><a @click.prevent="tab='men'">Men</a></li>
                <li :class="{'is-active': tab==='women'}" data-target="women"><a @click.prevent="tab='women'">Women</a></li>
                <li :class="{'is-active': tab==='stores'}" data-target="stores"><a @click.prevent="tab='stores'">Stores</a></li>
            </ul>
        </div>
        <!-- tab content -->
        <section class="section">
            <div class="container">
                <component :is="getActiveTabComponent" :tab="tab"></component>
            </div>
        </section>
    </section>
</template>

<script>
    export default {
        name: 'home-page',
        data(){
            return {
                tab: 'featured'
            }
        },

        computed: {
            getActiveTabComponent(){
                if(this.tab==='men' || this.tab==='women'){
                    return 'tab-categories';
                }else if(this.tab==='stores'){
                    return 'tab-stores';
                }else{
                    return 'tab-featured';
                }
            }
        },

        methods: {
            onTabChange(e){
                e.preventDefautl;
                console.log(e.target);
            }
        }
    }
</script>

<style scoped>
.content ul{
    margin-left: 0;
    margin-top: 0;
}
</style>