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
            <nav class="nav">
                <a href="/" class="nav__item active">Семена</a>
                <a href="/" class="nav__item">О нас</a>
                <a href="/" class="nav__item">Завод</a>
                <a href="/" class="nav__item">Новости</a>
                <a href="/" class="nav__item">Контакты</a>
            </nav>
            <div class="header__container-right">
                <div class="call">
                    <a href="tel: 8 800 250-64-69" class="call__phone">8 800 250-64-69</a>
                    <button type="button" class="call__order">Заказать звонок</button>
                </div>
                <a href="/" class="cart">
                    <img src="../../assets/img/cart.svg" alt="" class="cart__icon">
                    <p class="cart__value">0</p>
                </a>
            </div>
        </div>

    </header>
</template>

<script>
    export default {
        name: "Header"
    }
</script>