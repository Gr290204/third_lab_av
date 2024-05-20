<script setup>
import Swiper from 'swiper';
import { onMounted } from 'vue';
import {Pagination} from 'swiper/modules';
const possibilities = [
  {
    img:{
      src: '/Message.svg',
      alt: 'Общение с классом',
    },
    head: 'Общение с классом',
    description: 'Видеосвязь <br/>Чат с классом'
  },
  {
    img:{
      src: '/Monitor.svg',
      alt: 'Проведение занятий',
    },
    head: 'Проведение занятий',
    description: 'Презентация файлов <br />Демонстрация экрана'
  },
  {
    img:{
      src: '/Visiting.svg',
      alt: 'Посещаемость',
    },
    head: 'Посещаемость',
    description: 'Автоматическое <br />отслеживание <br />присутствующих'
  },
  {
    img:{
      src: '/History.svg',
      alt: 'История занятий',
    },
    head: 'История занятий',
    description: 'Материалы урока'
  }
]
onMounted(()=>{const swiper = new Swiper(".swiper", {
    modules:[Pagination],
    pagination: {
      el: ".swiper-pagination",
    },
  });})

</script>

<template>
    <section class="possibilities-mobile">
        <div class="container">
          <h2>Возможности</h2>
          <div class="swiper">
            <!-- Additional required wrapper -->
            <div class="swiper-wrapper">
              <!-- Slides -->
              <div class="swiper-slide"
              v-for="item in possibilities"
              >
                <div class="possibilities__item-wrap">
                  <div class="possibilities__item">
                    <div class="possibilities__item-img-wrap">
                      <img :src="item.img.src" :alt="item.img.alt" />
                    </div>
                    <h4>{{item.head}}</h4>
                    <p v-html="item.description"
                    </p>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="swiper-pagination"></div>
        </div>
      </section>
</template>

<style scoped></style>