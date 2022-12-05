<template>
    <div class="crumbs">
        <a v-for="crumbsItem in crumbsItems" href="/" class="crumbs__item">{{ crumbsItem }}</a>
        <p class="crumbs__item">{{ currentPage }}</p>
    </div>
</template>

<script>
    export default {
        name: "Crumbs",

        props: {
            crumbsItems: Array,
            currentPage: String
        }
    }
</script>