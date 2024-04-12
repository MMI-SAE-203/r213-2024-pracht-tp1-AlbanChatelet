<script setup lang="ts">
import { ref } from 'vue';

const maVar = ref(true)
</script>

<template>
  
  <button @click="maVar = false">Cacher</button>
  <button @click="maVar = true">Montrer</button>
  <button @click="maVar = !maVar"> Bascule</button>
  
  <h1 v-show="maVar"
  class="text-2xl">Quand j'arrive au lundi</h1>

  <section>
    <button class="text-xl">bouton 1</button>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam laborum, ut cupiditate fugit deleniti esse sit quas odio, rem dolores pariatur optio? Excepturi consequatur saepe dolorem sequi deserunt soluta modi!</p>
  </section>
  <section>
    <button class="text-xl">bouton 2</button>
    <p>Repellendus amet ad voluptatum nesciunt reiciendis aliquam perferendis delectus facilis corporis architecto! Eaque sit adipisci fuga. Incidunt porro architecto voluptas molestias! Voluptas quaerat explicabo veritatis mollitia laboriosam. Similique, enim eveniet.</p>
  </section>
  <section>
    <button class="text-xl">bouton 3</button>
    <p>Dolorem sequi similique ab incidunt? A quam tenetur, porro dolor praesentium beatae. Dicta, eligendi. In voluptatum at ut, beatae esse fugit, quos pariatur totam vitae maxime error vel dolor impedit.</p>
  </section>
</template>