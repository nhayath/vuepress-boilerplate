<template>
    <nav class="panel">
        <p class="panel-heading">{{ heading }}</p>

        <a v-for="category in categories" :href="'/' + category.slug + '.html'" class="panel-block">
            {{ category.name }}
        </a>
    </nav>
</template>

<script>
    const mensCategories = [{name: 'Shirts', slug: 'mens-shirts'}, {name: 'Jeans', slug: 'mens-jeans'}];
    const womensCategories = [{name: 'Tops', slug: 'womens-tops'}, {name: 'Jeans', slug: 'womens-jeans'}];

    export default {
        name: 'tab-categories',
        props: {
            tab: {
                type: String,
                default: 'men'
            }
        },
        data(){
            return {
                items: []
            }
        },

        computed: {
            categories(){
                if(this.tab==='men')
                    return mensCategories;
                
                return womensCategories;
            },

            heading(){
                if(this.tab==='men'){
                    return "Men's Clothing";
                }

                return "Women's Clothing";
            }
        }
    }
</script>

<style scoped>

</style>