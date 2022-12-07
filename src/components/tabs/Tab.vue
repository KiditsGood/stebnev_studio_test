<template>
    <div class="tabs__item" v-show="title == selectedTitle">
        <slot></slot>
    </div>
</template>

<script>
    import { inject } from 'vue'

    export default {
        name: "Tab",

        props: ['title'],

        setup() {
            const selectedTitle = inject("selectedTitle")

            return {
                selectedTitle
            }
        }
    }
</script>