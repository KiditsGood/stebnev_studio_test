<template>
    <div class="product">
        <div class="product__images">
           <ProductSlider />
        </div>
        <div class="product__info">
            <h1 class="product__info-title">СКАП 252 СВ</h1>
            <p class="product__info-desc">Среднеранний, простой гибрид зернового направления. Вегетационный период 110 дней. Оригинатор - ООО "Агроплазма" . Внесен в государственный реестр в 2020 г. Зерно желтое, зубовидное. Высота стебля до   см. Высота крепления початка 80-90 см. Масса 1000 зерен 295-302 г. Выход зерна при обмолоте - 80-82 %</p>
            <div class="chars">
                <p class="chars__item">ФАО: 194</p>
                <p class="chars__item">Назначение: зерно</p>
                <p class="chars__item">Группа спелости: раннеспелый</p>
            </div>
            <div class="way">
                <p class="way__name">Способ обработки:</p>
                <div @click="selectFlag = !selectFlag" class="way__select">
                    <p class="way__select-text">{{ selectValue }}</p>
                    <img src="../../assets/img/arrow.svg" alt="" class="way__select-icon" :class="{active: !selectFlag}">
                </div>
                <div class="way__hidden" :class="{active: !selectFlag}">
                    <p @click="selectFlag = !selectFlag; selectValue = selectItem" v-for="selectItem in selectItems" class="way__hidden-item">{{ selectItem }}</p>
                </div>
            </div>
            <div class="price">
                <p class="price__old">4 200, 00 ₽</p>
                <p class="price__new">3 000, 00 ₽</p>
            </div>
            <ColInput />
        </div>
    </div>
</template>

<script>
    import ProductSlider from "@/components/productslider/ProductSlider";
    import ColInput from "@/components/col-input/ColInput";
    export default {
        name: "ProductCard",
        components: {ColInput, ProductSlider},

        data() {
            return {
                selectValue: 'Фунгицид',
                selectItems: ['Фунгицид', 'Тест 1', 'Тест 2'],
                selectFlag: true
            }
        }
    }
</script>