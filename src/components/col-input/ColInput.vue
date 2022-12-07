<template>
    <div class="request">
        <div class="request__value">
            <div class="amount">
                <button :disabled="colValue <= 1" @click="minusCol" class="amount__button minus">
                    <span></span>
                </button>
                <input v-model="colValue" type="number" class="amount__input" min="1" max="999">
                <button :disabled="colValue >= 999" @click="plusCol" class="amount__button plus">
                    <span></span>
                    <span></span>
                </button>
            </div>
            <p class="request__value-wallet">п.е.</p>
        </div>
        <Button :butt-title="'добавить в заявку'" />
    </div>
</template>

<script>
    import Button from "@/components/button/Button";
    export default {
        name: "ColInput",
        components: {Button},

        data() {
            return {
                colValue: '1'
            }
        },

        methods: {
            minusCol() {
                this.colValue--
            },

            plusCol() {
                this.colValue++
            }
        }
    }
</script>

<style scoped>

</style>