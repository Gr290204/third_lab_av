<script setup>
document.addEventListener('DOMContentLoaded', function() {
    document.querySelector('.navigation__menu-button').addEventListener('click', function() {
    const menuLinks = document.querySelector('.navigation__menu-links');
    menuLinks.classList.toggle('active');

    const menubg = document.querySelector('.navigation__menu-back');
    menubg.classList.toggle('active');
   
    const button = this;
    if (button.src.includes('burger.svg')) {
       button.src = 'x.svg';
       document.body.style.overflow = "hidden"
    } else {
       button.src = 'burger.svg';
       document.body.style.overflow = ""
    }
    button.classList.toggle('active');
   });
});
  
</script>

<template>
<header>
        <div class="navigation">
            <div class="container">
                <div class="navigation__content">
                    <img src="/Logo.svg" alt="">
                    <ul class="navigation__links">
                        <li>
                            <a href="/"> Возможности </a>
                        </li>
                        <li>
                            <a href="/"> Как это работает? </a>
                        </li>
                    </ul>
                    <div class="navigation__menu">
                        <img class="navigation__menu-button" src="/burger.svg" alt="">
                        <div class="navigation__menu-links">
                            <ul>
                                <li class="navigation__menu-links-ability">
                                    <a href="/"> Возможности </a>
                                </li>
                                <li class="navigation__menu-links-how">
                                    <a href="/"> Как это работает? </a>
                                </li>
                            </ul>
                            <div class="navigation__menu-adres">
                                <p>г Сургут, ул Базовая, д. 34, офис 10
                                    ОГРН 1238600001200
                                    ИНН 8602309464</p>
                            </div>
                            <div>
                                <p>
                                    ООО Дотсолюшн © 2023
                                </p>
                            </div>

                        </div>

                        <div class="navigation__menu-back">

                        </div>
                    </div>

                </div>
            </div>
        </div>

    </header>
</template>

<style scoped></style>