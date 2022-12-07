<template>
    <button class="button button--green">{{ buttTitle }}</button>
</template>

<script>
    export default {
        name: "Button",

        props: {
            buttTitle: String
        }
    }
</script>