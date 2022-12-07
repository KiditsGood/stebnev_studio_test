<template>
    <header class="header">
        <div class="header__container">
            <div class="header__container-left">
                <a href="/" class="logo">
                    <img src="../../assets/img/logo.svg" alt="" class="logo__icon">
                </a>
                <button class="city">
                    <img src="../../assets/img/city.svg" alt="" class="city__icon">
                    Воронеж
                </button>
            </div>
            <nav class="nav" v-if="currentWidth > 991">
                <a href="/" class="nav__item active">Семена</a>
                <a href="/" class="nav__item">О нас</a>
                <a href="/" class="nav__item">Завод</a>
                <a href="/" class="nav__item">Новости</a>
                <a href="/" class="nav__item">Контакты</a>
            </nav>
            <div class="header__container-right" v-if="currentWidth > 991">
                <div class="call">
                    <a href="tel: 8 800 250-64-69" class="call__phone">8 800 250-64-69</a>
                    <button type="button" class="call__order">Заказать звонок</button>
                </div>
                <a href="/" class="cart">
                    <img src="../../assets/img/cart.svg" alt="" class="cart__icon">
                    <p class="cart__value">0</p>
                </a>
            </div>
            <div v-else class="header__mobile" :class="{open: openFlag}">
                <nav class="nav">
                    <a href="/" class="nav__item active">Семена</a>
                    <a href="/" class="nav__item">О нас</a>
                    <a href="/" class="nav__item">Завод</a>
                    <a href="/" class="nav__item">Новости</a>
                    <a href="/" class="nav__item">Контакты</a>
                </nav>
                <a href="tel: 8 800 250-64-69" class="call__phone">8 800 250-64-69</a>
            </div>
            <div v-if="currentWidth < 992" class="header__icons">
                <a href="/" class="header__icons-item">
                    <img src="../../assets/img/cart.svg" alt="" class="header__icons-item_icon">
                    <p class="header__icons-item_value">0</p>
                </a>
                <a href="tel: 8 800 250-64-69" class="header__icons-cart">
                    <img src="../../assets/img/phone.svg" alt="" class="header__icons-cart_icon">
                </a>
                <div @click="bodyOverflow" id="burger" :class="{open: openFlag}">
                    <span></span>
                </div>
            </div>
        </div>
    </header>
</template>

<script>
    export default {
        name: "Header",

        data() {
            return {
                currentWidth: window.innerWidth,
                openFlag: false
            }
        },

        methods: {
            bodyOverflow() {
                this.openFlag = !this.openFlag

                const bodySelect = document.querySelector('body')

                if (this.openFlag) {
                    bodySelect.style.overflow = 'hidden'
                }
                else {
                    bodySelect.style.overflow = 'visible'
                }
            }
        }
    }
</script>