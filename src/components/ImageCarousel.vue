<script setup>
import 'vue3-carousel/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'

const images = [
  { id: 1, url: 'https://i.ibb.co/4gpLMq6Y/515392636-727398926583294-4539056181117465170-n.jpg' },
  { id: 2, url: 'https://i.ibb.co/5XvHzwzp/518185889-2469311476760817-8629889246052518186-n.jpg' },
  { id: 3, url: 'https://i.ibb.co/XZ2Hy4LN/518729118-1241901500471633-6069714147377439546-n.jpg' },
  { id: 4, url: 'https://i.ibb.co/bgFdnRMQ/518822479-758983166494232-3641647119146419776-n.jpg' },
  { id: 5, url: 'https://i.ibb.co/TBQGM5JR/519085709-671391739241826-7352785591131756680-n.jpg' },
  { id: 6, url: 'https://i.ibb.co/cKvKKChS/519248656-2877441885977499-7646372025608854033-n.jpg' },
  { id: 7, url: 'https://i.ibb.co/vC21PTvH/519494511-763056802916928-5132886148020227561-n.jpg' },
  { id: 8, url: 'https://i.ibb.co/TM352jw5/520069441-724295316896874-2422071101070242824-n.jpg' },
  { id: 9, url: 'https://i.ibb.co/GvwG9ngL/521354455-4475987572628284-5070872523543778933-n.jpg' },
]

const config = {
  height: '100%',
  itemsToShow: 1,
  gap: 5,
  wrapAround: true,
}
</script>

<template>
  <Carousel v-bind="config" class="h-full">
    <Slide v-for="image in images" :key="image.id">
      <img :src="image.url" alt="image" class="slide-img" />
    </Slide>

    <template #addons>
      <Navigation />
      <Pagination />
    </template>
  </Carousel>
</template>

<style>
:root {
  background-color: #242424;
}

.carousel {
  --vc-pgn-background-color: rgba(255, 255, 255, 0.7);
  --vc-pgn-active-color: rgba(255, 255, 255, 1);
  --vc-nav-background: rgba(255, 255, 255, 0.7);
  --vc-nav-border-radius: 100%;
  --vc-carousel-height: 100%;
}

.slide-img {
  border-radius: 8px;
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
