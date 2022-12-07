<template>
    <div class="tabs">
        <div class="tabs__header">
            <button
                :key="title"
                v-for="title in tabTitles"
                @click="selectedTitle = title"
                class="tabs__header-item"
                :class="{active: title == selectedTitle}"
            >
                {{ title }}
            </button>
        </div>
        <slot></slot>
    </div>
</template>

<script>
    import { ref, provide } from 'vue'
    export default {
        name: "TabWrapper",

        setup(props, { slots }) {
            const tabTitles = ref(slots.default().map((tab) => tab.props.title))
            const selectedTitle = ref(tabTitles.value[0])

            provide("selectedTitle", selectedTitle)
            return {
                tabTitles,
                selectedTitle
            }
        }
    }
</script>