<template>
    <footer class="footer">
        <div class="footer__container">
            <div class="footer__container-top">
                <div class="footer__container-top_left">
                    <a href="/" class="footer__logo">
                        <img src="../../assets/img/logo.svg" alt="" class="footer__logo-icon">
                    </a>
                    <p class="footer__text">Мы имеем безупречную деловую репутацию и будем рады видеть Вас в числе наших партнеров.</p>
                </div>
                <div class="footer__container-top_right">
                    <p class="footer__text">Подпишитесь на нашу рассылку, и будете в курсе наших последних новостей и цен.</p>
                    <div class="subscribe">
                        <input id="sub" type="email" class="subscribe__input">
                        <label for="sub" class="subscribe__label"><span class="subscribe__label-star">*</span> E-mail</label>
                        <Button :butt-title="'Подписаться'" />
                    </div>
                </div>
            </div>
            <div class="footer__container-bottom">
                <p class="footer__rights">© 2022 HYBRID SK. Все права защищены.</p>
                <p class="stebnev">Разработано в <a href="https://stebnev-studio.ru/" class="stebnev__link">Stebnev-Studio</a></p>
            </div>
        </div>
    </footer>
</template>

<script>
    import Button from "@/components/button/Button";
    export default {
        name: "Footer",
        components: {Button}
    }
</script>