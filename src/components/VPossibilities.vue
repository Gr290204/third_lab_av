<script setup>
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
</script>

<template>
    <section class="possibilities">
        <div class="container">
          <h2>Возможности</h2>
          <div class="row">
            <div class="col-3" 
            v-for="(item, index) in possibilities"
            :key="index"
            >
              <div class="possibilities__item">
                <div class="possibilities__item-img-wrap">
                  <img :src="item.img.src" :alt="item.img.alt" />
                </div>
                <h4>{{item.head}}</h4>
                <p v-html="item.description"></p>
              </div>
            </div>
          </div> 
        </div>
      </section>
</template>

<style scoped></style>